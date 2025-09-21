# Eagan

Eagan is a TypeScript workspace built around Vite for fast iteration on modern web features. This repository keeps all application code in the `eagan/` directory so documentation, tooling, and source live in one predictable place.

## Quick Start
1. Install dependencies: `npm install`
2. Start the development server: `npm run dev`
3. Run the production build: `npm run build`
4. Execute the automated test suite: `npm test`
5. Lint the codebase: `npm run lint`

## Available Scripts
| Command | Description |
| --- | --- |
| `npm run dev` | Launches the Vite dev server using `eagan/vite.config.ts`. |
| `npm run build` | Produces an optimized production bundle. |
| `npm test` | Runs Vitest in CI mode with coverage enabled via `eagan/vitest.config.ts`. |
| `npm run lint` | Executes ESLint with the shared config in `eagan/eslint.config.mjs`. |

## Project Layout
```
.
|-- AGENTS.md             # Agent collaboration guidelines
|-- eagan/                # Application workspace root
|   |-- assets/           # Static assets and fixtures
|   |-- src/              # Production source code (TypeScript/JSX)
|   |-- tests/            # Test suites mirroring the src structure
|   |-- vite.config.ts    # Vite build and dev server configuration
|   `-- vitest.config.ts  # Vitest test runner configuration
|-- package.json          # npm scripts and dev dependencies
`-- README.md             # You are here
```

## Development Guidelines
- Write modern TypeScript or JavaScript with 2-space indentation, single quotes, and semicolons.
- Keep shared utilities small and composable; mirror source structure in `eagan/tests` for discoverability.
- Run `npm run lint` and `npm test` before pushing to maintain quality and coverage (target >= 80%).
- Prefer fixtures under `eagan/assets/fixtures` and clean up side effects with test hooks.

## Testing & Coverage
Vitest drives automated testing with V8 coverage. The `npm test` command runs in CI mode; use `npx vitest` locally for watch mode as needed. Aim for at least 80% statement and branch coverage, and include snapshots or fixtures only when deterministic.

## Commit & Pull Requests
Follow Conventional Commits (e.g., `feat: add timeline filter`). Scope each change to a single cohesive update, link relevant issues, and document test evidence or screenshots in PR descriptions. Ensure CI is green and resolve merge warnings before landing on `main`.

## Additional Resources
- `AGENTS.md` outlines how this repository expects multiple agents to collaborate.
- `eslint.config.mjs`, `tsconfig.json`, and `vite.config.ts` capture the tooling defaults referenced above.
