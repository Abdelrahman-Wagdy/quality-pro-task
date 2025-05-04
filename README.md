Welcome to quality pro repo. Uploaded to this repo 2 zip files each representing a task.


# PetStore API Testing Project

## Overview

This project contains automated API tests for the PetStore API using TestNG, RestAssured, and Allure for reporting. The tests cover CRUD operations for the User endpoints of the Swagger PetStore API.

## 🛠 Prerequisites

* Java 18 or higher
* Maven 3.6 or higher
* Docker (optional, for containerized execution)

## 📂 Project layout

```
PetStore/
├── src/
│   ├── main/
│   │   └── java/
│   │       ├── models/
│   │       │   └── UserModel.java
│   │       ├── services/
│   │       │   └── UserServices.java
│   │       └── utils/
│   │           └── Config.java
│   └── test/
│       ├── java/
│       │   └── usertests/
│       │       └── UserTests.java
│       └── resources/
│           ├── endpoints.properties
│           └── testng.xml
├── pom.xml
├── Dockerfile
```

## Dependencies

The project uses the following main dependencies:

- TestNG - Test framework
- RestAssured - API testing library
- Gson - JSON serialization/deserialization
- AssertJ - Fluent assertions
- JavaTuples - Tuple data structures
- Allure - Test reporting

## 🚀 Getting started
### Running Tests Locally

#### 1. Clone the repository

Run:
```bash
git clone https://github.com/Abdelrahman-Wagdy/quality-pro-task.git
cd PetStore
mvn clean test 
```
### Running Tests using Docker

#### 1. Clone the docker repo
```bash
docker pull abdelrahmanawagdy/petstoreapi:latest
```
#### 2. Run the docker image in a container
```bash
docker run -d --name myapp-container abdelrahmanawagdy/petstoreapi:latest
```

# Practice Automation – UI Test Framework

A lightweight, maintainable UI‐automation framework for the demo site <https://practice.automationtesting.in/> built with **Java 18**, **Selenium 4**, **Cucumber 7**, **TestNG 7** and **Allure** reporting.  Scenarios run in **parallel** on Chrome and Firefox and can be shipped in a single Docker container.

---

## 📂 Project layout
```
project-root/
├── src/
│   ├── main/
│   │   └── java/
│   │       └── support/
│   │           ├── BrowserActions.java
│   │           ├── BrowserManager.java
│   │           ├── DockerHelper.java
│   │           ├── DriverFactory.java
│   │           └── ReportMerger.java
│   └── test/
│       ├── java/
│       │   ├── features/
│       │   │   └── *.feature
│       │   ├── runners/
│       │   │   ├── ChromeTestRunner.java
│       │   │   └── FirefoxTestRunner.java
│       │   └── stepdefs/
│       │       └── Hooks.java
│       └── resources/
│           └── testng.xml
├── pom.xml
├── README.md
```

---

## 🛠 Prerequisites
* JDK 17 + (project uses 18 in `pom.xml`)
* Maven 3.9+
* Chrome / Firefox browsers installed locally

---

## 🚀 Getting started
Clone the repo and download all dependencies:
```bash
git clone https://github.com/Abdelrahman-Wagdy/quality-pro-task.git
cd PracticeAutomation
mvn -U clean verify      # compiles & pulls driver binaries via WebDriverManager
```

### 1 – Single‑browser run
```bash
# For Chrome only
mvn clean test -Dtest=ChromeTestRunner

# For Firefox only
mvn clean test -Dtest=FirefoxTestRunner
```

### 2 – Parallel Chrome + Firefox
The `testng.xml` suite spins two threads, each with its own Cucumber runner:
```bash
mvn test          # uses testng.xml → thread‑count="2" parallel="tests"
```

---

## 🧩 Extending the framework
1. **Add a new scenario** → create `*.feature` under `src/test/features`.
2. **Generate step stubs** → run once, copy snippets into a new class inside `stepdefs`.
3. **Map UI elements** → add locators & actions in a page‑object under `services/`.
4. **Tag** with `@Smoke`, `@Regression`, etc. to slice execution.


