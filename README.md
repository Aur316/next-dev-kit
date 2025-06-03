# How can you use this repository?

1. Clone the repository and install dependencies

```bash
git clone https://github.com/Aur316/next-builder-kit.git
```

```bash
cd next-builder-kit
```

```bash
rm -rf .git
```

2. If you'd rather start with a new repository based on this one, click the green <code style="color : green">Use this template</code> button at the top of the GitHub page. This will let you generate a fresh copy of the repository under your own GitHub account, preserving all files but without commit history.

3. Create with one command

```bash
npx next-builder-kit
```

# Getting Started

At first install the dependencies:

```bash
npm install
```

Run the development server:

```bash
npm run dev
```

Open http://localhost:3000 to view it in your browser.

## Tooling & Conventions: ESLint, Strict, TypeScript rules

- No <code>any</code> type allowed

- No console.log (only console.warn and console.error are permitted)

- Automatic unused import removal

- Tailwind CSS class order is automatically sorted

- ESLint autofix enabled on commit and save

## Commit Rules

Only:

- feat:
- fix:
- chore:
- docs:
- style:
- refactor:
- perf:
- test:
- ci:
- build:
- revert:

prefixes are allowed in commit messages.

All commits are linted with commitlint.

### Examples:

```bash
git commit -m "feat: add login form"
```

```bash
git commit -m "fix: button layout issue"
```

## Branch Name Rules

Only the following branch name patterns are accepted:

- feat/
- fix/
- chore/
- docs/
- style/
- refactor/
- perf/
- test/
- ci/
- build/
- revert/

### Examples:

```bash
feat/my-feature
```

```bash
fix/my-bug
```

Anything outside of this (e.g. main, dev, testbranch) is blocked from pushing.

## VS Code Format on Save

The .vscode/settings.json is versioned and ensures:

- Format on save is enabled

- ESLint autofix (including unused import removal) on save

- Tailwind class sorting on save via Prettier

- No manual formatting needed — just save the file

- Group and sort imports on save, and insert an empty line between each group

## Import pattern

Added index.ts files to all major module folders to centralize exports.
This allows simplified and consistent imports, improves maintainability, and decouples internal file structures from consumers.

### Preferences

1. Cleaner and shorter import paths
2. Easier refactors — no need to rewrite import paths if file names change
3. Promotes encapsulation and folder-as-module thinking
