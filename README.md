<p align="center">
  <img src="Credit-Bladi-Logo.png" alt="Credit Bladi logo" width="260">
</p>

# Credit Bladi — Docs & Project Hub

Moroccan mortgage credit simulator, compliant with Bank Al-Maghrib (BAM) regulatory rules.
This repo is the **entry point** for the project: it doesn't contain any code, only the links
and context a developer, tester, or manager needs to find the right repo.

## Repos

| Repo | Role | Stack |
|---|---|---|
| [`---Credit-Bladi---`](https://github.com/LouziAmine/---Credit-Bladi---) | **Backend** (API) | Java 25, Spring Boot 4 |
| [`---Bladi-Credit-Portal---`](https://github.com/LouziAmine/---Bladi-Credit-Portal---) | **Frontend** (web app) | Angular 22, TypeScript |

## What is Credit Bladi?

Credit Bladi computes mortgage loan simulations for two financing products: a **Conventional**
interest-based mortgage and a **Mourabaha** (Sharia-compliant, participative) financing. Pricing
depends on the applicant's professional status (employee, civil servant, freelancer, professional,
retired), each with its own BAM-regulated rate calculation. A separate, role-gated Administration
area lets bank staff (`MANAGER` role) adjust the regulatory parameters, manage staff accounts, and
review the compliance audit trail.

## 🎥 Onboarding walkthrough video

A screen-recorded walkthrough is available for anyone (developer, tester, backend or frontend)
who just cloned the project: cloning, installing dependencies, running the app, launching the
test suite, and generating the test reports.

[![Watch the onboarding walkthrough video](https://img.youtube.com/vi/uX9JC3fSl5s/maxresdefault.jpg)](https://www.youtube.com/watch?v=uX9JC3fSl5s)

## Who does what

- **Developer**: pick the repo matching what you're working on (backend API vs. frontend UI).
  Each repo's own README has the full setup (`Getting Started`, environment variables, run
  locally).
- **Tester**: both repos ship a `./run-tests.sh` interactive menu (unit, integration/E2E,
  performance, security scans — SAST/SCA/DAST). See each repo's `docs/testing.md` for reference
  results and annotated report screenshots.
- **Manager**: see each repo's `docs/business-workflow.md` for a non-technical walkthrough of the
  business rules (backend) and screen-by-screen user journeys (frontend).

## Running the full stack locally

1. Backend first (`---Credit-Bladi---`): `./mvnw spring-boot:run -Dspring-boot.run.profiles=dev` → `http://localhost:8080`
2. Frontend (`---Bladi-Credit-Portal---`): `npm install && npm start` → `http://localhost:4200`

The frontend talks to the backend at `http://localhost:8080/api/v1` in dev (see its
`environment.development.ts`).

## Contact

**Amine Louzi** (louzi.amine.pro.pro@gmail.com)
