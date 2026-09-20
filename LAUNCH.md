# NextGen AI Academy launch checklist

## 1. Domain + HTTPS
- Purchase a domain selected by the academy.
- Point DNS to the hosting provider.
- Enable HTTPS.
- Set `APP_URL=https://your-domain`.

## 2. Supabase
- Create a production project.
- Run `supabase_schema.sql`.
- Confirm email authentication settings.
- Keep the service-role key server-side only.
- Keep RLS enabled.

## 3. Payfast
- Create/verify the merchant account.
- Start with Sandbox credentials.
- Set `PAYFAST_SANDBOX=true`.
- Test successful and cancelled payments.
- Confirm the ITN reaches `/api/payfast/itn` over public HTTPS.
- Confirm the order changes from pending to paid only after ITN validation.
- Switch to live credentials only after testing.

Payfast's current custom integration documentation requires signature validation, source validation, amount comparison and server confirmation for ITNs.

## 4. Email / WhatsApp
- Resend: verify the sending domain and set `RESEND_API_KEY` and `EMAIL_FROM`.
- WhatsApp Cloud API: set the phone number ID, API version and token. Follow Meta's current messaging/template requirements for production outbound messages.

## 5. Legal + customer support
- Review `/privacy.html`, `/terms.html` and `/refunds.html` with the academy's actual business/legal details.
- Confirm support email and phone number.
- Add any required registration, accreditation or certificate wording only when it is accurate.

## 6. Final testing
- Signup/login
- Course visibility
- Payment creation
- Payfast return/cancel
- ITN validation
- Paid-course access
- Lesson completion
- Certificate eligibility
- Certificate PDF
- Email/WhatsApp notifications
- Mobile layout
- Admin access
