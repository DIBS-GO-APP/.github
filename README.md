# 🛠️ Dibs Go Developer Handbook

Welcome to the official Dibs Go development handbook. This document defines our shared principles, project structure, workflows, tooling standards, and team expectations across all repositories.
This file is still underconstruction and will be updated regularly 🏗️🚧.

---

## 🚀 Our Mission

Build modern, performant, and secure experiences for business to market and sell their products through our mobile apps.

---

## 🧭 Repository Structure & Purpose

| Repo Name                  | Description                                  |
|---------------------------|----------------------------------------------|
| `Dibs-Go-Admin-web`       | Admin dashboard frontend (Next.js)           |
| `Dibs-Go-Business-web`    | Business web dashboard frontend (Next.js)    |
| `Dibs-Go-Backend`         | Backend services (Spring-boot, Swagger)      |

---

## 🧱 Tech Stack Guidelines

### Frontend (Web)

- **Framework**: Next.js (v15+, App Router)
- **Styling**: Tailwind CSS (v4)
- **Theme System**: `next-themes` with CSS variables
- **Component System**: Flowbite or other tailwind libraries
- **API Layer**: `openapi-typescript-codegen` with Swagger

### Backend

- **Framework**: Spring-boot with spring-security
- **API Docs**: OpenAPI via Swagger
- **Security**: JWT, role-based access, middleware guards
- **I18n**: dynamic language support
- **Sendgrid**: support for mailing system through twilio

---

## 🌐 Environments & Branching

### Branch Structure (Git Flow)

- `main`: Production-ready code
- `staging`: Pre-production QA testing
- `dev`: Active development
- Feature branches follow this naming convention:
feature/<feature-name>
bugfix/<bug-name>
hotfix/<task-name>

consult the following cheat sheet for git flow for better branch managment: https://danielkummer.github.io/git-flow-cheatsheet/

> All PRs must target `dev` and be squash-merged.

---

## 🚀 Development Setup

Each repo includes a `README.md` with setup instructions, but globally:

# Recommended global tools

Use .env.example as the base for local config
Install dependencies via Yarn, not npm

---

# 📦 Code Standards
## ✅ Linting & Formatting
ESLint for JS/TS

Prettier for consistent formatting

## ✅ Git Conventions
Use Gitmoji for commit messages

Use meaningful PR descriptions

### Every PR must:

- Have a clear title and description
- Be reviewed by at least one other developer

---

# 📄 API Integration
All frontend projects using Swagger will have:

- Auto-generated API clients via openapi-typescript-codegen
- Scripts like:

```bash
yarn openapi
```
Fully typed service layers (no manual DTOs)

---

# 🧪 Testing & QA
Manual test instructions go in each PR when needed

---

# 🧱 Components & Design
Follow the Dibs design system

Use our theme tokens (defined in globals.css for web apps)

Prefer reusable, composable components

Every component should be tested with different themes if theme support exists

---

# 🛡️ Security Practices
Never commit secrets — use .env.local or Vault (coming soon)

Rotate API tokens regularly

Middleware guards (auth, permissions) must wrap all protected endpoints

Rate limiting and logging required for exposed endpoints

---

# 💬 Communication & Collaboration
Use GitHub Discussions or issues for design debates or create a thread on clickup dev channel
