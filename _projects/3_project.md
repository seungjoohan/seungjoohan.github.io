---
layout: page
title: Agentic Trading System
description: LLM-driven stock trading agent with live market data, sentiment analysis, and risk management
img: assets/img/flow-chart.jpg
importance: 2
category: work
github_url: https://github.com/seungjoohan/stock-prediction-system
---

I originally built this as a personal ML learning exercise: a simple Streamlit app that pulled stock data via yfinance, trained ARIMA and Prophet models on TSLA, AAPL, and GOOG, and served up predictions. The focus was on understanding how to take a model from notebook to production, not on whether the predictions were actually good (they weren't).

But, as LLM based agentic system dominated my feeds on every SNS, I couldn't help to build something of my own.

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/tradingdashboard.jpg" title="Trading Dashboard" class="img-fluid rounded z-depth-1" %}
    </div>
</div>

The agent runs continuously during market hours and operates in two loops. Every 5 minutes it ingests news from Finnhub and RSS feeds, runs LLM sentiment analysis, and indexes everything into a two-layer RAG store (SQLite for structured retrieval, ChromaDB for semantic similarity). Every 15 minutes it gathers live prices via WebSocket, current portfolio state, fundamentals, FRED macro data, and the last 7 days of sentiment history. Then it builds a prompt, and asks the LLM what to do. Any trades that come back get validated by a risk manager before touching Alpaca.

I'm currently running it in paper trading mode to see whether it actually makes money before letting it invest with my money. Next up is integrating ML-based stock prediction with current agentic trading system!

Skills involved:

- **LLM orchestration**: Groq (LLaMA/Mixtral) primary, Google Gemini fallback, rate-limited batch processing
- **Retrieval-Augmented Generation**: ChromaDB vector store + SQLite structured retrieval, `sentence-transformers/all-MiniLM-L6-v2` embeddings
- **Real-time data**: Finnhub WebSocket with reconnect, ping/pong keepalive, staleness detection
- **Risk management**: confidence threshold, position size caps, daily loss circuit breaker, VIX circuit breaker, earnings blackout, stop-loss
- **APIs**: Alpaca (execution), Finnhub (prices/news/fundamentals), FRED (macro), Groq, Gemini
- **Infrastructure**: SQLite (WAL mode), Streamlit dashboard

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/flow-chart.jpg" title="System architecture" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Every 15-minute decision cycle gathers live prices, portfolio state, macro data, and 7 days of RAG-retrieved sentiment history before calling the LLM.
</div>
