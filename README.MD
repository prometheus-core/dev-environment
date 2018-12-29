Anomaly Development Environment

Space for keeping all docker images or at least links and basic documentation about how to enable local dev environmet quickly.

Tool:
- Apache Hadoop (HDFS itself) - where files will be available for File streaming
- Apache Kudu - SQL like time series ready database (doesn't require hadoop, but we will discuss)
- Apache Spark - Distributed computational engine (we will use spark.ml DataFrame compatible library if possible, otherwise fallback
to older but feature rich MLlib API, or some existing solutions)
- Apache Kafka - Optional channel for streaming out prediction events out to external systems/components 
- Apache Nifi (Flow engine - CSV to CDM (Common Data Model), we can write such jobs in Spark itself, to be discussed
- Apache Livy - REST interface for Spark

Optional: We can deploy Cloudera Cluster with these components activated

TODO: Build Docker images for standalone and cluster deployments of each component and finally build single docker compose 
file to let deploy all at once (will require some networking configuration)
