# PTDF Project Performance Dashboard

![PTDF Dashboard Cover](./images/ptdf-dashboard-cover.png) <!-- Replace with your screenshot: e.g., ptdf-dashboard-cover.png -->

## Overview

The **PTDF Project Performance Dashboard** is an internal web application built to centralize and simplify project oversight for the Petroleum Technology Development Fund. It replaces scattered spreadsheets and long email threads with a single place where executives and managers can see projects, budgets, approvals, and progress at-a-glance. The system models the institution’s hierarchy (departments → subdivisions → teams) so progress and spend automatically roll up from projects to subdivisions and departments.

This is a production-ready portfolio project that demonstrates backend architecture, role-based access, approval workflows, automated notifications, and polished UI dashboards designed for institutional users.

---

## Why this matters

* Removes reliance on fragile spreadsheets and manual reporting.
* Speeds up approvals and reduces bottlenecks with automated routing and email reminders.
* Gives executives a single source of truth for performance, budgets, and milestones.
* Makes it easier for teams to record expenditures and update milestone progress consistently.

---

## Key Features

* Role-based access (Super Admin, Executive Secretary, General Manager, Staff, Dashboard Viewer)
* Project creation, milestones, and progress tracking
* Budget and expenditure tracking with roll-ups to subdivisions and departments
* Automated approval workflows with email notifications and reminders
* CSV & PDF export of reports and project summaries
* Clean, responsive UI with interactive KPI charts and dashboards
* Background queues for reliable notifications during peak load

---

## Tech Stack (simple summary for recruiters)

* **Backend:** Laravel 12 (PHP 8.2) — API and business logic
* **Database:** MySQL (production), SQLite (local development)
* **Frontend:** Tailwind CSS + DaisyUI, Alpine.js for small interactivity
* **Charts:** Chart.js for KPI visualizations
* **Build & Assets:** Vite
* **Emails:** SendGrid for transactional emails (approvals, reminders, security)
* **Background Processing:** Laravel queues for reliable notification delivery

---

## Project Structure (high level)

* `app/` — core business logic and models (Projects, Budgets, Users, Approvals)
* `routes/` — web and API routes with role-based middleware
* `resources/views/` — Blade views used for server-rendered pages & templates
* `public/` — built frontend assets (Vite output)
* `jobs/` — queued jobs for email notifications and long-running tasks
* `exports/` — CSV / PDF export templates and generation logic

---

## Screenshots

Add one or two clear screenshots here to highlight the main dashboard and an approval workflow:

```md
![Dashboard Overview](./images/ptdf-dashboard-overview.png)   <!-- Add: ptdf-dashboard-overview.png -->
![Approval Workflow](./images/ptdf-approval-workflow.png)     <!-- Add: ptdf-approval-workflow.png -->
```

---

## How I built it (process)

1. **Discovery & Requirements** — spoke with stakeholders to identify pain points (spreadsheet fragmentation, slow approvals).
2. **Data Modeling** — mapped real organization hierarchy (departments → subdivisions → teams) and designed models for projects, milestones, budgets, and approvals.
3. **API-first Backend** — developed Laravel APIs, migrations, and seeders so frontend and integrations could be built in parallel.
4. **UX & UI** — built a component-driven frontend with Tailwind + DaisyUI; focused on clarity and accessibility for decision makers.
5. **Workflows & Notifications** — implemented approval routing rules and queued email notifications using SendGrid and Laravel queues.
6. **Exports & Reporting** — added CSV and PDF exports for presentation-ready outputs and audit trails.
7. **Testing & Iteration** — tested flows with seeded demo data, iterated on UX and performance bottlenecks.

---


## What I learned / Highlights

* Designing roll-up calculations so department KPIs automatically reflect project-level updates.
* Building robust approval workflows that are transparent and auditable.
* Using queues to ensure notifications don’t block user flows and remain reliable under load.
* Creating clean, responsive dashboards that non-technical executives can trust instantly.

---

## Future improvements (ideas)

* Add a native mobile app for field updates.
* Add fine-grained audit logs and exportable audit trails for compliance.
* Integrate with financial systems for live budget sync.
* Add multi-tenant support for different agencies.

---


