# EARNBRIDGE website — pilot starter

Mobile-first React + Vite frontend for the EARNBRIDGE managed pilot.

## Setup
1. Create a Supabase project.
2. In Supabase SQL Editor, run `supabase/schema.sql`.
3. Copy `.env.example` to `.env` and set your Supabase project URL and publishable (anon) key.
4. Run `npm install`, then `npm run dev`.
5. Build with `npm run build`; static output is `dist/`.

## Cloudflare Pages
- Framework preset: Vite
- Build command: `npm run build`
- Build output directory: `dist`
- Environment variables: `VITE_SUPABASE_URL`, `VITE_SUPABASE_PUBLISHABLE_KEY`

Never put a Supabase service-role key in frontend code.

## Pilot limitations
This is a pilot frontend, not a live deployed marketplace. Admin authorization, payment collection, worker payouts, messaging, dispute handling and legal pages still need to be implemented and tested. No jobs, clients or payouts are guaranteed. Do not collect payments until the payment, refund and payout processes are verified.
