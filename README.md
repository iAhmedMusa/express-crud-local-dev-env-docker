# Basic Dockerized CRUD Application with Expressjs, Ejs and MongoDB

## Overview

This is a simple CRUD (Create, Read, Update, Delete) application built with Expressjs and MongoDB. The application is dockerized, allowing for easy deployment and scalability. The application can be configured using environment variables. A Docker Compose file are given there.

### Features

- Basic CRUD operations: Create, Read, Update, and Delete.
- Dockerized application for easy deployment.

### Prerequisites

Before running the application, make sure you have the following installed:

- Docker: [Install Docker](https://docs.docker.com/get-docker/)

## Setup

1. Clone the repository:

   ```bash
   git clone https://github.com/iAhmedMusa/express-crud-local-dev-env-docker.git
   cd express-crud-local-dev-env-docker
   ```

2. Set environment variables in the ``docker-compose`` file with the following content:

   ```env
   - MONGODB_SERVER=localhost
   - MONGODB_ADMINUSERNAME=admin
   - MONGODB_ADMINPASSWORD=password
   - DB_NAME=test_DB
   ```

   Update the values according to your preferences.

3. Run the command:

   ```bash
   docker-compose up --build
   ```

## Usage

Access the application at [http://localhost:3000](http://localhost:3000) after running the docker compose.

## Contributors

- Ahmed
- ahmedmusa.swe@gmail.com

Feel free to contribute and improve this basic CRUD application!