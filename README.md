# Wrapinator — Consolidated (Replit‑ready)

Everything in one folder: AI wraps, Replicate SDXL+ControlNet, Google Vertex Imagen Boost, RFQs, Vendors, Stripe (Checkout + Connect), OAuth, Credits, Rate Limits, Admin (Orders/Pricing/Users).

## Run
```
npm i
npx prisma db push
npm run dev
```

## Secrets (Replit → Tools → Secrets)
```
PUBLIC_URL=https://<your-repl-url>
ADMIN_SETUP_TOKEN=one_time_secret           # promote yourself once

# OpenAI
OPENAI_API_KEY=sk-...

# NextAuth
NEXTAUTH_URL=https://<your-repl-url>
NEXTAUTH_SECRET=<random-32b>
GOOGLE_CLIENT_ID=...
GOOGLE_CLIENT_SECRET=...
GITHUB_ID=...
GITHUB_SECRET=...

# Stripe
STRIPE_SECRET_KEY=sk_test_...
STRIPE_WEBHOOK_SECRET=whsec_...
STRIPE_PRICE_PRO_MONTHLY=price_XXXXXXXX
STRIPE_PRICE_HIRES=price_YYYYYYYY
HIRES_AMOUNT_CENTS=4900
HIRES_CREDITS=50
CONNECT_ACCOUNT_ID=acct_XXXXXXXXXXXX
PLATFORM_FEE_PCT=0.10

# Replicate
REPLICATE_API_TOKEN=...
REPLICATE_MODEL_VERSION=stability-ai/sdxl-controlnet-canny:latest
REPLICATE_REFINER_VERSION=stability-ai/sdxl-refiner:latest

# Default provider
DEFAULT_PROVIDER=replicate

# Google Vertex (for Photoreal Boost)
GOOGLE_PROJECT=your-project-id
GOOGLE_LOCATION=us-central1
GOOGLE_CREDENTIALS_JSON=<paste service account JSON string here>

# Rate limits
DAILY_LIMIT_GENERATE=25
DAILY_LIMIT_ANALYZE=50
DAILY_LIMIT_PREMIUM=10

# Default packs (seeded if none exist)
DEFAULT_PACKS_JSON=[{"name":"Starter","credits":40,"amount_cents":1000},{"name":"Basic","credits":100,"amount_cents":2500},{"name":"Pro","credits":300,"amount_cents":6000}]
``

## First steps
1) Login at `/login`.  
2) Promote yourself (once): `POST /api/admin/make-me?token=one_time_secret`.  
3) Visit `/admin/users`, `/admin/pricing`, `/admin/orders`.  
4) Generate on `/dashboard` (Batch Mode optional).  
5) See results on `/designs` → Rate / Hi‑Res / **Photoreal Boost**.  
6) Create RFQ on `/market`, quote via `/vendor`, accept with deposit.

Happy wrapping!
