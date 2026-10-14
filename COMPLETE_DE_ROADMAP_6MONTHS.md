# THE COMPLETE DATA ENGINEERING ROADMAP
## From Zero to Internship-Ready in 6 Months
## 4 Hours/Day | Every Topic | Every Project | Nothing Left Out
## By a 6-Year Google Data Engineer

---

## NUMBERS FIRST

```
Daily hours       → 4 hrs strictly focused
Total days        → 180 days
Total hours       → 720 hours
Target            → Paid DE internship (25,000 - 50,000/month)
Apply date        → End of 2nd year BTech
```

---

## THE COMPLETE DE SKILL TREE

```
FOUNDATION LAYER
├── Python
├── SQL + PostgreSQL
└── Linux + Command Line basics

CORE DE LAYER
├── Data Modeling
├── ETL / ELT Pipelines
├── Apache Airflow (Orchestration)
├── Docker (just enough)
└── Data Quality + Testing

CLOUD LAYER
├── GCP (Cloud Storage + BigQuery + IAM)
├── AWS basics (S3 + Redshift + Glue)
└── Cloud Architecture Design

ADVANCED DE LAYER
├── Apache Spark
├── Apache Kafka (Streaming basics)
├── dbt (Data Build Tool)
└── Delta Lake / Data Lakehouse

INTERVIEW LAYER
├── DSA (Data Structures + Algorithms)
├── System Design for DE
└── SQL Interview Problems
```

---

# MONTH 1 — FOUNDATION
## Python + SQL + Linux
## Hours: 120 hrs total (4 hrs/day × 30 days)

---

## WEEK 1-2 | PYTHON
### Time: 56 hours

**Why Python first:**
Every DE tool — Airflow, Spark, dbt — is controlled through Python.
Without Python you cannot do anything else in this roadmap.

---

### Topics to Cover:

**Week 1 (28 hrs):**
```
Day 1-2  → Variables, data types, operators, input/output, f-strings
Day 3-4  → if/elif/else, for loops, while loops, break/continue
Day 5-6  → Functions — def, return, default args, *args, **kwargs
Day 7    → Lists, tuples, sets, dicts — all operations
```

**Week 2 (28 hrs):**
```
Day 8-9  → File I/O — open, read, write, CSV, JSON
Day 10   → Error handling — try/except/finally, custom exceptions
Day 11   → OOP — classes, objects, __init__, methods, inheritance
Day 12   → Modules — import, pip, requirements.txt, virtual env
Day 13   → List comprehensions, lambda, map, filter
Day 14   → Python logging module — DEBUG/INFO/WARNING/ERROR levels
```

---

### 🎯 PROJECT 1: "Personal Finance Tracker CLI"

**What you build:**
A command line app that reads your expenses from a CSV file,
categorizes them, calculates totals per category, finds the most
expensive category, and writes a summary report to a new CSV.

**Why this project:**
Forces you to use: file I/O, functions, OOP, error handling,
loops, dicts — all at once. Not a toy. A real useful tool.

**Folder structure:**
```
finance-tracker/
├── data/
│   └── expenses.csv          ← your input data
├── src/
│   ├── reader.py             ← reads CSV
│   ├── categorizer.py        ← categorizes expenses
│   ├── calculator.py         ← does the math
│   └── reporter.py           ← writes output
├── main.py                   ← wires everything
├── requirements.txt
└── README.md
```

**You know Python when:**
You can build this without Googling anything except library docs.

---

## WEEK 3-4 | SQL + POSTGRESQL
### Time: 56 hours

**Why SQL is the most important skill in DE:**
Every single DE interview starts with SQL. If SQL is weak,
you fail before they even look at your project.

---

### Topics to Cover:

**Week 3 (28 hrs):**
```
Day 15   → SELECT, WHERE, ORDER BY, LIMIT, DISTINCT, aliases
Day 16   → JOINs — INNER, LEFT, RIGHT, FULL OUTER, SELF, CROSS
Day 17   → Aggregations — COUNT, SUM, AVG, MIN, MAX, GROUP BY, HAVING
Day 18   → Subqueries — scalar, correlated, EXISTS, IN vs EXISTS
Day 19   → Window Functions — ROW_NUMBER, RANK, DENSE_RANK, NTILE
Day 20   → Window Functions advanced — LAG, LEAD, running totals, PARTITION BY
Day 21   → CTEs — WITH clause, chaining CTEs, recursive CTEs
```

**Week 4 (28 hrs):**
```
Day 22   → PostgreSQL setup — install, DBeaver, data types, JSONB
Day 23   → DDL — CREATE TABLE, ALTER, DROP, constraints (PK, FK, UNIQUE, NOT NULL)
Day 24   → Indexes — B-tree, Hash, EXPLAIN ANALYZE, when indexes hurt
Day 25   → Transactions — ACID, BEGIN/COMMIT/ROLLBACK, isolation levels
Day 26   → Database design — normalization (1NF 2NF 3NF), Star Schema
Day 27   → Query optimization — slow query analysis, index strategy
Day 28   → LeetCode Database — 15 problems (Easy + Medium)
```

---

### 🎯 PROJECT 2: "SQL Murder Mystery + Custom Dataset"

**Part A:** Solve the full SQL Murder Mystery at mystery.knightlab.com
This takes 3-4 hours but teaches JOINs + subqueries in context.

**Part B:** Create your own dataset (500+ rows) about something
you care about — cricket stats, movie ratings, stock prices.
Load it into PostgreSQL. Write 20 complex queries on it:
```
- Top 5 performers by category using window functions
- Month over month growth using LAG
- Running totals using SUM OVER
- Rank within groups using DENSE_RANK + PARTITION BY
- Complex multi-table JOIN with aggregation
```

**You know SQL when:**
You can write any query in 1-2 minutes without Googling syntax.

---

## LINUX + COMMAND LINE BASICS
### Time: 8 hours (spread across Month 1 evenings)

```
Topics:
├── Navigation — cd, ls, pwd, mkdir, rm, cp, mv
├── File operations — cat, head, tail, grep, wc, find
├── Permissions — chmod, chown, sudo
├── Process management — ps, kill, top, background jobs (&)
├── Pipes and redirects — |, >, >>, 2>&1
├── Shell scripts — basic .sh files, variables, loops
└── SSH basics — connect to remote server
```

**Why:** Every cloud server, every Docker container, every Airflow
worker runs on Linux. You must be comfortable here.

**Mini task:** Write a shell script that reads a CSV file,
counts rows, and prints a summary. 30 lines max.

---

# MONTH 2 — CORE DATA ENGINEERING
## pandas + APIs + Data Modeling + ETL
## Hours: 120 hrs (4 hrs/day × 30 days)

---

## WEEK 5-6 | PYTHON FOR DATA ENGINEERING
### Time: 56 hours

```
Day 29-30 → pandas basics — read_csv, DataFrame, Series, loc/iloc,
             filtering, sorting, value_counts, info, describe
Day 31-32 → pandas intermediate — GroupBy, merge/join, pivot_table,
             apply, lambda, method chaining
Day 33-34 → pandas advanced — NaN handling, datetime, string ops,
             type conversion, memory optimization
Day 35    → pyarrow + Parquet — why columnar, read/write,
             compression, compare to CSV (size + speed)
Day 36    → APIs with requests — GET, POST, headers, params,
             pagination, authentication, store as JSON
Day 37    → pydantic — models, validation, type enforcement,
             custom validators, ValidationError handling
Day 38    → psycopg2 + SQLAlchemy — connect to PostgreSQL,
             execute queries, insert DataFrames, connection pooling
Day 39    → pytest basics — test functions, fixtures, assert,
             mock data, parametrize
Day 40    → Python project structure — src layout, __init__.py,
             .env with python-dotenv, logging best practices
Day 41-42 → Build and test a complete modular ETL:
             Extractor class, Transformer class, Loader class
```

---

## WEEK 7-8 | DATA MODELING + ETL CONCEPTS
### Time: 56 hours (but this is theory-heavy so mix with coding)

```
Day 43-44 → Data Modeling theory:
             - OLTP vs OLAP (transactional vs analytical)
             - Star Schema (fact + dimension tables)
             - Snowflake Schema
             - Wide tables vs normalized tables
             - When to use which

Day 45-46 → ETL vs ELT:
             - ETL: transform before loading (old way)
             - ELT: load raw, transform in warehouse (modern way)
             - When to use which
             - Real examples from Swiggy, Zomato, Flipkart

Day 47    → Idempotency:
             - What it means (run 10 times = same result)
             - Why pipelines must be idempotent
             - Upsert logic (INSERT ON CONFLICT)
             - Delete + insert pattern
             - Deduplication strategies

Day 48    → Data Quality:
             - 5 types of checks (null, schema, range, uniqueness, freshness)
             - Where to add checks in pipeline
             - What to do when check fails (alert, halt, quarantine)

Day 49    → Batch vs Streaming:
             - Batch: scheduled, high latency, simple (your focus now)
             - Streaming: real time, complex, Kafka/Flink (Month 5)
             - When each makes sense

Day 50-51 → SCD (Slowly Changing Dimensions):
             - Type 1: overwrite old value
             - Type 2: add new row with dates (most important)
             - Type 3: add new column
             - Implement SCD Type 2 in SQL + Python

Day 52-54 → Data Lineage + Monitoring:
             - What lineage means (track data from source to destination)
             - Build a pipeline_runs monitoring table
             - Log: rows_in, rows_out, duration, status, errors
             - Alert when pipeline fails

Day 55-56 → Late data + Backfill:
             - What happens when data arrives late
             - Backfill: reprocess historical data
             - How Airflow handles backfill
```

---

### 🎯 PROJECT 3: "End-to-End ETL Pipeline — Stock Price Tracker"

**What you build:**
Pull daily stock prices from Yahoo Finance API (free).
Clean and validate with pydantic + pandas.
Model into star schema: fact_prices + dim_companies + dim_dates.
Load into PostgreSQL.
Write 10 analytics queries on top.
Add a monitoring table that logs every pipeline run.

**Skills used:**
Python, APIs, pandas, pydantic, PostgreSQL, data modeling,
idempotency, data quality checks, monitoring, SCD Type 1.

**What makes it real:**
Your pipeline should handle: API timeout, empty response,
duplicate data, missing dates. Not just the happy path.

**Folder structure:**
```
stock-pipeline/
├── ingestion/
│   ├── api_client.py         ← fetches from Yahoo Finance
│   └── validator.py          ← pydantic models
├── transform/
│   ├── cleaner.py            ← pandas transformations
│   └── quality_checker.py   ← 5 data quality checks
├── load/
│   ├── db_loader.py          ← loads to PostgreSQL
│   └── monitoring.py         ← writes pipeline_runs table
├── sql/
│   ├── create_tables.sql     ← star schema DDL
│   └── analytics_queries.sql ← 10 queries
├── tests/
│   └── test_pipeline.py      ← pytest tests
├── main.py
└── README.md
```

---

# MONTH 3 — ORCHESTRATION + DOCKER
## Apache Airflow + Docker
## Hours: 120 hrs (4 hrs/day × 30 days)

---

## WEEK 9-10 | DOCKER BASICS
### Time: 28 hours

**Why Docker:**
Airflow runs in Docker. GCP uses containers. Every modern
data tool ships as a Docker image. You need just enough.

```
Day 57-58 → Docker concepts:
             - What a container is vs a virtual machine
             - Images, containers, Dockerfile, Docker Hub
             - docker run, docker ps, docker stop, docker rm
             - docker exec -it (get inside container)

Day 59-60 → Docker for DE:
             - Pull and run PostgreSQL in Docker
             - Pull and run Redis in Docker
             - docker-compose.yml — define multi-container apps
             - Volumes — persist data between container restarts
             - Networks — containers talking to each other

Day 61-62 → Write your own Dockerfile:
             - Base image, COPY, RUN, ENV, CMD
             - Build your ETL script as a Docker image
             - Run it as a container
             - Pass environment variables (.env)

Day 63    → Docker Compose for full stack:
             - PostgreSQL + your ETL app in one compose file
             - docker-compose up, down, logs
```

**Mini project:** Dockerize your Stock Price ETL from Project 3.
Run it with docker-compose up. Data should flow into PostgreSQL
running in a separate container.

---

## WEEK 11-14 | APACHE AIRFLOW
### Time: 84 hours

```
Day 64-65 → Airflow architecture:
             - Webserver, Scheduler, Worker, Metadata DB
             - How DAGs work (Directed Acyclic Graph)
             - Airflow setup with Docker Compose
             - Explore UI: DAGs, Graph View, Tree View, Logs

Day 66-67 → Writing DAGs:
             - DAG object — schedule_interval, start_date, catchup
             - BashOperator — run shell commands
             - PythonOperator — run Python functions
             - Task dependencies: task1 >> task2 >> task3
             - Branching: BranchPythonOperator

Day 68-69 → Operators deep dive:
             - FileSensor — wait for a file to appear
             - HttpSensor — wait for an API to be available
             - EmailOperator — send email on completion
             - PostgresOperator — run SQL from a DAG

Day 70-71 → Scheduling:
             - Cron syntax (*/5 * * * * = every 5 min)
             - Daily, hourly, weekly schedules
             - Backfill: reprocess historical dates
             - catchup=False vs True

Day 72-73 → Error handling in Airflow:
             - retries, retry_delay
             - on_failure_callback
             - SLA misses
             - Task timeouts
             - Deliberately fail a task and recover

Day 74-75 → Airflow best practices:
             - XComs — pass small data between tasks
             - Airflow Variables — store configs
             - Airflow Connections — store credentials
             - PostgresHook — connect to DB from DAG
             - Never hardcode credentials in DAG files

Day 76-77 → Advanced DAG patterns:
             - Dynamic DAGs — generate tasks programmatically
             - TaskGroups — group related tasks visually
             - Trigger rules — ALL_SUCCESS, ONE_FAILED, ALL_DONE
             - Pools — limit parallel task execution
```

---

### 🎯 PROJECT 4: "Automated News Sentiment Pipeline"

**What you build:**
Every hour, Airflow fetches top tech news from NewsAPI (free).
Runs basic sentiment analysis (TextBlob — simple positive/negative).
Stores articles + sentiment scores in PostgreSQL.
Tracks: which topics are getting more negative coverage over time.
Dashboard: simple HTML report generated daily.

**DAG structure:**
```
HttpSensor (check NewsAPI alive)
      ↓
PythonOperator (fetch articles)
      ↓
PythonOperator (run sentiment analysis)
      ↓
PythonOperator (data quality checks)
      ↓
PostgresOperator (load to DB)
      ↓
PythonOperator (generate HTML report)
      ↓
PythonOperator (update monitoring table)
```

**What makes it real:**
- Runs automatically every hour
- Has retry logic (3 retries, 5 min delay)
- Sends log alert on failure
- Idempotent (running twice doesn't duplicate data)
- Full monitoring table

---

# MONTH 4 — CLOUD
## GCP (Deep) + AWS (Basics)
## Hours: 120 hrs (4 hrs/day × 30 days)

---

## WEEK 15-18 | GCP — DEEP DIVE
### Time: 84 hours

```
Day 85-86 → GCP setup:
             - Create free account + activate $300 credits
             - Cloud Console tour
             - gcloud CLI setup
             - Projects, regions, zones

Day 87-88 → Cloud Storage (GCS):
             - Buckets, objects, folders
             - Storage classes (Standard, Nearline, Coldline)
             - Upload/download with gsutil and Python
             - Versioning, lifecycle rules
             - Build: gcs_utility.py module

Day 89-91 → BigQuery:
             - Datasets, tables, views
             - BigQuery SQL — same as PostgreSQL but with differences
             - Partitioning by DATE (most important for cost)
             - Clustering (like indexes for BQ)
             - INFORMATION_SCHEMA — query metadata
             - Query cost estimation (always check before running)
             - Python client: load DataFrame, run query, get results

Day 92-93 → BigQuery advanced:
             - Nested + repeated fields (STRUCT, ARRAY, UNNEST)
             - Materialized views
             - Scheduled queries
             - BigQuery ML (train a model with SQL — impressive for portfolio)
             - Streaming inserts vs batch load jobs

Day 94-95 → IAM + Security:
             - Service accounts — what they are, why they matter
             - Roles: BigQuery Admin, Storage Admin, Viewer
             - Download JSON key, use in Python
             - Never commit keys to GitHub (.gitignore)
             - Principle of least privilege

Day 96-97 → Cloud Functions:
             - Serverless Python functions triggered by events
             - HTTP trigger — call a function via URL
             - GCS trigger — function runs when file uploaded
             - Use case: trigger pipeline when new data file arrives

Day 98-99 → Pub/Sub basics:
             - Message queue — publisher sends, subscriber receives
             - Topics and subscriptions
             - Use case: decouple data producers from consumers
             - Connect to Cloud Functions

Day 100-101 → Looker Studio:
              - Connect BigQuery as data source
              - Build charts: line, bar, pie, scorecard, table
              - Filters, date ranges, calculated fields
              - Share dashboard with public link
```

---

## WEEK 19-20 | AWS BASICS
### Time: 36 hours

**Why AWS even though you're learning GCP:**
60% of companies use AWS. Knowing both makes you 2x hireable.
The concepts are identical — just different names.

```
GCP                  AWS equivalent
─────────────────────────────────────
Cloud Storage    →   S3
BigQuery         →   Redshift / Athena
Cloud Functions  →   Lambda
Pub/Sub          →   SQS / SNS
Cloud Composer   →   MWAA (Managed Airflow)
```

```
Day 102-103 → AWS setup:
              - Free tier account
              - IAM users, roles, policies
              - AWS CLI setup

Day 104-105 → S3:
              - Buckets, objects, versioning
              - Python with boto3 library
              - Upload/download/list operations

Day 106-107 → Redshift basics:
              - Columnar data warehouse (like BigQuery)
              - Connect with Python, run queries
              - Distribution styles (KEY, EVEN, ALL)

Day 108-109 → AWS Glue basics:
              - Managed ETL service
              - Glue Crawlers — auto-detect schema
              - Glue Jobs — run PySpark ETL

Day 110-112 → AWS Lambda:
              - Serverless functions
              - Trigger on S3 upload
              - Connect to RDS / Redshift
              - Deploy from Python
```

---

### 🎯 PROJECT 5: "AI TOKEN COST ANALYTICS PIPELINE" ← YOUR MAIN PROJECT

**This is the one. Build this properly.**

**What you build:**
Full end-to-end DE pipeline that tracks every LLM API call,
calculates cost, stores in BigQuery, shows live dashboard.

**Architecture:**
```
LLM API Calls (OpenAI + Gemini)
         ↓
Proxy Logger (Python — wraps every API call)
         ↓
GCS Raw Layer (JSON, partitioned by date/hour)
         ↓
[Airflow DAG — runs every hour]
         ↓
Transform (pandas — clean, validate, calculate derived fields)
         ↓
GCS Clean Layer (Parquet)
         ↓
BigQuery (partitioned by date, clustered by model)
         ↓
Looker Studio Dashboard
```

**BigQuery tables:**
```sql
token_events      ← every API call (fact table)
daily_summary     ← aggregated per model per day
price_history     ← SCD Type 2 for model pricing changes
pipeline_runs     ← monitoring + lineage
cost_alerts       ← triggered alerts log
```

**Dashboard cards:**
```
1. Total spend today / this week / this month
2. Cost breakdown by model (pie chart)
3. Token usage over time (hourly line chart)
4. Top 10 most expensive calls (table)
5. Efficiency score per model (tokens per dollar)
6. Month-to-date spend forecast
7. Pipeline health status
```

**Advanced features that make it stand out:**
```
✅ SCD Type 2 for price history
   (model prices change — track historical costs correctly)
✅ Idempotent pipeline
   (run 10 times = same result, no duplicates)
✅ Data quality checks at every step
✅ Monitoring table with row counts + duration
✅ Slack webhook alert when daily spend > threshold
✅ GitHub Actions CI (pytest runs on every push)
✅ Deployed on GCP (runs on schedule without your laptop)
✅ Cost optimization (partitioned + clustered BQ tables)
```

**This project alone can get you an internship.**

---

# MONTH 5 — ADVANCED TOOLS
## dbt + Spark + Kafka Basics
## Hours: 120 hrs (4 hrs/day × 30 days)

---

## WEEK 21-22 | DBT (DATA BUILD TOOL)
### Time: 56 hours

**Why dbt:**
dbt is taking over data transformation at every company.
It's how modern DE teams write SQL transformations in production.
Every job posting mentions it now.

```
Day 113-114 → What is dbt:
              - dbt transforms data INSIDE the warehouse (ELT)
              - You write SQL SELECT statements
              - dbt compiles them into CREATE TABLE / VIEW statements
              - Handles dependencies between models automatically

Day 115-116 → dbt setup:
              - Install dbt-core + dbt-bigquery
              - Connect to BigQuery
              - Project structure: models/, tests/, seeds/, macros/

Day 117-118 → dbt models:
              - Staging models (raw → cleaned)
              - Intermediate models (joins + calculations)
              - Mart models (final analytics tables)
              - ref() function — how models depend on each other
              - Materialization: table, view, incremental, ephemeral

Day 119-120 → dbt tests:
              - Built-in tests: not_null, unique, accepted_values, relationships
              - Custom tests
              - dbt test command
              - Schema.yml files

Day 121-122 → dbt advanced:
              - Incremental models (only process new data)
              - Macros (reusable Jinja SQL snippets)
              - Packages (dbt_utils, dbt_expectations)
              - Sources — declare raw data sources
              - Documentation: dbt docs generate + serve

Day 123-124 → Airflow + dbt:
              - Run dbt models from Airflow DAG
              - BashOperator: dbt run --select model_name
              - DbtTaskGroup pattern
```

---

### 🎯 PROJECT 6: "dbt Transformation Layer for Token Analytics"

Add a full dbt transformation layer on top of Project 5.

**dbt models:**
```
staging/
├── stg_token_events.sql       ← clean raw events
└── stg_price_history.sql      ← clean price data

intermediate/
├── int_events_with_cost.sql   ← join events + prices
└── int_daily_aggregates.sql   ← daily rollups

marts/
├── fct_token_events.sql       ← final fact table
├── dim_models.sql             ← model dimension
└── agg_daily_summary.sql      ← dashboard-ready table
```

**Add dbt tests:**
```yaml
- not_null: [event_id, timestamp, model, cost_usd]
- unique: [event_id]
- accepted_values: model in known_models
- relationships: model in dim_models
```

Now your pipeline is: ingest → GCS → BigQuery raw →
dbt transforms → BigQuery marts → Looker Studio.
That is a production-grade stack.

---

## WEEK 23-24 | APACHE SPARK BASICS
### Time: 56 hours

**Why Spark:**
When your data is too big for pandas (100GB+), you use Spark.
Every senior DE job requires Spark knowledge.

```
Day 125-126 → What is Spark:
              - Distributed computing — splits data across machines
              - In-memory processing (faster than disk)
              - PySpark — Python API for Spark
              - SparkContext, SparkSession

Day 127-128 → PySpark basics:
              - RDD vs DataFrame vs Dataset
              - Reading: CSV, JSON, Parquet into Spark DataFrame
              - Transformations: select, filter, withColumn, groupBy, agg
              - Actions: show, count, collect, write

Day 129-130 → PySpark SQL:
              - createOrReplaceTempView
              - spark.sql() — run SQL on Spark DataFrame
              - Window functions in PySpark
              - UDFs (User Defined Functions)

Day 131-132 → PySpark performance:
              - Partitions — how Spark splits data
              - Shuffling — expensive operation to avoid
              - Caching — df.cache() for reused DataFrames
              - Broadcast joins — for small + large table joins
              - Reading Parquet >> reading CSV for Spark

Day 133-134 → Spark on GCP:
              - Dataproc — managed Spark cluster on GCP
              - Submit PySpark job to Dataproc
              - Read from GCS, write to GCS
              - Connect to BigQuery from Spark
```

---

## WEEK 25 | KAFKA BASICS (STREAMING INTRO)
### Time: 20 hours — just enough to understand

```
Day 135-136 → What is Kafka:
              - Message streaming platform
              - Topics, partitions, producers, consumers
              - Why it exists (decouple fast producers from slow consumers)
              - Real use cases: Uber ride events, Swiggy order updates

Day 137-138 → Kafka setup + basics:
              - Run Kafka with Docker Compose
              - Create a topic
              - Produce messages with Python (kafka-python)
              - Consume messages with Python
              - Consumer groups

Day 139     → Kafka + DE:
              - Kafka → Spark Streaming (read live events)
              - Kafka → Airflow (trigger DAG on new message)
              - When to use Kafka vs batch pipeline
```

**Mini project:** Build a simple producer that sends fake
LLM API call events to a Kafka topic every second.
Build a consumer that reads them and prints a running cost total.
No storage yet — just understand the flow.

---

# MONTH 6 — INTERVIEW PREP
## DSA + SQL Interviews + System Design + Apply
## Hours: 120 hrs (4 hrs/day × 30 days)

---

## WEEK 26-27 | DSA FOR DE INTERVIEWS
### Time: 56 hours

**Reality check:** DE interviews have less DSA than SDE.
But most companies still test basic DSA in screening rounds.
You need: Arrays, Strings, HashMaps, Trees basics, Sorting.
You do NOT need: Advanced graphs, complex DP, segment trees.

```
Week 26:
Day 140-141 → Arrays — Two Pointer, Sliding Window, Prefix Sum
Day 142-143 → Strings — palindrome, anagram, substring problems
Day 144-145 → HashMaps + HashSets — frequency counting, dedup
Day 146     → Sorting — understand Merge Sort + Quick Sort logic
              (don't implement from scratch, understand complexity)

Week 27:
Day 147-148 → Linked Lists — reverse, cycle detection, merge
Day 149-150 → Trees — BFS, DFS, height, BST basics
Day 151-152 → Stacks + Queues — valid parentheses, sliding window max
Day 153     → Recursion — understand call stack, base case
```

**Target:** 60-80 LeetCode problems (40 Easy, 30 Medium, 10 Hard)
**Platform:** neetcode.io (watch pattern video first, then solve)

---

## WEEK 28 | SQL INTERVIEW PREP
### Time: 28 hours

**This is where DE interviews are really decided.**

```
Day 154-155 → Window function problems:
              - Running totals
              - Rank within group
              - Month over month growth
              - Gap and island problems

Day 156-157 → Complex JOIN problems:
              - Self joins
              - Multiple table joins
              - Finding records that don't exist in another table

Day 158-159 → Aggregation problems:
              - Median calculation in SQL
              - Percentage of total
              - Pivot tables in SQL
              - Cumulative distributions

Day 160     → Real interview questions:
              - LeetCode Database: all Medium + Hard
              - DataLemur: all free problems
              - stratascratch.com: company-specific questions
```

---

## WEEK 29 | SYSTEM DESIGN FOR DE
### Time: 28 hours

**Not full system design — just DE system design.**
Interviewers ask: "Design a pipeline that does X."

```
Day 161-162 → Framework for answering:
              1. Clarify requirements (batch or streaming? scale? latency?)
              2. Design data model (what tables? what schema?)
              3. Design pipeline (what tools? what steps?)
              4. Handle failures (retries? dead letter queue?)
              5. Monitor (how do you know it's working?)

Day 163-164 → Common design questions:
              - Design a pipeline for Swiggy order analytics
              - Design a real-time fraud detection pipeline
              - Design a data warehouse for an e-commerce company
              - Design a pipeline that handles late-arriving data

Day 165-166 → Answer these 5 questions without notes:
              - Why Airflow over cron?
              - Why Parquet over CSV?
              - Why BigQuery over PostgreSQL for analytics?
              - What is idempotency and why does it matter?
              - How do you handle a pipeline that fails at step 3?

Day 167     → Scalability concepts:
              - Horizontal vs vertical scaling
              - Sharding and partitioning
              - CAP theorem (basic understanding)
              - Lambda architecture vs Kappa architecture
```

---

## WEEK 30 | APPLY + MOCK INTERVIEWS
### Time: 28 hours

```
Day 168-169 → Polish everything:
              - GitHub: clean READMEs, architecture diagrams, demo videos
              - LinkedIn: update with projects, skills, bio
              - Resume: 1 page, project-focused, numbers everywhere

Day 170-171 → Cold outreach:
              - Find 50 startups on LinkedIn using DE stack
              - DM data engineers at those companies
              - Email CTOs of Series A companies
              - Message: "I built X using Y, here is the GitHub link"

Day 172-173 → Mock interviews:
              - 2 SQL mock interviews (timed, no help)
              - 2 DSA mock interviews
              - 1 system design mock interview
              - Record yourself and watch it back

Day 174-180 → Apply aggressively:
              - Apply to 50+ companies minimum
              - Internship portals: LinkedIn, Internshala, AngelList, YCombinator jobs
              - Don't wait until you feel "ready"
              - Apply from Day 1 of Month 6
```

---

# COMPLETE TOPIC CHECKLIST

## Python ✓
```
□ Variables, data types, operators
□ Control flow (if/for/while)
□ Functions (*args, **kwargs, default args)
□ OOP (classes, inheritance, dunder methods)
□ File I/O (CSV, JSON, text)
□ Error handling (try/except/finally)
□ Modules + virtual environments
□ List comprehensions, lambda, map, filter
□ Logging module
□ Type hints
□ pytest basics
```

## SQL + PostgreSQL ✓
```
□ SELECT, WHERE, ORDER BY, LIMIT, DISTINCT
□ All JOINs (INNER, LEFT, RIGHT, FULL, SELF, CROSS)
□ Aggregations + GROUP BY + HAVING
□ Subqueries (scalar, correlated, EXISTS)
□ Window Functions (ROW_NUMBER, RANK, LAG, LEAD, running totals)
□ CTEs (single, chained, recursive)
□ DDL (CREATE, ALTER, DROP, constraints)
□ Indexes (B-tree, Hash, EXPLAIN ANALYZE)
□ Transactions (ACID, isolation levels)
□ Database normalization (1NF, 2NF, 3NF)
□ Star Schema design
□ Query optimization
```

## Python for DE ✓
```
□ pandas (all levels — basic, intermediate, advanced)
□ pyarrow + Parquet
□ requests (APIs, pagination, auth)
□ pydantic (validation, models)
□ psycopg2 + SQLAlchemy
□ python-dotenv (.env secrets)
□ Modular ETL structure (Extractor, Transformer, Loader)
```

## Data Modeling ✓
```
□ OLTP vs OLAP
□ Star Schema + Snowflake Schema
□ Fact tables + Dimension tables
□ SCD Type 1, Type 2, Type 3
□ Wide vs normalized tables
□ Data Vault basics (awareness only)
```

## ETL Concepts ✓
```
□ ETL vs ELT
□ Idempotency
□ Batch vs Streaming
□ Data quality (5 check types)
□ Data lineage
□ Late data handling
□ Backfill strategies
□ Monitoring + alerting
```

## Docker ✓
```
□ Images, containers, Dockerfile
□ docker run, ps, stop, exec
□ docker-compose.yml
□ Volumes + Networks
□ Dockerize a Python app
```

## Apache Airflow ✓
```
□ Architecture (Webserver, Scheduler, Worker, Metadata DB)
□ DAG structure + parameters
□ All operators (Bash, Python, Email, Postgres, Sensor)
□ Task dependencies
□ Scheduling + cron
□ XComs + Variables + Connections
□ Error handling + retries + callbacks
□ Dynamic DAGs
□ TaskGroups
□ Trigger rules
```

## GCP ✓
```
□ Cloud Storage (buckets, Python client, lifecycle)
□ BigQuery (SQL, partitioning, clustering, Python client)
□ BigQuery advanced (nested fields, materialized views, cost optimization)
□ IAM + Service Accounts
□ Cloud Functions
□ Pub/Sub basics
□ Looker Studio dashboards
□ gcloud CLI
```

## AWS ✓
```
□ S3 + boto3
□ Redshift basics
□ AWS Glue basics
□ Lambda basics
□ IAM basics
```

## dbt ✓
```
□ dbt project structure
□ Staging, Intermediate, Mart models
□ ref() + source()
□ Materialization types
□ dbt tests
□ Incremental models
□ Macros + packages
□ dbt docs
□ Airflow + dbt integration
```

## Apache Spark ✓
```
□ Spark architecture
□ PySpark DataFrame operations
□ PySpark SQL
□ Performance (partitions, shuffle, cache, broadcast)
□ Spark on GCP (Dataproc)
```

## Kafka ✓
```
□ Topics, partitions, producers, consumers
□ Python producer + consumer
□ Consumer groups
□ Kafka + Spark Streaming (awareness)
```

## DSA ✓
```
□ Arrays (Two Pointer, Sliding Window, Prefix Sum)
□ Strings
□ HashMaps + HashSets
□ Linked Lists
□ Trees (BFS, DFS, BST)
□ Stacks + Queues
□ Sorting (understand, not memorize)
□ Recursion basics
□ 60-80 LeetCode problems
```

## SQL Interviews ✓
```
□ Window function problems
□ Complex JOIN problems
□ Aggregation problems
□ LeetCode Database (all Medium + Hard)
□ DataLemur (all free)
□ stratascratch (company questions)
```

## System Design for DE ✓
```
□ Design framework (5 steps)
□ 5 common design questions answered
□ Scalability concepts
□ Lambda vs Kappa architecture
```

---

# ALL 6 PROJECTS SUMMARY

```
PROJECT 1: Personal Finance Tracker CLI
          Skills: Python fundamentals, OOP, file I/O
          Time: End of Week 2

PROJECT 2: SQL Murder Mystery + Custom Dataset
          Skills: SQL all levels, PostgreSQL, data analysis
          Time: End of Week 4

PROJECT 3: Stock Price ETL Pipeline
          Skills: Python DE, APIs, pandas, pydantic, PostgreSQL,
                  data modeling, star schema, monitoring
          Time: End of Week 8

PROJECT 4: Automated News Sentiment Pipeline
          Skills: Docker, Airflow (full DAG), sentiment analysis,
                  automated scheduling, error handling
          Time: End of Week 14

PROJECT 5: AI Token Cost Analytics Pipeline ← MAIN PROJECT
          Skills: Everything — Python, Airflow, GCP, BigQuery,
                  GCS, Looker Studio, SCD Type 2, CI/CD, deploy
          Time: End of Week 20

PROJECT 6: dbt Transformation Layer
          Skills: dbt, incremental models, testing, documentation
          Time: End of Week 22
          (Add on top of Project 5 — makes it even stronger)
```

---

# MONTH BY MONTH SUMMARY

```
Month 1 → Python + SQL + Linux               → Project 1 + Project 2
Month 2 → Python DE + Data Modeling + ETL   → Project 3
Month 3 → Docker + Airflow                  → Project 4
Month 4 → GCP deep + AWS basics             → Project 5 (main)
Month 5 → dbt + Spark + Kafka               → Project 6
Month 6 → DSA + SQL interviews + Apply      → Get the internship
```

---

# TOOLS TO INSTALL (IN ORDER)

```
Month 1 → Python 3.11, VS Code, PostgreSQL, DBeaver, Git
Month 2 → pip packages (pandas, pyarrow, requests, pydantic, psycopg2)
Month 3 → Docker Desktop, Docker Compose
Month 4 → gcloud CLI, AWS CLI, BigQuery Python client
Month 5 → dbt-core, dbt-bigquery, PySpark, kafka-python
Month 6 → Nothing new — just interview platforms
```

---

# THE ONLY RULE THAT MATTERS

```
Never move to the next topic until you can build
the current one from scratch without looking it up.

Speed means nothing. Depth means everything.
```

---

*4 hours. Every day. 180 days. Internship guaranteed.*
*The roadmap is complete. Now execute.*
