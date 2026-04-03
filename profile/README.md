# TradeYard

**Procurement infrastructure for the landscape trade.**

TradeYard is a wholesale marketplace that connects landscape contractors with nurseries and material suppliers. Contractors source inventory, compare availability across vendors, and place orders — all backed by Stripe-secured payments and an AI procurement assistant. Vendors keep their customers, set their own pricing, and get paid before the truck leaves.

### What we build

- **Multi-vendor catalog** — canonical plant taxonomy with vendor-specific labels, cross-supplier search, and relationship-aware wholesale pricing.
- **TradeAgent** — an AI assistant (Anthropic Claude) that helps contractors find materials, compare options, and move toward checkout through natural conversation.
- **Stripe Connect checkout** — authorize on order, capture after vendor confirmation. Multi-vendor orders split cleanly; partial outcomes handled when a vendor declines.
- **Vendor workflow** — email-driven PO review with confirm, modify, or decline. Vendors control who can buy from them and at what price.
- **Trade-only access** — verified contractors see wholesale pricing; public visitors see the catalog without dollar amounts.

### Stack

| Layer | Tech |
|-------|------|
| Frontend | React 19, Vite, TypeScript, Tailwind, shadcn/ui |
| Backend | Supabase (Postgres, Auth, Edge Functions, Realtime) |
| Payments | Stripe (Connect, PaymentIntents with manual capture) |
| AI | Anthropic Claude via Supabase Edge Functions |
| Mobile | Capacitor (iOS / Android) |

### Repositories

| Repo | Purpose |
|------|---------|
| [`tradeyard-app`](https://github.com/tradeyard-org/tradeyard-app) | Web and mobile client — React + Vite frontend, Capacitor native shell |
| [`tradeyard-docs`](https://github.com/tradeyard-org/tradeyard-docs) | Architecture decision records, specs, runbooks, and partner documentation |

---

TradeYard LLC
