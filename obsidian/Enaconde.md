---
title: Enaconde
tags: [project, pos, super-app, pitch]
created: 2026-10-01
status: idea / pre-pitch
source: "[[IDEAS]]"
---

# Enaconde

## One-liner
POS (касс, ebarimt) for Mongolian shops. The POS is not the product. It is the **door that gets merchants onto a future super app** (Meituan + Amap style: locations, commerce, food delivery).

## Current state
- Repo contains only `IDEAS.md` (written 2026-09-16, pitch prep). No code yet.
- Pitch target: the **MGL group** of shops. The author is a member and owns a shop.

## Core ideas
1. **AI invoice (падаан) reader**: strongest idea. Photo → AI → product list → owner fixes small errors → Enter. Key risk: *matching* to existing products, so no duplicates.
2. **AI harness inside the POS** (typed, Mongolian). Closed list of allowed actions; every write is preview + owner confirm; reads and reports are free. Quick-action buttons (падаан оруул, өнөөдрийн борлуулалт, дуусч байгаа бараа).
3. **Phone barcode scanning**: web only (`BarcodeDetector`, ZXing-wasm fallback, HTTPS, 2s debounce). Needs POS connected to a server, so this is **phase 2**.

## The moat: shared barcode catalog
- Mongolian products (APU, Суу, Талх Чихэр, Говь) are in no international database, not even Open Food Facts.
- One shop names an unknown barcode once, and every shop in the group has it forever.
- Network effect: 50 shops = 50x faster; hard for a competitor to copy.
- Group purchasing power: aggregate sales ("40,000 units/month") for deals with APU and distributors. Software becomes something that earns money.

## Other features
Credit ledger (зээлийн дэвтэр), expiry alerts, auto-reorder suggestions, multi-shop view, shift report and cash variance, QPay/QR.

## Pitch strategy
- Lead with "I built this for my own shop and it works."
- Demo on my shop with real invoices; show an unknown barcode scanned on a second phone (network effect).
- Do **not** say "Meituan + Amap". Start with what they get next month (invoice in 2 min). Vision goes at the end.
- Be explicit: working now vs phase 2.

## Questions to prepare for
- Offline? Must be able to say a confident yes (sell offline, sync later).
- Data ownership: catalog shared, sales private, group sees only totals.
- Barcode-less goods: own labels / quick buttons.
- Older staff: prove it is *easier*, not just new.
- Pricing: monthly; maybe free for first N shops.
- Focus: POS vs marketplace?

## Open questions
- [ ] Tech stack?
- [ ] How many shops in the MGL group, and which POS do they use today?
- [ ] Offline-first architecture decision
- [ ] ebarimt integration details (which provider/API?)
- [ ] Which AI model for invoice reading, and cost per invoice?

## Next steps
1. Invoice reader
2. Matching logic
3. Test on own shop's real invoices

## Chat log
### 2026-10-01
- Started this note from `IDEAS.md`. Continue the conversation below; decisions and answers get added here.
