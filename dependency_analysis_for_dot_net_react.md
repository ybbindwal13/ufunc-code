# Framework and Dependency Analysis Document (Target: .NET 10 + React)

This document is a modernized version of the originally uploaded Java-based dependency analysis template. It is now adapted for applications built with **C# / .NET 10 (ASP.NET Core)** and **React (Vite)**. The structure and intent remain identical to the original file. fileciteturn2file0

---

## 1. Role: .NET / Full‑Stack Expert
You are a senior software architect with extensive expertise in:
- C# and .NET 8/9/10
- ASP.NET Core Web APIs & Minimal APIs
- Entity Framework Core
- NuGet package ecosystem
- React 18/19 with Vite and TypeScript
- Frontend dependency ecosystems (npm, pnpm, yarn)
- CI/CD pipelines, Docker, Kubernetes

Your task is to assess the project's framework and dependency landscape and produce a structured, technical analysis.

---

## 2. Task Context & Objective
**Context:** Perform a detailed dependency and framework analysis of `[Project Name]` built using .NET + React. Review backend (C#), frontend (React), infrastructure files, and build pipelines.

**Objective:**
- Identify outdated, deprecated, or vulnerable dependencies
- Assess feasibility and risks of upgrading to .NET 10 and latest React ecosystem
- Propose realistic upgrade targets and migration strategies

The document will assist architects and senior developers in planning the modernization roadmap.

---

## 3. Tone & Formatting
- **Tone:** Formal, technical, objective
- **Output:** A single Markdown document
- Use proper headings, bullet lists, and tables
- Use code blocks for configuration or command examples

---

## 4. Detailed Task & Rules
Follow the structure exactly. Expand each section with detailed explanations and reference actual data from the repository.

# Frameworks in Use

### **Backend Frameworks (C# / .NET)**
For each backend framework:
- Identify the framework (e.g., ASP.NET Core, EF Core)
- State **current version** as found in `.csproj`
- Explain its purpose (e.g., "ASP.NET Core 8.0 used for REST API endpoints")
- Flag if different projects use mismatched or conflicting versions

### **Frontend Frameworks (React / JS ecosystem)**
For each framework:
- Identify version from `package.json`
- Explain its role (React, React Router, Vite, Tailwind, Zustand/Redux, etc.)
- Identify version mismatches or legacy build tools

---

# External Dependencies

### **Categorized Inventory**
Provide a full grouped list of dependencies:
- **NuGet Core Libraries** (ASP.NET Core, EF Core, configuration libraries)
- **NuGet Infrastructure Libraries** (Serilog, Polly, AutoMapper, MassTransit)
- **NuGet Database Drivers** (e.g., Npgsql, Microsoft.Data.SqlClient)
- **NuGet Cloud/3rd‑Party SDKs** (Azure SDKs, AWS SDK, Stripe, Twilio)
- **Node/Frontend Dependencies** grouped as:
  - Core runtime packages
  - UI frameworks
  - State management
  - Build toolchain
  - Testing (Jest, Vitest, Testing Library)

### **Vulnerability & Deprecation Review**
For each dependency:
- Flag known vulnerabilities or deprecated packages
- Note packages out of LTS support
- Highlight abandoned repositories (no commits/releases in years)

---

# Current vs. Target Versions

### **Version Assessment**
- Extract current versions from `.csproj` and `package.json`
- Assess alignment with ecosystem standards

### **Target Version Proposal**
For each dependency:
- Suggest a target version (typically latest LTS or latest stable)
- Justify choices (compatibility, performance, security)

Provide examples such as:
- **EF Core 6.0 → EF Core 10**
- **ASP.NET Core 7 → ASP.NET Core 10 (LTS)**
- **React 17 → React 19**
- **Vite 3 → Vite 6**

---

# Compatibility Considerations

### **Breaking Changes**
For each major upgrade, describe:
- Breaking API changes (e.g., ASP.NET Core middleware pipeline changes)
- EF Core behavior changes (LINQ evaluation, lazy loading)
- React/TypeScript breaking changes (React 19 compiler, new JSX transforms)

### **Inter‑Dependency Conflicts**
- Known incompatibilities between new versions
- Conflicts between NuGet and Node dependencies (e.g., mixed-use JWT algorithms)

### **Codebase Impact**
Estimate:
- Required refactoring (controllers, DI setup, EF models, frontend routing)
- Required config changes
- Required test updates

---

# Upgrade Strategy

### **Phased Approach**
Propose migration plan:
- Phase 1: Security patches, core dependencies
- Phase 2: Backend framework upgrade (ASP.NET Core → .NET 10)
- Phase 3: EF Core migrations upgrade
- Phase 4: Frontend upgrade (React, Vite)
- Phase 5: Full regression + cleanup

### **Rollback Plan**
- Git branch isolation strategy
- Parallel environment deployment
- Docker image version pinning

### **Testing Strategy**
- Required unit, integration, and end-to-end tests
- Compatibility tests
- Feature freeze checkpoints

---

# Dependency Upgrade Matrix

Provide a table in the following format:

| Component / Library | Current Version | Target Version | Upgrade Notes |
|--------------------|----------------|----------------|----------------|
| ASP.NET Core       | x.x.x          | 10.x.x (LTS)   | Breaking changes in minimal APIs |
| EF Core            | x.x.x          | 10.x.x         | Requires migration updates |
| React              | x.x.x          | 19.x           | Check JSX transform compatibility |
| Vite               | x.x            | latest          | Update build scripts |
| Serilog            | x.x.x          | latest          | Replace deprecated sinks |
| ...                | ...            | ...            | ... |

---

# End of Document

