# CALENORA PLACEMENTS — Mobile-friendly static deployment

This is a one-file static website intended to make GitHub upload from a phone easier.

## Configure Supabase
The Supabase project URL and publishable key you previously supplied are already inserted. Do not replace them with a service-role key.

## Deploy from Android using GitHub + Vercel
1. Create a GitHub account and verify your email.
2. On github.com, create a new **public or private** repository named `calenora-placements` (private is fine for source code).
3. Open the repository → Add file → Upload files. Upload `index.html` from this folder. Commit the upload.
4. Create/sign in to Vercel and choose Add New → Project → Import the GitHub repository.
5. For Framework Preset choose **Other**. Leave the root directory as `./`; use no build command and no output directory for this plain static HTML project. Deploy.
6. In Supabase → Authentication → URL Configuration, set Site URL to the Vercel URL and add that URL to Redirect URLs. Also add `http://localhost:3000` only if you later use local development.
7. Test candidate signup with a separate test email, email confirmation, applying to a test job, and admin status updates.

## Features
- Candidate signup/sign-in
- Public active job listing and search
- Candidate apply and application tracking
- Admin job publishing, close/reopen, applicant list and status updates

## Limitations before real launch
- This is a starter, not security-audited production software.
- No CV upload, offer-letter file delivery, automated email notifications, interview calendar, payments, multiple recruiters or analytics exports.
- Configure reliable SMTP, privacy policy, terms, consent, retention, CAPTCHA/rate limiting, backups and monitoring before real candidate data.
- Your Supabase schema must have the `profiles`, `jobs`, and `applications` tables, the RLS policies, and the `handle_new_user` trigger. Admin profile must already have role `admin`.
