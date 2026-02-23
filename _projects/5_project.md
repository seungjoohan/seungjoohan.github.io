---
layout: page
title: visa tracker
description: visa policy news tracking and analysis system
img: assets/img/visa.jpg
importance: 2
category: work
github_url: https://github.com/seungjoohan/visa-tracker
---

From 2025, a period of rapid and dramatic visa policy changes have begun. Staying informed about critical immigration updates became a daily necessity. Manually monitoring multiple news sources was time-consuming and unreliable, risking missed policy announcements that can have immediate personal impact.

So, I built an automated visa news tracking and analysis system — and then kept going, turning it into a full RAG (Retrieval-Augmented Generation) platform.

**v1** collected news from NewsAPI, classified articles by urgency using sentence-transformer semantic similarity, and delivered daily HTML email summaries via GitHub Actions cron.

**v2** adds a RAG pipeline grounded in official policy documents:

- **Knowledge base**: 8 CFR Title 8 (federal immigration regulations) ingested from the public [eCFR API](https://www.ecfr.gov/), chunked into ~426 policy segments and embedded with `BAAI/bge-base-en-v1.5`
- **Vector store**: FAISS (IndexFlatIP with L2-normalized vectors for cosine similarity), stored locally and committed to the repo
- **LLM analysis**: Each article is analyzed by Claude Haiku with retrieved policy chunks as context, producing structured output — importance level, affected visa types, action required, deadline, and specific CFR citations
- **Fallback chain**: LLM+RAG → LLM only → semantic+keyword → keyword only, so the pipeline never breaks even without an API key
- **Evaluation framework**: Labeled article dataset, precision/recall/F1 metrics, and a comparison CLI to benchmark keyword vs. semantic vs. LLM vs. LLM+RAG classifiers side-by-side
- **Knowledge base updates**: Weekly GitHub Actions workflow checks the eCFR API for regulatory changes and re-ingests only when Title 8 has actually been updated

Skills involved:

- **RAG**: FAISS vector store, sentence-transformers, chunk retrieval, prompt construction
- **LLM**: Anthropic Claude API, structured JSON output, cost and latency tracking
- **Data**: [NewsAPI](https://newsapi.org/), [eCFR API](https://www.ecfr.gov/), XML parsing
- **ML**: Sentence transformers, semantic similarity, classification metrics (precision/recall/F1)
- **DevOps**: FastAPI, GitHub Actions, SMTP email

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/tracker.jpg" title="working progress of dnn modeler" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
