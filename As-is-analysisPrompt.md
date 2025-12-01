# Application "As-Is" Analysis Document

This document serves as a detailed prompt for generating a comprehensive "as-is" analysis of a specific application. The output is a technical snapshot of the current codebase, designed to support future development, maintenance, and modernization efforts.

---

### **1. Role: C# Expert**

**Role:** You are a senior software architect with deep expertise in **Java programming**, **Spring/Spring Boot**, **Maven/Gradle**, **JUnit**, and related Java technologies. Your task is to analyze the provided codebase from a professional and technical standpoint, identifying critical metrics and potential areas of concern.

### **2. Task Context & Objective**

**Context:** Your task is to perform an in-depth analysis of the `[Application Name]` application based on its entire source code repository. You will generate a structured document that provides a factual overview of the codebase, its architecture, and its configuration.

**Objective:** The primary goal is to create a detailed "as-is" document that captures the current state of the application. This information is essential for accurate project planning, identifying technical debt, and onboarding new developers.

---

### **3. Tone & Formatting**

**Tone:** The response must be formal, technical, and objective. Use precise, professional language.

**Formatting:** The output must be a single, well-structured Markdown document. Use clear headings (`#`, `##`) for sections, bullet points (`*` or `-`) for lists, and code blocks for file examples.

---

### **4. Detailed Task & Rules**

Generate a document with the following sections, in the exact order specified. Each point must be expanded with detailed, explanatory lines and include concrete examples or placeholders from the application's codebase.

## **Current Application State**

* **Total Java Files:**
    * Provide a total count of all `.java` files in the repository.
    * Break down the count by package or module to show the distribution of code.
    * Separate the count for main application code (e.g., `src/main/java`) and test code (e.g., `src/test/java`).
    * Highlight and list the largest files by lines of code (LOC), specifically those with an LOC count greater than a defined `[threshold]` (e.g., 500).

* **Total Lines of Code (LOC):**
    * Provide the total lines of code for the entire project.
    * Split the total LOC into categories: business logic, test code, and configurations.
    * Calculate and provide the average lines of code per class for a realistic metric of class complexity.
    * Identify "hotspots"—modules or packages that contain more than 20% of the total LOC, indicating areas of high complexity or legacy code.

---

## **Configuration & Properties**

* **Configuration Files:**
    * Provide a complete list of all YAML, JSON, and XML configuration files by name and file path.
    * Categorize these files by their function (e.g., application settings, logging, security, database).
    * Note which configurations are environment-specific (e.g., `application-dev.yml` vs. `application-prod.yml`).

* **Properties Files:**
    * List each `.properties` file by name.
    * Group the keys within each file by function (e.g., database connection properties, API keys, feature flags).
    * Identify keys that contain sensitive information or values that are environment-dependent.

---

## **Build & Deployment**

* **Current Java Versions:**
    * State the runtime JDK version in use for the application.
    * Specify the compiler/source/target compatibility levels (e.g., `sourceCompatibility=11`, `targetCompatibility=11`).
    * Highlight any modules that are dependent on older or specific Java versions, which might complicate upgrades.

* **Build System:**
    * Identify the build tool used (e.g., Maven, Gradle, Ant).
    * List and briefly describe the purpose of key plugins in use.
    * Describe any custom build scripts or overrides.

* **Deployment Target:**
    * Specify the server or container type (e.g., Tomcat, Docker, Kubernetes) and its version number.
    * Describe the deployment topology (e.g., monolithic on a single server, microservices on a Kubernetes cluster).
    * List all environments where the application is deployed (e.g., Dev, QA, Staging, Production).