# DataCops for Shopify: Setup Guide

Complete technical guide to setting up DataCops first-party tracking infrastructure on a Shopify store.

## What this covers

- Why Shopify stores lose 30-40% of conversion data (ITP, ad blockers, consent)
- CNAME-based first-party tracking: how it works and why it bypasses standard blocks
- Step-by-step Shopify setup: script tag, CNAME, ad platform connections, consent banner
- Server-side CAPI to Meta, Google Ads, TikTok Events API, LinkedIn Insight
- Fraud filtering with 361B+ IP database before events forward to CAPI
- Honest comparison vs. Elevar, Stape, and standalone CMPs
- Pricing: free tier through enterprise

## Architecture

```
yourdomain.com
  └── datacops.yourdomain.com (CNAME → cdn.datacops.com)
        ├── First-party analytics (ad-blocker immune)
        ├── Bot/fraud filter (361B IP database)
        ├── Server-side CAPI fan-out (Meta / Google / TikTok / LinkedIn)
        └── TCF 2.2 consent (stored first-party)
```

## Quick start

1. Sign up at [joindatacops.com](https://joindatacops.com) (free, no card)
2. Add `<script>` tag to `theme.liquid` before `</head>`
3. Add CNAME: `datacops` → `cdn.datacops.com`
4. Connect ad platforms via API credentials in dashboard
5. Live in 5 to 30 minutes

## Current status

- GDPR/CCPA: Active
- TCF 2.2: Active
- SOC 2 Type II: In progress
- ISO 27001: Planned

DataCops publishes compliance status accurately. See [enterprise page](https://joindatacops.com/enterprise) for current state.

---

Research by [DataCops](https://www.joindatacops.com) · First-party tracking, consent infrastructure & fraud prevention.
