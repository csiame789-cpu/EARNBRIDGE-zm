# EARNBRIDGE website — pilot starter

A mobile-first React + Vite frontend connected to the EARNBRIDGE Supabase project.

## Included
- Public landing page and service categories
- Client project request form (signed-in clients)
- Worker sign-up and profile creation
- Email/password sign-in and sign-out
- Early admin workspace placeholder (not a secure admin console)

## Supabase configuration
Create deployment environment variables from `.env.example`:
- `VITE_SUPABASE_URL`
- `VITE_SUPABASE_PUBLISHABLE_KEY`
- `VITE_ADMIN_EMAILS` (UI visibility only; not authorization)

The publishable key is intended for browser use. Never put a Supabase service-role or secret key in this project.

## Run locally
```bash
npm install
cp .env.example .env
# Set the publishable key in .env
npm run dev
```

## Build
```bash
npm run build
```
The static site is output to `dist/`.

## Deploy to Cloudflare Pages
1. Push this folder to a GitHub repository.
2. In Cloudflare Pages, connect the repository.
3. Framework preset: **Vite**.
4. Build command: `npm run build`.
5. Build output directory: `dist`.
6. Add the three environment variables above in Pages settings, then redeploy.

## Important before public launch
- Confirm Supabase Auth email confirmation and redirect URLs.
- Verify Data API grants and RLS policies for every frontend operation.
- Implement server-authorized admin access and an audit trail; the current admin screen is only a UI placeholder.
- Publish Terms, Privacy, contact details and a complaint process.
- Test registration, email confirmation, login, client request submission and worker profile creation on mobile.
- Do not collect client payments until a supported payment provider, refund process and worker payout process have been verified.

This is a pilot frontend starter, not a live deployed marketplace. No jobs, clients or payouts are guaranteed.
