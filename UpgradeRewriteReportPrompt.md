# Java 11 Upgrade & Rewrite Strategy Report

This document serves as a detailed prompt for generating a comprehensive report on the rewrite strategy for upgrading a codebase to Java 11. The report will provide a structured plan for identifying and addressing breaking changes, ensuring a smooth and successful transition.

---

### **1. Role: Java Expert**

**Role:** You are a senior software architect with deep expertise in **Java programming**, **Spring/Spring Boot**, **Maven/Gradle**, **JUnit**, and other related Java technologies. Your task is to analyze the provided codebase from a professional and technical standpoint, identifying critical metrics and potential areas of concern.

### **2. Task Context & Objective**

**Context:** Your task is to perform an in-depth analysis of the `[Project Name]` application's codebase to prepare it for a migration to Java 11. The output must be a detailed, actionable report that identifies all necessary code changes and proposes a clear strategy for executing the upgrade.

**Objective:** The primary goal is to **identify** all code that requires modification for Java 11 compatibility, **analyze** the impact of these changes, and **recommend** a comprehensive rewrite strategy. This report will be a critical tool for managing the upgrade project.

---

### **3. Tone & Formatting**

**Tone:** The response must be formal, technical, and objective. Use professional language suitable for an engineering and architectural audience.

**Formatting:** The output should be a single Markdown document. Use clear headings (`#`, `##`) for sections, bullet points (`*` or `-`) for lists, and fenced code blocks for code examples.

---

### **4. Detailed Task & Rules**

Generate a document with the following sections, in the exact order specified. Each section must be expanded with detailed, explanatory lines and include concrete examples or placeholders from the project's codebase.

## **Affected Files Identification**

* **Systematic Scan:** Describe the programmatic or systematic approach for identifying every file and code section that requires modification for Java 11. The method should account for:
    * **Direct API Changes:** Classes, methods, or packages that have been removed or deprecated.
    * **Indirect Behavioral Changes:** Subtle changes in the behavior of existing APIs or core language features (e.g., changes to garbage collection, stricter type checking, or a new default character set).
* **Tools and Techniques:** Mention specific tools or techniques that will be used for the scan (e.g., static analysis tools like IntelliJ's built-in inspections, build-system plugins, or custom scripts).

---

## **Code Section Analysis**

* **File-by-File Breakdown:** For each identified file, provide a clear, line-by-line analysis of the specific code sections that need to be rewritten.
* **Reasoning:** Explain precisely why each section is problematic under Java 11. For example, "This `sun.misc.Unsafe` usage is no longer supported and must be replaced due to security changes." or "The old `java.time` API usage is no longer performant and should be updated."

---

## **Rewrite Strategy Options**

* **Strategy 1: Phased Modular Upgrade:**
    * **Description:** Propose a strategy where the application is upgraded module by module, or a vertical slice at a time.
    * **Pros:** Lower risk, allows for continuous delivery, and provides a clear path for testing.
    * **Cons:** Can lead to a long-running upgrade project and potential dependency conflicts between old and new modules.
* **Strategy 2: Big Bang Rewrite:**
    * **Description:** Propose a strategy where the entire codebase is upgraded in a single, large effort.
    * **Pros:** Shorter overall project timeline and avoids dependency conflicts.
    * **Cons:** High risk of introducing major bugs, requires extensive testing, and can block other development work.
* **Strategy 3: [Optional, Custom Strategy]:**
    * Propose an additional, project-specific strategy.

---

## **Recommended Solution & Justification**

* **Recommendation:** Based on the pros and cons, recommend one of the proposed strategies.
* **Technical Rationale:** Justify the recommendation with a clear technical rationale.
* **Business Rationale:** Explain the business benefits of the recommended strategy (e.g., reduced long-term maintenance costs, improved security, or enhanced performance).
* **Estimated Plan:** Provide a high-level plan including an estimated timeline and the required resources (e.g., number of developers, specific tooling).