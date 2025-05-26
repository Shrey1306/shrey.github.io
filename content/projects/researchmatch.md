---
title: "ResearchMatch"
draft: false
description: "AI-Powered Research Position Matching Platform with Multi-LLM Evaluation"
tags: ["Python", "JavaScript", "Redis", "Streamlit", "NLTK", "Scikit-learn", "OpenAI", "DeepSeek", "Mistral", "Llama", "AWS", "Kubernetes", "Kafka", "Flink", "Pinecone"]
image: "/img/researchMatch.png"
link: "https://substack.com/profile/197564043-shrey-gupta/note/c-120214927"
---

Built a comprehensive web application that matches students with research positions using multiple data sources and comprehensive matching algorithms.

Current MVP Architecture:
- Traditional Scraping: Crawls faculty pages using BeautifulSoup and DuckDuckGo API
- Four LLM Scrapers: DeepSeek, GPT-4, Mistral & Llama for research topic extraction
- Matching Engine: Keyword, TF-IDF & Word2Vec ranking with citation metrics
- Streamlit Dashboards: Real-time metrics with Redis caching

Performance Insights:
- LLM vs. Scraping: Keyword scraping and Llama outperformed GPT-class models on F1 (≈ 0.27 vs 0.24)
- Caching optimization: Reduced TF-IDF & Word2Vec latency from ~5ms to sub-ms
- Real-time monitoring with box-plots and rolling 90% CIs

Cloud-Native Architecture (For the future):
- Ingestion: AWS Step Functions with K8s scraper jobs on Fargate
- Enrichment: Flink/Kinesis stream processing for LLM microservices
- Storage: Iceberg + S3 data lake, Aurora Postgres, Pinecone vector search
- Core APIs: gRPC/GraphQL services for matching and personalization
- Edge & UI: CloudFront with global Redis cache, Next.js SPA
- Observability: Prometheus, OpenTelemetry, CloudWatch

Future Features:
- Incremental scraping using change-feeds
- Hybrid ranker combining BM25, ANN & re-ranking LLM
- Personalized digests through Notification Hub

Developed for CS6675: Advanced Internet Systems and Applications at Georgia Tech.

<a href="https://substack.com/profile/197564043-shrey-gupta/note/c-120214927" target="_blank" rel="noopener">🔗 Read on Substack</a> 