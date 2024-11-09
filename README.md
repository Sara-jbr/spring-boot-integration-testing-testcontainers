# Spring Boot Integration Testing with Testcontainers

This repository demonstrates how to use **Testcontainers** in **Spring Boot** for integration testing. Testcontainers provide lightweight, disposable containers that can run databases or other services, enabling reliable and isolated tests in Spring Boot applications.

## What is Spring Boot Testcontainers?

**Spring Boot Testcontainers** is a library that allows developers to run Docker containers during integration tests. This is especially useful for tests that require external services like databases, message brokers, or even web servers, as it lets each test run in an isolated, reproducible environment. By leveraging Docker containers, Testcontainers ensures that every integration test has a consistent environment, making it easier to test against actual dependencies in a realistic way without relying on a local setup or a shared testing infrastructure.

- **Isolation**: Each test has its own environment, reducing dependency conflicts.
- **Consistency**: Tests run in identical environments every time, regardless of the developer’s machine setup.
- **Flexibility**: Various services, databases, and configurations can be easily adjusted by changing the container setup.

### Why Use Testcontainers?

In traditional integration testing, setting up databases or other dependencies can be complex and environment-dependent. By using Docker containers, Testcontainers simplifies this setup, making tests more consistent and portable.

### Common Use Cases

- **Database Integration Tests**: Running tests against a real instance of a database (like PostgreSQL, MySQL, MongoDB) in a container instead of using an in-memory database.
- **Messaging Services**: Testing services that depend on message brokers like Kafka or RabbitMQ in a realistic, containerized environment.
- **Microservices**: Spinning up multiple containers to test how services interact in an isolated environment.

## Prerequisites

To run this project, ensure you have the following:

1. [**Java**](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html): JDK 11 or higher
2. [**Spring Boot**](https://spring.io/projects/spring-boot): Version 2.5 or higher
3. [**Docker**](https://www.docker.com/get-started): Installed and running on your machine
4. [**Maven**](https://maven.apache.org/download.cgi): For building and running tests

## Getting Started

Follow these steps to set up and run the integration tests with Testcontainers.

### 1. Clone the Repository

Clone this repository to your local machine:
```bash
git clone https://github.com/yourusername/yourrepository.git
cd yourrepository
```
## Install dependencies

```bash
mvn clean install
```
## Run tests
### To run All tests:

```bash
mvn test
```
### To run specific test:

```bash
mvn test -Dtest=YourTestClass#methodName
```
