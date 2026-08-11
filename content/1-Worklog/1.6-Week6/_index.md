---
title: "Week 6 Worklog"
date: 2024-01-01
weight: 6
chapter: false
pre: " <b> 1.6. </b> "
---


### Week 6 Objectives:

* Implement Stream 3 (Monitoring & Alerting): CloudWatch Custom Metrics, CloudWatch Dashboards, Alarms, SNS Topics, and AWS Chatbot integrated with Slack.
* Implement Stream 4 (RAGAS Evaluation): Research RAGAS framework, schedule EventBridge Scheduler rules, and build Lambda Evaluation Runner to auto-assess RAG output.

### Tasks to be carried out this week:

| Day | Task | Start Date | Completion Date | Reference Material |
| --- | --- | --- | --- | --- |
| Mon | - **CloudWatch Advanced & Custom Metrics**: Push custom metrics from Lambda using `boto3` (`put_metric_data`); build comprehensive CloudWatch Dashboard (Lambda invocation/error rate, API Gateway 4xx/5xx, SQS queue depth). | 07/27/2026 | 07/27/2026 | AWS CloudWatch Documentation |
| Tue | - **CloudWatch Alarms & SNS Topics**: Configure specific alarms for Lambda Errors, API Gateway 5xx, DLQ Depth (Critical), and Bedrock Throttle (Critical); set up `alerts-info` and `alerts-critical` SNS topics with test email subscriptions. | 07/28/2026 | 07/28/2026 | AWS SNS & CloudWatch Alarms |
| Wed | - **AWS Chatbot & Slack Integration**: Connect AWS Chatbot with Slack Workspace via OAuth authorization, route `alerts-critical` to `#rag-alerts` channel, and test notifications using simulated Lambda errors. | 07/29/2026 | 07/29/2026 | AWS Chatbot Guide |
| Thu | - Research **RAGAS framework** (Faithfulness, Answer Relevancy, Context Precision) & EventBridge Scheduler; create a rule running daily at 2 AM to trigger evaluation. | 07/30/2026 | 07/30/2026 | RAGAS Framework Docs |
| Fri | - Write **Lambda RAGAS Evaluation Runner**: Sample ~20 Q&A pairs from recent 24h ChatHistory, calculate 3 core metrics, store output JSON in S3 Evaluation Results; test run and summarize weekly progress. | 07/31/2026 | 07/31/2026 | Internal Test & Evaluation |

### Week 6 Achievements:

* **Comprehensive Observability**: Designed a centralized CloudWatch Dashboard displaying system telemetry and custom metrics published directly from Lambda code.
* **Automated Slack Alerting**: Implemented multi-tier CloudWatch Alarms linked to SNS Topics and AWS Chatbot, streaming critical operational alerts straight to the `#rag-alerts` Slack channel.
* **Automated RAG Quality Scoring**: Deployed the automated RAGAS evaluation pipeline running via EventBridge Scheduler at 2 AM daily, measuring Faithfulness, Answer Relevancy, and Context Precision.
