---
title: "Content Strategy for a Developer Solutions Hub"
date: 2024-01-01
description: "Built the content strategy for a product solutions library reaching 2M+ monthly page views."
tags: ["content strategy", "SEO", "developer audience", "product marketing"]
weight: 1
---

**Live site:** [aws.amazon.com/solutions](https://aws.amazon.com/solutions/)

---

## The Situation

Hundreds of implementation guides, architecture diagrams, and deployment docs existed in a solutions library. They were published independently by contributors with no shared standards, no taxonomy, and no measurement. Discoverability was poor. Engagement was flat. A 9-week editorial backlog meant content arrived stale.

The library needed to work as a product, not a repository.

## What I Built

![Content architecture diagram showing the taxonomy from Domain through Category, Use Case, and Solution types, with a governance pipeline at the bottom](/images/solutions-architecture.svg)

**A four-level taxonomy** that organizes every piece of content into Domain > Category > Use Case > Solution Type. This structure drives navigation, search, internal linking, and contributor assignments. Nothing publishes without a home in the taxonomy.

**An editorial governance system** adopted by 300+ contributors. The style guide defines naming conventions, description formats, character limits, page component specs, and writing standards. I then integrated the rules programmatically into CI/CD pipelines so that linting catches violations before human review. Time-to-publish dropped from 6 weeks to 2.

**A search and discoverability strategy** designed around intent. Structured metadata, hierarchical linking, and content architecture optimized for both traditional SEO and AI answer engines. Organic search discoverability increased 35% in year one.

**A measurement framework** tracking page views, engagement rates, search conversion, and content gaps. Monthly reviews to senior leadership. Data drove editorial priorities, not opinions.

## Results

| Metric | Outcome |
|--------|---------|
| Monthly page views | 2M+ |
| Organic search lift | +35% (year one) |
| Page engagement lift | +40% (year one) |
| Time-to-publish | 6 weeks → 2 weeks |
| Editorial backlog | 9 weeks → 0 |
| Contributors governed | 300+ |

## What I'd Do Differently

Start with measurement before redesigning architecture. Some early decisions were intuition-based that data later validated, but others it contradicted. Baseline metrics first would have accelerated iteration.

Invest in AI discoverability from day one. We retrofitted AEO after the architecture was set. Designing for LLM extractability upfront would have saved a full content refresh cycle.
