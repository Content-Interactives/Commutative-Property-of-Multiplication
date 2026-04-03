# Commutative Property of Multiplication

Next.js 15 app (static export) demonstrating commutative multiplication with sliders and visual grouping. Production build uses `basePath` for GitHub Pages.

**Live:** https://content-interactives.github.io/Commutative-Property-of-Multiplication/

**Curriculum and standards:** [Standards.md](Standards.md)

## Stack

- Next.js 15 (App Router), React 19, TypeScript
- Tailwind CSS 4, Radix UI (`@radix-ui/react-slider`, `@radix-ui/react-alert-dialog`)
- `class-variance-authority`, `clsx`, `tailwind-merge`, `lucide-react`, `tw-animate-css`
- `output: 'export'` → static site in `out/`
- `next.config.ts`: `basePath` is `/Commutative-Property-of-Multiplication` when `NODE_ENV === 'production'`; `images.unoptimized: true` for static export

## Scripts

| Command | Purpose |
|--------|---------|
| `npm run dev` | Next dev server |
| `npm run build` | Static export to `out/` |
| `npm run start` | Run production server locally (optional) |
| `npm run lint` | `next lint` |

## Deploy

`.github/workflows/deploy.yml`: on push to `main`, runs `npm ci`, `npm run build`, deploys `out/` to `gh-pages` via JamesIves/github-pages-deploy-action.

## Entry points

- `src/app/page.tsx` — page shell
- `src/components/interactive/CommutativePropertyInteractive.tsx` — interactive
- Shared UI under `src/components/ui/`
