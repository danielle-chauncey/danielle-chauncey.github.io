---
title: "Solutions Marketing Toolkit: Positioning to Battlecards"
date: 2024-07-01
description: "The full bill of materials for a distributed database launch: positioning framework, competitive battlecards, and a seller-ready one-pager."
tags: ["solutions marketing", "battlecards", "sales enablement", "competitive positioning"]
weight: 3
---

**Companion to:** [GA Launch: Multi-Region Serverless Database]({{< ref "aurora-dsql-launch.md" >}})

> These are illustrative samples built to show how I structure a solutions bill of materials: positioning, competitive battlecards, and seller-ready enablement. Competitive figures are a point-in-time snapshot (June 2026) and are shown to demonstrate approach, not as current pricing.

---

## The Principle

A launch narrative is not an asset. Sellers do not carry a positioning doc into a first call.

The test I hold every piece to: **if a seller is not using it, it does not count.** So the toolkit works backward from the sales conversation. Positioning defines what is true. Battlecards arm the objection. The one-pager is what actually rides along to the call.

Four connected artifacts, one source of truth:

| Artifact | Audience | Job it does |
|----------|----------|-------------|
| Positioning framework | Marketing, product, field | Single source of truth for what the product is and who it's for |
| Battlecard (per competitor) | Sales, in the deal | Win/loss triggers, talk track, objection handling |
| One-pager | Sales, pre-call | The thing that ships to the prospect and rides into the call |

---

## Artifact 1: Positioning Framework

Built on persona-first messaging with a promise/reason-to-believe spine. Three audiences, distinct evaluation criteria, one narrative that doesn't contradict itself.

**Value proposition (the formula):**

> For developers building globally distributed applications who need strong data consistency without operational complexity, Aurora DSQL is a serverless SQL database that delivers multi-region strong consistency with zero infrastructure management.

**Promises and reasons to believe:**

| Promise | Reason to believe |
|---------|-------------------|
| Write SQL you already know | PostgreSQL wire-compatible. No proprietary query language. No retraining. |
| Strong consistency without managing replication | ACID transactions across regions. Sub-10ms in-region reads. No manual failover. |
| Serverless. No clusters, no capacity planning | Scales to zero when idle. Pay only for what you use. |

**Messaging layered by persona:**

| Persona | Core message | Proof type |
|---------|-------------|------------|
| Developer (evaluates by building) | "Write SQL you already know." | PostgreSQL compatible, minutes-to-first-query |
| Platform architect (designs the system) | "Eliminate the consistency vs. availability tradeoff." | Zero ops, no replica management |
| Decision-maker (approves the spend) | "Reduce database engineering headcount." | Predictable cost, vendor consolidation |

---

## Artifact 2: Competitive Battlecards

One card per competitor. The structure is the same each time so a seller finds what they need mid-call without reading prose.

**Sections in every card:** at-a-glance (positioning, audience, pricing model) → when we win → when we lose → head-to-head table → talk track → traps to avoid → objection handling → their recent moves → proof points.

The parts most people skip are the ones that matter: **when we lose** and **traps to avoid**. A battlecard that only lists wins is a brochure.

### Excerpt: the talk track (vs. Google Cloud Spanner)

> **Open (acknowledge, don't dismiss):** "Spanner is a serious product. Google built it for their own mission-critical systems. If you're evaluating it, you're solving a real problem and we respect that."
>
> **Bridge (reframe the criteria):** "The question is whether you want to adopt a proprietary query language and commit to GCP for this workload. Spanner's PostgreSQL interface exists but it's limited."
>
> **Land (our advantage, in their language):** "DSQL gives you the same multi-region strong consistency without the operational overhead or language switch. Your team writes PostgreSQL they already know. No nodes to manage. No idle costs."

### Excerpt: traps to avoid

- Do not claim DSQL is more battle-tested. Spanner has a decade head start. **Own the newness honestly.**
- Do not position DSQL as "Spanner but cheaper." That makes us sound derivative.
- Do not argue consistency mechanisms. Customers care that it works, not how.

### Excerpt: objection handling (the honest column)

| What they say | The truth | Your response |
|---------------|-----------|---------------|
| "DSQL is too new. Spanner has 10+ years in production." | Fair. DSQL is newer. | "Spanner has more history. DSQL is built on the Aurora engine that already runs some of the world's largest workloads. Start with a non-critical workload, build confidence, then expand." |
| "We need five nines. Can DSQL match that?" | DSQL offers 99.99%. Spanner offers 99.999% multi-region. | "If five nines is the deciding factor, Spanner does offer that. Evaluate whether the cost and operational premium of node-based infrastructure is worth the extra nine for your workload." |

The second competitor card (CockroachDB) runs the same structure against a different axis: multi-cloud portability and open source vs. zero-ops and native integration.

---

## Artifact 3: Seller One-Pager

The asset that actually rides into the call. Persona → why they care → *when to bring it up*. That last column is what makes it usable instead of filed away.

| Persona | Why they care | When to bring it up |
|---------|--------------|---------------------|
| Backend / full-stack developer | PostgreSQL they know. No ops burden. Minutes to first query. | Evaluating a database for a new project, or considering migration. |
| Platform architect | Kills the consistency vs. availability tradeoff. No replica management. | Designing multi-region systems, or weighing Spanner/CockroachDB. |
| VP Engineering / CTO | Fewer database engineers. Predictable cost. No over-provisioning. | Infra cost reduction, team allocation, vendor consolidation. |

Paired with a resource table that tells the seller exactly which asset to send and when: product page pre-call, developer guide for technical evaluation, Console for the live demo, the matching battlecard when a competitor comes up.

---

## Why It Holds Together

Nothing is invented at the copy stage. The landing page, the blog, the battlecard talk track all derive from the same positioning doc. When the message needs to change, it changes in one place and flows down.

That is the difference between writing assets and building a system that produces them.

## What I'd Do Differently

Write the one-pager and the first-call talk track *first*, then back into the positioning doc. I built positioning from product inputs and adapted for the field later. Starting from the sales conversation would have produced tighter enablement earlier and exposed weak proof points sooner.
