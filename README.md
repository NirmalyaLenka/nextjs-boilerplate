# Next.js Starter

A minimal **Next.js App Router** starter built with TypeScript, React, and Tailwind CSS. The repository currently contains the default Create Next App landing page; it is a starting point for a custom application, not a finished product.

## Overview

- **Framework:** Next.js 15
- **Language:** TypeScript
- **UI:** React 19 and Tailwind CSS 4
- **Routing:** Next.js App Router
- **Typography:** Geist and Geist Mono through `next/font`
- **Package manager:** npm (the committed `package-lock.json` keeps installs reproducible)

## Requirements

- Node.js 20 LTS recommended
- npm (included with Node.js)

## Run locally

Clone the repository and enter its directory:

```bash
git clone https://github.com/NirmalyaLenka/nextjs-boilerplate.git
cd nextjs-boilerplate
npm ci
npm run dev
```

Open [http://localhost:3000](http://localhost:3000). Edit `app/page.tsx` and save to see changes during development.

## Available commands

| Command | Purpose |
| --- | --- |
| `npm run dev` | Start the local development server with Turbopack |
| `npm run build` | Create a production build |
| `npm run start` | Serve the production build (run `npm run build` first) |
| `npm run lint` | Run the lint command configured in `package.json` |

Run the production build before deployment. The commands above are documented from the package manifest; they have **not** been represented as passing CI checks in this documentation update.

**Lint-script limitation:** `package.json` defines `npm run lint` as `next lint`, but the manifest does not declare `eslint` or `eslint-config-next`. The lint command may therefore fail in a clean install until the lint tooling is configured. This was identified from the manifest; the command was not executed, and no dependencies were changed.

## Repository map

```text
nextjs-boilerplate/
├── app/
│   ├── favicon.ico       # Browser tab icon
│   ├── globals.css       # Global styles and Tailwind entry point
│   ├── layout.tsx        # Root layout, fonts, and page metadata
│   └── page.tsx          # Current home page / primary editing point
├── public/
│   ├── file.svg          # Starter illustration asset
│   ├── globe.svg         # Starter illustration asset
│   ├── next.svg          # Next.js logo asset
│   ├── vercel.svg        # Vercel logo asset
│   └── window.svg        # Starter illustration asset
├── .gitignore            # Files excluded from version control
├── next.config.ts        # Next.js configuration
├── package.json          # Dependencies and npm scripts
├── package-lock.json     # Locked npm dependency tree
├── postcss.config.mjs    # PostCSS / Tailwind integration
├── tsconfig.json         # TypeScript compiler configuration
└── README.md             # Setup, structure, and maintenance notes
```

### Where to make changes

- **Page content and layout:** `app/page.tsx`
- **Global styling:** `app/globals.css`
- **Site-wide metadata and fonts:** `app/layout.tsx`
- **Static assets:** `public/`
- **Framework configuration:** `next.config.ts`
- **Dependencies and commands:** `package.json`

Keep route-specific pages and components in `app/` as the application grows. Add separate `components/`, `lib/`, or `public/images/` directories only when the project needs them; they are not present in the current tree.

## Current scope and limitations

- The home page is still the default starter screen.
- No product-specific features, API routes, authentication, database, or automated test suite are currently documented as implemented.
- No hardware, firmware, or bill of materials applies to this web starter.
- Before treating this as a production application, replace the starter content and metadata, define the application's requirements, add tests and CI checks, and review dependency/security posture.

## Deployment

Build locally with `npm run build`, then deploy to a Node.js-compatible host or [Vercel](https://vercel.com/). Review the [Next.js deployment guide](https://nextjs.org/docs/app/building-your-application/deploying) and configure environment variables in the deployment platform rather than committing secrets.

## Skills and technologies

![Next.js](https://img.shields.io/badge/Next.js-15-black?logo=next.js)
![TypeScript](https://img.shields.io/badge/TypeScript-5-3178C6?logo=typescript)
![React](https://img.shields.io/badge/React-19-61DAFB?logo=react)
![Tailwind CSS](https://img.shields.io/badge/Tailwind_CSS-4-06B6D4?logo=tailwindcss)

## Maintenance & audit

- **Last updated:** 14 November 2026
- **Review scope:** README accuracy, setup instructions, package scripts, and repository paths.
- **Changes in this pass:** Added a documented limitation for the `next lint` script because the package manifest does not declare `eslint` or `eslint-config-next`. Application code and dependencies were not changed.
- **Verification:** No build, lint, automated test, or deployment run was performed as part of this documentation-only pass. Do not interpret this date as a verified release or production-readiness claim.
- **Next review:** Recheck the documented commands and dependency versions when application code or the package manifest changes.
