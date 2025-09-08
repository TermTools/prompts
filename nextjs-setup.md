📝 Prompt for Claude (Next.js Setup)

You are a senior frontend engineer. Act as an autonomous operator: create a modern Next.js project from scratch, configure styling, linting, and testing, and verify everything works. Do not just list commands—run what’s needed, fix issues, and confirm success.

Assumptions

Machine has recent Node.js LTS + npm (or yarn/pnpm).

OS may be macOS, Linux, or Windows. Use OS-appropriate commands.

No version pinning unless required by dependencies.

Goals

Set up a new Next.js app with:

✅ Latest stable Next.js (App Router by default).

✅ TypeScript enabled (default, fallback to JS if not available).

✅ Tailwind CSS for styling.

✅ ESLint + Prettier with non-conflicting config.

✅ Testing via Jest or Vitest + React Testing Library.

✅ Git hooks with Husky + lint-staged.

✅ .editorconfig, .gitignore, .env.example.

✅ Clean starter UI with a Tailwind-styled homepage and a passing test.

✅ Git initialized with first commit.

Behavior

Adapt to environment, fix missing deps, retry installs if needed.

Output short numbered steps, concise logs, and verification at the end.

Keep config minimal and conventional.

Steps to perform

Scaffold a Next.js app (create-next-app). Default name: my-next-app. Use TypeScript.

Install Tailwind CSS + PostCSS + Autoprefixer, configure purge paths.

Configure ESLint + Prettier (React + Hooks rules, extend Prettier).

Set up testing (Vitest or Jest + React Testing Library). Add a sample test.

Add Husky + lint-staged for pre-commit hooks.

Create .editorconfig, .gitignore, .env.example.

Update package.json scripts: dev, build, start, test, lint, format, prepare.

Replace default page with Tailwind-styled homepage.

Run dev server, build, tests, lint, and format — confirm all pass.

Initialize Git repo, make first commit.

Verification Checklist

✅ npm run dev serves app locally (print URL)

✅ Build & start commands succeed

✅ Tests pass

✅ Lint & format succeed

✅ Husky hooks trigger

✅ Tailwind styles render

✅ Git repo initialized with commit

Output exactly these steps, commands, and verifications. Be autonomous: run, fix, and confirm success without asking follow-ups unless absolutely required.

