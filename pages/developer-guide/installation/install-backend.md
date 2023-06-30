---
title: Installing the Backend System
sidebar: doc_sidebar
permalink: install-backend.html
toc: false
---

{% include warning.html title="Warning" content="Documentation for v1.0 official release is currently under construction. Note that the information on this page may be outdated." %}

Follow these instructions to install, build, and verify the backend system.

# System Requirements

To operate the backend system, the system requirement are:

- A 64-bit Linux machine running Ubuntu or Debian either as bare metal or a cloud instance.
- Access to the local machine or development server as a non-root user with sudo privileges. 

> The following installation steps are for the Ubuntu/Debian environment.

# Prerequisites

## I. Update the Environment

1. Open a Linux terminal window.

2. Make sure your environment system packages are up to date.

   ```
   sudo apt update
   sudo apt upgrade
   ```

## II. Install Java 17

1. Install the OpenJDK package.

   ```
   sudo apt install -y openjdk-17-jdk-headless unzip
   ```

2. Verify that you have successfully installed version 17.

   ```
   java -version
   ```

## III. Install Docker and Docker Compose

1. Follow the instructions at https://docs.docker.com/engine/install/ubuntu/ to install Docker and Docker Compose.
   
2. Confirm successful installation.
      ```
      sudo docker --version
      sudo systemctl status docker
      ```

# Build

>  For your convenience, we've created some config files for you. To optionally use them, navigate to [this GitHub directory](https://github.com/S-HealthStack/S-HealthStack.github.io/tree/main/files/installing-the-backend){:target="_blank"}, download [**backend-config-files.zip**](https://github.com/S-HealthStack/S-HealthStack.github.io/blob/main/files/installing-the-backend/backend-config-files.zip), extract the contents to your chosen temporary location, and move each desired file into place as you encounter them in the steps below.

## IV. Create a Network

   1. Create a docker network repository proxy (hrp) to connect docker containers.

      ```
      sudo docker network create hrp
      ```

## V. Clone Backend System

1. If you do not have Git, install it using the instruction here: [Git - Installing Git (git-scm.com)](https://git-scm.com/book/en/v2/Getting-Started-Installing-Git)

2. Download the latest implementation of the Samsung Health Stack backend system from GitHub.

   ```
   git clone https://github.com/S-HealthStack/backend-system
   ```

3. Move to the backend-system directory. Most of 

   ```
   cd backend-system
   ```



## VI. Deploy Postgres

1. If you wish to connect to the running Postgres container, follow the [Configuring the Database](configure-database.md) page instructions.

2. If you wish to use a new PostgreSQL, start the PostgreSQL object-relational database system container.

   ```
   sudo docker run \
     -d \
     --name hrp-postgres \
     --network hrp \
     -e POSTGRES_PASSWORD=password \
     postgres:14.5
   ```
   ***Understanding:***
   
   This command creates a Docker container based on the PostgreSQL 14.5 image, sets the container name to `hrp-postgres`, connects the container to the Docker network `hrp`, and sets the environment variable `POSTGRES_PASSWORD` to `password`.

## VII. Deploy SuperTokens

You don't have to use SuperTokens. You can implement a backend adapter to complement the authorization service of your choice. If you choose to use supertokens:
1. In Postgres, create a database named `supertokens`.

2. Deploy [SuperTokens](https://supertokens.com/){:target="_blank"}.

   ```
   sudo docker run \
     -p 3567:3567 \
     --name hrp-supertokens \
     --network hrp \
     -e POSTGRESQL_USER=postgres \
     -e POSTGRESQL_HOST=hrp-postgres \
     -e POSTGRESQL_PORT=5432 \
     -e POSTGRESQL_PASSWORD=password \
     -e POSTGRESQL_DATABASE_NAME=supertokens \
     -d \
     supertokens/supertokens-postgresql
   ```

## VIII. Deploy Account Service

1. In Postgres, create a database named `tokens`.

2. Create a Docker image of account-service.

   ```
   ./gradlew :account-service:build -x detekt
    sudo docker build --tag hrp-account-service:0.9.0 ./account-service/
   ```

3. Deploy the account service and identify your mail server.

   ```
   sudo docker run \
     -p 8080:8081 \
     --name hrp-account-service \
     --network hrp \
     -e SMTP_HOST=smtp.server.addr \
     -e SMTP_PORT=smtp_port \
     -e MAIL_USER=username \
     -e MAIL_USER_PASSWORD=password \
     -e SUPER_TOKEN_URL=http://hrp-supertokens:3567 \
     -e JWK_URL=http://hrp-supertokens:3567/recipe/jwt/jwks \
     -e DB_URL=hrp-postgres:5432 \
     -e DB_NAME=tokens \
     -e DB_USERNAME=postgres \
     -e DB_PASSWORD=password \
     -d \
     hrp-account-service:0.9.0
   ```
   
   ***Understanding:***
   
   This command runs a Docker container for an account service, with various environment variables set. The container is based on the `hrp-account-service:0.9.0` image and is named `hrp-account-service`. It is connected to the `hrp` network, and it exposes port `8080` on the Docker host. The environment variables set in the container include the SMTP server host address and port, email account credentials, super token URL, JWK URL, PostgreSQL database URL, database name, username, and password. These values should be customized to match the value you want to use in your environment.

## IX. Create Firebase Service Account

1. If you do not have an account, create a Firebase account and a project with default settings by visiting: [Firebase (google.com)](https://firebase.google.com/)

2. Go to the [Firebase console]([Firebase console](https://console.firebase.google.com/)) and select your project.

3. Click on the gear icon in the top left corner to access your project settings.

4. Click on the **Service accounts** tab.

5. Click **Generate new private key** button to generate a new service account key file.

6. Return to the terminal and create a Firebase **service-account-key.json** file.

   ```
   cd <install_path>/backend-system/platform
   touch service-account-key.json
   ```

7. Update the **service-account-key.json** file with the private key generated in step 5 using the instructions at [https://firebase.google.com/docs/admin/setup?authuser=0](https://firebase.google.com/docs/admin/setup?authuser=0){:target="_blank"}.
   >  Be sure to keep this file private and securely stored. It contains your unique security key.

## X. Deploy Platform

1. Test and format the code.
   
   ```
   ./gradlew :platform:ktlintFormat test
   ```
   
2. Create a jar file of the application.

   ```
   ./gradlew :platform:build -x detekt
   ```

3. Create a Docker image of hrp-platform 0.9.0 in the platform directory.

   ```
   sudo docker build --tag hrp-platform:0.9.0 ./platform/
   ```

4. In Postgres, create a database named `healthstack`.

5. Run the hrp-platform container.

   ```
   sudo docker run \
     -d \
     -p 3030:3030 \
     --name hrp-platform \
     --network hrp \
     -e DB_HOST=hrp-postgres \
     -e DB_NAME=healthstack \
     -e DB_USERNAME=postgres \
     -e DB_PASSWORD=password \
     -e GOOGLE_APPLICATION_CREDENTIALS=service-account-key.json \
     -e JWK_URL=http://hrp-supertokens:3567/recipe/jwt/jwks \
     -e ACCOUNT_SERVICE_URL=http://hrp-account-service:8081 \
     hrp-platform:0.9.0
   ```

6. Verify the hrp-platform container is running.

   ```
   sudo docker ps | grep hrp-platform
   ```

## XI. Deploy trino-rule-update-service

1. If **trino-rule-update-service** directory does not exist create the directory.

   ```
   mkdir trino-rule-update-service
   ```

2. If the **trino-rule-update-service/Dockerfile** does not exist or does not contain the following content create the file with the following content:

   ```
   FROM openjdk:17.0.2-jdk-oracle
   ARG JAR_FILE=build/libs/*.jar
   COPY ${JAR_FILE} application.jar
   ENTRYPOINT ["java","-jar","/application.jar"]
   ```

3. Create a Docker image of trino-rule-update-service.

   ```
   ./gradlew :trino-rule-update-service:build -x detekt
    
   sudo docker build --tag hrp-trino-rule-update-service:0.9.0 ./trino-rule-update-service/
   ```

4. Create a healthstack directory at the root level of your system or at a location of your choice.

   ```
   mkdir /root/healthstack
   ```

5. Create a **rule-update** directory inside the healthstack directory.

   ```
   mkdir /root/healthstack/rule-update
   ```

6. Create a `rules.json` file inside the `rule-update` directory. You can use the optionally provided file from the GitHub zip file located at: **backend-config-files\rule-update** or create your own file with your custom rules.

   ```
   touch /root/healthstack/rule-update/rules.json
   ```

7. Add content to **rules.json**

   ```
   echo "\
   {
     "catalogs": [
       {
         "user": "admin",
         "catalog": ".*",
         "allow": "all"
       },
       {
         "catalog": "postgresql",
         "allow": "all"
       },
       {
         "catalog": "system",
         "allow": "none"
       }
     ],
     "tables": [
       {
         "user": "7149a094-944d-4348-9793-ad33178525be",
         "catalog": "postgresql",
         "schema": "project_1_research",
         "table": ".*",
         "privileges": [
           "SELECT"
         ]
       },
       {
         "user": "7149a094-944d-4348-9793-ad33178525be",
         "catalog": "postgresql",
         "schema": "project_2_research",
         "table": ".*",
         "privileges": [
           "SELECT"
         ]
       },
       {
         "user": "7149a094-944d-4348-9793-ad33178525be",
         "catalog": "postgresql",
         "schema": "project_4_research",
         "table": ".*",
         "privileges": [
           "SELECT"
         ]
       },
       {
         "user": ".*",
         "privileges": []
       }
     ]
   }
   " > /root/healthstack/rule-update/rules.json
   ```

8. Deploy trino-rule-update-service.

   ```
   sudo docker run \
     --name hrp-trino-rule-update-service \
     --network hrp \
     -e FIXED_DELAY_MILLISEC=5000 \
     -e ACCOUNT_SERVICE_URL=http://hrp-account-service:8080 \
     -v /root/healthstack/rule-update:/etc/trino/access-control \
     -d \
     hrp-trino-rule-update-service:0.9.0
   ```

## XII. Deploy Trino

1. Download trinodb/trino version 402.

   ```
   sudo docker pull trinodb/trino:402
   ```

2. Move to the **healthstack** directory within root, if not there.

3. Create **catalog** directory and **jvm.config**

   ```
   mkdir -p trino/etc/catalog && touch trino/etc/catalog/jvm.config 
   ```

4. Create the **trino/etc/catalog/jvm.config** file with these contents:

   ```
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
   -XX:ReservedCodeCacheSize=256M
   -XX:PerMethodRecompilationCutoff=10000
   -XX:PerBytecodeRecompilationCutoff=10000
   -Djak.attach.allowAttachSelf=true
   -Didk.nio.maxCachedBufferSize=2000000
   -XX:+UnlockDiagnosticVMOptions
   -XX:+UseAESCTRIntrinsics" > trino/etc/catalog/jvm.config
   ```

5. Ensure you are in **healthstack** directory and create necessary directory and file for **postgresql.properties**

   ```
   mkdir -p trino/etc/postgresql && touch trino/etc/postgresql/postgresql.properties 
   ```

6. Create the **trino/etc/postgresql/postgresql.properties** file with these contents:

   ```
   connector.name=postgresql
   connection-url=jdbc:postgresql://hrp-postgres:5432/healthstack
   connection-user=postgres
   connection-password=password
   ```

7. Run the hrp-trino container trinodb/trino image (mapping the hrp-trino default port 8080).

   ```
   sudo docker run \
     -d \
     --name hrp-trino \
     --network hrp \
     -v /root/healthstack/rule-update:/etc/trino/access-control \
     -v /root/healthstack/trino/etc/catalog/jvm.config:/etc/trino/jvm.config \
     -v /root/healthstack/trino/etc/postgresql/postgresql.properties:/etc/trino/catalog/postgresql.properties \
     trinodb/trino:402
   ```



## XIII. Deploy data-query-service

1. Change the directory to the **backend-system**

2. Build the application data-query-service and generate a jar file, performing a code test.

   ```
   ./gradlew :data-query-service:build -x detekt
   ```

3. Create a Docker image of data-query-service tag 0.9.0 in the **data-query-service** directory.

   ```
   sudo docker build --tag hrp-data-query-service:0.9.0 ./data-query-service/
   ```

4. Run the hrp-data-query-service container.

   ```
   sudo docker run \
     -d \
     -p 3031:3031 \  
     --name hrp-data-query-service \
     --network hrp \
     -e TRINO_CATALOG=postgresql \
     -e TRINO_DEFAULT_USER=postgres \
     -e TRINO_HOST=hrp-trino \
     -e TRINO_PORT=8080 \
     -e JWK_URL=http://hrp-supertokens:3567/recipe/jwt/jwks \
     hrp-data-query-service:0.9.0
   ```

5. Verify hrp-data-query-service is running.

   ```
   sudo docker ps
   ```

## XIV. Haproxy Configuration

1. Change directory to the **/root/healthstack**

2. Create **haproxy** directory and move into it

   ```
   mkdir haproxy && cd haproxy 
   ```

3. Create required **four** files. These files are also available within the .zip to copy and paste.

   ```
   touch 404.http cors.lua cors-origins.lst haproxy.cfg
   ```

4. Create the Haproxy service **haproxy/404.http** file with these contents:

   ```
   echo "\ 
   HTTP/1.0 404 Not Found
   Cache-Control: no-cache
   Connection: close
   Content-Type: text/html
   <!DOCTYPE html><html><head><title>404 - Error report</title></head>
   <body>404 Not Found</body>
   </html>" > 404.http
   ```

5. Create the **haproxy/cors.lua** file with these contents:

   ```
   echo "\ 
   core.register_service("cors-response", "http", function(applet)
   applet:set_status(200)
   applet:add_header("Content-Length","0")
   applet:add_header("Access-Control-Allow-Origin",applet.headers["origin"][0])
   applet:add_header("Access-Control-Allow-Credentials","true")
   applet:add_header("Access-Control-Allow-Headers","*")
   applet:add_header("Access-Control-Allow-Methods","GET, HEAD, POST, PUT, DELETE, PATCH, OPTIONS")
   applet:add_header("Access-Control-Max-Age", "1728000")
   applet:start_response()
   end)" > cors.lua
   ```

6. Create the **haproxy/cors-origins.lst** file with these contents:

   ```
   echo "\ 
   localhost.*
   .*\.mydomain\.com:[8080|8443]" > cors-origins.lst
   ```

7. Create the **haproxy/haproxy.cfg** file with these contents:

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
   bind :3035
   compression algo gzip
   compression type text/css text/html text/javascript application/javascript text/plain text/xml application/json
    
   # CORS configuration
   # capture origin HTTP header
   capture request header origin len 128
   # add Access-Control-Allow-Origin HTTP header to response if origin matches the list of allowed URLs
   http-response add-header Access-Control-Allow-Origin %[capture.req.hdr(0)] if !METH_OPTIONS { capture.req.hdr(0) -m reg -f /usr/local/etc/haproxy/cors-origins.lst }
   # if a preflight request is made, use CORS preflight backend
   http-request use-service lua.cors-response if METH_OPTIONS { capture.req.hdr(0) -m reg -f /usr/local/etc/haproxy/cors-origins.lst }
    
   acl has_account-service path_beg /account-service
   acl has_sql_query path_reg ^\/api\/projects\/[0-9]*\/sql$
   acl has_graphql_query path_reg ^\/api\/projects\/[0-9]*\/graphql$
   acl has_platform path_beg /api/projects
    
   use_backend account-service if has_account-service
   use_backend query-service if has_sql_query
   use_backend query-service if has_graphql_query
   use_backend platform if has_platform
   default_backend empty
    
   backend platform
   http-request set-header Host localhost
   http-response set-header Server None
   server platform hrp-platform:3030 check
    
   backend account-service
   http-request set-header Host localhost
   http-response set-header Server None
   server account-service hrp-account-service:8081 check
       
   backend query-service
   http-request set-header Host localhost
   http-response set-header Server None
   server query-service hrp-data-query-service:3031 check
    
   backend empty
   errorfile 503 /usr/local/etc/haproxy/errors/404.http" > haproxy.cfg
   ```

8. Run the hrp-proxy container.

   ```
   sudo docker run \
     -d \
     -p 3035:3035 \
     -p 8404:8404 \
     --name hrp-proxy \
     --network hrp \
     -v /root/healthstack/haproxy/haproxy.cfg:/usr/local/etc/haproxy/haproxy.cfg:ro 
     -v /root/healthstack/haproxy/404.http:/usr/local/etc/haproxy/errors/404.http:ro 
     -v /root/healthstack/haproxy/cors-origins.lst:/usr/local/etc/haproxy/cors-origins.lst:ro -v /root/healthstack/haproxy/cors.lua:/usr/local/etc/haproxy/cors.lua:ro  
     haproxy:2.6.6
   ```

## XV. Deploy docker-compose.yml

1. Create the **docker-compose.yml** file with these contents:
   ```
   version: '3.5'
    
   services:
     postgres:
       container_name: hrp-postgres
       image: postgres:14.5
       environment:
         POSTGRES_PASSWORD: ${POSTGRES_PASSWORD:-password}
       ports:
         - "5432:5432"
       networks:
         - hrp
       restart: unless-stopped
     supertokens:
       container_name: hrp-supertokens
       image: supertokens/supertokens-postgresql
       depends_on:
           - postgres
       environment:
           POSTGRESQL_USER: ${POSTGRESQL_USER:-postgres}
           POSTGRESQL_HOST: ${POSTGRESQL_HOST:-hrp-postgres}
           POSTGRESQL_PORT: ${POSTGRESQL_PORT:-5432}
           POSTGRESQL_PASSWORD: ${POSTGRESQL_PASSWORD:-password}
           POSTGRESQL_DATABASE_NAME: ${POSTGRESQL_DATABASE_NAME:-supertokens}
       ports:
           - "3567:3567"
       networks:
           - hrp
     platform:
       container_name: hrp-platform
       image: hrp-platform:0.9.0
       depends_on:
           - postgres
       environment:
           DB_HOST: ${DB_HOST:-hrp-postgres}
           DB_PASSWORD: ${DB_HOST:-password}
           GOOGLE_APPLICATION_CREDENTIALS:    ${GOOGLE_APPLICATION_CREDENTIALS:-service-account-key.json}
           JWK_URL: ${JWK_URL:-http://hrp-supertokens:3567/recipe/jwt/jwks}
           ACCOUNT_SERVICE_URL: ${ACCOUNT_SERVICE_URL:-http://hrp-account-service:8081}
       ports:
           - "3030:3030"
       networks:
         - hrp
     account-service:
       container_name: hrp-account-service
       image: hrp-account-service:0.9.0
       depends_on:
           - supertokens
       environment:
           SMTP_HOST: ${SMTP_HOST:-smtp.gmail.com}
           SMTP_PORT: ${SMTP_PORT:-465}
           MAIL_USER: ${MAIL_USER:-testl@gmail.com}
           MAIL_USER_PASSWORD: ${MAIL_USER_PASSWORD:-PasswordTest}
           SUPER_TOKEN_URL: ${SUPER_TOKEN_URL:-http://hrp-supertokens:3567}
           JWK_URL: ${JWK_URL:-http://hrp-supertokens:3567/recipe/jwt/jwks}
         
       ports:
           - "8081:8081"
       networks:
           - hrp
     trino:
       container_name: hrp-trino
       image: trinodb/trino:402
       depends_on:
           - postgres
       ports:
           - "8080:8080"
       volumes:
           - ./rule-update/:/etc/trino/access-control/
           - ./trino/etc/catalog/jvm.config:etc/trino/jvm.config 
           - ./trino/etc/postgresql/postgresql.properties:/etc/trino/catalog/postgresql.properties
       networks:
           - hrp
    
     data-query-service:
       container_name: hrp-data-query-service
       image: hrp-data-query-service:0.9.0
       depends_on:
           - trino
       environment:
           TRINO_CATALOG: ${TRINO_CATALOG:-postgresql}
           TRINO_HOST: ${TRINO_HOST:-hrp-trino}
           TRINO_PORT: ${TRINO_PORT:-8080}
           JWK_URL: ${JWK_URL:-http://hrp-supertokens:3567/recipe/jwt/jwks}
           debug: true
       ports:
           - "3031:3031"
       networks:
           - hrp
     trino-rule-update-service:
       container_name: hrp-trino-rule-update-service
       image: hrp-trino-rule-update-service:0.9.0
       environment:
           FIXED_DELAY_MILLISEC: ${FIXED_DELAY_MILLISEC:-5000}
           ACCOUNT_SERVICE_URL: ${ACCOUNT_SERVICE_URL:-http://hrp-account-service:8081}
       depends_on:
           - account-service
       volumes:
           - ./rule-update/rules.json:/etc/trino/access-control/rules.json
       networks:
           - hrp
     web:
       container_name: open-source-portal
       image: docker.io/library/open-source-portal
       depends_on:
           - account-service
       ports:
         - "80:80"
       networks:
         - hrp
       restart: unless-stopped
     haproxy:
       image: haproxy:2.6.6
       container_name: hrp-balancer
       depends_on:
           - web
       ports:
         - "3035:3035"
         - "8404:8404"
       volumes:
           - ./haproxy/haproxy.cfg:/usr/local/etc/haproxy/haproxy.cfg:ro
           - ./haproxy/404.http:/usr/local/etc/haproxy/errors/404.http:ro
           - ./haproxy/cors-origins.lst:/usr/local/etc/haproxy/cors-origins.lst:ro
           - ./haproxy/cors.lua:/usr/local/etc/haproxy/cors.lua:ro
       networks:
         - hrp
       restart: unless-stopped
    networks:
     hrp:
       external: true
       driver: bridge
   ```
   
2. Start the **docker-compose.yml** file.

   ```
   sudo docker-compose up -d
   ```

3. Retrieve logs of the container present at the time of execution.

   ```
   sudo docker logs -f hrp-platform
   ```


# Wrap Up

## XVI. Create Initial Account

> If you intend to use the web portal and a mail server, skip this step and proceed to [web portal installation and setup](install-portal.md).

### With Mail Server
When a mail server is available, perform these steps:

1. Create an account for the initial user.

   ```
   curl --location --request POST 'localhost:8080/account-service/signup'
   --header 'Content-Type: application/json'
   --data-raw '{
     "email": "your_address@your_email.com",
     "password": "your_password"
   }'
   ```
2. Check the account activation email and activate the login.
> The system `Team Admin` [team role](../../portal-guide/study-management/role-based-access-control.md) to the first user to create an account. Because this role has advanced access privileges to the Samsung Health Stack, we recommend that your system administrator creates the first account.


### Without Mail Server
When a mail server is not available, perform these steps:

1. Create the `Team Admin` team role.

   ```
   curl --location --request PUT 'localhost:3567/recipe/role'
   --header 'Content-Type: application/json'
   --data-raw '{ "role": "team-admin" }'
   ```

   > Successful result: 
   >
   > ```
   > {
   >   "status": "OK",
   >   "createdNewRole":true
   > }
   > ```

2. Create the initial user login.

   ```
   curl --location --request POST 'localhost:3567/recipe/signup'
   --header 'cdi-version: 2.15'
   --header 'Content-Type: application/json'
   --data-raw '{ "email": "your_address@your_email.com", "password": "your_password" }'
   ```

   > Successful result is similar to: 
   >
   > ```
   > {
   >   "status": "OK",
   >   "user": {
   >       "email": "your_address@your_email.com",
   >       "id": "785d492b-688f-49c1-adbb-e9c00ed0c5b4",
   >       "timeJoined": 1664864683438
   >   }
   > }
   > ```

3. Copy the returned `id` to the `userId` field in the following command to assign the `Team Admin` team role to the user.

   ```
   curl --location --request PUT 'localhost:3567/recipe/user/role'
   --header 'Content-Type: application/json'
   --data-raw '{
     "userId": "785d492b-688f-49c1-adbb-e9c00ed0c5b4",
     "role": "team-admin"
   }'
   ```

   > Successful result: 
   >
   > ```
   > {
   >   "status": "OK",
   >   "didUserAlreadyHaveRole":false
   > }
   > ```

4. Copy the returned `email` to the `email` field and the returned `id` to the `userId` field in the following command to retrieve a verifcation token.

   ```
   $ curl --location --request POST 'localhost:3567/recipe/user/email/verify/token' \
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
   >   "status":"OK",
   >   "token":"MTEwMjg5OTNjY2...ZDY0ZjUyZjc0M2Vj"
   > }
   > ```

5. Copy the returned `token` to the `token` field to activate your account.

   ```
   $ curl --location --request POST 'localhost:3567/recipe/user/email/verify' \
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
   >   "status":"OK",
   >   "userId":"7e5b869e-ed96-4768-9595-93a459f9f5ad",
   >   "email":"team-admin@samsung.com"
   > }
   > ```

<!-- ## XIV. Launch the Web Portal-->

<!-- 1. In Chrome, navigate to http://localhost. -->

<!-- 2. Specify the port you configured in the **haproxy.cfg** file.-->

<!--    1. Press F12 to open the inspector.-->
<!--    2. Click the **Application** tab.-->
<!--    3. Select **Local Storage > localhost**.-->
<!--    4. Change the value for the `API_URL` key to `http://localhost:3035`.-->
<!-- 3. Press F5 to reload the page and open the web portal.-->

<!-- ## XIV. Verify Project Access-->

<!-- 1. Test the API calls.-->

<!--   ```-->
<!--   curl --location --request GET localhost:3030/api/projects-->
<!--   ```-->

<!--   > If you get an unauthorized message, the platform has deployed successfully.-->

<!-- ## XV. Launch the Web Portal-->
