# A-to-Z Library staff dashboard starter
For جامعۃ الرشیدیہ آسیاآباد مکران بلوچستان.

## Connect
1. Install Node.js 20+.
2. Copy `.env.example` to `.env.local`.
3. Keep the project URL as `https://mhidoejtgqcbzxmrresg.supabase.co`.
4. Paste the **publishable** key from Supabase → Project Settings → API Keys into `VITE_SUPABASE_PUBLISHABLE_KEY`.
5. Never put a service-role key in this frontend.
6. Run `npm install` and `npm run dev`.

## Staff access
New accounts should remain members until approved. The project owner can promote verified staff by Auth user UUID, e.g.:
`update public.profiles set role = 'librarian' where id = 'VERIFIED-UUID';`
Use `head_librarian` for the lead. Never let users set their own roles.

## Included
Staff sign-in, role-gated catalogue access, search, title + first copy entry in one RPC transaction, additional copy entry, category selector, shelf location and condition, responsive UI.

## Before a real 20,000+ copy rollout
This starter loads up to 2,000 titles and 10,000 copies; add server-side pagination before production-scale use. Also add CSV import/export, barcode labels, checkout/return screens, reports, automated tests, restore drills, MFA for administrators, and a security review. It is source code, not a deployed public website or Android/iOS app.
