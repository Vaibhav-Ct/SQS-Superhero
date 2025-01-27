# SQS Based SuperHeroes Management System 🦸‍♂️

## Introduction
Welcome to the **SuperHeroes Management System**! This project is a simple Spring Boot application designed to manage superhero data. You can create, retrieve, update, and delete superhero records using RESTful APIs.

## Features
- 🌟 Insert a new superhero using POST requests.
- 🔍 Retrieve superhero details by name or universe using GET requests.
- 🔄 Update existing superhero details using PUT requests.
- ❌ Delete a superhero by name using DELETE requests.

# SQS Superhero Service

## Overview

`SQS Superhero Service` is a Spring Boot-based application that manages superhero data and leverages Amazon Simple Queue Service (SQS) for handling asynchronous message processing. The service includes functionalities to add, update, delete, and query superhero records while efficiently managing message queues for real-time updates.

## Features

- **AWS SQS Integration**: Uses AWS SQS for decoupled messaging and asynchronous processing.
- **CRUD Operations**: Offers endpoints for creating, reading, updating, and deleting superhero records.
- **Spring Boot Powered**: Utilizes Spring Boot for streamlined application setup and deployment.
- **RESTful API**: Accessible interfaces for smooth interaction with the application.

## Setup and Installation

### Prerequisites

- Java 11 or higher
- Maven or Gradle
- AWS Account with access to SQS
- Configured AWS CLI or AWS SDK with necessary credentials

### Installation Steps

1. **Clone the Repository**

    ```bash
    https://github.com/Vaibhav-Ct/SQS-Superhero.git
    cd sqs-superhero-service
    ```

2. **Configure AWS Credentials**

    Ensure your AWS credentials are configured. This can be done using the AWS CLI with `aws configure`, or by setting environment variables:

    ```bash
    export AWS_ACCESS_KEY_ID=your_access_key_id
    export AWS_SECRET_ACCESS_KEY=your_secret_access_key
    ```

3. **Configure Application Properties**

    Open `src/main/resources/application.properties` and configure your SQS settings:

    ```properties
    aws.sqs.queue.url=your_sqs_queue_url
    aws.sqs.region=your_aws_region
    ```

4. **Build and Run the Application**

    If you are using Maven, run:

    ```bash
    mvn spring-boot:run
    ```

    Or if you are using Gradle:

    ```bash
    ./gradlew bootRun
    ```

## API Endpoints

- **GET /api/superhero**
  - Retrieve a list of superheroes, optionally filtered by name or universe.

- **POST /api/superhero**
  - Create a new superhero.

- **PUT /api/superheroes/{name}**
  - Update superhero details based on the name.

- **DELETE /api/superheroes/{name}**
  - Delete a superhero based on the name.

- **PUT /api/update_async?name={update_name}**
  - Send an asynchronous update message with the superhero name.

## Technology Stack

- **Java 11**
- **Spring Boot**
- **AWS SQS**
- **AWS SDK for Java v2** for SQS integration
- **Gradle/Maven**

