# Big Data with BigQuery
- **BigQuery** is a fully managed data warehouse.
- A **data warehouse** is a large store, containing terabytes and petabytes of data gathered from a wide range of sources within an organization, that's used to guide management decisions.
- A **data lake** is just a pool of raw, unorganized, and unclassified data, which has no specified purpose.
- A **data warehouse** on the other hand, contains structured and organized data, which can be used for advanced querying.
- Being fully managed means that **BigQuery** takes care of the underlying infrastructure, so you can focus on using SQL queries to answer business questions–without worrying about deployment, scalability, and security.

## BigQuery Features
- **BigQuery** provides two services in one: **storage** plus **analytics**.
- It’s a place to store petabytes of data. For reference, 1 petabyte is equivalent to 11,000 movies at 4k quality.
- BigQuery is also a place to analyze data, with built-in features like machine learning, geospatial analysis, and business intelligence.
- BigQuery is a fully managed serverless solution, meaning that you don’t need to worry about provisioning any resources or
managing servers in the backend but only focus on using SQL queries to answer your organization's questions in the frontend.
- BigQuery has a flexible pay-as-you-go pricing model where you pay for the number of bytes of data your query processes and for any permanent table storage.
- If you prefer to have a fixed bill every month, you can also subscribe to flat-rate pricing where you have a reserved amount of resources for use.
- Data in BigQuery is encrypted at rest by default without any action required from a customer.
- By encryption at rest, we mean encryption used to protect data that is stored on a disk, including solid-state drives, or backup media.
- BigQuery has built-in machine learning features so you can write ML models directly in BigQuery using SQL.
- Also, if you decide to use other professional tools—such as Vertex AI from Google Cloud—to train your ML models, you can export datasets from BigQuery directly into Vertex AI for a seamless integration across the data-to-AI lifecycle.

## What does a typical data warehouse solution architecture look like?
Diagram comes here
- The input data can be either real-time or batch data.
- If it's streaming data, which can be either structured or unstructured, high speed, and large volume, Pub/Sub is needed to digest the data.
- If it’s batch data, it can be directly uploaded to Cloud Storage.
- After that, both pipelines lead to Dataflow to process the data.
- That’s the place we ETL – extract, transform, and load – the data if needed.
- BigQuery sits in the middle to link data processes using Dataflow and data access through analytics, AI, and ML tools.
- The job of the analytics engine of BigQuery at the end of a data pipeline is to ingest all the processed data after ETL, store and analyze it, and possibly output it for further use such as data visualization and machine learning.
- BigQuery outputs usually feed into two buckets: business intelligence tools and AI/ML tools.
- If you’re a business analyst or data analyst, you can connect to visualization tools like Looker, Looker Studio, Tableau, or other BI tools.
- If you prefer to work in spreadsheets, you can query both small or large BigQuery datasets directly from Google Sheets and even perform common operations like pivot tables.
- Alternatively if you’re a data scientist or machine learning engineer, you can directly call the data from BigQuery through AutoML or Workbench.
- These AI/ML tools are part of Vertex AI, Google's unified ML platform.
- BigQuery is like a common staging area for data analytics workloads.
- When your data is there, business analysts, BI developers, data scientists, and machine learning engineers can be granted access to your data for their own insights.

## BigQuery Services- Storage and Analytics
- BigQuery provides two services in one.
- It’s both a fully managed storage facility to load and store datasets, and also a fast SQL-based analytical engine.
- The two services are connected by Google's high-speed internal network.
- It’s this super-fast network that allows BigQuery to scale both storage and compute independently, based on demand.

### Storage
Let’s take a look at how BigQuery manages the storage and metadata for datasets.
- BigQuery can ingest datasets from a variety of different sources, including internal data, which is data saved directly in BigQuery, external data, multi-cloud data, and public datasets.
- After the data is stored in BigQuery, it’s fully managed by BigQuery and is automatically replicated, backed up, and set up to autoscale.
- BigQuery also offers the option to query external data sources–like data stored in other Google Cloud storage services like Cloud Storage, or in other Google Cloud database services like Spanner or Cloud SQL–and bypass BigQuery managed storage.
- That means a raw CSV file in Cloud Storage or a Google Sheet can be used to write a query without being ingested by BigQuery first.
- One thing to note here: inconsistency might result from saving and processing data separately.
- To avoid that risk, consider using Dataflow to build a streaming data pipeline into BigQuery.
- In addition to internal/native and external data sources, BigQuery can also ingest data from: Multi-cloud data, which is data stored in multiple cloud services, such as AWS or Azure.
- If you don't have data of your own, you can analyze any of the datasets available in the public dataset marketplace.
#### Basic patterns to load data into BigQuery.
- The first is a batch load, where source data is loaded into a BigQuery table in a single batch operation.
- This can be a one-time operation or it can be automated to occur on a schedule.
- A batch load operation can create a new table or append data into an existing table.
- The second is streaming, where smaller batches of data are streamed continuously so that the data is available for querying in near-real time.
- And the third is generated data, where SQL statements are used to insert rows into an existing table or to write the results of a query to a table.

### Analytics
Of course, the purpose of BigQuery is not just to save data; it’s for analyzing data and helping to make business decisions.
- BigQuery is optimized for running analytic queries over large datasets.
- It can perform queries on terabytes of data in seconds and on petabytes in minutes.
- This performance lets you analyze large datasets efficiently and get insights in near real time.
- Let’s look at the analytics features that are available in BigQuery.
- BigQuery supports: Ad hoc analysis using Standard SQL, the BigQuery SQL dialect.
- Geospatial analytics using geography data types and Standard SQL geography functions.
- Building machine learning models using BigQuery ML.
- Building rich, interactive business intelligence dashboards using BigQuery BI Engine.
- By default, BigQuery runs interactive queries, which means that the queries are executed as needed.
- BigQuery also offers batch queries, where each query is queued on your behalf and the query starts when idle resources are available, usually within a few minutes.
