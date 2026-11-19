# Money Dashboard

Personal finance dashboard: summary of income and expenses from account transactions,
budget by category, monthly cycle with a custom start date.

## Stack

- Next.js (App Router), strict TypeScript, Tailwind CSS
- All code in `src/`, alias `@/*` → `src/*`
- Package manager: npm

## Commands

- `npm run dev`: dev server
- `npm run build`: production build
- `npm run lint`: ESLint
- `npx tsc --noEmit`: type checking

## Structure

- `src/app/(app)/`: pages requiring login (dashboard, transactions, reports)
- `src/app/login/`: public pages for login page
- `src/app/register/`: public pages for register page
- `src/components/ui/`: basic components (Button, Card, Badge), each type of components should be put on specified folder
- `src/components/widgets/`: dashboard bento cards, one file per widget
- `src/lib/`: pure helpers (formatting, cycle calculations, aggregation)
- `src/types/`: shared types (Transaction, Category, Cycle)

## Conventions

- Default Server Component; use `“use client”` only if state or events are required
- Component filenames use PascalCase; helper filenames use camelCase
- Currency is stored as an integer in Rupiah (no decimals); use `formatRupiah()` for formatting
- Dates use the helper in `src/lib/cycle.ts`; do not calculate manually
- Colors and radii follow the tokens in `tailwind.config` / `globals.css`; do not hardcode hex values

## Rules

Always hold a You Arent Gonna Need it mentality. Do not overengineer. Never expand scope without permission. Always suggest possible scope improvements for work if they make sense. All work must be justifiable. Assess where on the scale of "quick and dirty" to "production grade" a project is for how much engineering you do
