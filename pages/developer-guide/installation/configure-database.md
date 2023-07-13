---
title: Configuring the Database
permalink: configure-database.html
sidebar: doc_sidebar
toc: false
---

## Configuring the Database

The Samsung Health Stack is build to work with PostgreSQL Database. There are two methods to configure PostgreSQL database. You can edit `application.yml` or use `application.properties`

### Using application.yml

`application.yml` file contains configuration settings for a Spring Framework application. To connect your PostgreSQL database, update the following properties in the `codeconfig` section located at `platform/src/main/resources/application.yml`within the backend-system's directory:

```
codeconfig:
  db:
    url: postgresql://${DB_HOST}:${DB_PORT}/${DB_NAME}
    host: ${DB_HOST}
    port: ${DB_PORT}
    name: ${DB_NAME}
    schema: ${DB_SCHEMA}
    user: ${DB_USERNAME}
    password: ${DB_PASSWORD}
```

- `DB_HOST`: Replace with the hostname or IP address of your PostgreSQL server.
- `DB_PORT`: Replace with the port number on which your PostgreSQL server listens (default is 5432).
- `DB_NAME`: Replace with the name of your PostgreSQL database.
- `DB_SCHEMA`: Replace with the schema name (if applicable) you want to use for your application.
- `DB_USERNAME`: Replace with the username for your PostgreSQL database.
- `DB_PASSWORD`: Replace with the password for your PostgreSQL database.

For example, if your PostgreSQL server is listening on `localhost` and you have a database named `mydatabase` with a schema named `public`, and you want to use the username `myusername` and password `mypassword`, you would update the `config` section as follows:

```
config:
  db:
    url: postgresql://localhost:5432/mydatabase
    host: localhost
    port: 5432
    name: mydatabase
    schema: public
    user: myusername
    password: mypassword
```

After making these changes, save the `application.yml` file and restart your Spring application.



### Using application.properties 

To connect to your own PostgreSQL database using `application.properties` file in a Spring Boot application, you can set the following properties:

```
codespring.datasource.url=jdbc:postgresql://localhost:5432/mydatabase
spring.datasource.username=myusername
spring.datasource.password=mypassword
```

Here, `spring.datasource.url` is the JDBC URL to connect to your PostgreSQL database, which includes the database server hostname (`localhost` in this example), the port number (`5432` in this example), and the name of the database (`mydatabase` in this example). You can update these values as per your PostgreSQL configuration.

The `spring.datasource.username` and `spring.datasource.password` properties are used to specify the username and password to connect to your PostgreSQL database.

You can also set additional properties such as `spring.datasource.driver-class-name` to specify the JDBC driver class name if it's not included in your classpath.

Once you have updated the `application.properties` file, you can start your Spring Boot application and it should be able to connect to your PostgreSQL database using the specified configuration.



## Understanding `application.yml` file

`application.yml` file contains configuration settings for a Spring Framework application. Let's break it down section by section:

```
codeconfig:
  db:
    url: postgresql://${DB_HOST}:${DB_PORT}/${DB_NAME}
    host: ${DB_HOST}
    port: ${DB_PORT}
    name: ${DB_NAME}
    schema: ${DB_SCHEMA}
    user: ${DB_USERNAME}
    password: ${DB_PASSWORD}
  new-database-config:
    prefix: project_
    postfix: _research
  jwks:
    url: ${JWK_URL:http://127.0.0.1:3567/recipe/jwt/jwks}
  account-service:
    url: ${ACCOUNT_SERVICE_URL:http://127.0.0.1:8080}
```

This section defines various configuration properties under the `config` namespace. It includes:

- `db`: A set of properties defining the URL, host, port, database name, schema, username, and password for a PostgreSQL database.
- `new-database-config`: A set of properties defining a prefix and postfix to use when creating a new database.
- `jwks`: A property defining the URL for a JSON Web Key Set (JWKS) endpoint.
- `account-service`: A property defining the URL for an account service.

```
codelogging:
  level:
    root: info
```

This section sets the logging level for the application to `info`. This means only messages with a severity of `INFO`, `WARN`, `ERROR`, or `FATAL` will be logged.

```
codespring:
  flyway:
    url: jdbc:${config.db.url}
    user: ${config.db.user}
    password: ${config.db.password}
```

This section defines configuration settings for the Flyway database migration tool, which is a popular tool for managing database schema changes. It includes:

- `url`: The JDBC URL for the PostgreSQL database, using the `config.db.url` property defined earlier.
- `user`: The username for connecting to the PostgreSQL database, using the `config.db.user` property defined earlier.
- `password`: The password for connecting to the PostgreSQL database, using the `config.db.password` property defined earlier.

```
server:
  port: 3030
```

This section defines the port on which the application will listen for incoming requests. In this case, it will listen on port 3030.

Overall, this `application.yml` file defines a set of configuration properties for a Spring Framework application, including settings for connecting to a PostgreSQL database and managing database schema changes using the Flyway migration tool.