# CLAUDE.md — Project Intelligence & AI Assistant Guidelines

This document provides project context, technical stack definitions, architectural conventions, and instructions for AI coding assistants (Claude Code, Cursor, Antigravity) working in this repository.

---

## 1. Project Overview

**Flyrank Capstone Project** — Frontend Engineering Track  
A modern web application demonstrating clean frontend architecture, AI-assisted development workflows, and strict engineering standards.

- **Track:** AI Frontend Engineering Internship
- **Phase:** Environment Setup & AI Toolchain (Phase 1)
- **Author:** Nitish (`nitishfr05`)

---

## 2. Tech Stack

| Domain | Technology / Specification |
|---|---|
| **Runtime Environment** | Node.js v24.x (Active LTS) |
| **Package Manager** | npm (v10+) |
| **Frontend Framework** | React / Next.js / Vite |
| **Language** | JavaScript (ES2024+) / TypeScript |
| **Styling** | Vanilla CSS / Modern CSS Modules / TailwindCSS |
| **Version Control** | Git + Conventional Commits 1.0.0 |
| **AI Toolchain** | Claude Code CLI, Cursor IDE, Antigravity |

---

## 3. Engineering Conventions

### 3.1 Git & Conventional Commits
All commits in this repository **must** strictly follow the [Conventional Commits 1.0.0](https://www.conventionalcommits.org/en/v1.0.0/) specification:

```
<type>(<optional scope>): <description>

[optional body]

[optional footer(s)]
```

#### Allowed Commit Types:
- `feat`: A new user-facing feature
- `fix`: A bug fix
- `docs`: Documentation changes only (README, CLAUDE.md, etc.)
- `style`: Changes that do not affect the meaning of the code (formatting, semi-colons)
- `refactor`: Code changes that neither fix a bug nor add a feature
- `perf`: A code change that improves performance
- `test`: Adding missing tests or correcting existing tests
- `build`: Changes affecting the build system or external dependencies
- `ci`: Changes to CI configuration files and scripts
- `chore`: Other changes that don't modify src or test files (scaffolding, tooling)

#### Commit Message Rules:
- Use imperative, present tense ("add feature" not "added feature" or "adds feature").
- Do not capitalize the first letter after the colon.
- No period (`.`) at the end of the subject line.

---

### 3.2 Code Style & Quality Standards

- **Naming Conventions:**
  - Variables & Functions: `camelCase` (e.g., `fetchUserData`, `isLoading`)
  - React Components & Types: `PascalCase` (e.g., `UserProfileCard`, `NavigationMenu`)
  - Constants & Config: `UPPER_SNAKE_CASE` (e.g., `MAX_RETRY_COUNT`, `API_BASE_URL`)
  - Files & Folders: `kebab-case` or `PascalCase` for React components
- **JavaScript/TypeScript Practices:**
  - Prefer `const` over `let`; never use `var`.
  - Use ES module syntax (`import` / `export`).
  - Favor declarative and functional programming patterns over imperative mutations.
  - Implement strict error handling and input validation.
- **Component Architecture:**
  - Keep components modular, accessible (WCAG compliant), and single-responsibility.
  - Separate business logic and data fetching from UI presentation where applicable.

---

## 4. File & Folder Structure

```text
flyrank-capstone/
├── .cursorrules           # Cursor IDE AI rules
├── .gitignore             # Standard Git ignore specifications
├── CLAUDE.md              # Claude Code & AI context guide (this file)
├── LICENSE                # MIT License
├── README.md              # Project documentation & setup instructions
├── package.json           # Node manifest & scripts
├── public/                # Static assets
└── src/                   # Application source code
    ├── assets/            # Images, icons, and styling tokens
    ├── components/        # Reusable UI components
    ├── hooks/             # Custom React hooks
    ├── pages/ or app/     # Routing and views
    ├── services/          # API & external service integrations
    └── utils/             # Helper utilities and formatters
```

---

## 5. Development Workflow & Commands

```bash
# Install dependencies
npm install

# Start local development server
npm run dev

# Run test suite
npm test

# Lint and format code
npm run lint
npm run format

# Build production bundle
npm run build
```

---

## 6. AI Assistant Instructions

When assisting in this codebase, AI models must:
1. Adhere strictly to the tech stack and architecture outlined above.
2. Formulate concise, accurate commit messages using the Conventional Commits specification.
3. Validate that generated code builds cleanly and contains zero placeholder or dummy fallbacks without explanation.
4. Provide context-aware suggestions and explain architectural trade-offs.
