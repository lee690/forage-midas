# Midas
Project repo for the JPMC Advanced Software Engineering Forage program

## In this project...

Your team has been asked to build out the Midas system, a high-profile, high-stakes project which is sure to attract the right kind of attention if you can pull it off. In other words, doing well on this project would be an excellent career move. The Midas system architecture has already been nailed down, and tasking has been distributed to the various members of your team. You will be working on Midas Core - the component which receives, validates, and records financial transactions. This component depends on quite a few external resources - Kafka to receive new transactions, a SQL database to record and validate them, and a REST API to incentivize them. Your job over the course of this program will be to integrate all of these disparate resources into the final system.

One of your teammates has already put together a scaffold for the project according to the proposed system architecture. They managed to define a few classes, but otherwise, the codebase is quite bare. Midas Core uses Spring Boot, which should make the job of integrating external resources far easier than it would be with vanilla Java. Spring Boot - an extension of Spring - provides your application with a robust Dependency Injection framework, and takes care of much of the boilerplate associated with connecting your application to external dependencies. Spring Boot adopts a somewhat opinionated view of how your application should communicate with the aforementioned resources, but in this case, that’s a good thing - it saves us quite a bit of time wiring everything together. Your first task is to get your local development environment set up, familiarize yourself with the codebase, and make some last-minute preparations before you begin work on the project in earnest.

## Technology Used

This project will involve several key technologies based on the description of the Midas system architecture and requirements. Here’s a summary of the technologies used:

#### 1. Java 17
The main programming language for building the Midas Core, which handles transaction processing, validation, and integration with other components.
Java 17 is a long-term support (LTS) version, providing stability and modern Java features.

#### 2. Spring Boot
Spring Boot simplifies Java development, especially for web applications and microservices.
In this project, Spring Boot will handle dependency injection, RESTful API creation, and integration with other resources like databases and message brokers.

#### 3. Apache Kafka
Kafka is a distributed messaging system used for handling real-time data feeds.
In the Midas system, Kafka will receive incoming financial transactions, which Midas Core will then process. This allows transactions to be efficiently queued, received, and processed in a scalable way.

#### 4. SQL Database (likely PostgreSQL or MySQL)
A relational database will be used to store, validate, and retrieve transaction records.
SQL databases provide a structured way to store data and enforce data integrity, which is crucial for handling financial transactions.

#### 5. H2 Database (for Development and Testing)
H2 is an in-memory relational database commonly used for development and testing in Java projects.
It allows you to test database-related logic without needing to set up a full database server.

#### 6. REST API
The project will expose a REST API to handle incentives or other functions related to transactions.
Spring Boot makes it straightforward to create REST endpoints, which will allow other components or services to interact with Midas Core.

#### 7. Maven
Maven is a build automation and dependency management tool for Java projects.
It helps manage project dependencies, build the project, and simplify configurations.

#### 8. Test Containers and Spring Boot Testing Framework
Test Containers (such as Kafka from org.testcontainers) and Spring Boot Testing will be used for unit and integration testing.

These tools help simulate external services, such as Kafka and databases, allowing you to test components of Midas Core independently.
This tech stack will allow you to build a scalable, testable, and highly reliable transaction processing system.
