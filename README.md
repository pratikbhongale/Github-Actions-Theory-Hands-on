# CI/CD Tools – GitHub Actions & Jenkins

## CI/CD Tools 

Common CI/CD tools:

* GitHub Actions
* Jenkins
* GitLab CI
* Travis CI

Among these, the **most trusted and widely used tools** are:

* **GitHub Actions**
* **Jenkins**

---

## What is CI/CD?

**CI/CD** stands for:

* **CI – Continuous Integration**
* **CD – Continuous Deployment**

CI/CD is an **automated process** used to build, test, and deploy applications continuously.

---

## Software Development Lifecycle (SDLC)

Whenever you create an application, you follow these steps:

1. **Planning**
2. **Design**
3. **Coding**
4. **Deployment**
5. **Maintenance**

This process is **continuous**, not one-time.

### Planning

* Planning is usually done **step by step**
* Tools used:

  * **Jira** – for task and sprint planning
  * **Confluence** – for documentation

---

### Coding

Applications can be built using:

* **JavaScript frameworks**:

  * React
  * Express
* **Python frameworks**:

  * Flask
  * Django

---

### Deployment

Applications can be deployed to:

* **Play Store** (mobile applications)
* **Web servers**
* **Cloud platforms** (AWS, Azure, GCP)

---

## Maintenance & Feature Enhancement

Over time:

* Applications degrade
* Bugs appear
* New features are required

So, you must:

* Fix bugs
* Enhance features
* Release new versions

This process is called **maintenance**.

---

## Rollout of an Application

**Rollout** means the **systematic introduction of a new version** of an application.

Whenever we roll out an application, we must perform **mandatory checks**.

---

## Mandatory Checks Before Rollout (CI Process)

### 1. Code Quality Check

* Ensures clean, readable, and formatted code
* Uses **linting tools**

**Examples:**

* Python: `flake8`
* JavaScript: `eslint`
* VS Code: `prettier`

> Linting means **making your code clean and pretty**

---

### 2. Code Reviews

* Developers review code changes
* Ensures best practices and avoids mistakes

---

### 3. Testing

Different types of testing:

* Unit Testing
* Functional Testing
* Load Testing
* Stress Testing
* White Box Testing
* Black Box Testing
* Performance Testing

**Testing tools examples:**

* JavaScript: Cypress
* Python: Selenium, Pytest

---

### 4. Code Coverage

* Checks how much of the code is tested
* Given as a percentage

**Example:**

* If coverage ≥ 70% → rollout allowed
* If coverage < 70% → rollout blocked

---

### Code Report

When we combine:

* Code quality
* Code reviews
* Testing
* Code coverage

We get a **code report**.

This report decides whether the application can be rolled out or not.

---

## Earlier vs Current Scenario

### Earlier

* All checks were **manual**
* Time-consuming
* Error-prone

### Current Scenario

* CI tools automate all checks
* Faster
* Reliable
* Consistent

This automation is called **Continuous Integration (CI)**.

---

## Continuous Deployment (CD)

After **CI is successful**, the next step is **Continuous Deployment**.

In CD:

* We write **scripts or jobs**
* Application is deployed automatically
* Deployment is based on configurations
* Target platforms:

  * Cloud platforms
  * Web servers
  * App stores

---

## Test Driven Development (TDD)

In **TDD**:

* Test cases are written **before** the code
* Code is written to pass the tests

Testing frameworks:

* JavaScript: Cypress
* Python: Selenium, Pytest

All these tests are part of **CI**.

---

## CI Includes

CI mainly includes:

1. Writing test cases
2. Code quality checks
3. Linting
4. Code coverage analysis

---

## Code Quality & Linting

* Linting tools format and clean code
* Provide reports on code cleanliness

**Examples:**

* Python: `flake8`
* VS Code extension: `prettier`

These tools provide **percentage reports** on code quality.

---

## Code Coverage

* Measures performance and test coverage of code
* Helps decide whether deployment should proceed

---

## CI → CD Flow

1. Code is pushed to repository
2. CI runs:

   * Code quality checks
   * Tests
   * Coverage
3. If CI passes → CD triggers
4. Application is deployed automatically

---

## GitHub Actions

**GitHub Actions** is a **CI/CD pipeline tool provided by GitHub**.

---

## GitHub Actions Folder Structure

To create a GitHub Actions pipeline:

```text
.github/
 └── workflows/
     └── pipeline.yml
```

Steps:

1. Create `.github` folder
2. Create `workflows` folder inside it
3. Create `.yml` or `.yaml` file

---

## GitHub Actions Example

```yaml
on:
  push:
    branches:
      - main

jobs:
  build:
    runs-on: ubuntu-latest

    steps:
      - uses: actions/checkout@v2
      - name: Build
        run: |
          echo "Build"
```

---

## Explanation

* **on.push** → Event trigger
* **branches** → Runs when code is pushed to `main`
* **jobs** → Multiple nodes like Build, Test, Deploy
* **runs-on** → Machine type
* **checkout** → Fetches repository code
* **run** → Executes commands

---

## Real-World CI/CD Example

1. Developer pushes code
2. GitHub Actions triggers CI
3. Tests & checks run automatically
4. Code report is generated
5. If threshold is met → deployment starts
6. Application is deployed to cloud
7. Users receive updated version

---

## Benefits of CI/CD

* Faster delivery
* Automated testing
* Better code quality
* Reduced bugs
* Easy maintenance
* Reliable deployments

---

## Conclusion

CI/CD is a **core practice in modern software development**.
Tools like **GitHub Actions and Jenkins** help automate integration, testing, and deployment, ensuring **high-quality and continuously delivered applications**.


Just tell me 👌
