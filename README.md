# Billionaire Circle membership platform

## Features
- Luxury responsive landing page inspired by your supplied Cirque website screenshots.
- Ten membership tiers, sequential member numbers and a 10,000-member cap.
- Member registration/login and dashboard.
- Detailed membership application and admin approve/reject.
- Admin pricing manager for initiation and annual fees per tier.
- USD default; selectable USD, NGN, GBP, EUR, CAD, AUD, GHS, ZAR, KES, AED, CHF and JPY.
- Payment record submission and manual admin verification; no card/payment gateway is connected.
- Referral submission and admin listing.
- Member loan enquiries with 70% illustrative calculation; no deposit collection or loan disbursement.
- Admin overview, applications, members, pricing, payments, loans and referrals.

## Run
1. Install Node.js 20+.
2. Copy `.env.example` to `.env`.
3. Set a long random SESSION_SECRET and your own ADMIN_EMAIL and strong ADMIN_PASSWORD.
4. Run `npm install`, then `npm start`.
5. Open http://localhost:3000. SQLite database is created under data/.

## Tiers
Sovereign #1–10 (10); Imperial #11–50 (40); Dynasty #51–150 (100); Presidential #151–400 (250); Royal #401–1,000 (600); Platinum #1,001–2,000 (1,000); Diamond #2,001–3,500 (1,500); Golden #3,501–5,500 (2,000); Elite #5,501–8,000 (2,500); Classic #8,001–10,000 (2,000).

## Before public launch
This is a starter platform, not a certified banking, lending or payment product. Add HTTPS, secure persistent hosting, backups, email verification, password reset, admin MFA, CSRF protection, audit logs, monitoring and security testing. Connect a licensed payment processor only after merchant onboarding, refund policy and server-verified webhooks are implemented. Currency selection stores a currency code; it does not convert exchange rates or settle international payments. The 70% upfront loan-deposit structure may trigger lending, consumer-credit, advance-fee, deposit-taking and fraud rules. Obtain written legal/regulatory advice in every target country before asking for advance payments. Do not promise the proposed $500,000 spending card, donated properties, investment access or other benefits unless legally and operationally backed. Replace placeholder contact details and legal pages with approved entity details, privacy policy, terms, refund policy, KYC/AML and consumer disclosures. 

## Deploy online (Render)
This repository includes `render.yaml` for Render deployment. Upload the project contents to a GitHub repository, then in Render choose **New → Blueprint** and connect that repository. Set `ADMIN_EMAIL` and a unique strong `ADMIN_PASSWORD` when prompted. The Blueprint pins Node.js 24.22.2 and mounts a persistent disk at `/var/data` for the SQLite database.

**Hosting note:** persistent disk storage requires a paid Render service. Do not use an ephemeral free instance for real member records because its local database can be lost on restart/redeploy. See `DEPLOY-TO-RENDER.txt` for the complete steps.
