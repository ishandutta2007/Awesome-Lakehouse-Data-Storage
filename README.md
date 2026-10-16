# Awesome-Lakehouse-Data-Storage

# Top Lakehouse & Data Storage Ecosystem

**Curated List of SaaS Products & Open-Source GitHub Projects**  
*Focused on Open Table Formats, Query Engines & Data Lakehouse Architectures*  
**Last updated: March 2026**

This repository tracks notable **SaaS platforms** and **open-source projects** for **Lakehouse & Data Storage**. These tools enable ACID transactions, schema evolution, time travel, and multi-engine analytics directly on object storage, bridging the gap between data lakes and data warehouses without vendor lock-in.

**Examples** include Snowflake, Databricks Lakehouse, Google BigQuery, Amazon Redshift, Starburst Galaxy, ClickHouse Cloud, Dremio Cloud, Teradata Vantage, Firebolt, and SingleStore (the category leaders).

**Open-source emphasis**: This section is heavily expanded with every major active project for self-hosting, multi-engine query federation, and open table format interoperability — ideal for data engineers, platform teams, and organizations building transparent, vendor-neutral lakehouse architectures.

Contributions welcome! Open a PR to add/update entries. Keep descriptions factual and link to official sites.

## Table of Contents
- [SaaS/Hosted Platforms](#saas-hosted-platforms)
- [Open-Source GitHub Projects](#open-source-github-projects)
- [How to Contribute](#how-to-contribute)
- [Disclaimer](#disclaimer)

## SaaS/Hosted Platforms

- **[Snowflake](https://www.snowflake.com/)**  
  Cloud-native data warehouse with separated storage/compute, Iceberg table support, and Snowpark for Python/Java workloads; owns the Iceberg REST catalog spec via Polaris contribution .

- **[Databricks Lakehouse](https://www.databricks.com/)**  
  Unified analytics platform built on Delta Lake, with MLflow, Unity Catalog governance, and Photon query engine; strongest Delta Lake integration and governance .

- **[Google BigQuery](https://cloud.google.com/bigquery)**  
  Serverless multi-cloud data warehouse with BigLake for Iceberg/Delta querying, BI Engine caching, and native Gemini integration.

- **[Amazon Redshift](https://aws.amazon.com/redshift/)**  
  AWS data warehouse with Spectrum for lake queries, Redshift Managed Storage, and AQUA query acceleration; deep S3 and Glue Catalog integration.

- **[Starburst Galaxy](https://www.starburst.io/)**  
  Managed Trino service for cross-cloud lakehouse analytics, with Warp Speed caching and Starburst's governance layer on top of open-source Trino .

- **[ClickHouse Cloud](https://clickhouse.com/)**  
  Managed OLAP database for real-time analytics with sub-second queries on billions of rows; often paired with Iceberg/Delta for lakehouse scenarios .

- **[Dremio Cloud](https://www.dremio.com/)**  
  Open data lakehouse platform with Apache Arrow-based SQL engine, Reflections materialized views, and native Iceberg support; queries data directly on S3 .

- **[Teradata Vantage](https://www.teradata.com/)**  
  Enterprise analytics platform with VantageCloud Lake offering native object store access and query federation.

- **[Firebolt](https://www.firebolt.io/)**  
  Cloud data warehouse optimized for sub-second analytics on semi-structured data; self-hosted Core edition free forever .

- **[SingleStore](https://www.singlestore.com/)**  
  Distributed SQL database combining transactional and analytical workloads with universal storage (row + columnar).

## Open-Source GitHub Projects

- **[Apache Iceberg](https://github.com/apache/iceberg)**  
  **The industry-standard open table format** — vendor-neutral governance under Apache Software Foundation, partition evolution, hidden partitioning, multi-engine support across Spark, Flink, Trino, Snowflake, BigQuery, and DuckDB. The default choice for open, portable lakehouse architectures .

- **[Delta Lake](https://github.com/delta-io/delta)**  
  Storage layer bringing ACID transactions to Apache Spark; Linux Foundation hosted with Databricks contributing majority of development. Best when Databricks is the center of gravity; UniForm improves external read interoperability .

- **[Apache Hudi](https://github.com/apache/hudi)**  
  Streaming-first table format with native CDC support, DeltaStreamer ingestion, and mature Merge-on-Read (MoR) for high-volume upserts and deletes. Ideal for Spark-heavy mutable table workloads .

- **[Apache Paimon](https://github.com/apache/paimon)**  
  Streaming lakehouse format built for Flink-first architectures with changelog-native semantics, primary-key tables, and continuous updates. Emerging standard for Flink-centric CDC pipelines .

- **[Trino](https://github.com/trinodb/trino)**  
  **The dominant open-source distributed SQL query engine** for lakehouse analytics — federated queries across Hive, Iceberg, Delta, Hudi, RDBMS, and object storage with no data movement required .

- **[StarRocks](https://github.com/StarRocks/starrocks)**  
  Next-gen sub-second MPP database claiming 3x query performance vs alternatives; queries Iceberg, Hive, Delta, and Hudi directly without importing data. Linux Foundation project .

- **[Databend](https://github.com/datafuselabs/databend)**  
  **Open-source Snowflake alternative** written in Rust — unified analytics, vector search, full-text search, and geospatial on object storage. GPL licensed, with cloud and self-hosted options .

- **[Apache Polaris](https://github.com/apache/polaris)**  
  Vendor-neutral Iceberg REST Catalog implementation donated by Snowflake and Dremio under Apache governance. Enables multi-engine catalog interoperability without vendor lock-in .

- **[Pivot](https://github.com/pivotlake/pivot)**  
  High-performance analytics engine in Rust on open data formats (Delta Lake and Iceberg). Runs on object storage with morsel-driven parallelism and SIMD execution; queries data without replicating into a separate real-time database .

- **[kamu-cli](https://github.com/kamu-data/kamu-cli)**  
  Decentralized lakehouse and stream processing network — "Git for data" with cryptographic integrity, peer-to-peer dataset sharing, and verifiable SQL pipelines. Open Data Fabric (ODF) format inspired by Iceberg and Delta .

- **[CowsDB](https://github.com/cowsdb/cowsdb)**  
  Serverless OLAP engine with 100% ClickHouse HTTP API compatibility. Written in Rust, runs as a stateless service — useful for CI pipelines and HTTP-based analytics services .

### Additional Strong Open-Source Options

- **[Apache XTable](https://github.com/apache/incubator-xtable)** — Cross-format metadata translation between Iceberg, Delta, and Hudi without copying data.
- **[DuckLake](https://github.com/duckdb/ducklake)** — DuckDB native lakehouse format storing metadata in SQL database; achieved 90% storage reduction vs PostGIS in production tests .
- **[Apache Pinot](https://github.com/apache/pinot)** — Real-time distributed OLAP datastore for low-latency user-facing analytics at massive scale .
- **[Apache Druid](https://github.com/apache/druid)** — High-performance real-time analytics database for event-driven data.
- **[Spice AI](https://github.com/spiceai/spiceai)** — SQL query and AI inference engine with CDC, vector search, and embedded LLM gateway; migration path from Dremio .
- **[Nessie](https://github.com/projectnessie/nessie)** — Git-like version control for data lakes with Iceberg catalog branching and tagging.
- **[Project Nessie](https://github.com/projectnessie/nessie)** — Transactional catalog for Iceberg with Git-style branching for data versioning workflows .

**Frameworks for building custom systems**: Combine **Apache Iceberg** as the table format, **Apache Polaris** as the REST catalog, **Trino** or **StarRocks** as the query engine, and **MinIO** or S3-compatible storage for a fully open lakehouse stack. For streaming-first pipelines, **Apache Paimon** with **Flink** provides changelog-native semantics. For serverless analytics on smaller datasets, **DuckLake** with **DuckDB** delivers exceptional simplicity and storage efficiency .

## How to Contribute

1. Fork the repo.
2. Add/edit entries in `README.md` (follow existing format).
3. Include: name, link, 1–2 sentence description, and whether it's SaaS or open-source.
4. Submit PR with a short explanation.

Star the repo if you find it useful!

## Disclaimer

- This is a **community-curated** list — not exhaustive and not an endorsement.
- Lakehouse tools must comply with data governance regulations (GDPR, HIPAA, SOC2) and organizational data residency requirements.
- Self-hosted open-source solutions require proper security configuration, access control, and operational monitoring.
- Table format choice involves trade-offs: Iceberg prioritizes portability, Delta prioritizes Databricks integration, Hudi prioritizes streaming upserts, and Paimon prioritizes Flink-native semantics .

---

**Made for data engineers, platform architects, analytics leaders, and open-source enthusiasts.**  
Let's make lakehouse architectures more open, portable, and vendor-neutral.
