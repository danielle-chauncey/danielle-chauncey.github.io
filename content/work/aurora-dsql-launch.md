---
title: "GA Launch: Multi-Region Serverless Database"
date: 2024-06-01
description: "Led end-to-end positioning, messaging, and go-to-market for a first-of-its-kind distributed SQL database."
tags: ["product launch", "positioning", "developer audience", "go-to-market"]
weight: 2
---

**Live site:** [docs.aws.amazon.com/aurora-dsql](https://docs.aws.amazon.com/aurora-dsql/latest/userguide/) | [aws.amazon.com/rds/aurora/dsql](https://aws.amazon.com/rds/aurora/dsql/)

**Framework used:** [launch-system](https://github.com/danielle-chauncey/launch-system) (T1 classification)

---

## Why This Was Hard

A hyperscale cloud provider was launching its first multi-region serverless SQL database. Three problems made this complex:

1. **Internal competition.** The same provider already offered 15+ database products. Positioning had to explain why this exists without cannibalizing existing offerings.
2. **Three audiences, one narrative.** Developers evaluate through code. Architects evaluate through TCO and reliability. Decision-makers evaluate through headcount reduction. The messaging had to serve all three without contradicting.
3. **Hard deadline.** GA date was fixed. Five parallel workstreams had to converge simultaneously.

## The Workstreams

I owned all five workstreams below. Cross-functional coordination across engineering, TPMs, sales, and marketing.

![Swimlane timeline showing 5 parallel workstreams across 8 weeks: Positioning, Product Documentation, Console UX, GTM and Landing Page, and Field Enablement, converging on GA Day](/images/dsql-launch-swimlane.svg)

### Positioning and Messaging (Weeks 1-6)

Defined three personas with distinct evaluation criteria and built layered messaging:

| Persona | Core Message | Proof Type |
|---------|-------------|------------|
| **Developer** | "Write SQL you already know." | Technical: PostgreSQL compatible, minutes-to-first-query |
| **Platform Architect** | "Eliminate the consistency vs. availability tradeoff." | Architecture: zero ops, no replica management |
| **Decision-Maker** | "Reduce database engineering headcount." | Business: predictable costs, vendor consolidation |

Built competitive positioning against Google Spanner (proprietary query language), CockroachDB (self-managed complexity), DynamoDB (eventual consistency), and the provider's own single-region offering.

### Product Documentation (Weeks 1-8)

Developer guide, API reference, getting started tutorial, code samples. Wrote for the developer who evaluates by building, not reading marketing pages.

### Console UX (Weeks 3-7)

Designed the provisioning flow and in-console education. The Console is part of the product, not a marketing surface.

### GTM and Landing Page (Weeks 5-8)

Landing page copy, announcement blog, social seeding. All derived from the messaging doc. No new positioning invented at the copy stage.

### Field Enablement (Weeks 5-8)

Battlecards, talk tracks, first-call deck, objection handling for the three most common sales objections:

> "We already use your existing database."
> "We've evaluated Spanner."
> "How is this different from your NoSQL offering?"

## Results

- Successful GA launch. All five workstreams shipped on deadline.
- Positioning adopted by sales, marketing, and developer relations
- Competitive differentiation defended in enterprise deals against Spanner and CockroachDB
- Field enablement materials used from day one (not "filed away")

## What I'd Do Differently

Bring sales into messaging development at week 1, not week 5. We built positioning from product inputs and adapted for field use later. Starting with sales conversations and working backward would have produced tighter first-call materials earlier.

Separate the documentation and marketing workstreams across two people with shared messaging guidelines. Owning both gave full narrative control but compressed deadlines made parallel execution unsustainable at this scope.
