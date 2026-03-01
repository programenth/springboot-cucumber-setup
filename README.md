## Spring Boot + Cucumber BDD Setup 🚀
*by Sachin Verma*

[![Securing the Modern Web: A Deep Dive into JWT with RSA256](https://miro.medium.com/v2/resize:fit:720/format:webp/1*_E-Xzc43sJmI-ytAYmkYhA.png)](https://medium.com/@sachinverma_78701/how-i-set-up-cucumber-gherkin-to-test-a-spring-boot-web-app-step-by-step-87066f505c4a)

A production-grade Behavior-Driven Development (BDD) setup using **Cucumber, Gherkin, and RestAssured** to test a Spring Boot web app. 

This repository intentionally separates test automation from the main application code to keep CI/CD pipelines clean, independent, and scalable.

## 🛠 Tech Stack
* **Java 17** & **Maven**
* **Cucumber (v7.x)** for Gherkin execution and Spring integration
* **RestAssured** for API testing
* **Target App:** [springboot-cucumber-testapp](https://github.com/sachinv-redhawk/springboot-cucumber-testapp) (A lightweight Spring Boot + H2 app)

---

## 🏗 Architecture Highlights

Instead of dumping everything into step definitions, this project uses a clean, layered architecture:
* **`clients/`**: Dedicated REST clients (e.g., `UserClient`) to handle HTTP requests.
* **`stepdefs/`**: Stateless, readable Cucumber step definitions that only handle intent and assertions.
* **`utils/`**: A `ContextStorage` component to bridge state (like generated IDs) across steps.
* **`runners/`**: Tag-based JUnit test runners (`@smoke`, `@functional`) for targeted execution.
* **`features/`**: Plain English, business-readable test scenarios.

---
👉 **Full technical walkthrough & Code:** [https://medium.com/@sachinverma_78701/how-i-set-up-cucumber-gherkin-to-test-a-spring-boot-web-app-step-by-step-87066f505c4a](https://medium.com/@sachinverma_78701/how-i-set-up-cucumber-gherkin-to-test-a-spring-boot-web-app-step-by-step-87066f505c4a)

Happy Coding! 🚀
