# Basic CRUD Application with Dockerized MongoDB

## Overview

This is a simple CRUD (Create, Read, Update, Delete) application built with Node.js, Express, and MongoDB. The application is dockerized, allowing for easy deployment and scalability. The MongoDB server is also containerized and can be configured using environment variables.

### Features

- Basic CRUD operations: Create, Read, Update, and Delete.
- Dockerized application for easy deployment.
- MongoDB container with configurable environment variables.

## Prerequisites

Before running the application, make sure you have the following installed:

- Docker: [Install Docker](https://docs.docker.com/get-docker/)
- Node.js: [Install Node.js](https://nodejs.org/)

## Setup

1. Clone the repository:

   ```bash
   git clone https://github.com/iAhmedMusa/express-crud-local-dev-env-docker.git
   cd express-crud-local-dev-env-docker
   ```

2. Install Node.js dependencies:

   ```bash
   npm install
   ```

3. Create a `.env` file in the project root with the following content:

   ```env
   MONGODB_SERVER=localhost
   MONGODB_ADMINUSERNAME=admin
   MONGODB_ADMINPASSWORD=password
   DB_NAME=test_DB
   ```

   Update the values according to your preferences.

## Dockerization

The application and MongoDB are dockerized for easy deployment. To build and run the Docker containers, follow these steps:

1. Build the Docker image:

   ```bash
   docker build -t your-image-name .
   ```

2. Run the Docker container:

   ```bash
   docker run -p 3000:3000 --env-file .env your-image-name
   ```

   Replace `your-image-name` with a suitable name for your Docker image.

## Environment Variables

### For Application (`server.js`)

- `PORT`: Port on which the application will run. Default is `3000`.

### For configuration MongoDB

- `MONGODB_SERVER`: MongoDB server address. Default is `localhost`.
- `MONGODB_ADMINUSERNAME`: MongoDB admin username. Default is `admin`.
- `MONGODB_ADMINPASSWORD`: MongoDB admin password. Default is `password`.
- `DB_NAME`: MongoDB database name. Default is `test_DB`.


## Usage

Access the application at [http://localhost:3000](http://localhost:3000) after running the Docker container.

## Contributors

- Ahmed
- ahmedmusa.swe@gmail.com

Feel free to contribute and improve this basic CRUD application!