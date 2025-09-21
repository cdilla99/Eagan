# Repository Guidelines

## Project Structure & Module Organization
The repository root holds high-level docs (`README.md`, `AGENTS.md`) and npm metadata (`package-lock.json`). Application work lives inside `eagan/`; treat it as the workspace root for features. Create `eagan/src` for production code, `eagan/tests` for suites, and `eagan/assets` for fixtures or static files, mirroring module names to keep navigation predictable. Keep feature folders focused and keep shared utilities small and composable.

## Build, Test, and Development Commands
This project is managed with npm. Run `npm install` at the root to sync dependencies before any change. Add scripts to `package.json` using the following conventions: `npm run dev` for local watchers, `npm run build` for production bundles, and `npm test` for automated suites. Document any additional command in `README.md` so new contributors can reproduce your workflow.

## Coding Style & Naming Conventions
Write modern JavaScript or TypeScript with 2-space indentation, mandatory semicolons, and single quotes unless a template literal is clearer. Use PascalCase for exported classes, camelCase for functions and variables, and kebab-case for filenames (`user-profile.ts`). Configure ESLint and Prettier to encode these rules, and run them locally (or via `npm run lint`) before committing.

## Testing Guidelines
Target at least 80% statement and branch coverage using Jest or Vitest. Store unit specs next to the implementation as `*.test.ts` or in `eagan/tests` mirroring the source tree. Keep deterministic fixtures under `eagan/assets/fixtures`, and clean up side effects via hooks. Run `npm test` before opening a pull request and capture any failing output in the PR description.

## Commit & Pull Request Guidelines
Follow Conventional Commits (`feat:`, `fix:`, `chore:`) in the imperative mood. Scope each pull request to a single cohesive change, link the relevant issue, and include testing notes or screenshots for UI work. Request at least one review, ensure CI is green, and resolve merge warnings before merging to `main`.
