# Fleet Manager

A Spring Boot-based backend application for fleet management operations.

---

## 🛠️ Tech Stack & Requirements

- **Java Version:** 17
- **Framework:** Spring Boot `4.1.1`
- **Build Tool:** Maven (via `./mvnw` wrapper)
- **Database:** PostgreSQL

---

## 📦 Injected Dependencies

Below is the complete list of dependencies configured in `pom.xml`:

### 1. Core & Runtime Dependencies

| Group ID | Artifact ID | Scope / Option | Description |
| :--- | :--- | :--- | :--- |
| `org.springframework.boot` | `spring-boot-starter-data-jpa` | Compile | Provides Spring Data JPA with Hibernate for Object-Relational Mapping (ORM) and data persistence. |
| `org.springframework.boot` | `spring-boot-starter-flyway` | Compile | Integrates Flyway for automated relational database schema migrations. |
| `org.springframework.boot` | `spring-boot-starter-security` | Compile | Spring Security starter providing authentication, authorization, and protection against common exploits. |
| `org.springframework.boot` | `spring-boot-starter-webmvc` | Compile | Spring MVC starter for building RESTful Web Services and Web applications. |
| `org.flywaydb` | `flyway-database-postgresql` | Compile | Flyway extension supporting PostgreSQL database migration tasks. |
| `org.postgresql` | `postgresql` | `runtime` | Official PostgreSQL JDBC driver for database connectivity. |
| `org.projectlombok` | `lombok` | `optional` | Annotation library to reduce boilerplate code (getters, setters, builders, constructors). |

---

### 2. Testing Dependencies

| Group ID | Artifact ID | Scope | Description |
| :--- | :--- | :--- | :--- |
| `org.springframework.boot` | `spring-boot-starter-data-jpa-test` | `test` | Test suite and utilities specifically for testing Data JPA repositories and entities. |
| `org.springframework.boot` | `spring-boot-starter-flyway-test` | `test` | Utilities and test support for verifying Flyway database migrations. |
| `org.springframework.boot` | `spring-boot-starter-security-test` | `test` | Support for testing Spring Security rules, annotations, and mock user contexts. |
| `org.springframework.boot` | `spring-boot-starter-webmvc-test` | `test` | MockMVC and Web-layer testing utilities for Spring MVC controllers. |

---

### 3. Maven Build Plugins & Annotation Processors

- **`spring-boot-maven-plugin`**: Packages the project as an executable JAR/WAR archive and manages application execution.
- **`maven-compiler-plugin`**: Configured with annotation processor paths for `lombok` to auto-generate getters, setters, and constructors during compilation.

---

## 📁 Directory Structure

```
fleet-manager/
├── client/                                  # Frontend client application (placeholder)
├── server/                                  # Backend Spring Boot source directory
│   ├── main/
│   │   ├── java/com/fleet_manager/demo/     # Application source code & entry point
│   │   └── resources/                       # Configs (application.properties), db migrations, templates
│   └── test/                                # Integration and unit tests
├── .mvn/                                    # Maven wrapper configuration
├── mvnw / mvnw.cmd                          # Maven wrapper execution scripts
├── pom.xml                                  # Maven project object model & dependencies
└── README.md                                # Project documentation
```

---

## 🚀 Getting Started

### Prerequisites
- JDK 17 installed
- PostgreSQL instance running locally or via Docker

### Build the Project
```bash
./mvnw clean package
```

### Run the Application
```bash
./mvnw spring-boot:run
```
