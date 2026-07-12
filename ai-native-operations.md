---
title: "AI-Native Marketing Operations"
date: 2025-01-01
description: "Built three agent-based systems that run 70% of daily marketing operations: MCP document workflows, a 14K-file RAG knowledge base, and LLM editorial governance."
tags: ["AI", "automation", "MCP", "RAG", "content operations"]
weight: 4
---

**Stack:** Claude Code, MCP, Python, Git, vector storage, CI/CD

**GitHub:** [danielle-chauncey/launch-system](https://github.com/danielle-chauncey/launch-system) (framework), [danielle-chauncey.github.io](https://github.com/danielle-chauncey/danielle-chauncey.github.io) (this site)

---

## The Premise

Most marketers describe AI as a tool they use. I build AI systems that run my operations. The distinction matters: using ChatGPT to write a draft is adoption. Building an agent workflow that pulls data from 8 sources, assembles a structured document, runs quality checks, and delivers it without human intervention is engineering.

These three systems are operational. I built them without engineering support. They run daily.

![Architecture diagram showing three parallel systems: MCP Document Workflows, RAG Knowledge Base, and LLM Editorial Governance](/images/ai-workflows-architecture.svg)

---

## System 1: MCP Document Workflows

**Problem:** Preparing executive briefing materials required pulling data from 8+ teams (sales, legal, compliance, public policy, comms, product) on 24-hour turnarounds. The process was manual, fragmented, and dependent on one person's institutional knowledge.

**What I built:** An agent-based workflow using Model Context Protocol (MCP) that orchestrates document assembly. The system connects to internal data sources via MCP servers, cross-references account history, synthesizes inputs from multiple teams, and outputs structured briefing formats. It handles retrieval, formatting, and quality checks autonomously.

**How it works:**
1. MCP servers expose internal knowledge bases and data sources
2. Claude Code orchestrates: queries data, retrieves context, assembles structure
3. Quality checks run against editorial standards before output
4. Final document delivered in standardized format

**Result:** 70% of program operations now run through AI-assisted systems. Turnaround time for executive materials dropped from hours to minutes for standard requests. The workflow is repeatable and doesn't depend on one person's memory.

---

## System 2: RAG Knowledge Base (14,000+ Files)

**Problem:** Six years of institutional knowledge across 14,000+ files (implementation guides, architecture docs, editorial standards, process documentation) was inaccessible. Finding the right reference meant knowing it existed. New contributors had no way to search precedents.

**What I built:** A retrieval-augmented generation system that ingests, indexes, and serves answers from the full document corpus via natural language queries.

**The pipeline:**
1. **Ingest:** Parse 14,000+ files across formats (Markdown, AsciiDoc, XML)
2. **Chunk:** Split into semantically coherent segments
3. **Embed:** Generate vector representations
4. **Index:** Store in vector database with metadata
5. **Retrieve:** Semantic search on natural language queries
6. **Rank:** Re-rank results by relevance
7. **Answer:** Generate response grounded in retrieved context

**Result:** Replaced manual search with conversational retrieval. Team members query the knowledge base daily for standards, precedents, and reference material. Reduced onboarding time for new contributors. The system surfaces answers from documents people didn't know existed.

---

## System 3: LLM Editorial Governance

**Problem:** A style guide adopted by 300+ contributors was comprehensive but hard to operationalize. Contributors couldn't easily check whether their draft met standards without reading a 50-page document. The editorial review team was a bottleneck.

**What I built:** An LLM trained on the style guide that reviews content against editorial standards and returns actionable feedback before human review. Integrated into the CI/CD publishing pipeline.

**The flow:**
1. Contributor submits draft
2. LLM review checks tone, terminology, structure against style guide
3. Feedback returned in seconds (not days)
4. CI/CD linting catches formatting and structural violations automatically
5. Only compliant content reaches human review

**Result:** 25% improvement in AI-generated response relevance. Reduced editorial review cycles. Gave 300+ contributors instant self-service governance. Scaled editorial quality without scaling headcount.

---

## Why This Is Different From "Using AI"

| Using AI | Building AI systems |
|----------|-------------------|
| Ask ChatGPT to write a blog post | Design a pipeline that generates, reviews, and publishes content autonomously |
| Use Copilot for code suggestions | Build MCP servers that connect data sources to agent workflows |
| Summarize a document with AI | Build a RAG system that makes 14,000 documents queryable |
| Check grammar with AI | Train an LLM on your style guide and integrate it into CI/CD |

The systems I built are infrastructure. They run without me in the loop. They scale without additional headcount. They improve as the underlying models improve.

---

## What I'd Do Differently

Start with retrieval quality metrics before scaling the knowledge base. I optimized for coverage (get all 14K files in) before optimizing for precision (are the right chunks being retrieved?). This led to a period where the system was comprehensive but noisy. Precision tuning should have come first on a smaller corpus, then scaled.

For the editorial governance system, I'd version the style guide as structured data from day one. Training on a PDF worked but updating the LLM's knowledge when the guide changes requires reprocessing. A structured, versioned source of truth would make updates incremental.
