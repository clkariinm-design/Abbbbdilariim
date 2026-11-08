# StudentHub

Responsive single-school management website with English/Somali interface, admin and teacher roles, student records, classes, subjects, daily attendance, exams, homework and continuous assessment. No finance or payment module.

## Technology
- Static HTML, CSS and JavaScript (no build step)
- Supabase Auth + PostgreSQL with Row Level Security
- Cloudflare Pages hosting

## Supabase
Project URL: `https://xbumipplteiqwtwmkjsc.supabase.co`

The frontend uses the Supabase publishable key in `app.js`. Publishable keys are intended for browser apps; access is restricted by database RLS. Never put a service-role or secret key in browser code.

## Run / deploy
Serve this folder as a static website, or deploy the repository root to Cloudflare Pages. Build command: none. Output directory: `/` (root).

## First-time setup still required
- Database tables and RLS policies are already provisioned.
- Public self-registration is intentionally disabled.
- An administrator Auth user and matching `public.profiles` row must be created securely before sign-in. Do not create an admin role from an untrusted browser form.
- Teacher Auth accounts and profile rows must be provisioned by the administrator; class assignments are stored in `class_teachers`.
- Configure Auth email confirmation and allowed redirect URLs for the deployed domain.

## Current implementation
Dashboard, student listing/add, class and subject management, daily attendance, assessment creation, teacher list and school settings. Grade entry/reporting and secure in-app teacher account provisioning remain follow-on work; database tables `marks` and `grading_scales` are ready for these features.
