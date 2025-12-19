# Next.js Quick Template
A **speed-first** Next.js starter template for MVPs, hackathons, and personal projects.<br>
Build an authenticated app in minutes, not hours.

## Features
- Next.js (App Router)
- Supabase Auth (Google One Tap only)
- Tailwind CSS + shadcn/ui
- TypeScript (strict)
- Dark / Light mode
- Vercel-ready

## Quick Start
```bash
git clone <repo-url>
cd <repo-name>
pnpm install
pnpm dev
```

Open [http://localhost:3000](http://localhost:3000)

## Authentication
- Google OAuth only (via Supabase)
- No email/password
- No complex auth flows

You just need to enable Google Provider in Supabase Auth.

## Project Structure
```bash
app/
  (auth-pages)/    # sign-in / sign-up
  auth/callback/   # OAuth callback
  protected/       # Auth-required pages

components/
  ui/              # shadcn/ui
utils/
  supabase/
```

## Deploy
Optimized for Vercel.<br>
Just set env vars and deploy.