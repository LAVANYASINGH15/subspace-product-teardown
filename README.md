# Subspace.money — Product Teardown
### 5 Gaps I'd Fix From Day One

**Lavanya Singh**
B.Tech in Information Technology, 2022–2026
Rajiv Gandhi Institute of Petroleum Technology, Jais
30 May 2026

---

> *A product teardown based on real app usage and Play Store reviews — every gap comes with a ship plan.*

---

## Why Subspace

Subspace.money is India's subscription management and group finance platform — bootstrapped, profitable, with ₹36.5 Cr ARR (FY25) and zero external funding. Core features include shared subscriptions, split billing, gift cards, rentals, and a Negotiate API for automated price negotiation.

I chose Subspace because it has a live app with real users, real transactions, and real friction — which means real observations, not guesswork.

---

## Methodology

- Used the live Android app as a real customer (May 2026)
- Reviewed Play Store ratings and 1-star reviews (App rated 3.5 stars)
- Frameworks used: SWOT, Jobs-to-be-Done lens on ICP gaps, Impact vs Effort prioritisation

---

## The 5 Gaps

---

### Gap 01 — New users hit a wall — no value shown before signup
**Pillars:** GTM & ICPs · UX

#### What I Saw
The very first screen is a WhatsApp login prompt or phone number field. No hero copy, no pricing, no catalog preview, no social proof — all before signing up. A user arriving from a friend's referral sees a login wall with nothing backing the claim.

> **Fig 1 — First screen on app open (May 2026)**
> No value prop, no pricing, no catalog — login wall is the first thing a new user sees.

#### The Opportunity
Every referral Subspace earns is being partially wasted. The user already did the hard work of finding the app — but without seeing prices upfront, a meaningful % bounces before converting. This is the easiest conversion lift on the table: show the value before asking for the phone number.

#### What I'd Ship
Ship a public browse layer — live subscription prices, available slots, discount percentages — all visible without login. Gate only the checkout step. Add one line above the CTA: *"India's cheapest streaming subscriptions — split and save up to 80%."* This is a 1-sprint frontend change with a measurable impact on sign-up conversion in 2 weeks.

---

### Gap 02 — Users are losing real money — and there's no button to fix it
**Pillars:** Features / Services · UX · Customer Trust

#### What I Saw
No "protected by Subspace" badge, no dispute button, no refund policy anywhere on the plan detail screen. Play Store reviews (May 2026, 3.5 stars) show a consistent pattern: admins logging users out, subscriptions never activating, refunds not processing for months.

> **Fig 2 — Play Store reviews, 1-star (Feb 2026)**
> Rohith: admin removed him from a group after he left a 1-star rating. Swadhin: paid for Amazon Prime, admin logged him out, no refund issued. No in-app dispute option exists — users have no recourse.

#### The Opportunity
Shared subscriptions are the core product — but each transaction is a P2P trust exchange with no safety net. Users who get burned leave 1-star reviews that become the first thing a new user sees. A 3.5-star rating is a growth ceiling — it is structurally impossible to scale word-of-mouth when the word being spread is "I lost money."

#### What I'd Ship
Ship "Subspace-Verified Slots": Subspace holds admin credentials in an encrypted vault so joiners never depend on admin goodwill. Add a visible 7-day refund SLA on every plan card. Put a one-tap dispute button on the active subscription screen. Surface a "Protected by Subspace" trust badge at checkout. This converts the biggest churn driver into the biggest trust signal.

---

### Gap 03 — The catalog is 100% consumer — an entire segment is being ignored
**Pillars:** GTM & ICPs · Features / Services

#### What I Saw
Browsing the full catalog reveals only consumer OTT and lifestyle apps — Netflix, Spotify, Canva, JioHotstar, Swiggy One. No Teams section, no business plan pricing, no way for a founder or small team to manage shared SaaS tools. The Negotiate API is mentioned nowhere in the app.

> **Fig 3 — Shared Subscriptions catalog (May 2026)**
> Every listing is a consumer OTT or lifestyle app. No Teams plan, no business tier, no SaaS tools for small teams anywhere in the catalog.

#### The Opportunity
India has millions of bootstrapped startups where one person pays for 10–15 SaaS tools, often sharing logins informally across the team. This is exactly what Subspace already solves for consumers — but nobody has built it for small teams. The Negotiate API already exists. The infra is there. The gap is just a product surface and a different ICP.

#### What I'd Ship
Launch "Subspace for Teams" — a lightweight workspace dashboard where a team admin adds a card, Subspace auto-detects recurring SaaS spend, and one-click negotiates or cancels. Price at ₹999/mo per workspace. Target bootstrapped founders in Bangalore and Hyderabad first. This is a 3-month MVP on existing infrastructure that opens an entirely new ARR stream.

---

### Gap 04 — Rentals asks for my location but won't tell me what's available
**Pillars:** Features / Services · UX

#### What I Saw
Tapping into Rentals immediately shows a "Change Location" popup — but after setting a location, there is no city coverage map, no catalog of available devices, no condition grading (A/B/C), and no damage protection policy visible. The Play Store listing promises "10-minute delivery" but the app gives no clarity on which cities this is live in.

> **Fig 4 — Rentals section, first screen (May 2026)**
> Immediately asks for location — but after setting it, no city coverage map, no device catalog, no condition grades, no damage policy appears. The feature exists but gives users nothing to trust.

#### The Opportunity
Rentals involves handing someone a ₹80,000 MacBook. That needs more trust signals than a Netflix subscription — not fewer. When users can't find out whether their city is covered, what condition the device is in, or what happens if something breaks, they don't take the risk.

#### What I'd Ship
Build a proper rentals landing experience: a live city coverage map, device listings with A/B/C condition grades and real photos, an explicit "damage covered up to ₹X" policy shown before checkout, and a real delivery ETA counter. If only Bangalore is live, say so clearly — specificity builds more trust than vague promises of "10-minute delivery."

---

### Gap 05 — Angry users are Subspace's biggest growth problem — and it's fixable
**Pillars:** GTM & ICPs · Features · Growth

#### What I Saw
3.5 stars on Play Store with a consistent stream of 1-star reviews through May 2026. Complaints cluster around three issues: admins unresponsive, subscriptions not activating after payment, refunds not processing for weeks. The founder is personally responding to reviews with a phone number — which shows awareness, but the fix is being handled outside the product.

> **Fig 5 — Play Store reviews, 1-star (Nov 2025 – Apr 2026)**
> Utsav: randomly logged out, group owner slow to resolve. Anurag: wallet balance negative after 11 months, unresolved by support. Same 2–3 complaints repeating across months — not isolated incidents, a systemic pattern. App rated 3.5 stars.

#### The Opportunity
Subspace's entire growth engine runs on referrals and word-of-mouth. But a 3.5-star app with visible refund complaints is actively working against that engine. The good news: these are not random complaints — they are the same 2–3 fixable problems appearing over and over. Fix them once, fix the rating permanently.

#### What I'd Ship
Make dispute resolution a product feature, not a WhatsApp call. Add an in-app "Something went wrong" button on every active subscription card that opens a structured dispute flow with a 48-hour SLA. Show a live status tracker so users feel heard without needing to call anyone. When resolved, prompt a review update. A 4.2+ rating unlocks a different quality of word-of-mouth — and the fix is already 80% done through Gap 02.

---

## SWOT Snapshot

| | |
|---|---|
| **Strengths** | ₹36.5 Cr ARR, zero external funding. Negotiate API is a genuine technical moat. Network effects: each sharer brings 3–4 joiners. India-first catalog, UPI-native. |
| **Weaknesses** | Admin trust gap — no escrow or protection layer. Login wall kills cold conversion. No SMB/Teams product despite having the infra. Rentals lacks city coverage and trust signals. |
| **Opportunities** | Millions of Indian SMBs with unmanaged SaaS spend. BNPL bundling for annual subscriptions. Super-app partnerships for low-CAC distribution. Expand beyond OTT to utilities and local subscriptions. |
| **Risks** | 3.5 stars — trust erosion is a growth ceiling. Platform risk: Netflix cracking down on sharing. Super-apps could replicate subscription tracking as a native feature. Word-of-mouth breaks when users are angry. |

---

## What I'd Prioritise on Day 1

| Priority | Ship This | Impact | Effort | Why First |
|---|---|---|---|---|
| 1 | Fix the admin trust layer — credential vault + dispute button | High | Medium | Users lose real money. One bad week kills the referral loop. |
| 2 | Public browse before login — show value before asking for a number | High | Low | 1 sprint. Directly unblocks cold conversion. |
| 3 | Subspace for Teams — lightweight SMB dashboard | High | High | New ARR on existing infra. 3-month MVP. |
| 4 | Rentals transparency — city map, condition grades, damage policy | Medium | Low | Credibility fix before the next rentals push. |
| 5 | Turn angry reviews into a retention loop — in-app dispute + refund SLA | High | Medium | 3.5 stars is a ceiling. Fix trust, fix referrals. |

---

*All observations from direct app usage and Play Store reviews, May 2026*
*Frameworks: SWOT · Jobs-to-be-Done · Impact vs Effort prioritisation*
*Product Intern Assignment · Vocallabs / Subspace · May 2026*
