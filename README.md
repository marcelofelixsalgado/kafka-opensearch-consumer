# Kafka OpenSearch

This project takes data from a local Kafka topic and send it to a OpenSearch database.

## What is OpenSearch?
OpenSearch is an open source fork of ElasticSearch. It is a scalable, flexible, and extensible open-source software suite for search, analytics, and observability applications licensed under Apache 2.0. Powered by Apache Lucene and driven by the OpenSearch Project community, OpenSearch offers a vendor-agnostic toolset you can use to build secure, high-performance, cost-efficient applications. Use OpenSearch as an end-to-end solution or connect it with your preferred open-source tools or partner projects.

## Integration flow

```
Local Kafka Topic -> Kafka Consumer -> OpenSearch database
```

## Running

1- Download and run kafka-producer-wikimedia locally:
https://github.com/marcelofelixsalgado/kafka-producer-wikimedia

2- OpenSearch startup
```
doker compose up
```

3- Check OpenSearch
```
http://127.0.0.1:9200
```

4- Run OpenSearchConsumer.java class

5- Open OpenSearch dashboard
```
http://127.0.0.1:5601
```

6- Click on "Dev tools" link

7- On the left side field, execute:

GET /wikimedia/_search?scroll=10m
{
"size": 10000
}

8- Check the results