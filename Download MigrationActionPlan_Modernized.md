# Migration Action Plan (Target: .NET Modernization + React UI)

This document serves as a detailed prompt for generating a phased modernization action plan based on migration challenges and transformation analysis. The goal is to modernize the backend to ASP.NET Core and build a new UI using React.

---

### 1. Role: .NET + React Modernization Expert

You are a senior software architect with expertise in:
- Latest .NET (.NET Core / 6 / 8 / 10)
- ASP.NET MVC to ASP.NET Core migration
- C# application architecture
- React (Vite, TypeScript, Routing)
- NuGet, npm, and CI/CD pipelines
- Phased migration execution and incremental cutover strategies

Your task is to produce a phased migration action plan for the provided project.

---

### 2. Task Context & Objective

Based on the “Migration Challenges and Transformation Analysis” document for the `[Project Name]` application, transform the modernization strategy into actionable steps for:

- Backend migration to ASP.NET Core Web API
- UI rebuild using React

Your output must result in a **clear execution roadmap**.

---

### 3. Tone & Formatting

- **Output:** Markdown document
- **Style:** Direct, action-oriented, technical
- **Use:** Headings, bullet points, bold labels, and short execution statements

No source code is required — only **strategic, time-bound actions**.

---

### 4. Detailed Task & Rules

Follow the sections below exactly.  
Each section must include **backend + frontend actions**, and must specify **owners + KPIs**.

---

## Immediate Actions

- **Modernization Confirmation**
  - Action: Approve ASP.NET Core + React modernization direction
  - Owner: Project Manager
  - KPI: Signed modernization charter

- **Scope Definition**
  - Action: Select the first feature to migrate (Booking, Payment, Authentication, etc.)
  - Owner: Solution Architect
  - KPI: Phase 1 feature document

- **Risk Identification**
  - Action: Create migration risk log
  - Owner: Tech Lead
  - KPI: Completed risk register (top 3 risks + mitigation)

---

## Technical & Business Challenges

- **Backend Challenges**
  - Action: Identify controllers to extract and refactor into ASP.NET Core Web APIs
  - Owner: Senior C# Engineer
  - Example: Extract `BookingsController` logic into `/api/bookings` using minimal APIs

- **Frontend Challenges**
  - Action: Identify Razor views requiring React replacements
  - Owner: Frontend Lead
  - Example: Convert `Views/Booking/HotelBooking.cshtml` into `BookingPage.tsx`

- **Tooling Preparation**
  - Action: Create templates for:
    - ASP.NET Core Web API
    - React (Vite + TypeScript)
  - Owner: DevOps Engineer
  - KPI: Repositories initialized

---

## Migration Strategy

- Convert backend logic to ASP.NET Core API endpoints
- Build corresponding UI using React + Axios/fetch
- Run old Razor page and new React page **in parallel**
- Switch traffic gradually using:
  - Reverse proxy routing
  - Feature flags
  - Config toggles (e.g., `/app/*` routes)

**Backend Tasks:**
- Convert `.csproj` to SDK style
- Replace `web.config` with `appsettings.json`
- Implement dependency injection in `Program.cs`

**Frontend Tasks:**
- Create React project with:
  - Vite
  - TypeScript
  - React Router
- Map API endpoints to service layer (e.g., `/api/bookings`)

---

## Timeline (First 30 Days)

> Force the LLM to output a calendar-based action plan.

- **Day 1–5**
  - Create ASP.NET Core API skeleton
  - Create React application

- **Day 6–10**
  - Implement first API endpoint (GET bookings)
  - Build basic React component + layout

- **Day 11–20**
  - Connect React UI to API with Axios
  - Validate data flow and form submission

- **Day 21–30**
  - Performance testing, regression detection
  - Switch route using feature flag (`/booking` vs `/app/booking`)

**Every milestone MUST include:**
- **Owner**
- **KPI**
- **Deliverable**

---

## Deliverables

- Working ASP.NET Core API endpoint
- Matching React page rendering identical feature
- Documentation of routing strategy
- Feature toggle for page switching
- Retro notes for final migration plan

---

## Output Requirements (For LLM)

The LLM must provide:

- Phased migration execution plan
- Action steps with:
  - Owners
  - KPIs
  - Deliverables
- No source code (only strategy)

---

End of Document.
