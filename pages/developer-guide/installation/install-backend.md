---
title: Installing the Backend System
sidebar: doc_sidebar
permalink: install-backend.html
toc: false

---

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

#### IV. Run

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
   docker compose up -d
   ```

   Please note that the supertokens container is optional and is to be replaced with your own authorization service if necessary.

4. Check the backend cluster is up and running.

   ```
   docker ps -a
   ```

   ![viewing-graphs-1](./../../../../../../images/install-docker-services.png)

#### V. [Create Initial Account](#create-initial-account-anchor)

### Method 2: Manual Build (Under Construction)

> You can download [backend-config-files-v1.zip](https://github.com/S-HealthStack/S-HealthStack.github.io/blob/main/files/installing-the-backend/baI will schedule some time for us to connect.kend-config-files-v1.zip) from [GitHub directory](https://github.com/S-HealthStack/S-HealthStack.github.io/tree/main/files/installing-the-backend). Extract the contents to your chosen temporary location, and move each desired file into place as you encounter them in the steps below.

#### I: Create a Docker network

Before we start running services, let's create a network for all the services to communicate with each other. In the Docker Compose file, this is defined at the end as the network `hrp`.

```bash
docker network create hrp
```

This creates a bridge network which allows containers connected to it to communicate.

#### II: Start the PostgreSQL service

In the Docker Compose file, the first service defined is `postgres`. We will start this service first.

```bash
docker run -d --network=hrp --name=hrp-postgres \
-e POSTGRES_PASSWORD=mypassword \
-e POSTGRES_MULTIPLE_DATABASES="healthstack, supertokens, tokens" \
-p 5432:5432 \
-v ./multi_db:/docker-entrypoint-initdb.d \
--restart=unless-stopped \
postgres:14.5
```

This command is running the `postgres:14.5` Docker image as a container named `hrp-postgres`. The `-e` option sets environment variables, `-p` exposes ports, `-v` mounts volumes, and `--restart` configures the restart policy.

#### III: Start the SuperTokens service

SuperTokens is an open-source authentication service.

```bash
docker run -d --network=hrp --name=hrp-supertokens \
--depends-on hrp-postgres \
-e POSTGRESQL_USER=postgres \
-e POSTGRESQL_HOST=hrp-postgres \
-e POSTGRESQL_PORT=5432 \
-e POSTGRESQL_PASSWORD=mypassword \
-e POSTGRESQL_DATABASE_NAME=supertokens \
-p 3567:3567 \
--restart=unless-stopped \
supertokens/supertokens-postgresql
```

This command uses the `supertokens/supertokens-postgresql` image. It sets environment variables using `-e`, and exposes port `3567` with `-p`.

#### IV: Start the Account-Service

This service likely handles account-related tasks such as authentication and password reset. Here is how to start it:

```bash
docker build -t account-service ./backend-system/account-service/

docker run -d --network=hrp --name=hrp-account-service \
--depends-on hrp-supertokens \
-e SMTP_HOST=smtp.gmail.com \
-e SMTP_PORT=587 \
-e MAIL_USER=test@gmail.com \
-e MAIL_USER_PASSWORD=1234567 \
-e SUPER_TOKEN_URL=http://hrp-supertokens:3567 \
-e JWK_URL=http://hrp-supertokens:3567/recipe/jwt/jwks \
-e DB_URL=hrp-postgres:5432 \
-e DB_USERNAME=postgres \
-e DB_PASSWORD=mypassword \
-e DB_NAME=tokens \
-e PASSWORD_RESET_URL=http://192.168.50.146/password-reset \
-e INVITATION_URL=http://192.168.50.146/account-activation \
-e VERIFICATION_URL=http://192.168.50.146/email-verification \
-e debug=false \
-p 8080:8080 \
--restart=unless-stopped \
account-service
```

This command first builds the Docker image for the account-service using the Dockerfile located in `./backend-system/account-service/` directory. The resulting image is tagged as `account-service`. Then it runs this image as a container named `hrp-account-service`.

#### V: Start the Platform service

```bash
docker build -t hrp-platform ./backend-system/platform/

docker run -d --network=hrp --name=hrp-platform \
--depends-on hrp-postgres \
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

#### VI: Start the Trino service

```bash
docker run -d --network=hrp --name=hrp-trino \
--depends-on hrp-postgres \
-p 8090:8080 \
-v ./rule-update/:/etc/trino/access-control/ \
-v ./trino/etc/jvm.config:/etc/jvm.config \
-v ./trino/etc/catalog/postgresql/postgresql.properties:/etc/trino/catalog/postgresql.properties \
-v ./trino/etc/catalog/di-postgresql/dipostgresql.properties:/etc/trino/catalog/dipostgresql.properties \
--restart=unless-stopped \
trinodb/trino:402
```

#### VII: Start the Data-Query-Service

```bash
docker build -t hrp-data-query-service ./backend-system/data-query-service/

docker run -d --network=hrp --name=hrp-data-query-service \
--depends-on hrp-trino \
-e TRINO_ORIGINAL_CATALOG=postgresql \
-e TRINO_HOST=hrp-trino \
-e TRINO_PORT=8080 \
-e JWK_URL=http://hrp-supertokens:3567/recipe/jwt/jwks \
-e debug=false \
-p 3030:3030 \
--restart=unless-stopped \
hrp-data-query-service
```

#### VIII: Run Trino Container

```bash
docker run -d \
--network hrp \
--name hrp-trino \
-p 8090:8080 \
-v ./rule-update/:/etc/trino/access-control/ \
-v ./trino/etc/jvm.config:/etc/jvm.config \
-v ./trino/etc/catalog/postgresql/postgresql.properties:/etc/trino/catalog/postgresql.properties \
-v ./trino/etc/catalog/di-postgresql/dipostgresql.properties:/etc/trino/catalog/dipostgresql.properties \
trinodb/trino:402
```

- This command launches the Trino container, a distributed SQL query engine that will connect with your PostgreSQL database.
- The necessary configuration files and rules are mounted into the container.

#### IX: Run Data Query Service Container

##### Build Data Query Service Image

Navigate to the `data-query-service` directory inside `backend-system` and build the image:

```bash
docker build -t hrp-data-query-service .
```

##### Run Data Query Service container

```bash
docker run -d \
--network hrp \
--name hrp-data-query-service \
-e TRINO_ORIGINAL_CATALOG=postgresql \
-e TRINO_HOST=hrp-trino \
-e TRINO_PORT=8080 \
-e JWK_URL=http://hrp-supertokens:3567/recipe/jwt/jwks \
-e debug=false \
hrp-data-query-service
```

- This step runs the Data Query Service container, which connects to the Trino service for querying data from your databases.
- Environment variables configure connections and other settings.

#### X: Run Trino Rule Update Service Container

##### Build Trino Rule Update Service Image

Navigate to the `trino-rule-update-service` directory inside `backend-system` and build the image:

```bash
docker build -t trino-rule-update-service .
```

##### Run Trino Rule Update Service container

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

- This container runs the service responsible for updating the rules in Trino.

#### XI: Run Cloud Storage Service Container

##### Build Cloud Storage Service Image

Navigate to the `cloud-storage-service` directory inside `backend-system` and build the image:

```bash
docker build -t cloud-storage-service .
```

##### Run Cloud Storage Service container

```bash
docker run -d \
--network hrp \
--name hrp-cloud-storage-service \
-e JWK_URL=http://hrp-supertokens:3567/recipe/jwt/jwks \
-e STORAGE_TYPE=GCP \
-e GCP_PROJECT_ID=healthstack2023 \
-e GCP_BUCKET_NAME=mybucket \
-e GCP_SIGNED_URL_DURATION=60 \
-e AWS_REGION=aws_region \
-e AWS_ACCESS_KEY_ID=aws_key \
-e AWS_SECRET_ACCESS_KEY=aws_secret_access_key \
-e AWS_BUCKET_NAME=aws_bucket \
-e AWS_PRE_SIGNED_URL_DURATION=60 \
-v ./service-account-key.json:/etc/gcp/service-account-key.json \
cloud-storage-service
```

- This command runs the cloud storage service, which connects with Google Cloud Platform and AWS for cloud-based storage solutions.

#### XII: Run HAProxy Container

```bash
docker run -d \
--network hrp \
--name hrp-balancer \
-p 8080:8080 \
-p 8404:8404 \
-v ./haproxy/haproxy.cfg:/usr/local/etc/haproxy/haproxy.cfg:ro \
-v ./haproxy/404.http:/usr/local/etc/haproxy/errors/404.http:ro \
-v ./haproxy/cors.lua:/usr/local/etc/haproxy/cors.lua:ro \
haproxy:2.7
```

- This command runs the HAProxy container, which balances the load between various services in your architecture, ensuring efficient distribution of network traffic.

### Conclusion

You've successfully deployed the entire system using Docker CLI commands. All the services are now running and communicating with each other within the custom bridge network named 'hrp'.

You can verify the status of all containers by running:

```bash
docker ps
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
     "password": "your_password"
   }'
   
   ```

2. Check the account activation email and activate the login.

> The system `Team Admin` [team role](../../portal-guide/study-management/role-based-access-control.md) to the first user to create an account. Because this role has advanced access privileges to the Samsung Health Stack, we recommend that your system administrator creates the first account.

##### Without Mail Server

When a mail server is not available, perform these steps:

1. Create the `Team Admin` team role.

   ```
   curl --location --request PUT 'localhost:8080/recipe/role' --header 'Content-Type: application/json' --data-raw '{ "role": "team-admin" }'
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
   curl --location --request POST 'localhost:8080/recipe/signup' \
   --header 'cdi-version: 2.15' \
   --header 'Content-Type: application/json' \
   --data-raw '{ "email": "your_address@your_email.com", "password": "your_password" }'
   ```

   > Successful result is similar to:
   >
   > ```
   > {
   > "status": "OK",
   > "user": {
   >    "email": "your_address@your_email.com",
   >    "id": "785d492b-688f-49c1-adbb-e9c00ed0c5b4",
   >    "timeJoined": 1664864683438
   > }
   > }
   > ```

3. Copy the returned `id` to the `userId` field in the following command to assign the `Team Admin` team role to the user.

   ```
   curl --location --request PUT 'localhost:8080/recipe/user/role' \
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
   curl --location --request POST 'localhost:8080/recipe/user/email/verify/token' \
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
   curl --location --request POST 'localhost:8080/recipe/user/email/verify' \
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


