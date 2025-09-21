# Copilot Instructions

This document provides AI-powered coding assistants with essential guidance for contributing to the Eagan project.

## Project Overview & Architecture

Eagan is a modern web application built with TypeScript and Vite. The entire application workspace is located inside the `eagan/` directory, which should be treated as the root for all development activities.

- **Source Code**: Production code resides in `eagan/src`.
- **Tests**: Automated tests are in `eagan/tests`, mirroring the `eagan/src` directory structure.
- **Static Assets**: All static files, including test fixtures, are stored in `eagan/assets`.
- **Configuration**: Key configuration files are located in the `eagan/` directory:
  - `vite.config.ts`: For the Vite build and development server.
  - `vitest.config.ts`: For the Vitest test runner.
  - `eslint.config.mjs`: For ESLint linting rules.
  - `tsconfig.json`: For TypeScript compiler options.

The project is structured as a monorepo, with the root `package.json` containing scripts that delegate to the tools configured within the `eagan/` workspace.

## Development Workflow

All development commands should be run from the repository root.

- **Install Dependencies**:
  ```bash
  npm install
  ```

- **Run Development Server**:
  ```bash
  npm run dev
  ```
  This starts the Vite development server.

- **Run Tests**:
  ```bash
  npm test
  ```
  This executes the test suite using Vitest. For watch mode during development, run `npx vitest`.

- **Build for Production**:
  ```bash
  npm run build
  ```
  This creates an optimized production build.

- **Lint Code**:
  ```bash
  npm run lint
  ```
  This checks the code against the project's ESLint rules.

## Coding Style & Conventions

- **Language**: Write modern TypeScript.
- **Formatting**: Use 2-space indentation, single quotes for strings, and mandatory semicolons.
- **Naming**:
  - `PascalCase` for classes and types.
  - `camelCase` for functions and variables.
  - `kebab-case` for filenames (e.g., `user-profile.ts`).
- **Commits**: Follow the [Conventional Commits](https://www.conventionalcommits.org/) specification (e.g., `feat:`, `fix:`, `chore:`).

## Testing

- **Framework**: Tests are written with [Vitest](https://vitest.dev/).
- **Location**: Unit tests should be placed in `eagan/tests` and mirror the `src` directory structure. For example, a test for `eagan/src/components/Button.ts` would be `eagan/tests/components/Button.test.ts`.
- **Coverage**: Aim for at least 80% test coverage.
- **Fixtures**: Deterministic test fixtures should be placed in `eagan/assets/fixtures`.
