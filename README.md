# FitFlow

A fitness and nutrition application built step by step while learning full-stack development.

## Current stage

A minimal React + TypeScript frontend created with Vite. It displays a FitFlow welcome page. No backend, database, authentication, workout tracking, or nutrition functionality has been added yet.

## Requirements

- Node.js compatible with Vite (verified here with 24.20.0)
- npm (verified here with 11.19.0)
- Git

Java is installed for a future backend, but is not used by this frontend.

## Run locally

From the repository root:

```sh
cd frontend
npm ci
npm run dev
```

Open the Local URL printed by Vite, usually http://localhost:5173. Stop the server with Ctrl+C. Edit `src/App.tsx` and save to see the page update.

## Check the project

From `frontend/`:

```sh
npm run build
npm run lint
```

The build checks TypeScript and creates production assets in `dist/`. Lint checks source code for common mistakes. To serve a completed build locally, use `npm run preview`.

## Project map

- `frontend/index.html`: the HTML entry point, including the element React renders into.
- `frontend/src/main.tsx`: attaches React to that element and renders `App`.
- `frontend/src/App.tsx`: the root UI component.
- `frontend/src/App.css`: styles for the welcome component.
- `frontend/src/index.css`: shared styles for the whole page.
- `frontend/package.json`: dependency declarations and npm commands.
- `frontend/package-lock.json`: resolved dependency versions; commit this file for reproducible installations.
- `frontend/vite.config.ts`: configures Vite's React support.
- `frontend/tsconfig*.json`: TypeScript compiler settings for app and build configuration code.
- `.gitignore`: excludes dependencies, build output, local environment files, credentials, and editor files.

`node_modules/` and `dist/` are generated and are not committed. Frontend environment variables are visible in the browser; never put secrets in them.

## Connect GitHub manually

GitHub CLI was not installed during setup. In GitHub, create an empty repository named `FitFlow`; choose your preferred visibility and leave the README, .gitignore, and license initialization options unchecked.

Then run from this repository's root, replacing `YOUR_USERNAME`:

```sh
git remote add origin https://github.com/YOUR_USERNAME/FitFlow.git
git push -u origin main
```

If authentication is requested, use a personal access token through Git's credential prompt, not your GitHub account password. Never put a token in a remote URL or a project file.

Alternatively, if you later install and authenticate GitHub CLI:

```sh
gh auth login
gh repo create FitFlow --private --source=. --remote=origin --push
```

Use the CLI alternative only if the repository and `origin` remote have not already been created.

## Before the Exercise Card

Understand the render path: `index.html` → `main.tsx` → `App.tsx`. A React component is a function that returns JSX (markup inside JavaScript/TypeScript). CSS controls appearance. Later, props will let a parent pass exercise data to a reusable card; TypeScript will describe the shape of that data.

Git tracks local history; GitHub hosts a remote copy. Review `git status` and `git diff --staged` before each commit.
