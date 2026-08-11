---
title: "Week 5 Worklog"
date: 2024-01-01
weight: 5
chapter: false
pre: " <b> 1.5. </b> "
---


### Week 5 Objectives:

* Build API Gateway (REST API, CORS) integrated with Amazon Cognito User Pool user authentication.
* Integrate Amazon ElastiCache (Semantic Cache using Cosine Similarity) to optimize costs and latency.
* Design DynamoDB tables (ChatHistory, FeedbackStore) and set up Bedrock Guardrails (sensitive topic filtering, PII masking).
* Finalize and test Stream 2 (Realtime QA Pipeline) end-to-end using Postman.

### Tasks to be carried out this week:

| Day | Task | Start Date | Completion Date | Reference Material |
| --- | --- | --- | --- | --- |
| Mon | - Deploy Amazon API Gateway (REST API), enable CORS, and configure user authentication with Amazon Cognito User Pool. | 07/20/2026 | 07/20/2026 | AWS API Gateway & Cognito Docs |
| Tue | - Integrate Amazon ElastiCache (Redis) as a Semantic Cache layer applying Cosine Similarity to minimize latency and LLM costs. | 07/21/2026 | 07/21/2026 | AWS ElastiCache Developer Guide |
| Wed | - Design and create Amazon DynamoDB tables: `ChatHistory` (conversation logs) and `FeedbackStore` (user ratings & feedback). | 07/22/2026 | 07/22/2026 | Amazon DynamoDB Docs |
| Thu | - Configure Amazon Bedrock Guardrails: define sensitive topic filters, PII data masking, and Prompt Injection safeguards. | 07/23/2026 | 07/23/2026 | Amazon Bedrock Guardrails Guide |
| Fri | - Complete Stream 2 integration and perform end-to-end testing via Postman (verifying Auth Token, Cache Hit/Miss, Guardrails). | 07/24/2026 | 07/24/2026 | Postman API Testing |

### Week 5 Achievements:

* **API Security & User Auth**: Secured REST API endpoints with Cognito User Pool authorizers and enabled cross-origin resource sharing (CORS).
* **Performance & Cost Optimization**: Implemented ElastiCache Semantic Cache, returning instant cached responses for repetitive queries and cutting LLM usage costs.
* **Data Protection & Storage**: Enforced Bedrock Guardrails for PII masking/content moderation and stored interaction history in DynamoDB tables.
* **Verified Stream 2**: Successfully performed end-to-end API testing using Postman.
