# Fractis — "Ship & Monetize" App Plan

## Recommended App: **QuoteKit — Instant Quote & Invoice Generator for Freelancers**

A single-purpose SaaS that lets freelancers create, send, and get paid on branded quotes/invoices in under 60 seconds. Built almost entirely by OpenCode, hosted on Vercel, monetized via Stripe from day one.

### Why this app
- **Fractis fit**: Fractis already does client work (Lilla, Astral, TDA/IDS, ASSA ABLOY) — they understand freelancer pain points intimately.
- **OpenCode-buildable**: CRUD + auth + PDF generation + Stripe. No exotic infra.
- **Immediate monetization**: Freemium with paywall on "send unlimited / remove watermark / custom branding" — converts on first use.
- **Low CAC**: SEO + Product Hunt + freelancer communities (Reddit r/freelance, IndieHackers).

### Core features (MVP, ~1 week OpenCode build)
1. Email/password + Google auth (Clerk or Supabase Auth)
2. Create quote/invoice with line items, tax, discount
3. Live branded PDF preview + download
4. Send via email link (no recipient signup)
5. Client accepts quote → converts to invoice → Stripe payment link
6. Dashboard: status (draft/sent/paid/overdue), revenue
7. Free tier: 3 docs/month, watermarked. Pro: $9/mo unlimited + branding + reminders

### Tech stack (OpenCode-friendly)
- Next.js 15 (App Router) + TypeScript
- Supabase (Postgres + Auth + RLS) — free tier
- Stripe Checkout + Customer Portal
- Resend for transactional email
- @react-pdf/renderer for PDFs
- Tailwind + shadcn/ui
- Deploy: Vercel (free → $20/mo)

### Monetization ladder
- Free: 3 docs/mo, watermarked, Fractis branding
- Pro $9/mo: unlimited, no watermark, custom logo/colors, payment reminders, recurring invoices
- Team $29/mo: multi-user, white-label, API
- Lifetime deal $99 (launch only) for cash injection

### Build plan (OpenCode execution order)
1. Scaffold Next.js + Supabase + Tailwind + shadcn
2. Auth flows + protected routes
3. DB schema: users, clients, documents, line_items, payments
4. Document editor (quote/invoice toggle) + PDF render
5. Email send + public accept page
6. Stripe integration + webhook → status updates
7. Dashboard + filters
8. Landing page + SEO meta + OG image
9. Polish: empty states, loading, error boundaries
10. Deploy + Stripe live mode + domain

### Go-to-market (immediate)
- Product Hunt launch
- "Free invoice generator" SEO landing (high-intent keyword)
- Reddit/IndieHackers show-and-tell
- Fractis existing client network → first 10 paying users
- Affiliate: 30% recurring for creator referrals

### Revenue projection (conservative)
- Month 1: 50 signups, 5 paid → $45 MRR
- Month 3: 500 signups, 40 paid → $360 MRR
- Month 6: 2,000 signups, 150 paid → $1,350 MRR + lifetime deals

### Risks & mitigations
- Crowded market → niche down to "freelance designers/devs" with branded templates
- Churn → annual discount + reminder automation
- Support load → in-app help + canned responses

### Fractis branding angle
Market as "built by a design studio that gets freelancers" — credibility + design quality as differentiator.

### Deliverables I can produce now
- Full Next.js scaffold with all routes
- Supabase migration SQL
- Stripe webhook handler
- Landing page copy + SEO
- Email templates

Say "build it" and I'll scaffold the repo and start shipping.
