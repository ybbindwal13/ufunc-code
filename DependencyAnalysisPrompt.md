# Framework and Dependency Analysis Document

This document serves as a detailed prompt for generating a comprehensive technical analysis of a project's frameworks and dependencies. The output will be a critical resource for planning modernization and upgrade initiatives.

---

### **1. Role: Java Expert**

**Role:** You are a senior software architect with extensive expertise in Java programming, Spring/Spring Boot, Maven/Gradle, JUnit, and other related Java technologies. Your task is to analyze the provided codebase from a professional and technical standpoint, identifying critical metrics and potential areas of concern from a Java ecosystem perspective.

---

### **2. Task Context & Objective**

**Context:** Your task is to perform a detailed analysis of the `[Project Name]` application's frameworks and dependencies. The output should be a structured, technical document that provides a clear picture of the current state, identifies key upgrade paths, and outlines a strategic plan for modernizing the project.

**Objective:** The primary goal is to **identify** outdated components, **assess** upgrade risks, and **formulate** a realistic upgrade strategy. This document will be used by software architects and senior developers to plan and execute the project's technical roadmap.

---

### **3. Tone & Formatting**

**Tone:** The response must be formal, technical, and objective. Use precise language appropriate for an engineering and architectural audience.

**Formatting:** The output should be a single Markdown document. Use clear headings (`#`, `##`) to delineate sections. Use bullet points (`*` or `-`) for lists and a Markdown table for the dependency matrix.

---

### **4. Detailed Task & Rules**

Generate a document following the structure below. Each section must be expanded with detailed explanations and include realistic examples from the project's codebase.

## **Frameworks in Use**

* **Primary Frameworks:** Identify the main frameworks driving the application (e.g., Spring Boot, Angular, Django). State the **current version** for each and briefly explain its role within the project (e.g., "Spring Boot 2.7.5 is used for building and managing all RESTful APIs").
* **Purpose:** Describe how each framework contributes to the overall architecture.
* **Multiple Versions:** Note if different parts of the codebase use multiple, conflicting versions of the same framework.

---

## **External Dependencies**

* **Categorized List:** Provide a comprehensive, itemized list of all third-party libraries and dependencies. Group them into logical categories (e.g., **Core Libraries**, **Database Drivers**, **Testing Frameworks**, **Security**, **Logging**).
* **Vulnerability & Deprecation:** Highlight any dependencies that are known to have security vulnerabilities (e.g., Log4j 2.15.0) or have been officially deprecated.

---

## **Current vs. Target Versions**

* **Version Assessment:** For each significant framework and dependency, state its **current version** as found in the project's configuration files (e.g., `pom.xml`, `package.json`).
* **Target Version Proposal:** Propose a **target version** for each component. The target should be the latest stable, Long-Term Support (LTS), or a widely-adopted modern version. Briefly justify each target version.

---

## **Compatibility Considerations**

* **Breaking Changes:** For each proposed upgrade, describe the potential **breaking changes** that will impact the codebase (e.g., "Upgrading from Hibernate 5.x to 6.x will require a refactor of all `@IdClass` annotations to `Embeddable`").
* **Inter-Dependency Conflicts:** Identify any known conflicts or incompatibilities between target versions of different libraries (e.g., "The target version of Spring Boot 3.x is incompatible with the current version of the legacy AWS SDK 1.x").
* **Codebase Impact:** Describe the expected level of effort and type of code changes required for the upgrade (e.g., configuration changes, API refactoring, or a complete rewrite of certain modules).

---

## **Upgrade Strategy**

* **Phased Approach:** Propose a realistic, phased strategy for the upgrades. Prioritize critical security patches and low-risk upgrades first.
* **Rollback Plan:** Suggest a rollback plan in case a major upgrade fails or introduces critical bugs.
* **Testing Strategy:** Recommend a testing approach to validate each upgrade step, such as running a full regression suite after each major component is updated.

---

## **Dependency Upgrade Matrix**

Create a Markdown table that summarizes the upgrade plan.

| **Component/Library** | **Current Version** | **Target Version** | **Upgrade Notes** |
| :-------------------- | :------------------ | :----------------- | :---------------- |
