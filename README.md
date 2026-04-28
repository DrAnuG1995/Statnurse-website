# StatNurse Landing Page

Single-page early-access site for StatNurse, served via GitHub Pages at https://statnurse.app.

## Stack
- Static HTML, no build step
- Signups posted to Supabase project `ishxbkgouqmaollnbdul` via REST API
- Live signup counter via the `get_nurse_signup_count()` Postgres RPC

## Files
- `index.html` - the entire landing page
- `img/` - logo and headshot
- `CNAME` - custom domain config for GitHub Pages

## Updating the page
Edit `index.html`, commit, push. GitHub Pages republishes automatically (~1 min).

## Backend / database
Schema lives in the StatDoctor monorepo at
`direct-shift-connect/supabase/migrations/006_nurse_signups.sql`.
Apply via Supabase SQL editor on project `ishxbkgouqmaollnbdul`.

## Welcome email (not yet enabled)
Edge Function (`send-signup-email`) and trigger (migration 007) are scaffolded
in the monorepo but not deployed. See deploy steps in that repo when ready.
