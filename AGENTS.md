# AGENTS.md

## Cursor Cloud specific instructions

### Product overview

Single-page React 19 + Vite 6 artist portfolio (Clara Veiga) with client-side routing (`react-router-dom`), bilingual UI (EN/PT via `LanguageContext`), and Tailwind CSS v4. No separate backend process — only the Vite dev server is required for local development.

### Services

| Service | Command | Port | Notes |
|---------|---------|------|-------|
| Vite dev server | `npm run dev` | **3000** (from `package.json` script `--port=3000`) | `vite.config.ts` also sets `server.port: 10000` but the npm script overrides it |

Use tmux for long-running dev: e.g. session `vite-dev-server` with `npm run dev` in `/workspace`.

### Standard commands

See `README.md` and `package.json`:

- **Install:** `npm install`
- **Dev:** `npm run dev` → http://127.0.0.1:3000/
- **Build:** `npm run build` → `dist/`
- **Preview build:** `npm run preview` (uses port 10000 per `vite.config.ts`)
- **Lint:** `npm run lint` (`tsc --noEmit`) — see caveats below
- **Tests:** none defined in this repo

### Environment variables

Copy `.env.example` to `.env.local` for local runs. `GEMINI_API_KEY` is wired in `vite.config.ts` but **not used by current `src/` code**; the portfolio runs without it. README mentions Gemini for AI Studio deployment context.

### Gotchas

- **`npm run lint` may fail** on a clean checkout due to existing TypeScript issues (`ErrorBoundary` class component typing in `src/App.tsx`, duplicate `allowedHosts` key in `vite.config.ts`). **`npm run build` still succeeds** despite the duplicate-key warning.
- `better-sqlite3` and `express` are listed in `package.json` but have no usage under `src/` — native addon build still runs on `npm install`.
- No Husky/pre-commit hooks or `.devcontainer` in this repo.

### Hello-world verification

After `npm run dev`, open `/`, toggle EN/PT in the navbar, visit `/works` and `/contact` — core routing and i18n behavior.
