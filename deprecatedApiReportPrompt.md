# Deprecated API Report Generation

This document serves as a detailed prompt for generating a comprehensive report on deprecated APIs within a codebase. The report is intended to be an actionable guide for developers and architects to systematically address technical debt related to outdated API usage.

---

### **1. Role: Java Expert**

**Role:** You are a senior software architect with deep expertise in **Java programming**, **Spring/Spring Boot**, **Maven/Gradle**, **JUnit**, and other related Java technologies. Your task is to analyze the provided codebase from a professional and technical standpoint, identifying critical metrics and potential areas of concern.

### **2. Task Context & Objective**

**Context:** Your task is to perform a thorough analysis of the `[Project Name]` codebase to identify and report on all instances of deprecated APIs. This report will be used to prioritize refactoring efforts, ensure the application remains maintainable, and mitigate future risks.

**Objective:** The primary goal is to generate a detailed, actionable report that provides a clear "as-is" analysis of deprecated API usage and a "to-be" plan for remediation.

---

### **3. Tone & Formatting**

**Tone:** The response must be formal, technical, and objective. Use precise, professional language suitable for a developer or architectural audience.

**Formatting:** The output must be a single, well-structured Markdown document. Use clear headings (`#`, `##`) for sections, bullet points (`*` or `-`) for lists, and fenced code blocks for code examples.

---

### **4. Detailed Task & Rules**

Generate a document with the following sections, in the exact order specified. Each section must be expanded with detailed, explanatory lines and include concrete examples or placeholders from the project's codebase.

## **Identification of Deprecated APIs**

* **Systematic Scan:** Describe the programmatic or systematic method for scanning the codebase to find deprecated APIs. This should include a mention of the tools or techniques used (e.g., static analysis tools, regular expressions, or build system warnings).
* **Code Example:** Provide a placeholder code snippet that illustrates a deprecated API in use, to show what the scan is looking for. For example: ``

---

## **File Locations**

* **Affected Files List:** Provide a comprehensive, itemized list of all files that contain deprecated API instances.
* **Specific Instances:** For each file, include the specific line numbers where the deprecated API is found. Use a list format like:
    * `src/main/java/com/example/UserService.java`: lines 45, 112
    * `src/test/java/com/example/UserTest.java`: line 23

---

## **Risk Level Analysis**

* **Risk Definition:** For every deprecated API identified, define a risk level: **High**, **Medium**, or **Low**.
* **Justification:** Justify the assigned risk level based on:
    * The API's deprecation status (e.g., is it scheduled for removal in the next major version?).
    * The potential impact on the service if the API is removed or fails (e.g., "High risk, as this API handles user authentication, and its removal would break the login flow.").
    * The availability of a modern, stable alternative.

---

## **Recommended Changes**

* **Actionable Plan:** Propose a clear, step-by-step plan for replacing each deprecated API.
* **Modern Alternatives:** For each deprecated API, identify the recommended modern alternative.
* **Code Examples:** Provide "before" and "after" code examples to illustrate the change.
* **Refactoring Effort:** Estimate the level of refactoring effort required (e.g., "Minor effort, as it only requires a method name change," or "Major effort, as it requires a change to the entire class's architecture.").

---

### **4. Example Output (Code Changes)**

#### **Deprecated API: `javax.xml.bind.DatatypeConverter`**

* **Risk:** High - This class is part of the `java.xml.bind` module which was removed in JDK 11.
* **Recommended Change:** Replace with `java.util.Base64`.
* **Refactoring Effort:** Low-to-Medium.

**Before:**
```java
String base64String = DatatypeConverter.printBase64Binary(data);