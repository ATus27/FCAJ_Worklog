---
title: "Week 7 Worklog"
date: 2024-01-01
weight: 7
chapter: false
pre: " <b> 1.7. </b> "
---


### Week 7 Objectives:

* Optimize Retrieval quality (OpenSearch Hybrid Search tuning & Chunk Size adjustment).
* Perform preliminary load testing on API Gateway and perform least-privilege IAM policy reviews.
* Finalize Terraform & IaC structure (modularization, resource import, writing deployment README).
* Write operations documentation (Runbook), prepare slides, and conduct the official Demo presentation.

### Tasks to be carried out this week:

| Day | Task | Start Date | Completion Date | Reference Material |
| --- | --- | --- | --- | --- |
| Mon | - **Retrieval Quality Optimization**: Tune Hybrid Search ratio in OpenSearch (increasing vector search weight over BM25 from 50/50 to 70/30); reduce chunk size from 300 to 200 tokens; re-run 5 previously low-scoring queries — 4/5 showed significant improvement. | 08/03/2026 | 08/03/2026 | OpenSearch & Vector Search Docs |
| Tue | - **Preliminary Load Test & Security Audit**: Conduct load testing (50 concurrent requests to API Gateway) and review all IAM policies against least-privilege principles. | 08/04/2026 | 08/04/2026 | AWS IAM & Load Testing Guide |
| Wed | - **Finalize Terraform & IaC**: Clean up code, split into distinct modules per stream (ingestion, chat-api, monitoring, evaluation), import manually created resources into Terraform state, write deployment README. | 08/05/2026 | 08/05/2026 | Terraform Docs & Best Practices |
| Thu | - **Write Operational Runbook & Prepare Presentation**: Document overall architecture, alert response protocols (e.g., DLQ Depth > 0), periodic maintenance checklists; prepare slide deck and demo script. | 08/06/2026 | 08/06/2026 | Project Runbook & Presentation |
| Fri | - **Official Team Demo**: Live demonstration covering document upload ➔ Q&A ➔ simulated Slack alert ➔ RAGAS evaluation report; record feedback and summarize the 5-week project journey. | 08/07/2026 | 08/07/2026 | Team Review & Demo |

### Week 7 Achievements:

* **Improved RAG Retrieval Performance**: Boosted answer accuracy by fine-tuning OpenSearch Hybrid Search weights (70/30) and decreasing chunk size to 200 tokens.
* **Modularized Infrastructure as Code**: Cleanly separated Terraform code into 4 distinct modules, imported 100% of resources into state, and provided step-by-step deployment instructions.
* **Complete Operations Runbook & Successful Demo**: Delivered comprehensive incident response runbook and executed a seamless end-to-end system demo.
