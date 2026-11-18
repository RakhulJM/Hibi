# Hibi 日々

**A little corner of the internet that belongs only to you.**

Hibi is a private, local-first personal journal with a calm scrapbook-inspired interface, encrypted local storage, portable encrypted backups, and optional encrypted Supabase sync.

> The application source is public; personal journal data, backups, passphrases and encryption keys must remain private.

## Project status

The project source is being added in an initial implementation increment. Read [Current Status](docs/CURRENT_STATUS.md), [Security](docs/SECURITY.md), and [Agile Working Agreement](docs/AGILE.md) before using it with real personal data.

## Run locally

Requirements: Node.js 20.19+ or 22.12+, npm.

```bash
npm install
npm run dev
```

Then run the checks:

```bash
npm run typecheck
npm test
npm run build
```

## Privacy first

Hibi encrypts journal content in the browser before writing it to IndexedDB. Keep your vault passphrase safe. Do not commit `.env.local`, exported backups, browser profiles, or real diary content. Optional cloud sync requires a separately provisioned Supabase project and must be tested before relying on it.

## Agile development

Hibi uses a prioritised product backlog, one-week iterations, acceptance criteria, a Definition of Ready, a Definition of Done, sprint reviews and retrospectives. See [`docs/AGILE.md`](docs/AGILE.md).

## Technology

React, TypeScript, Vite, Tailwind CSS, Dexie/IndexedDB, Web Crypto API, Lucide React, optional Supabase, and `vite-plugin-pwa`.
