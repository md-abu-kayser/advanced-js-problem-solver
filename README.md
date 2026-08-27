# Advanced JavaScript Problem Solver

<p align="center">
  <strong>2,825+ Interactive JavaScript Challenges • Step-by-Step Explanations • AI-Assisted Learning</strong>
</p>

<p align="center">
  A structured, interactive learning platform for developers who want to
  strengthen JavaScript fundamentals, modern ECMAScript concepts,
  problem-solving skills, and practical coding ability.
</p>

<p align="center">
  <a href="https://github.com/md-abu-kayser/advanced-js-problem-solver">
    <img src="https://img.shields.io/badge/GitHub-Repository-181717?style=for-the-badge&logo=github" alt="GitHub Repository" />
  </a>
  <a href="./LICENSE">
    <img src="https://img.shields.io/badge/License-MIT-blue.svg?style=for-the-badge" alt="MIT License" />
  </a>
  <img src="https://img.shields.io/badge/Challenges-2825%2B-0A66C2?style=for-the-badge" alt="2825+ Challenges" />
  <img src="https://img.shields.io/badge/React-19.1.1-61DAFB?style=for-the-badge&logo=react&logoColor=black" alt="React 19.1.1" />
  <img src="https://img.shields.io/badge/TypeScript-Strict-3178C6?style=for-the-badge&logo=typescript&logoColor=white" alt="TypeScript" />
  <img src="https://img.shields.io/badge/Vite-6.2.0-646CFF?style=for-the-badge&logo=vite&logoColor=white" alt="Vite 6.2.0" />
</p>

<p align="center">
  <a href="#overview">Overview</a> •
  <a href="#features">Features</a> •
  <a href="#architecture">Architecture</a> •
  <a href="#tech-stack">Tech Stack</a> •
  <a href="#getting-started">Getting Started</a> •
  <a href="#adding-new-problems">Adding Problems</a> •
  <a href="#roadmap">Roadmap</a>
</p>

---

## Overview

**Advanced JavaScript Problem Solver** is a React + TypeScript learning platform built around a large, structured collection of interactive JavaScript challenges.

Instead of presenting isolated coding questions, the application organizes problems by topic and pairs them with:

- Clear problem statements
- Guided explanations
- Reference implementations
- Practical problem-solving context
- AI-assisted hints and explanations
- Utility tools for learning and experimentation

The repository also demonstrates how a modern frontend application can combine **structured educational content with generative AI capabilities**.

---

# Why This Project Exists

Learning JavaScript effectively requires more than watching tutorials.

Developers need to repeatedly:

```text
Understand
    ↓
Attempt
    ↓
Fail
    ↓
Debug
    ↓
Reason
    ↓
Compare Solutions
    ↓
Practice Again
```

This project is designed around that loop.

Instead of treating coding problems as isolated exercises, the platform aims to provide a complete learning experience where developers can move from **problem discovery → implementation → explanation → guided assistance** within one application.

---

# Core Objectives

The project focuses on five primary objectives:

### 1. Practice

Provide a large and organized JavaScript problem library.

### 2. Understanding

Give developers explanations instead of only final answers.

### 3. Problem Solving

Encourage reasoning and implementation rather than passive reading.

### 4. Assistance

Use AI to help learners explore difficult concepts, request hints, and ask follow-up questions.

### 5. Extensibility

Make the problem library easy to expand without redesigning the application.

---

# Platform Highlights

```text
2,825+
Interactive Challenges

          +

Structured Explanations

          +

Reference Solvers

          +

AI-Assisted Learning

          +

Data-Driven Architecture
```

---

# Features

## Problem Library

Problems are organized into topic-specific collections rather than being stored as one large dataset.

Example categories include:

- Beginner fundamentals
- Arrays
- Loops
- Functions
- Closures
- ES6+
- Advanced JavaScript concepts
- Mini projects
- Utility-oriented challenges

The category-driven structure makes the platform easier to navigate and easier to expand.

---

## Interactive Problem Experience

Each problem is designed to provide more than a title and description.

The platform can expose:

```text
Problem
   │
   ├── Description
   │
   ├── Explanation
   │
   ├── Reference Solution
   │
   └── AI Assistance
```

This creates a more complete learning workflow than simply publishing a list of coding questions.

---

## AI Learning Assistant

The platform integrates Google's Generative AI ecosystem to provide an AI-assisted learning experience.

Typical use cases include:

- Asking questions about a problem
- Requesting hints
- Asking for clarification
- Exploring alternative approaches
- Requesting example code
- Understanding why a solution works

Conceptually:

```text
Learner
   │
   ▼
Problem Context
   │
   ▼
AI Assistant
   │
   ├── Hint
   ├── Explanation
   ├── Example
   └── Follow-up Question
```

---

## Data-Driven Problem Architecture

Problems are intentionally separated from UI components.

A topic can contain:

```text
topic/
├── problems.ts
├── explanations.ts
└── solvers.ts
```

This allows new educational content to be added without rewriting the application interface.

---

## Calculator & Utility Tools

The application includes helper utilities intended to support problem-solving sessions.

These include:

- Calculator functionality
- Mathematical utilities
- Supporting helper components

The calculator/utility layer is intended to reduce context switching while solving problems.

---

## Authentication-Ready Architecture

Authentication hooks and UI flows are prepared so the application can later connect to a real authentication backend.

Potential future use cases include:

- User accounts
- Learning progress
- Favorites
- Problem history
- Personalized learning paths

The current project should not be interpreted as a fully deployed authentication backend unless one is actually configured.

---

# Architecture

## High-Level Architecture

```text
┌─────────────────────────────────────────────────────────────┐
│                         USER                                │
└─────────────────────────────┬───────────────────────────────┘
                              │
                              ▼
┌─────────────────────────────────────────────────────────────┐
│                    REACT APPLICATION                        │
│                                                             │
│  Pages │ Components │ Hooks │ UI │ State                    │
└─────────────────────────────┬───────────────────────────────┘
                              │
                 ┌────────────┴────────────┐
                 ▼                         ▼
┌─────────────────────────┐    ┌──────────────────────────────┐
│   Problem Knowledge     │    │      External Services       │
│                         │    │                              │
│ problems.ts             │    │ Google Generative AI         │
│ explanations.ts         │    │                              │
│ solvers.ts              │    │ Future Auth / APIs           │
└────────────┬────────────┘    └──────────────┬───────────────┘
             │                                │
             └────────────────┬───────────────┘
                              ▼
                    ┌──────────────────────┐
                    │     UI Response      │
                    └──────────────────────┘
```

---

# Application Flow

A typical learning session can be represented as:

```text
Open Application
       ↓
Choose Topic
       ↓
Browse Problems
       ↓
Open Problem
       ↓
Understand Requirements
       ↓
Attempt Solution
       ↓
Review Explanation
       ↓
Compare Reference Solver
       ↓
Ask AI for Help
       ↓
Refine Understanding
       ↓
Move to Next Challenge
```

---

# Architectural Principles

## Separation of Content and Presentation

Educational data lives separately from presentation components.

```text
Content
  ├── Problems
  ├── Explanations
  └── Solvers

Presentation
  ├── Cards
  ├── Pages
  ├── Modals
  └── Assistant UI
```

This makes the content layer reusable and easier to maintain.

---

## Convention-Based Expansion

Adding another problem category should follow the existing pattern instead of introducing a new architecture for every topic.

```text
src/problems/
├── beginner-basics/
├── arrays/
├── functions/
├── closures/
└── advanced/
```

Each category can expose the same basic content contract.

---

# Tech Stack

## Frontend

| Technology   | Purpose                              |
| ------------ | ------------------------------------ |
| React 19.1.1 | UI library                           |
| TypeScript   | Type-safe application development    |
| Vite 6.2.0   | Development server and build tooling |
| Tailwind CSS | Utility-first styling                |
| daisyUI      | UI component layer                   |
| React Icons  | Icon system                          |

---

## AI

| Technology           | Purpose                                                       |
| -------------------- | ------------------------------------------------------------- |
| Google Generative AI | AI-assisted explanations, hints, and code-oriented assistance |

The repository currently references the Google GenAI ecosystem and its frontend integration.

---

## Utilities

| Technology   | Purpose                             |
| ------------ | ----------------------------------- |
| mathjs       | Mathematical and utility operations |
| Google Fonts | Typography                          |
| Font Awesome | Icons                               |
| Heroicons    | Interface icons                     |

---

## Developer Experience

| Technology | Purpose              |
| ---------- | -------------------- |
| ESLint     | Static code analysis |
| Prettier   | Code formatting      |
| PostCSS    | CSS processing       |
| Git        | Version control      |

---

# Repository Structure

```text
advanced-js-problem-solver/
│
├── public/
│   └── static-assets/
│
├── src/
│   │
│   ├── components/
│   │   ├── AIAssistant.tsx
│   │   ├── Calculator.tsx
│   │   ├── ProblemCard.tsx
│   │   ├── Problems.tsx
│   │   └── ...
│   │
│   ├── problems/
│   │   │
│   │   ├── beginner-basics/
│   │   │   ├── problems.ts
│   │   │   ├── explanations.ts
│   │   │   └── solvers.ts
│   │   │
│   │   ├── arrays/
│   │   │   ├── problems.ts
│   │   │   ├── explanations.ts
│   │   │   └── solvers.ts
│   │   │
│   │   └── ...
│   │
│   ├── services/
│   │   └── geminiService.ts
│   │
│   ├── App.tsx
│   ├── index.tsx
│   └── ...
│
├── .env
├── .gitignore
├── package.json
├── tailwind.config.js
├── vite.config.ts
└── README.md
```

The existing repository follows this general component + problem-data + service organization.

---

# Problem Data Model

The problem library follows a simple, extensible content model.

## `problems.ts`

Contains problem metadata such as:

```ts
export const problems = [
  {
    id: "array-001",
    title: "Find the Largest Number",
    description: "...",
  },
];
```

---

## `explanations.ts`

Maps problem identifiers to educational explanations.

Conceptually:

```ts
export const explanations = {
  "array-001": {
    approach: "...",
    reasoning: "...",
    complexity: "...",
  },
};
```

---

## `solvers.ts`

Contains reference implementations for the corresponding problems.

Conceptually:

```ts
export const solvers = {
  "array-001": `
    function findLargest(numbers) {
      // implementation
    }
  `,
};
```

The existing README explicitly defines these three files as the core problem-content structure.

---

# Adding New Problems

One of the main architectural goals is making the problem bank easy to extend.

## Step 1 — Create a Topic

Add a directory:

```text
src/problems/your-topic/
```

---

## Step 2 — Add Problem Definitions

Create:

```text
problems.ts
```

Example:

```ts
export const problems = [
  {
    id: "your-topic-001",
    title: "Your Problem",
    description: "Describe the problem clearly.",
  },
];
```

---

## Step 3 — Add Explanation

Create:

```text
explanations.ts
```

Example:

```ts
export const explanations = {
  "your-topic-001": `
    Explain the reasoning step by step.
  `,
};
```

---

## Step 4 — Add Reference Solver

Create:

```text
solvers.ts
```

Example:

```ts
export const solvers = {
  "your-topic-001": `
    function solve(input) {
      return input;
    }
  `,
};
```

---

## Step 5 — Register the Category

Add the new category to the central problem aggregation layer.

```text
src/problems/index.ts
```

This keeps problem discovery centralized.

---

# Content Authoring Guidelines

When creating a new challenge, prefer:

### Clear Problem Statements

The reader should know exactly what needs to be implemented.

### Explicit Inputs

Explain what the function receives.

### Explicit Outputs

Explain what should be returned.

### Edge Cases

Mention meaningful edge cases where necessary.

### Reference Reasoning

Explain why the solution works rather than only showing code.

### Practical Naming

Use descriptive IDs and titles.

Poor:

```text
problem1
test2
newQuestion
```

Better:

```text
array-two-sum
closure-counter
promise-all-reimplementation
deep-clone-object
```

---

# Getting Started

## Prerequisites

Install the following:

- Node.js 18 or later
- npm or Yarn
- A Google Cloud / Google AI project with the required Generative AI access

The project currently documents Node.js 18+ as the baseline.

---

# Installation

Clone the repository:

```bash
git clone https://github.com/md-abu-kayser/advanced-js-problem-solver.git
```

Enter the project directory:

```bash
cd advanced-js-problem-solver
```

Install dependencies:

```bash
npm install
```

Or:

```bash
yarn install
```

---

# Environment Configuration

Create a local environment file:

```text
.env
```

Example:

```env
VITE_GOOGLE_API_KEY=your_api_key_here
VITE_GOOGLE_API_ENDPOINT=https://generativeai.googleapis.com/v1
```

The current project documents these values for its AI assistant configuration.

## Important Security Consideration

Because variables prefixed with `VITE_` are intended for client-side applications, they should **not** be treated as secret server-side credentials.

For a production application, a safer architecture is:

```text
React Client
     │
     ▼
Application Backend
     │
     ▼
Generative AI Provider
```

rather than exposing sensitive provider credentials directly in the browser.

This is an important distinction between a development/demo architecture and a production credential-management architecture.

---

# Development

Start the development server:

```bash
npm run dev
```

Then open:

```text
http://localhost:5173
```

The existing project documents Vite's development server on port `5173`.

---

# Production Build

Build the application:

```bash
npm run build
```

Preview the production build locally:

```bash
npm run preview
```

The existing setup documents these commands as the production build workflow.

---

# Development Scripts

| Command           | Description                      |
| ----------------- | -------------------------------- |
| `npm run dev`     | Start Vite development server    |
| `npm run build`   | Build application for production |
| `npm run preview` | Preview production build         |
| `npm run lint`    | Run linting                      |
| `npm run format`  | Format source code               |
| `npm run test`    | Run configured tests             |

> Use `npm run` to inspect the exact scripts available in the current `package.json`.

---

# Code Quality

The project uses common frontend development tooling to support consistency.

## ESLint

Use ESLint to identify code-quality and static-analysis issues.

```bash
npm run lint
```

## Prettier

Use Prettier to maintain consistent formatting.

```bash
npm run format
```

The repository currently identifies ESLint and Prettier as part of its development tooling.

---

# Testing & Validation

The architecture is designed to make problem solvers independently testable.

For example:

```ts
import { solvers } from "./solvers";

describe("array-001", () => {
  it("returns the expected result", () => {
    const solve = solvers["array-001"];

    // test implementation
  });
});
```

However, the current repository documentation states that **formal unit tests are not shipped with the application yet**.

This README therefore treats testing as an extension point rather than claiming a fully established automated test suite.

---

# Recommended Testing Strategy

As the project grows, testing can be divided into three layers.

```text
                 Testing Pyramid

                     E2E
                    /   \
                   /     \
              Integration
                /       \
               /         \
             Unit Tests
```

### Unit Tests

Validate individual solver functions.

### Integration Tests

Validate problem loading and related application logic.

### End-to-End Tests

Validate the complete learner journey.

For example:

```text
Open topic
   ↓
Open problem
   ↓
View explanation
   ↓
Open solver
   ↓
Use AI assistant
```

---

# AI Integration Architecture

The AI assistant is isolated through a service layer rather than tightly coupling provider logic to every component.

Conceptually:

```text
AIAssistant.tsx
       │
       ▼
geminiService.ts
       │
       ▼
Google Generative AI
```

This creates a useful abstraction boundary.

If the provider changes later, the UI should not need to know the implementation details of the underlying AI service.

---

# Frontend Component Responsibilities

The project can be understood through several important component boundaries.

| Component         | Responsibility                 |
| ----------------- | ------------------------------ |
| `AIAssistant.tsx` | AI interaction UI              |
| `Calculator.tsx`  | Learning utility/calculator    |
| `ProblemCard.tsx` | Problem summary and navigation |
| `Problems.tsx`    | Problem listing and discovery  |
| `App.tsx`         | Application shell              |

The current repository documents these components as core parts of the frontend structure.

---

# Performance Considerations

The current application can be evolved with several performance strategies.

## Code Splitting

Load larger sections of the application only when needed.

## Lazy Loading

Lazy-load pages and feature-level components.

## Content Chunking

Avoid loading every educational problem payload into memory when a much smaller subset is needed.

## AI Request Control

AI requests should be triggered intentionally and should avoid unnecessary repeated calls.

## UI Responsiveness

Keep expensive calculations and rendering work away from the main interaction path wherever possible.

---

# Scalability Strategy

The current data-driven architecture makes several forms of growth possible.

## More Problems

```text
2,825+
   ↓
5,000+
   ↓
10,000+
```

Additional problems can follow the same data contract without requiring a new UI architecture.

## More Topics

```text
JavaScript
├── Fundamentals
├── Arrays
├── Functions
├── Objects
├── Closures
├── Async JavaScript
├── DOM
├── Browser APIs
└── Advanced Concepts
```

## More Languages

The current roadmap already considers expansion into additional programming languages.

A future abstraction could become:

```text
Learning Platform
├── JavaScript
├── TypeScript
├── Python
└── Java
```

---

# Future Architecture

A possible evolution of the application:

```text
                        Web Client
                            │
                            ▼
                     Application API
                            │
             ┌──────────────┼──────────────┐
             ▼              ▼              ▼
         Problems        Progress       AI Service
         Service         Service        Gateway
             │              │              │
             └──────────────┼──────────────┘
                            ▼
                       Data Storage
```

This would support persistent user progress, personalization, analytics, and more sophisticated AI workflows.

---

# Product Evolution

The platform can evolve from a static problem library into a personalized learning system.

```text
                    Problem Library
                           │
                           ▼
                    User Attempts
                           │
                           ▼
                     Progress Data
                           │
                           ▼
                 Skill Classification
                           │
                           ▼
              Personalized Recommendations
                           │
                           ▼
                   Next Best Problem
```

This creates the foundation for adaptive learning.

---

# Roadmap

The documented roadmap includes:

```text
[ ] User authentication with a backend
[ ] Persist user progress
[ ] Favorite problems
[ ] Community problem submissions
[ ] Mobile experience improvements
[ ] Additional language support
[ ] GitHub Actions preview deployments
```

These roadmap items are based on the existing project direction.

---

# Contribution Workflow

Contributions are welcome.

## Fork

Fork the repository and clone your fork.

```bash
git clone https://github.com/md-abu-kayser/advanced-js-problem-solver.git
```

## Create a Branch

```bash
git checkout -b feature/add-new-problems
```

## Make Changes

Follow the existing architecture and naming conventions.

## Validate

```bash
npm run lint
npm run format
npm run build
```

## Commit

Use a meaningful Conventional Commit-style message:

```bash
git commit -m "feat(problems): add closure practice challenges"
```

## Push

```bash
git push origin feature/add-new-problems
```

Then open a Pull Request.

---

# Contribution Guidelines

When contributing new problems:

### Keep IDs Stable

Problem IDs should remain unique and predictable.

### Avoid Duplicate Problems

Search existing categories before adding a new challenge.

### Explain the Reasoning

A good educational problem should teach a concept rather than simply provide a solution.

### Include Edge Cases

Important input boundaries should be represented in the explanation.

### Keep Solvers Readable

Reference implementations are educational resources, so readability matters.

### Keep UI and Content Separate

New educational content should normally be added through the existing data-driven system rather than hard-coded into UI components.

---

# Commit Convention

Recommended commit prefixes:

```text
feat      → New functionality
fix       → Bug fix
refactor  → Code restructuring
docs      → Documentation
test      → Tests
chore     → Tooling / maintenance
perf      → Performance improvement
```

Examples:

```text
feat(problems): add array transformation challenges
feat(ai): improve assistant prompt context
fix(problems): correct solver output
refactor(content): normalize problem metadata
docs(readme): improve project documentation
test(solvers): add edge-case coverage
chore(deps): update frontend dependencies
```

---

# Engineering Standards

The project aims to maintain:

```text
✓ TypeScript-first development
✓ Functional React components
✓ Reusable components
✓ Data-driven problem content
✓ Clear service boundaries
✓ Consistent naming
✓ ESLint validation
✓ Prettier formatting
✓ Small focused changes
✓ Meaningful commits
✓ Documentation alongside architecture changes
```

---

# Project Use Cases

This repository can serve several purposes.

### For Learners

Use it as a structured JavaScript practice environment.

### For Educators

Use the problem/explanation/solver model as a content-authoring foundation.

### For Developers

Study the architecture of a React + TypeScript + Vite application.

### For AI Application Development

Explore how generative AI can be integrated into an educational frontend workflow.

### For Portfolio Review

The repository demonstrates frontend engineering, structured content architecture, API/service integration, and AI-assisted UX.

---

# Project Philosophy

The core philosophy is simple:

> **Do not just solve problems. Understand why the solution works.**

The platform therefore treats:

```text
Problem
+
Reasoning
+
Implementation
+
Explanation
+
Experimentation
=
Learning
```

as the fundamental learning model.

---

# Known Limitations

The current project should be understood within its present implementation scope.

### Automated Testing

Formal tests are not currently shipped as a complete test suite.

### Authentication

Authentication hooks are prepared for extension rather than representing a complete production identity system.

### AI Credentials

Frontend-exposed `VITE_` environment variables should not be treated as a secure mechanism for hiding provider secrets.

### Persistent Learning Data

A full progress/personalization system requires a persistent backend and data layer.

---

# Documentation Resources

## JavaScript

- [MDN JavaScript](https://developer.mozilla.org/en-US/docs/Web/JavaScript)
- [ECMAScript Specification](https://tc39.es/ecma262/)

## Frontend

- [React](https://react.dev/)
- [TypeScript](https://www.typescriptlang.org/docs/)
- [Vite](https://vite.dev/)
- [Tailwind CSS](https://tailwindcss.com/docs/)
- [daisyUI](https://daisyui.com/)

## AI

- [Google AI Developer Documentation](https://ai.google.dev/)

## Tooling

- [ESLint](https://eslint.org/docs/latest/)
- [Prettier](https://prettier.io/docs/)

---

# License

This project is licensed under the **MIT License**.

See the [LICENSE](./LICENSE) file for details.

---

# Maintainer

<p align="center">
  <strong>Md Abu Kayser</strong>
</p>

<p align="center">
  Full-Stack Developer
</p>

<p align="center">
  <a href="https://github.com/md-abu-kayser">
    GitHub
  </a>
  •
  <a href="mailto:abu.kayser.official@gmail.com">
    Email
  </a>
</p>

---

<p align="center">
  <a href="#advanced-javascript-problem-solver">⬆ Back to top</a>
</p>

<p align="center">
  <strong>Built for deliberate practice, deeper reasoning, and continuous improvement.</strong>
</p>

<p align="center">
  Made with ❤️ and ☕ by Md Abu Kayser
</p>
