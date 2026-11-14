# ARBIT setup

## Supabase connection (required for real accounts)
1. Create a Supabase project.
2. Open SQL Editor and run `arbit-supabase-setup.sql`.
3. In Authentication > Providers > Email, disable email confirmations. This app maps a unique username to an internal address (`username@arbit.local`) so users can sign up with username + password only. This address is not an inbox; password reset by email is therefore not available in this version. Keep user passwords private.
4. Copy Project URL and the anon/public key from Project Settings > API. Never use the service_role key in this HTML.
5. In `index.html`, replace `YOUR_SUPABASE_URL` and `YOUR_SUPABASE_ANON_KEY`.
6. Upload `index.html` to your GitHub Pages repository (and keep the SQL file for reference).

## Important
- User data is stored in `arbit_user_data` with Row Level Security. Each signed-in user can read/write only their own row.
- The app stores a local copy for convenience and syncs changes to Supabase. Use JSON Backup before major updates.
- `Remember me` keeps the Supabase session on the device; untick it to avoid persisting login. Always Logout on a shared device.
- Discipline punch time uses the device clock in Bangladesh timezone and can be manipulated. Server-verified timestamps are a later hardening step.
- Event reminders are in-app only; browser-closed push notifications are not included.
- The Supabase URL/key are project configuration, not secrets; never place a service_role key in client-side code.
