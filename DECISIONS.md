# Decision Points

## DP1 — Rejection

**What can a client see and do after a creator declines?**

The client sees a red "Declined" badge, their original message, and a **"Find similar gigs"** button that filters the marketplace to the same category. If the creator provided a reason, it's shown in italics.

**Why:** Giving clients a recovery path keeps them on the platform instead of leaving frustrated. The badge preserves a record so it doesn't feel like a bug. The "Find similar" CTA redirects their intent toward other creators who might accept, which benefits the marketplace ecosystem.

---

## DP2 — Double Booking

**Can a gig accept a new booking while another is still Pending?**

Yes — multiple pending bookings can exist simultaneously, but only one can be **Accepted** at a time. When a creator accepts one booking, all other pending bookings for that gig are automatically declined with reason "Gig was filled by another booking."

**Why:** If a gig locked on the first pending request, a flaky client could freeze a creator's income indefinitely. Allowing parallel pendings mirrors real marketplaces like Upwork and Fiverr. The auto-decline on acceptance prevents clients from waiting forever, closing the loop cleanly.

---

## DP3 — Discovery

**How are gigs ranked on the marketplace page?**

Default sort is **newest first**, but with a **"Rising Creator" boost** — gigs from creators with zero accepted bookings float to the top and receive a green badge. Clients can override via a sort dropdown (Newest / Price: Low→High / Price: High→Low).

**Why:** Pure newest-first buries good gigs under spam. Pure cheapest creates a race to the bottom that hurts creators. The rising boost gives new creators visibility, which aligns with the hackathon theme of "young creators monetizing their skills." The sort dropdown preserves user agency for clients who care about price.

---

## Standard API Declaration

We did **not** implement a standard API. All functionality is browser-based. Grading should use a browser agent driving the UI.
