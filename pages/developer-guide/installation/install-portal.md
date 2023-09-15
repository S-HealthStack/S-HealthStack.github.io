---
title: Installing the Web Portal
sidebar: doc_sidebar
permalink: install-portal.html
toc: false
---

## System Requirements

To operate the backend system, you must have one of the following:

- A 64-bit Mac OS (Intel or ARM)
- A 64-bit Linux machine (Ubuntu or Debian)

## Prerequisites

- Successfully installed and running backend system (refer to the [backend system installation guide](install-backend.md)).
- Docker installed on your machine. If it's not, please follow this [guide to install Docker](https://docs.docker.com/get-docker/).

## I. (Optional) Create Development Environment

This section is only required if you are planning to make changes to the source code.

1. Install NodeJS version 16.15.0 or higher from [https://nodejs.org/en/download/](https://nodejs.org/en/download/).

2. Setup the Yarn package manager:

    1. Run `corepack enable` in your terminal to activate Yarn.

    2. Inside your project directory, run `yarn` to install project dependencies.

    3. Run `yarn dev` to start the yarn development server.

## II. Build a Production Environment

1. Clone the portal repository from GitHub by running 

    ```
    git clone https://github.com/S-HealthStack/web-portal.git
    ```

2. Navigate to the cloned repository.

    ```
    cd web-portal
    ```

3. Determine your `API_URL` and `PUBLIC_PATH`. Here `API_URL` is the base API URL to access endpoints and `PUBLIC_PATH` is the path that will be used to host the app.

4. Build a Docker image with the desired variables provided as build arguments:

    ```
    docker build . -t open-source-portal \
    --build-arg API_URL="http://localhost:8080" \
    --build-arg PUBLIC_PATH='/' \
    --build-arg MOCK_API='/api'
    ```

5. Run the Docker image:

    ```
    docker run -d -p 8081:80 open-source-portal
    ```

At this point, the resulting Docker image is running nginx on port `80`.

> If you prefer to build static files instead of using Docker:
>
> 1. Install NodeJS version 16.15.0 or higher.
> 2. Run `corepack enable` to activate yarn.
> 3. Run `yarn` to install dependencies.
> 4. Run `yarn build` with desired variables set using environment. For example, `API_URL=https://example.com yarn build`.

The resulting static files will be located in the `/build` folder and can be hosted using any web server.

## III. Launch Web Portal and Create Account

1. Open your web browser (Chrome is recommended as of this writing) and navigate to your `PUBLIC_PATH` URL, for example: `http://localhost:8081/`.

2. In the **Sign in** dialog box that appears, click **Create account**.

3. Follow the prompts to generate an account activation email.

4. Open the email and complete the account creation and sign in process.

> Note: If you are the very first person to create an account, the system adds the `Team Admin` team role to your account settings. This role has advanced access privileges to the system, therefore it's recommended for your system administrator to create the first account.

