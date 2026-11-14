ARBIT — Supabase Ready Release

The supplied Supabase Project URL and Publishable Key have been inserted into index.html.

Next:
1. Replace index.html in the root of your Arbit- GitHub repository with this index.html.
2. Supabase Dashboard > Authentication > Providers > Email: keep Email provider enabled.
3. Turn OFF Confirm email for username-only sign-up (menu wording may vary).
4. Open the GitHub Pages website and test Sign Up, Logout, then Login.

Username rules: 3–24 lowercase English letters, digits, or underscore.
Password: at least 8 characters.
The app uses username@arbit.local internally as the Supabase Auth email identifier; people type only their username in ARBIT.

Security:
- The Publishable key is intended for browser use. Never place a Secret key or service_role key in HTML/GitHub.
- User data isolation relies on Supabase Auth and Row Level Security policies from the SQL setup.
- Test using two separate accounts to verify each sees only their own records.
- Remember Me keeps the session on this device; unchecked keeps it for the current browser session.
