# Project Structure Document Generation

This document serves as a detailed prompt for generating a comprehensive "as-is" document of a project's structure. The output should be a clear, technical reference for developers, architects, and stakeholders, detailing the organization and architecture of the codebase.

---

### **1. Task Context**

**Context:** Your task is to analyze the provided source code for the `[Project Name]` application. Based on this analysis, you will generate a detailed project structure document. The purpose of this document is to provide a clear, factual overview of the codebase's organization to aid in onboarding, maintenance, and future architectural decisions. The analysis should be objective and based solely on the provided code and configuration files.

---

### **2. Tone and Formatting**

**Tone:** The response must be formal, technical, and objective. It should use precise language suitable for a professional engineering audience.

**Formatting:** The output must be a single, well-structured document using Markdown. Use clear headings (`##`, `###`) for each section and sub-section. Use bullet points (`*` or `-`) for lists.

---

### **3. Detailed Task and Rules**

You must generate a document with the following sections, in the order specified. Each section must be expanded with detailed, explanatory lines, and include realistic examples or placeholders that reflect the actual project.

* **Project Structure Overview**
    * **High-Level Folder Hierarchy:**
        * Describe the main root-level folders (`src`, `docs`, `config`, etc.).
        * Explain the overall project layout: Is it a **monolithic** structure (one single `src` folder) or a **modular** layout (multiple top-level directories for different components)?
        * Identify and explain the purpose of any **custom** or non-standard folders found in the codebase (e.g., `scripts/`, `migrations/`).
    * **Modules and Submodules:**
        * List each primary module and provide a brief, one-sentence purpose for each (e.g., `project-api`: Manages all RESTful endpoints).
        * Describe the **dependencies** between modules. Specify which modules depend on others.
        * Categorize modules as **reusable** (components that could be used by other applications) versus **tightly coupled** (specific to this application's core logic).
    * **Naming Conventions:**
        * Document the specific rules for **class, package, and file naming**. Provide clear examples (e.g., `PascalCase` for classes, `kebab-case` for file names).
        * List common **prefixes or suffixes** used to denote a layer or role (e.g., `Controller` for the API layer, `Service` for business logic).
        * Note any observed **deviations or inconsistencies** from the established conventions.

* **Layered Architecture Breakdown**
    * **UI/Presentation Layer:** Describe the components and responsibilities of this layer. Include examples like API controllers or frontend components.
    * **Service/Business Logic Layer:** Explain the role of this layer in orchestrating business operations. Note its separation from presentation and data concerns.
    * **Data Access/DAO/Repository Layer:** Detail how this layer interacts with the database, providing an abstraction over data storage.
    * **Integration/Messaging Layer:** Describe any components responsible for communication with external systems, APIs, or message queues.
    * **Cross-Cutting Concerns:** Identify and explain where concerns like logging, security, and exception handling are implemented and organized within the structure.

* **Legacy or Unused Modules**
    * Identify and list any **deprecated or duplicate modules**. Provide a brief explanation for why they are considered legacy.
    * Point out any **old code** that is not actively maintained but remains in the repository.
    * List specific modules or files that are clear **candidates for refactoring or removal**, along with a brief justification.