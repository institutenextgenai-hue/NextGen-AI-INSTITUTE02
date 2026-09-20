# NextGen AI Academy — Production-Ready Commercial Website

This package is a deployable foundation for the real NextGen AI Academy website. It is **not a live public deployment** until the academy connects its own production services and domain.

## Included
- Public academy website and founder profile
- Three paid courses and starter lesson content
- Supabase Auth + PostgreSQL schema with RLS
- Automatic student profile creation after signup
- Student dashboard and lesson progress
- Payfast hosted checkout structure with pending-order linkage
- Payfast ITN signature, merchant, source-IP, amount and server-validation checks
- Completion-gated PDF certificates
- Resend email notification hook
- WhatsApp Cloud API notification hook
- Basic admin enrolment view
- Privacy, Terms and Refund policy pages
- Environment configuration and launch checklist

## Production setup
1. Deploy the Node app to an HTTPS host.
2. Create a production Supabase project and run `supabase_schema.sql` in the SQL editor.
3. Create the Payfast merchant account and configure sandbox credentials for testing first.
4. Configure `APP_URL` to the deployed HTTPS URL.
5. Configure Resend with a verified sending domain if email notifications are wanted.
6. Configure WhatsApp Cloud API if WhatsApp notifications are wanted.
7. Set all secrets in the hosting provider's secret/environment manager. Never commit `.env` or secrets.
8. Run end-to-end tests before switching Payfast from sandbox to production.
9. Add the academy's final legal/business details to the policy pages before public launch.

## Important
The Payfast integration follows Payfast's current custom integration/ITN requirements, but the merchant account and live credentials must be supplied by the academy. Do not paste secrets into chat.
