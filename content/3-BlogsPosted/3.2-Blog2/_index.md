---
title: "Blog 2"
date: 2024-01-01
weight: 1
chapter: false
pre: " <b> 3.2. </b> "
---
# What Should a Data Engineer Prioritize When Learning AWS in the AWS Study Group?

Hello everyone,

After participating in the AWS Study Group, I found that the learning roadmap is quite comprehensive, covering foundational knowledge such as IAM, VPC, EC2, and S3, as well as advanced Data and AI/ML services.

Initially, I thought I needed to learn everything in the prescribed order. However, since my goal is to become a Data Engineer, I asked myself a question:

*"If my study time is limited, which topics should I prioritize first to best support my future work in Data Engineering?"*

After reviewing the entire roadmap and learning more about AWS services, here are the main conclusions I have drawn.

## First, AWS Fundamentals Are Still an Essential Starting Point
No matter how modern a Data Pipeline is, its underlying infrastructure still relies on AWS's storage, computing, and security foundations.

Therefore, services such as:
- Amazon S3: Serves as the primary Data Lake for all data flows.
- AWS IAM: Manages access and secure permissions for each Service and User.
- Amazon EC2 & VPC: Provides an understanding of networking and servers for operating self-managed tools or agents when necessary.
are essential areas of knowledge that I need to master.

However, if I had to prioritize them based on their practical applications in Data Engineering, I would spend more time focusing on services related to data processing, storage, and data flows (the Data Engineering Ecosystem).
## Amazon S3 & Data Lake Architecture – Top Priority
Previously, when working on assignments or personal projects, data was usually stored in CSV/JSON files on my computer or in a small relational database.

However, in enterprise environments, Amazon S3 plays a critical role:
- Organizing a Data Lake architecture into different data layers (Bronze/Raw, Silver/Cleaned, and Gold/Curated).
- Managing file formats optimized for large-scale data querying, such as Parquet, ORC, and Avro.
- Optimizing storage costs using Lifecycle Rules and different storage classes (S3 Standard, S3 Glacier).

Understanding and correctly applying S3 as a Data Lake is the first skill that a Data Engineer needs to master.
## AWS Glue & ETL Pipelines – The Heart of Data Processing
While we are often familiar with writing individual Python scripts to clean data on personal computers, at an enterprise scale, AWS Glue becomes a powerful tool:
- AWS Glue Data Catalog & Crawler: Automatically discovers schemas and manages metadata across the entire Data Lake.
- Serverless Spark (Glue ETL Jobs): Processes and transforms massive datasets through Batch Processing without requiring us to manually build and manage Spark clusters.
- Glue Workflow / Orchestration: Connects preprocessing, data quality validation, and data loading steps into an automated pipeline.

Mastering AWS Glue enables Data Engineers to handle data transformation tasks flexibly and scalably.
## Amazon Redshift – Data Warehouse for Analytics & Reporting
After the data has been cleaned in the Data Lake, the next step is to load it into a Data Warehouse to support BI Dashboards and complex business queries.

Amazon Redshift is a service that I am particularly interested in:
- Understanding Columnar Storage and data distribution mechanisms such as Distribution Keys and Sort Keys to optimize SQL query performance.
- Integrating Redshift Spectrum to query data directly from S3 without having to load the entire dataset into the Data Warehouse.
- Designing data models such as Star Schema and Snowflake Schema for standardized enterprise reporting.
## Amazon Kinesis / Amazon MSK – Real-Time Streaming Data Processing
In many real-world applications, such as user event identification, system log monitoring, and financial transactions, data does not only arrive in batches but continuously flows as a stream.

Working with services such as Amazon Kinesis (Data Streams, Firehose) or Amazon MSK (Managed Streaming for Apache Kafka) enables Data Engineers to:
- Build Real-Time Ingestion architectures.
- Send streaming data directly to a Data Lake (S3) or Data Warehouse for immediate processing and analysis.
## Amazon Athena & AWS Lake Formation – Fast Analytics & Data Security
- Amazon Athena: Allows users to run ad-hoc SQL queries directly on files stored in S3 without having to build a database. This is an extremely convenient tool for exploring raw data.
- AWS Lake Formation: Helps establish security policies and fine-grained access control, including Row-Level and Column-Level Security, on a Data Lake more easily than manually configuring IAM permissions.
## Topics I Will Continue to Learn
Of course, being a Data Engineer does not stop at data-specific services. Knowledge of the following areas is also essential:
- **Networking & VPC Peering:** To securely connect a Data Warehouse with internal databases (On-premises DB).
- **Amazon CloudWatch & AWS EventBridge:** To monitor pipelines and automatically trigger alerts when ETL jobs encounter errors.
- **Infrastructure as Code (Terraform / AWS CDK):** To manage the entire Data Pipeline infrastructure as source code.

đều rất cần thiết. Nhưng ở giai đoạn hiện tại, ưu tiên hàng đầu của mình vẫn là làm chủ luồng đi của dữ liệu từ **Ingestion → Storage → Transformation → Warehouse**.
## Cuối cùng
Tham gia AWS Study Group giúp mình nhận ra Data Engineer không chỉ là viết query SQL hay code Python, mà là biết chọn đúng dịch vụ Cloud phù hợp cho từng bài toán dữ liệu, tối ưu được cả về hiệu năng (Performance) lẫn chi phí (Cost) cho doanh nghiệp.

Ưu tiên tập trung vào bộ dịch vụ S3, Glue, Redshift, Athena, Kinesis chính là con đường ngắn nhất giúp mình sẵn sàng cho các bài toán thực tế của một Data Engineer.

Nếu mọi người cũng đang định hướng theo Data Engineering hoặc Analytics Engineering, rất mong nhận được thêm chia sẻ và góc nhìn từ mọi người!
Cảm ơn mọi người đã đọc bài viết!

## Link
<https://www.facebook.com/groups/awsstudygroupfcj/permalink/2236445443787082/?rdid=XxPEuBNX5l2ZEBPZ#>