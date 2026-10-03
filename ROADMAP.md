# Product roadmap

The portfolio should earn trust through working, clearly labeled software. A service is marked **planned**, **prototype**, or **live** based on what actually works; testimonials appear publicly only after the author submits them and an admin approves them.

## 1. Establish the service foundation

- Keep the site deployable as a static GitHub Pages frontend.
- Add a data-driven services catalogue and individual detail pages.
- Make the status and current limitations visible on each service.
- Keep local credentials in `.pat/`; never commit Supabase secrets.

## 2. Ship the first useful service: ATS Resume Tailor

Build on the existing resume analyzer prototype.

- Accept resume text/file and a job description.
- Show a match summary and specific, explainable suggestions.
- Produce an editable, ATS-readable draft while preserving the candidate's actual experience.
- Let the user review and export the result.
- Add a case study only after the end-to-end workflow works and can be demonstrated.
- Add model-based generation only behind a server or Supabase Edge Function; never ship an AI provider secret or Supabase service-role key to the browser.

## 3. Add Supabase authentication and roles

- Use Supabase Auth for sign-in; enforce access in database policies and trusted functions, not by hiding frontend controls.
- Suggested roles: `su` (full owner access), `admin` (moderation and content management), and `basic` (use services and submit testimonials).
- Keep any `admin/admin`, `su/password`, and `basic/basic` accounts confined to an isolated local development stack. Do not provision or enable them on the public deployment.
- Put only public Supabase URL/publishable key in browser configuration. Keep the service-role key server-side and store local-only values under ignored `.pat/`.

## 4. Add testimonial submission and review

- Add a form for a visitor or signed-in user to submit their name, relationship/context, and testimonial.
- Save new entries as pending; provide an admin review screen to approve or reject.
- Show only approved testimonials publicly.
- Add validation, rate limiting or spam protection, and database row-level security.
- Do not seed or write invented testimonials. Use real submissions with the author's permission.

## 5. Expand the auxiliary services

Release one service at a time, with a working demo and clear limitations:

1. Resume analyzer / ATS resume tailor
2. Document Q&A with cited source passages
3. Business knowledge assistant for a bounded document set
4. CSV/Excel data analyzer
5. Small API and workflow automation tools based on real use cases

## 6. Validate and publish each release

For each release, run lint, formatting, and build checks; test mobile and keyboard flows; verify authorization and database policies; document architecture, trade-offs, demo/source links, and limitations. Publish only features whose status is accurately represented.
