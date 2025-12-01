# Application "As-Is" Analysis Document (Target: .NET 10 + React)

This document is a detailed prompt for generating a comprehensive **"as-is"** analysis of an application implemented in **C# / .NET 10 (ASP.NET Core)** for backend services and **React (Vite)** for frontend. The structure of this document follows the previously uploaded Java-based template but is fully adapted to your modernized target tech stack.

---

## 1. Role: .NET / Full-Stack Expert
You are a senior software architect with expertise in:
- C# and .NET 10+
- ASP.NET Core APIs
- Entity Framework Core
- Modern frontend architecture with React + Vite
- xUnit/NUnit test frameworks
- Docker, CI/CD, cloud deployment

Your task is to inspect the repository and provide a complete technical snapshot of the system.

---

## 2. Task Context & Objective
Perform an in-depth analysis of the entire source code for **[Application Name]**.

### **Objective**
Produce a *single*, well-structured Markdown document that describes:
- Codebase shape
- Architecture
- Configurations
- Build pipeline
- Deployment model
- Tech debt
- Modernization risks

This will be used to plan upgrades and refactoring.

---

## 3. Tone & Formatting
- **Tone:** Formal, technical, objective
- **Output:** Markdown only
- Use clear headings, bullets, and code blocks
- Respect the order and section names exactly

---

## 4. Detailed Task & Rules
You must generate the document in the exact order shown below.

# Current Application State

### **C# Code Inventory**
- Count all `.cs` files.
- Split count into:
  - Backend production code (`src/**`)
  - Test projects (`tests/**`)
- Identify largest `.cs` files above `[threshold]` LOC.
- Describe responsibilities of each large file.

### **Frontend Code Inventory**
- Count `.jsx`, `.tsx`, `.js`, `.ts`, `.css`, `.html`.
- Break down by folder (components, pages, hooks, services).
- Identify large frontend files above `[threshold]` LOC.

### **Total LOC Analysis**
- Total LOC across entire repo
- LOC by:
  - backend
  - backend tests
  - frontend
  - configuration & scripts
- Find hotspots (folders with >20% LOC)

### **Project Graph & Dependencies**
- List all `.csproj` files
- Show dependency graph
- List NuGet dependencies per project
- List `package.json` dependencies
- Identify private/legacy dependencies

---

# Configuration & Properties

### **Configuration Files**
- `appsettings.json` and environment variants
- `docker-compose.yml`, `Dockerfile`
- Kubernetes manifests, Helm charts (if present)

For each config file:
- Summarize purpose
- List key sections

### **Secrets Handling**
- Identify checked-in secrets (without printing values)
- Flag sensitive config keys
- Identify `.env` files

### **Frontend Configuration**
- Document `vite.config.*`
- Document environment variables used by React app
- Identify how API base URL is configured

---

# Build & Deployment

### **.NET Runtime & SDK**
- Extract `TargetFramework` from `.csproj`
- Identify SDK version via `global.json` (if present)

### **Node / Frontend Runtime**
- Node version requirements
- Vite & React versions

### **Build Pipelines**
- List GitHub Actions, GitLab CI, Azure pipelines
- Summaries of build steps
- Any custom build scripts

### **Containerization**
- All Dockerfiles
- Multi-stage usage
- Base images
- docker-compose services
- Kubernetes manifests

### **Environments & Releases**
- Identify dev, QA, staging, prod
- Deployment artifacts (images, binaries, static frontend bundles)

---

# Runtime & Infrastructure

### **Databases & Storage**
- DB technologies
- EF Core migrations
- External stores (Redis, S3, Blob)

### **Authentication & Security**
- Identify JWT / Identity configuration
- Highlight insecure patterns

### **Logging & Observability**
- Logging frameworks (Serilog, built-in logging)
- Metrics & tracing (OpenTelemetry)
- Health check endpoints

---

# Code Quality & Tests

### **Tests**
- Total test projects
- Total test files
- Frameworks used
- Gaps in test coverage

### **Static Analysis**
- Roslyn analyzers
- StyleCop / SonarQube
- ESLint & Prettier for frontend

### **Tech Debt & Anti-Patterns**
- Large controllers
- Mixed concerns
- EF entities leaking through API
- Async misuse
- Thread-safety issues

---

# API Surface & Frontend Integration

### **API Surface**
- List all ASP.NET Core endpoints
- For each: method, path, DTOs

### **Frontend Integration**
- How React calls backend
- CORS configuration
- API client wrappers

---

# Migration & Modernization Risks
Provide risks + mitigation, such as:
- Framework version drift
- Coupling between layers
- Insecure configs
- Missing health checks
- Hardcoded URLs in frontend

---

# Deliverables
The LLM must output:
1. Executive summary
2. Full section-by-section analysis
3. Commands to measure code metrics
4. Prioritized remediation list
5. Upgrade-readiness checklist for .NET 10 + React

---

# Reference Commands
```bash
# count backend C#
find src -name '*.cs' | wc -l

# count frontend JS/TS/React files
find frontend -type f \( -name '*.js' -o -name '*.ts' -o -name '*.jsx' -o -name '*.tsx' \) | wc -l

# total lines of code
find . -name '*.cs' -print0 | xargs -0 cat | wc -l

# largest C# files
for f in $(find src -name '*.cs'); do wc -l $f; done | sort -nr | head
```

---

This Markdown file is now ready to be used as the LLM prompt for modernization analysis aligned with your .NET + React architecture.