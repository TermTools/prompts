# Generic React App Setup

You are an expert frontend engineer. Act as an **autonomous operator**: decide tools, run commands, fix issues, and confirm success without asking follow‑up questions unless absolutely required. **Do not list every command** up front—**execute** what is needed, adapting to the environment.

## Assumptions

* User machine has a recent **Node.js LTS** and **npm** (or yarn/pnpm). If versions are incompatible, **detect and adapt** (e.g., use `corepack` or switch to npm).
* OS can be macOS, Linux, or Windows (PowerShell). Use OS-appropriate commands.

## Goals

Create a new modern React project with:

* Fast build tooling (prefer **Vite** or equivalent).
* **Tailwind CSS** configured.
* **ESLint + Prettier** with sensible, non-conflicting rules.
* Optional **TypeScript** (default: **enabled** unless missing types/tooling—then fall back to JS gracefully).
* **Testing** via **Vitest** + **React Testing Library** with a sample test.
* Useful npm scripts (`dev`, `build`, `preview`, `test`, `lint`, `format`).
* **Husky** pre-commit hook: run `lint` and `format` on staged files (use `lint-staged`).
* Project metadata: `.editorconfig`, `.gitignore`, example `.env.example`.
* Clean starter UI (App with a Tailwind starter page and passing test).
* Initialized **git** repo with first commit.

## Constraints & Best Practices

* **No version pinning** unless required by the toolchain. Use latest stable defaults.
* Keep config minimal and conventional. Avoid framework lock-in beyond React.
* Ensure ESLint and Prettier **do not conflict** (extend `eslint-config-prettier`).
* Tailwind purge/content paths must cover `index.html` and all files in `src/`.
* Prefer `npm` unless an existing lockfile dictates otherwise.
* Use relative, cross-platform commands; avoid shell-specific features when possible.

## Behavior & Recovery

* Detect environment (Node, package manager, OS) and **self-correct** errors (retry installs, fix missing peer deps, regenerate configs if needed).
* If a command fails, **diagnose**, apply the fix, and retry.
* Keep output **concise**: short status lines + the essential diffs/paths created.

## Steps (operate autonomously)

1. Create project folder (default name: `my-react-app`). If folder exists, make the process **idempotent** (don’t overwrite without backup).
2. Scaffold a React app (prefer Vite). Use **TypeScript** template when available; otherwise use JS.
3. Install dependencies and devDependencies for React, Tailwind, PostCSS, Autoprefixer.
4. Initialize Tailwind config and PostCSS config; wire up Tailwind in the main CSS.
5. Install and configure ESLint + Prettier (React + Hooks rules). Ensure `"extends": ["eslint:recommended", "plugin:react/recommended", "plugin:react-hooks/recommended", "prettier"]` and add a Prettier config.
6. Set up Vitest + React Testing Library; add a sample component test and vitest config if needed.
7. Add Husky + lint-staged; pre-commit runs lint and prettier on staged files.
8. Create `.editorconfig`, `.gitignore`, and `.env.example` with a sample variable; ensure Vite loads env via `import.meta.env`.
9. Update `package.json` scripts: `dev`, `build`, `preview`, `test`, `lint`, `format`, and `prepare` (for Husky).
10. Replace the default App with a minimal Tailwind-styled landing screen and a passing sample test.
11. Run `dev` server and confirm URL is reachable locally; run tests and linter to confirm green.
12. Initialize git and create the first commit with a clear message.

## Verification Checklist (print at end)

* ✅ `npm run dev` serves app locally (show URL)
* ✅ `npm run build` completes
* ✅ `npm run preview` serves built app
* ✅ `npm run test` passes sample test
* ✅ `npm run lint` and `npm run format` succeed
* ✅ Husky pre-commit hook triggers on commit
* ✅ Tailwind classes render in the starter page
* ✅ Git repo initialized with initial commit

## Output Format

* Print **brief progress logs** while executing.
* At the end, print a short **Next Steps** list (how to start dev server, where to edit files) and the verification checklist.

(Proceed now. Execute commands and make fixes as needed without asking follow-ups unless absolutely necessary.)

