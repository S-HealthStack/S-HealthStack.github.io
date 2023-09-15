
# Installing the Backend System

Follow these instructions to install, build, and verify the backend system.

## System Requirements

To operate the backend system, you must have one of the following:

- A 64-bit Mac OS (Intel or ARM)
- A 64-bit Linux machine (Ubuntu or Debian)

## Prerequisites

### I. Update the Environment

1. Open a `Terminal` window; if using Linux or Mac.

2. If you are using Linux, make sure your environment system packages are up to date.

   ```
   sudo apt update
   sudo apt upgrade
   ```

### II. Install Java 17

1. Install the OpenJDK package.
   **Mac:** 

   Go to https://www.oracle.com/java/technologies/javase/jdk17-archive-downloads.html. Download the kit based on your system requirements. Install the JDK.

   **Linux:**

   ```
   sudo apt install -y openjdk-17-jdk-headless unzip
   ```

2. Verify that you have successfully installed version 17.

   ```
   java -version
   ```

   Make sure it is:

   `java version "17.0.8" 2023-07-18 LTS
   Java(TM) SE Runtime Environment (build 17.0.8+9-LTS-211)
   Java HotSpot(TM) 64-Bit Server VM (build 17.0.8+9-LTS-211, mixed mode, sharing)`

### III. Install Docker and Docker Compose

1. Download Docker Desktop to get all the necessary packages for this installation: [https://www.docker.com/products/docker-desktop/](https://www.docker.com/products/docker-desktop/)

2. Open the Docker Desktop.

3. Confirm successful installation.

   **MAC:**

   ```
   docker info
   ```

   **Linux:**

   ```
   sudo docker --version
   sudo systemctl status docker  `
   ```

### VI. Clone Backend System

1. If you do not have Git, install it using the instruction here: [Git - Installing Git (git-scm.com)](https://git-scm.com/book/en/v2/Getting-Started-Installing-Git)

2. If you wish to iterate and develop on the backend, please fork the repo and then clone it from your own account. You can find steps to fork here: [https://docs.github.com/en/get-started/quickstart/fork-a-repo](https://docs.github.com/en/get-started/quickstart/fork-a-repo)

3. Download the latest implementation of the Samsung Health Stack backend system from GitHub.

   ```
   git clone https://github.com/S-HealthStack/backend-system.git
   ```


> The folder in which you cloned the `backend-system` will be referred to as `<install_path>` within this document.

### V. Firebase Service

1. If you do not have an account, create a Firebase account and a project with default settings by visiting: [Firebase (google.com)](https://firebase.google.com/)
2. Go to the [Firebase console]([Firebase console](https://console.firebase.google.com/)) and select your project.
3. Click on the gear icon in the top left corner to access your project settings.
4. Click on the `Service accounts` tab.
5. Click the `Generate new private key` button to generate a new service account key file (we used Node.js on our Mac test).

   NOTE: You don't need to follow any further instructions on Firebase at this point - all you had to do was generate the key.

6. Return to the terminal and create a Firebase `service-account-key.json` file.

   ```
   cd backend-system/platform
   touch service-account-key.json
   ```

7. Update the `service-account-key.json` file with the private key generated in step 5 so `service-account-key.json` looks like the key you created/downloaded from Firebase.

8. .gitignore this `service-account-key.json` file as it includes sensitive info about your Firebase account.

## Installation

### Method 1: Using Docker Compose

#### I. backend-config-files-v1.zip

1. Download `backend-config-files-v1.zip` from [https://github.com/S-HealthStack/S-HealthStack.github.io/blob/main/files/installing-the-backend/backend-config-files-v1.zip](https://github.com/S-HealthStack/S-HealthStack.github.io/blob/main/files/installing-the-backend/backend-config-files-v1.zip)

2. Extract the files and place them at the level of `backend-system`. Your file structure should look as follows for `<install_path>`:

   ```
   backend-system
   docker-compose.yml
   haproxy
   multi_db
   rule-update
   trino
   ref.tgz
   .env
   ```

#### II. Database (Optional)

1. If you don't want to use our provided sample database, following the [Configuring the Database](configure-database.md) page instructions if you want to connect to the running Postgres container.

2. (Optional) Update PostgreSQL root user password and SMTP relay server host, username, port, and password. We use SMTP service to send account invitation/activation/password reset emails.

   ```
   POSTGRES_PASSWORD=<new-value-here>
   SMTP_HOST=<new-value-here>
   SMTP_PORT=<new-value-here>
   MAIL_USER=<new-value-here>
   MAIL_USER_PASSWORD= <new-value-here>
   ```

3. (Required if performing Step 2)  Sync password with Trino PostgreSQL catalog file downloaded located at: `<install_path>/trino/etc/catalog/postgresql/postgresql.properties`

   ```
   connector.name=postgresql
   connection-url=jdbc:postgresql://hrp-postgres:5432/healthstack
   connection-user=postgres
   connection-password= <new-value-here>
   ```

#### III. Compile

1. Move into the backend-system directory.

   ```
   cd backend-system
   ```

2. Compile and package the backend-related microservices:

   **Mac & Linux**:

   ```
   ./gradlew clean
   ./gradlew build -x detekt
   ```

   <!-- **Window:** Remove the `./`.

   ```
   gradlew clean
   gradlew build -x detekt
   ``` -->

3. (Optional) If you prefer to build a specific component only (e.g. account-service). Use appropriate target in Gradle:

   ```
   cd <package-path> ./gradlew :account-service:build -x detekt)
   ```

#### IV. Edit `.env` 

Within the zip, there is an `.env` file that needs to be updated with the right configurations. Here's the context for each configuration option:

1. **POSTGRES_PASSWORD**: This is the password for the PostgreSQL database. It's essential to keep this secure, as it grants access to the database.
2. **PASSWORD_RESET_URL**, **INVITATION_URL**, **VERIFICATION_URL**: These URLs are likely used by the web application to handle user account actions, such as resetting a password, accepting an invitation, or verifying an email address.
3. **SMTP Configuration (SMTP_HOST, SMTP_PORT, MAIL_USER, MAIL_USER_PASSWORD)**: This section configures the Simple Mail Transfer Protocol (SMTP) settings, enabling the application to send emails. In this example, Gmail's SMTP server is being used, and the settings include the host address, port number, email username, and password.
4. **TRINO_ORIGINAL_CATALOG** and **TRINO_DE_IDENTIFIED_CATALOG**: These could be related to the Trino querying engine, specifying catalogs to be used. Trino (formerly known as PrestoSQL) allows querying data across various data sources. The catalog in Trino is a collection of schemas, and a schema is a collection of tables.
5. **Cloud storage service configuration**: This is likely a placeholder for configurations related to a cloud storage service. Specifics would depend on the service being used, such as AWS S3, Azure Blob Storage, etc., and might include keys, bucket names, or other authentication details.

#### V. Enable Account Creation Without Mail Server (Optional)

> This setting allows for direct API calls to SuperTokens. As this increases the risk of a security breach, only make these changes if you do not have access to a mail server. Additionally, make sure that the port used is not accessible from outside the development environment.

Modify the supertokens service under `docker-compose.yml` file as follows to enable account creation and verification without mail server access. After the installation is complete, follow [these steps](#without-mail-server) to create an account.

```
supertokens:
    container_name: hrp-supertokens
    image: supertokens/supertokens-postgresql
    depends_on:
        - postgres
    environment:
        POSTGRESQL_USER: ${POSTGRESQL_USER:-postgres}
        POSTGRESQL_HOST: ${POSTGRESQL_HOST:-hrp-postgres}
        POSTGRESQL_PORT: ${POSTGRESQL_PORT:-5432}
        POSTGRESQL_PASSWORD: ${POSTGRES_PASSWORD:-password}
        POSTGRESQL_DATABASE_NAME: ${POSTGRESQL_DATABASE_NAME:-supertokens}
    ports:
        - "3567:3567"
    networks:
        - hrp
    restart: unless-stopped
```

#### VI. Run

1. Create a Docker network

   Before we start running services, let's create a network for all the services to communicate with each other. In the Docker Compose file, this is defined at the end as the network `hrp`.

   ```bash
   docker network create hrp
   ```

   This creates a bridge network which allows containers connected to it to communicate.

2. Move back to the `<install_path>`

   `cd ..` or `cd <install_path>`

3. Run provided compose file to build and start the backend cluster:

   ```
   docker compose up --build --detach
   ```

   Please note that the supertokens container is optional and is to be replaced with your own authorization service if necessary.

4. Check the backend cluster is up and running.

   ```
   docker ps -a
   ```

   ![viewing-graphs-1](.\install-backend.assets\install-docker-services.png)

### Method 2: Manual Build

> If you prefer to engage with the process, please carefully follow each and every step outlined in method two for creating the files manually. Alternatively, for a more streamlined approach, you can download the necessary files directly from this link: [backend-config-files-v1.zip](https://github.com/S-HealthStack/S-HealthStack.github.io/tree/main/files/installing-the-backend). The choice is yours, depending on your comfort and familiarity with the procedures involved.

#### I: Create a Docker network

Before we start running services, let's create a network for all the services to communicate with each other. In the Docker Compose file, this is defined at the end as the network `hrp`.

```bash
docker network create hrp
```

This creates a bridge network which allows containers connected to it to communicate.

#### II: Start the PostgreSQL Service

1. **Start the PostgreSQL Container**:

   ```bash
   docker run -d --network=hrp --name=hrp-postgres \
   -e POSTGRES_PASSWORD=mypassword \
   -p 5432:5432 \
   --restart=unless-stopped \
   postgres:14.5
   ```

2. **Wait for the PostgreSQL Container to Start**: It might take a few seconds for the PostgreSQL container to initialize. You can check the logs to see when it's ready:

   ```bash
   docker logs -f hrp-postgres
   ```
   To exit the log view and return to the command prompt, simply press Ctrl + C.

3. **Connect to the PostgreSQL Container**:

   ```bash
   docker exec -it hrp-postgres psql -U postgres
   ```

4. **Create the Required Databases**:

   ```sql
   CREATE DATABASE healthstack;
   CREATE DATABASE supertokens;
   CREATE DATABASE tokens;
   \q
   ```

#### III: Start the SuperTokens service

1. **Run the Docker Container:**

   In this step, you'll launch the SuperTokens service, using a PostgreSQL database for storage. SuperTokens is an open-source authentication service. You can learn more about it here: [SuperTokens](https://supertokens.com/). <br><br> If you can utilize a mail server, execute the following command:

   ```bash
   docker run -d --network=hrp --name=hrp-supertokens \
   -e POSTGRESQL_USER=postgres \
   -e POSTGRESQL_HOST=hrp-postgres \
   -e POSTGRESQL_PORT=5432 \
   -e POSTGRESQL_PASSWORD=mypassword \
   -e POSTGRESQL_DATABASE_NAME=supertokens \
   --expose 3567 \
   --restart=unless-stopped \
   supertokens/supertokens-postgresql
   ```

   This command sets up the SuperTokens container with the necessary environment variables and network configurations. The password (`mypassword`) should be the same as what was set in the previous step for the PostgreSQL database. Port `3567` is exposed for communication, and the container will restart automatically unless stopped. <br><br> If you do not have access to a mail server, execute the following command:
   > This setting allows for direct API calls to SuperTokens. As this increases the risk of a security breach, only make these changes if you do not have access to a mail server. Additionally, make sure that the port used is not accessible from outside the development environment.

   ```bash
   docker run -d --network=hrp --name=hrp-supertokens \
   -e POSTGRESQL_USER=postgres \
   -e POSTGRESQL_HOST=hrp-postgres \
   -e POSTGRESQL_PORT=5432 \
   -e POSTGRESQL_PASSWORD=mypassword \
   -e POSTGRESQL_DATABASE_NAME=supertokens \
   -p 3567:3567 \
   --restart=unless-stopped \
   supertokens/supertokens-postgresql
   ```

2. **Verify the Platform Service is Running:**

   ```bash
   sudo docker ps | grep hrp-supertokens
   ```

   This command helps you verify that the `hrp-supertokens` container is running as expected.

#### IV: Start the Account-Service

The Account Service handles various account-related tasks. Here’s how you can build and start it:

1. **Create a Jar file of the account-service**

   ```
   ./gradlew :account-service:build -x detekt
   ```

2. **Move to the `<Install_Path>` and Build the Docker Image:**

   ```
   cd <install_path>
   ```

   ```bash
   docker build -t account-service ./backend-system/account-service/
   ```

   This command builds the Docker image for the account-service using the Dockerfile located in the specified directory. The image is tagged as `account-service`.

3. **Run the Docker Container:**

   ```bash
   docker run -d --network=hrp --name=hrp-account-service \
   -e SMTP_HOST=smtp.gmail.com \
   -e SMTP_PORT=587 \
   -e MAIL_USER=test@gmail.com \
   -e MAIL_USER_PASSWORD=1234567 \
   -e SUPER_TOKEN_URL=http://hrp-supertokens:3567 \
   -e JWK_URL=http://hrp-supertokens:3567/recipe/jwt/jwks \
   -e DB_URL=hrp-postgres:5432 \
   -e DB_USERNAME=postgres \
   -e DB_PASSWORD=mypassword \ # Use the same password set in the previous step
   -e DB_NAME=tokens \
   -e PASSWORD_RESET_URL=http://0.0.0.0/password-reset \
   -e INVITATION_URL=http://0.0.0.0/account-activation \
   -e VERIFICATION_URL=http://0.0.0.0/email-verification \
   -e debug=false \
   --expose 8080 \
   --restart=unless-stopped \
   account-service
   ```

   This command runs the Docker container named `hrp-account-service`. It includes various environment variables for configuration, such as the SMTP settings, SuperTokens URLs, database connection details, and specific URL endpoints. The container is connected to the `hrp` network and exposes port `8080`. It will restart automatically unless stopped. Additionally, customize the values to your own setup if needed. 

   - **Email Settings (`test@gmail.com`, `1234567`)**: Replace these with the actual email address and password used by your application for sending emails. This could be a Gmail address or another SMTP-supported email, along with the corresponding authentication details.
   - **SMTP Settings (`smtp.gmail.com`, `587`)**: These values are specific to Gmail’s SMTP server. If you are using a different email provider, update these values with the correct SMTP host and port.
   - **URLs (`http://0.0.0.0/password-reset`, etc.)**: These URLs are likely used for various account-related actions such as password resetting, account activation, and email verification. Customize them to match the appropriate endpoints within your application.

4. **Verify the Platform Service is Running:**

   ```bash
   sudo docker ps | grep hrp-account-service
   ```

   This command helps you verify that the `hrp-account-service` container is running as expected.

#### V: Start the Platform Service

The Platform service is essential for the application's core functionality. Follow these instructions to build the Docker image and start the Platform service:

1. **Create a JAR File of the Application:**

   ```bash
   ./gradlew :platform:build -x detekt
   ```

   This command will compile the platform module and create a JAR file, excluding any Detekt tasks. Make sure that this JAR file is located where the Dockerfile for the platform expects it.

2. **Move to the `<Install_Path>` and Build the Docker Image:**

   ```
   cd <install_path>
   ```

   ```bash
   docker build -t hrp-platform ./backend-system/platform/
   ```

   This command creates the Docker image for the hrp-platform from the files located in `<install_path>/backend-system/platform/`. The image will be tagged as `hrp-platform`.

3. **Run the Platform Container:**
   ```bash
   docker run -d --network=hrp --name=hrp-platform \
   -e DB_HOST=hrp-postgres \
   -e DB_USERNAME=postgres \
   -e DB_PASSWORD=mypassword \
   -e DB_PORT=5432 \
   -e DB_NAME=healthstack \
   -e DB_SCHEMA=public \
   -e GOOGLE_APPLICATION_CREDENTIALS=service-account-key.json \
   -e JWK_URL=http://hrp-supertokens:3567/recipe/jwt/jwks \
   -e ACCOUNT_SERVICE_URL=http://hrp-account-service:8080 \
   -e debug=false \
   -p 3030:3030 \
   --restart=unless-stopped \
   hrp-platform
   ```

   Ensure `GOOGLE_APPLICATION_CREDENTIALS` is path to the `service-account-key.json` downloaded from Firebase earlier.

4. **Verify the Platform Service is Running:**

   ```bash
   sudo docker ps | grep hrp-platform
   ```


#### VII: Start the Trino Service

Trino, formerly known as Presto, is a high-performance, distributed SQL query engine for big data. It's able to handle a large quantity of data and return queried results in real-time. Here's how you can deploy Trino:

1. **Pull the Trino Docker Image:**
   ```bash
   docker pull trinodb/trino:402
   ```

2. **Create Necessary Directories and Files:**
   Create the following directories and files required for the Trino service configuration:
   ```bash
   mkdir -p rule-update trino/etc/catalog trino/etc/catalog/postgresql trino/etc/catalog/di-postgresql
   touch trino/etc/jvm.config trino/etc/catalog/postgresql/postgresql.properties \
   trino/etc/catalog/di-postgresql/dipostgresql.properties
   ```

3. **Configure JVM Settings:**
   The `jvm.config` file sets various JVM properties that control aspects such as memory allocation, garbage collection, and other operational details of the JVM. Write the necessary configuration parameters into the `jvm.config` file using the following commands:

   ```bash
   echo "\
   -server
   -Xmx16G
   -XX:InitialRAMPercentage=80
   -XX:MaxRAMPercentage=80
   -XX:G1HeapRegionSize=32M
   -XX:+ExplicitGCInvokesConcurrent
   -XX:+ExitOnOutOfMemoryError
   -XX:+HeapDumpOnOutOfMemoryError
   -XX:-OmitStackTraceInFastThrow
   -XX:ReservedCodeCacheSize=512M
   -XX:PerMethodRecompilationCutoff=10000
   -XX:PerBytecodeRecompilationCutoff=10000
   -Djdk.attach.allowAttachSelf=true
   -Djdk.nio.maxCachedBufferSize=2000000
   -XX:+UnlockDiagnosticVMOptions
   -XX:+UseAESCTRIntrinsics
   # Disable Preventive GC for performance reasons (JDK-8293861)
   -XX:-G1UsePreventiveGC" > trino/etc/jvm.config
   ```

4. **Configure Postgres Connection:**
   The `postgresql.properties` file is used to configure the connection to the PostgreSQL database for Trino. This configuration includes essential details like the connector name (for PostgreSQL), connection URL (with hostname, port, and database name), connection user, and connection password.

   ```bash
   echo "\
   connector.name=postgresql
   connection-url=jdbc:postgresql://hrp-postgres:5432/healthstack
   connection-user=postgres
   connection-password=mypassword" > trino/etc/catalog/postgresql/postgresql.properties
   ```

5. **Configure De-identified Postgres Connection:**
   The `dipostgresql.properties` file is used to configure the connection to the PostgreSQL database for de-identified datasets. Customize the variables to connect a different PostgreSQL database instance for de-identified data.

   ```bash
   echo "\
   connector.name=postgresql
   connection-url=jdbc:postgresql://hrp-postgres:5432/healthstack
   connection-user=postgres
   connection-password=mypassword" > trino/etc/catalog/di-postgresql/dipostgresql.properties
   ```

6. **Run the Trino Container:**
   Start the Trino service in a Docker container named `hrp-trino`. Adjust the paths in the volume mappings if you have custom locations for the `jvm.config` and other files:

   ```bash
   docker run -d --network=hrp --name=hrp-trino \
   -v ./rule-update/:/etc/trino/access-control/ \
   -v ./trino/etc/jvm.config:/etc/jvm.config \
   -v ./trino/etc/catalog/postgresql/postgresql.properties:/etc/trino/catalog/postgresql.properties \
   -v ./trino/etc/catalog/di-postgresql/dipostgresql.properties:/etc/trino/catalog/dipostgresql.properties \
   -p 8090:8080 \
   --restart=unless-stopped \
   trinodb/trino:402
   ```

   This sequence of commands ensures that Trino is properly configured and running within your environment. If your configuration files are located in directories other than the ones shown here, make sure to modify the paths in the above commands accordingly.

7. **Verify the Trino Service is Running:**

   ```bash
   sudo docker ps | grep hrp-trino
   ```

#### VIII: Deploy the Data Query Service

1. ##### **Build the Data Query Service Image:**

   Navigate to the `data-query-service` directory inside `backend-system`, then build the Docker image to prepare the Data Query Service for deployment.

   ```bash
   cd <install_path>/backend-system/data-query-service/
   ```

      ```bash
   docker build -t hrp-data-query-service .
      ```

2. **Run the Data Query Service Container:**

      Launch the container, ensuring it's part of the `hrp` network. This container will communicate with the Trino service to query data from your databases. The environment variables below are used to configure the necessary connections and settings.

      ```bash
   docker run -d \
   --network=hrp \
   --name=hrp-data-query-service \
   -e TRINO_ORIGINAL_CATALOG=postgresql \
   -e TRINO_HOST=hrp-trino \
   -e TRINO_PORT=8080 \
   -e JWK_URL=http://hrp-supertokens:3567/recipe/jwt/jwks \
   -e debug=false \
   --expose 3030 \
   --restart=unless-stopped \
   hrp-data-query-service
      ```

   Configuration parameters such as `TRINO_ORIGINAL_CATALOG`, `TRINO_HOST`, `TRINO_PORT`, and `JWK_URL` are used to specify the Trino service connection details and authentication using JSON Web Token keys.

3. **Verify the Deployment:**

      ```bash
   docker ps | grep hrp-data-query-service
      ```


#### IX: Deploy Trino Rule Update Service

Trino Rule Update Service is responsible for updating the rules in Trino. Follow these steps to set up this service:

1. **Build Trino Rule Update Service Image:**

   Navigate to the `trino-rule-update-service` directory inside `backend-system` and build the Docker image.

      ```bash
   ./gradlew :trino-rule-update-service:build -x detekt
   docker build -t trino-rule-update-service .
      ```

2. **Prepare Configuration Files:**

   Navigate to the `<install_path>` directory. Create a `rules.json` file under the previously created `rule-update` directory to define custom rules.

      ```bash
   cd <install_path>
   touch rule-update/rules.json
      ```

     You can populate the `rules.json` file with content, either from an existing file or by creating your own. For example:

      ```bash
   echo "\
   {}
   " > rule-update/rules.json
      ```

3. **Run Trino Rule Update Service Container:**

   Start the Trino Rule Update Service container by executing the following command:

      ```bash
   docker run -d \
   --network hrp \
   --name hrp-trino-rule-update-service \
   -e FIXED_DELAY_MILLISEC=5000 \
   -e ACCOUNT_SERVICE_URL=http://hrp-account-service:8080 \
   -e debug=false \
   -v ./rule-update/rules.json:/etc/trino/access-control/rules.json \
   trino-rule-update-service
      ```

   `FIXED_DELAY_MILLISEC` sets the interval in milliseconds for checking updates, and `ACCOUNT_SERVICE_URL` specifies the URL of the account service.

4. **Verify the Deployment:**

      ```bash
   docker ps | grep hrp-trino-rule-update-service
      ```

#### X: Run Cloud Storage Service Container

1. **Build Cloud Storage Service Image**

   Navigate to the `cloud-storage-service` directory inside `backend-system` and build the image:

   ```bash
   docker build -t cloud-storage-service .
   ```

2. **Run Cloud Storage Service Container**

   Execute the following command to run the cloud storage service container, connecting it with a cloud-based storage solution of your choice. The example command below connects the container to a Google Cloud Platform (GCP) instance.
   > Our backend system supports connections to Google Cloud Platform, Amazon Web Services, and Azure. To connect to a different cloud-based storage solution, replace the environmental variables in the sample command. The necessary variables to connect to each solution can be found [here](https://github.com/S-HealthStack/backend-system/blob/main/cloud-storage-service/src/main/resources/application.yml).

   ```bash
   docker run -d \
   --network hrp \
   --name hrp-cloud-storage-service \
   -e JWK_URL=http://hrp-supertokens:3567/recipe/jwt/jwks \
   -e STORAGE_TYPE=GCP \
   -e SIGNED_URL_DURATION=60 \
   -e GCP_PROJECT_ID=healthstack2023 \
   -e GCP_BUCKET_NAME=mybucket \
   -e GOOGLE_APPLICATION_CREDENTIALS=/etc/gcp/service-account-key.json \
   -v ./service-account-key.json:/etc/gcp/service-account-key.json \
   --expose 8080 \
   --restart=unless-stopped \
   cloud-storage-service
   ```

   - Make sure that the path to `service-account-key.json` is correct; this file contains the credentials needed for connecting to GCP.

3. **Verify Cloud Storage Service is Running**

   ```bash
   docker ps | grep hrp-cloud-storage-service
   ```


#### XI: Configure and Run HAProxy

1. **Create the HAProxy directory and navigate to the directory:**
   
   Run the following commands to create and navigate to the `haproxy` directory.
   ```bash
   cd <install_path>
   mkdir haproxy && cd haproxy
   ```

2. **Create the required three files:**

   ```bash
   touch 404.http cors.lua haproxy.cfg
   ```

3. **Populate the HAProxy service `404.http` file:**

   ```bash
   echo "\
   HTTP/1.0 404 Not Found
   Cache-Control: no-cache
   Connection: close
   Content-Type: text/html
   
   <!DOCTYPE html><html><head><title>404 - Error report</title></head>
   <body>404 Not Found</body>
   </html>" > 404.http
   ```

4. **Populate the `cors.lua` file:**

   ```bash
   echo "\
   --
   -- Cross-origin Request Sharing (CORS) implementation for HAProxy Lua host
   --
   -- CORS RFC:
   -- https://www.w3.org/TR/cors/
   --
   -- Copyright (c) 2019. Nick Ramirez <nramirez@haproxy.com>
   -- Copyright (c) 2019. HAProxy Technologies, LLC.
   
   local M={}
   
   -- Loops through array to find the given string.
   -- items: array of strings
   -- test_str: string to search for
   function contains(items, test_str)
     for _,item in pairs(items) do
       if item == test_str then
         return true
       end
     end
   
     return false
   end
   
   M.wildcard_origin_allowed = function(allowed_origins)
     if contains(allowed_origins, "*") then
       return "*"
     end
     return nil
   end
   
   M.specifies_scheme = function(s)
     return string.find(s, "^%a+://") ~= nil
   end
   
   M.specifies_generic_scheme = function(s)
     return string.find(s, "^//") ~= nil
   end
   
   M.begins_with_dot = function(s)
     return string.find(s, "^%.") ~= nil
   end
   
   M.trim = function(s)
     return s:gsub("%s+", "")
   end
   
   M.build_pattern = function(pattern)
     -- remove spaces
     pattern = M.trim(pattern)
   
     if pattern ~= nil and pattern ~= '' then
       -- if there is no scheme and the pattern does not begin with a dot, 
       -- add the generic scheme to the beginning of the pattern
       if M.specifies_scheme(pattern) == false and M.specifies_generic_scheme(pattern) == false and M.begins_with_dot(pattern) == false then
         pattern = "//" .. pattern
       end
   
       -- escape dots and dashes in pattern
       pattern = pattern:gsub("([%.%-])", "%%%1")
   
       -- an asterisk for the port means allow all ports
       if string.find(pattern, "[:]+%*$") ~= nil then
         pattern = pattern:gsub("[:]+%*$", "[:]+[0-9]+")
       end
   
       -- append end character
       pattern = pattern .. "$"
       return pattern
     end
   
     return nil
   end
   
   -- If the given origin is found within the allowed_origins string, it is returned. Otherwise, nil is returned.
   -- origin: The value from the 'origin' request header
   -- allowed_origins: Comma-delimited list of allowed origins. (e.g. localhost,https://localhost:8080,//test.com)
   --   e.g. localhost                : allow http(s)://localhost
   --   e.g. //localhost              : allow http(s)://localhost
   --   e.g. https://mydomain.com     : allow only HTTPS of mydomain.com
   --   e.g. http://mydomain.com      : allow only HTTP of mydomain.com
   --   e.g. http://mydomain.com:8080 : allow only HTTP of mydomain.com from port 8080
   --   e.g. //mydomain.com           : allow only http(s)://mydomain.com
   --   e.g. .mydomain.com            : allow ALL subdomains of mydomain.com from ALL source ports
   --   e.g. .mydomain.com:443        : allow ALL subdomains of mydomain.com from default HTTPS source port
   -- 
   --  e.g. ".mydomain.com:443, //mydomain.com:443, //localhost"
   --    allows all subdomains and main domain of mydomain.com only for HTTPS from default HTTPS port and allows 
   --    all HTTP and HTTPS connections from ALL source port for localhost
   --    
   M.get_allowed_origin = function(origin, allowed_origins)
     if origin ~= nil then
       -- if wildcard (*) is allowed, return it, which allows all origins
       wildcard_origin = M.wildcard_origin_allowed(allowed_origins)
       if wildcard_origin ~= nil then
         return wildcard_origin
       end
   
       for index, allowed_origin in ipairs(allowed_origins) do
         pattern = M.build_pattern(allowed_origin)
   
         if pattern ~= nil then
           if origin:match(pattern) then
             core.Debug("Test: " .. pattern .. ", Origin: " .. origin .. ", Match: yes")
             return origin
           else
             core.Debug("Test: " .. pattern .. ", Origin: " .. origin .. ", Match: no")
           end
         end
       end
     end
   
     return nil
   end
   
   -- Adds headers for CORS preflight request and then attaches them to the response
   -- after it comes back from the server. This works with versions of HAProxy prior to 2.2.
   -- The downside is that the OPTIONS request must be sent to the backend server first and can't 
   -- be intercepted and returned immediately.
   -- txn: The current transaction object that gives access to response properties
   -- allowed_methods: Comma-delimited list of allowed HTTP methods. (e.g. GET,POST,PUT,DELETE)
   -- allowed_headers: Comma-delimited list of allowed headers. (e.g. X-Header1,X-Header2)
   function preflight_request_ver1(txn, allowed_methods, allowed_headers)
     core.Debug("CORS: preflight request received")
     txn.http:res_set_header("Access-Control-Allow-Methods", allowed_methods)
     txn.http:res_set_header("Access-Control-Allow-Headers", allowed_headers)
     txn.http:res_set_header("Access-Control-Max-Age", 600)
     core.Debug("CORS: attaching allowed methods to response")
   end
   
   -- Add headers for CORS preflight request and then returns a 204 response.
   -- The 'reply' function used here is available in HAProxy 2.2+. It allows HAProxy to return
   -- a reply without contacting the server.
   -- txn: The current transaction object that gives access to response properties
   -- origin: The value from the 'origin' request header
   -- allowed_methods: Comma-delimited list of allowed HTTP methods. (e.g. GET,POST,PUT,DELETE)
   -- allowed_origins: Comma-delimited list of allowed origins. (e.g. localhost,localhost:8080,test.com)
   -- allowed_headers: Comma-delimited list of allowed headers. (e.g. X-Header1,X-Header2)
   function preflight_request_ver2(txn, origin, allowed_methods, allowed_origins, allowed_headers)
     core.Debug("CORS: preflight request received")
   
     local reply = txn:reply()
     reply:set_status(204, "No Content")
     reply:add_header("Content-Type", "text/html")
     reply:add_header("Access-Control-Allow-Methods", allowed_methods)
     reply:add_header("Access-Control-Allow-Headers", allowed_headers)
     reply:add_header("Access-Control-Max-Age", 600)
   
     local allowed_origin = M.get_allowed_origin(origin, allowed_origins)
   
     if allowed_origin == nil then
       core.Debug("CORS: " .. origin .. " not allowed")
     else
       core.Debug("CORS: " .. origin .. " allowed")
       reply:add_header("Access-Control-Allow-Origin", allowed_origin)
   
       if allowed_origin ~= "*" then
         reply:add_header("Vary", "Accept-Encoding,Origin")
       end
     end
   
     core.Debug("CORS: Returning reply to preflight request")
     txn:done(reply)
   end
   
   -- When invoked during a request, captures the origin header if present and stores it in a private variable.
   -- If the request is OPTIONS and it is a supported version of HAProxy, returns a preflight request reply.
   -- Otherwise, the preflight request header is added to the response after it has returned from the server.
   -- txn: The current transaction object that gives access to response properties
   -- allowed_methods: Comma-delimited list of allowed HTTP methods. (e.g. GET,POST,PUT,DELETE)
   -- allowed_origins: Comma-delimited list of allowed origins. (e.g. localhost,localhost:8080,test.com)
   -- allowed_headers: Comma-delimited list of allowed headers. (e.g. X-Header1,X-Header2)
   function cors_request(txn, allowed_methods, allowed_origins, allowed_headers)
     local headers = txn.http:req_get_headers()
     local transaction_data = {}
     local origin = nil
     local allowed_origins = core.tokenize(allowed_origins, ",")
     
     if headers["origin"] ~= nil and headers["origin"][0] ~= nil then
       core.Debug("CORS: Got 'Origin' header: " .. headers["origin"][0])
       origin = headers["origin"][0]
     end
   
     -- Bail if client did not send an Origin
     -- for example, it may be a regular OPTIONS request that is not a CORS preflight request
     if origin == nil or origin == '' then
       return
     end
     
     transaction_data["origin"] = origin
     transaction_data["allowed_methods"] = allowed_methods
     transaction_data["allowed_origins"] = allowed_origins
     transaction_data["allowed_headers"] = allowed_headers
   
     txn:set_priv(transaction_data)
   
     local method = txn.sf:method()
     transaction_data["method"] = method
   
     if method == "OPTIONS" and txn.reply ~= nil then
       preflight_request_ver2(txn, origin, allowed_methods, allowed_origins, allowed_headers)
     end
   end
   
   -- When invoked during a response, sets CORS headers so that the browser can read the response from permitted domains.
   -- txn: The current transaction object that gives access to response properties.
   function cors_response(txn)
     local transaction_data = txn:get_priv()
   
     if transaction_data == nil then
       return
     end
     
     local origin = transaction_data["origin"]
     local allowed_origins = transaction_data["allowed_origins"]
     local allowed_methods = transaction_data["allowed_methods"]
     local allowed_headers = transaction_data["allowed_headers"]
     local method = transaction_data["method"]
   
     -- Bail if client did not send an Origin
     if origin == nil or origin == '' then
       return
     end
   
     local allowed_origin = M.get_allowed_origin(origin, allowed_origins)
   
     if allowed_origin == nil then
       core.Debug("CORS: " .. origin .. " not allowed")
     else
       if method == "OPTIONS" and txn.reply == nil then
         preflight_request_ver1(txn, allowed_methods, allowed_headers)
       end
       
       core.Debug("CORS: " .. origin .. " allowed")
       txn.http:res_set_header("Access-Control-Allow-Origin", allowed_origin)
   
       if allowed_origin ~= "*" then
         txn.http:res_add_header("Vary", "Accept-Encoding,Origin")
       end
     end
   end
   
   -- Register the actions with HAProxy
   core.register_action("cors", {"http-req"}, cors_request, 3)
   core.register_action("cors", {"http-res"}, cors_response, 0)
   
   return M
   " > cors.lua
   ```

5. **Populate the `haproxy.cfg` file:**

   ```
   echo "\
   global
   	lua-load /usr/local/etc/haproxy/cors.lua
   defaults
   	log global
   	mode http
   	timeout connect 5000ms
   	timeout client 50000ms
   	timeout server 50000ms
   	option httplog
   	log stdout local0
   
   frontend stats
   	bind *:8404
   	stats enable
   	stats uri /
   	stats refresh 10s
   frontend http_frontend
   	bind :8080
   	compression algo gzip
   	compression type text/css text/html text/javascript application/javascript text/plain text/xml application/json
   
   	# CORS configuration
   	# please update CORS configuration if you want to restrict API access 
   	# http-request lua.cors "GET,PUT,POST" "example.com,localhost,localhost:8080" "X-Custom-Header1,X-Custom-Header2"
   
   	http-request capture req.hdr(Origin) len 20
   	http-request lua.cors "*" "*" "*"
   	http-response lua.cors 
   	
   	acl has_account-service path_beg /account-service
       	acl has_sql_query path_reg ^\/api\/projects\/[0-9]*\/sql$
       	acl has_graphql_query path_reg ^\/api\/projects\/[0-9]*\/graphql$
       	acl has_platform path_beg /api/projects
   	acl has_storage path_beg /cloud-storage
      
       	use_backend account-service if has_account-service
       	use_backend query-service if has_sql_query
       	use_backend query-service if has_graphql_query
   	use_backend platform if has_platform
   	use_backend storage-service if has_storage
   	
   	default_backend empty
   
   
   backend platform
   	http-request set-header Host localhost
   	http-response set-header Server None
   	server platform hrp-platform:3030 check
   backend account-service
   	http-request set-header Host localhost
   	http-response set-header Server None
   	server account-service hrp-account-service:8080 check
   backend query-service
   	http-request set-header Host localhost
   	http-response set-header Server None
   	server query-service hrp-data-query-service:3030 check
   backend storage-service
           http-request set-header Host localhost
           http-response set-header Server None
           server query-service hrp-cloud-storage-service:8080 check
   
   
   backend empty
   	errorfile 503 /usr/local/etc/haproxy/errors/404.http
   " > haproxy.cfg
   
   ```

6. **Run the HAProxy container with the following command:**

   ```
   cd <install_path>
   docker run -d \
   --network hrp \
   --name hrp-balancer \
   -p 8080:8080 \
   -p 8404:8404 \
   -v ./haproxy/haproxy.cfg:/usr/local/etc/haproxy/haproxy.cfg:ro \
   -v ./haproxy/404.http:/usr/local/etc/haproxy/errors/404.http:ro \
   -v ./haproxy/cors.lua:/usr/local/etc/haproxy/cors.lua:ro \
   --restart=unless-stopped \
   haproxy:2.7
   ```

7. **Confirm that the HAProxy container is running:**

   ```bash
   docker ps -a | grep hrp-balancer
   ```


### Conclusion

You've successfully deployed the entire system using Docker CLI commands. All the services are now running and communicating with each other within the custom bridge network named 'hrp'.

You can verify the status of all containers by running:

```bash
docker ps -a
```

And manage the network with:

```bash
docker network ls
docker network inspect hrp
```

### Wrap Up

#### Create Initial Account

> If you intend to use the web portal and a mail server, skip this step and proceed to [web portal installation and setup](install-portal.md).

##### With Mail Server

When a mail server is available, perform these steps:

1. Create an account for the initial user.

   ```
   curl --location --request POST 'localhost:8080/account-service/signup' --header 'Content-Type: application/json'--data-raw '{
     "email": "your_address@your_email.com",
     "password": "your_password",
     "profile": {}
   }'
   
   ```

2. Check the account activation email and activate the login.

> The system `Team Admin` [team role](../../portal-guide/study-management/role-based-access-control.md) to the first user to create an account. Because this role has advanced access privileges to the Samsung Health Stack, we recommend that your system administrator creates the first account.

##### Without Mail Server

> The following steps can only be executed if the relevant SuperTokens port settings were changed. If the commands return a 404 response, make sure that port 3567 was mapped to the hrp-supertokens container.

When a mail server is not available, perform these steps:

1. Create the `Team Admin` team role.

   ```
   curl --location --request PUT 'localhost:3567/recipe/role' --header 'Content-Type: application/json' --data-raw '{ "role": "team-admin" }'
   ```

   > Successful result:
   >
   > ```
   > {
   > "status": "OK",
   > "createdNewRole":true
   > }
   > ```

2. Create the initial user login.

   ```
   curl --location --request POST 'localhost:3567/recipe/signup' \
   --header 'cdi-version: 2.15' \
   --header 'Content-Type: application/json' \
   --data-raw '{ "email": "your_address@your_email.com", "password": "your_password"}'
   ```

   > Successful result is similar to:
   >
   > ```
   > {
   > "status": "OK",
   > "user": {
   > "email": "your_address@your_email.com",
   > "id": "785d492b-688f-49c1-adbb-e9c00ed0c5b4",
   > "timeJoined": 1664864683438
   > }
   > }
   > ```

3. Copy the returned `id` to the `userId` field in the following command to assign the `Team Admin` team role to the user.

   ```
   curl --location --request PUT 'localhost:3567/recipe/user/role' \
   --header 'Content-Type: application/json' \
   --data-raw '{
     "userId": "785d492b-688f-49c1-adbb-e9c00ed0c5b4",
     "role": "team-admin"
   }'
   
   ```

   > Successful result:
   >
   > ```
   > {
   > "status": "OK",
   > "didUserAlreadyHaveRole":false
   > }
   > ```

4. Copy the returned `email` to the `email` field and the returned `id` to the `userId` field in the following command to retrieve a verifcation token.

   ```
   curl --location --request POST 'localhost:3567/recipe/user/email/verify/token' \
   --header 'Content-Type: application/json' \
   --data-raw '{
     "userId": "7e5b869e-ed96-4768-9595-93a459f9f5ad",
     "email": "team-admin@samsung.com"
   }'
   
   ```

   > Successful result:
   >
   > ```
   > {
   > "status":"OK",
   > "token":"MTEwMjg5OTNjY2...ZDY0ZjUyZjc0M2Vj"
   > }
   > ```

5. Copy the returned `token` to the `token` field to activate your account.

   ```
   curl --location --request POST 'localhost:3567/recipe/user/email/verify' \
   --header 'Content-Type: application/json' \
   --data-raw '{
       "method": "token",
       "token": "MTEwMjg5OTNjY2...ZDY0ZjUyZjc0M2Vj"
   }'
   ```

   > Successful result:
   >
   > ```
   > {
   > "status":"OK",
   > "userId":"7e5b869e-ed96-4768-9595-93a459f9f5ad",
   > "email":"team-admin@samsung.com"
   > }
   > ```
   