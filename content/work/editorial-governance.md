---
title: "Editorial Governance Framework at Scale"
date: 2023-06-01
description: "Designed a style guide for 300+ contributors and integrated it into CI/CD pipelines, cutting time-to-publish from 6 weeks to 2."
tags: ["content strategy", "editorial governance", "CI/CD", "automation"]
weight: 3
---

**Sample:** [View redacted style guide on this site](/work/style-guide-sample/)

---

## Problem

A hyperscale cloud provider had 300+ contributors publishing implementation guides, architecture diagrams, and deployment documentation to a product content hub. There were no shared editorial standards. Every contributor wrote in their own style, used different terminology, structured pages differently.

The result was a 9-week editorial backlog. Published content took 6 weeks from draft to live. Quality was inconsistent. Readers encountered contradictory terminology across pages. The editorial review team was a bottleneck that couldn't scale.

## My Role

Primary author of the style guide. I owned editorial governance end-to-end: defining the standards, getting adoption across 300+ contributors, and building the automation that enforced them.

## Approach

**Content taxonomy.** Before writing style rules, I mapped the full content hierarchy: Domain > Category > Use Case > Solution Type. Every naming convention, description format, and structural guideline derives from this taxonomy. Contributors don't just know how to write; they know where their content fits.

**Practical over prescriptive.** The guide covers seven areas: content taxonomy, naming guidelines, use case descriptions, category descriptions, solution pages, technical guidance, and writing standards. Each section has formats, character limits, examples, and anti-patterns. The goal was to make the right choice the easy choice.

**Programmatic enforcement.** I worked with engineering to integrate editorial rules into the CI/CD publishing pipeline. Automated linting catches terminology violations, structural issues, and formatting errors before human review. Contributors get feedback in minutes, not weeks.

**LLM extension.** Later, I built an LLM trained on the style guide that reviews drafts against editorial standards and returns actionable feedback. This gave contributors instant self-service guidance without waiting for editorial review.

## Results

- Adopted by 300+ contributors across the organization
- 9-week editorial backlog eliminated
- Time-to-publish cut from 6 weeks to 2
- LLM review system improved AI-generated response relevance by 25%
- Became the foundation for a RAG knowledge base indexing 14,000+ files

## What I'd Do Differently

I'd build the CI/CD integration from day one, before publishing the guide. We wrote the guide, got adoption, and then built automation. That middle period (guide exists, automation doesn't) created a false sense of governance. People referenced the guide but didn't consistently follow it until the linting caught violations automatically.
