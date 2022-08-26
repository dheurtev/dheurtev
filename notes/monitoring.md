# My picks for monitoring (including logging and tracing)

Tools and packages I am using are marked `in use`.
Tools and packages I used are marked as `past`.

- [Introduction](#introduction)
- [Network monitoring](#network-monitoring)
- [Event Logging](#event-logging)
- [Ingestion and processing tools](#ingestion-and-processing-tools)
- [Databases](#databases)
- [Dashboard](#dashboard)
- [Monitoring as a service](#monitoring-as-a-service)

## Introduction ##
- [Monitoring vs. logging vs. tracing](https://www.bmc.com/blogs/monitoring-logging-tracing/)
- [Comparison](https://prometheus.io/docs/introduction/comparison/)
- [ELK stack alternatives](https://betterstack.com/community/comparisons/elk-stack-alternatives/)
- [Kubernetes monitoring tools](https://medium.com/codex/5-top-kubernetes-log-monitoring-tools-d8c0494deb30)

- **Logging** : track error reporting and related data in a centralized way. can show any discrete event within an application or system, such as a failure, and error, or a state transformation. Sysadmin oriented. High level review. Human warning.
- **Tracing**: overview to a discrete, event-triggered log, tracing encompasses a much wider, continuous view of an application. following a program’s flow and data progression. Dev oriented. Noisy. Which function, The function’s duration, Parameters passed, How deep into the function the user could get
- **Monitoring**: instrumenting an application and then collecting, aggregating, and analyzing metrics to improve your understanding of how the system behaves. primarily diagnostic – for instance, alerting developers when a system isn’t work as it should. Dev oriented. Noisy. Human warning.

## Network monitoring ##
**[`^        back to top        ^`](#)**
### Push model ###
#### Protocols ####
- [SNMP](https://en.wikipedia.org/wiki/Simple_Network_Management_Protocol): Simple Network Management Protocol (SNMP) is an IP-based application layer protocol that exchanges information between a network management solution and any SNMP-enabled device. `in use`
- [Syslog](https://en.wikipedia.org/wiki/Syslog): standard for message logging. `in use`
#### Tools ####
- [Nagios Core - Nagios](https://www.nagios.org/): free and open-source computer-software application that monitors systems, networks and infrastructure. `GPLv2` `past`
- [RRDtool (round-robin database tool)](https://oss.oetiker.ch/rrdtool/): RRDtool aims to handle time series data such as network bandwidth, temperatures or CPU load. The data is stored in a circular buffer based database, thus the system storage footprint remains constant over time. `GPLv2`
### Pull model ###
### Agents ###
- Zabbix
- [Collectd](https://collectd.org/): very popular collection agent. Unix daemon that collects, transfers and stores performance data of computers and network equipment. Used by Graphite and in Prometheus. `MIT License` and `GPLv2`
- [StatsD](https://github.com/statsd/statsd): A network daemon that runs on the Node.js platform and listens for statistics, like counters and timers, sent over UDP or TCP and sends aggregates to one or more pluggable backend services (e.g., Graphite). [Also used in Datadog](https://www.datadoghq.com/blog/statsd/). `MIT License`
### Tools ###
- [Zabbix](https://www.zabbix.com/): open-source software tool to monitor IT infrastructure such as networks, servers, virtual machines, and cloud services. Zabbix collects and displays basic metrics. Agent. `GPLv2` `past`
- [Prometheus](https://prometheus.io/): free software application used for event monitoring and alerting. It records real-time metrics in a time series database built using a HTTP pull model, with flexible queries and real-time alerting. [CNCF Graduated Project](https://www.cncf.io/projects/prometheus/).`Apache License 2.0`
  * Don't feed logs into Prometheus, use ELK
  * collect and process metrics, not an event logging system

## Event Logging ##
**[`^        back to top        ^`](#)**

### ELK Stack and OpenSearch (fork)###
#### ELK ####

[ELK](https://www.elastic.co/fr/elastic-stack/): Elasticsearch, Kibana, Beats et Logstash
  * [Beats](https://www.elastic.co/fr/beats/): Beats is a free and open platform for single-purpose data shippers. `Apache 2.0 License` 
  * [Logstash](https://www.elastic.co/fr/logstash/): free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to an Elasticsearch data warehouse. `Apache 2.0 License`
  * [Elasticsearch](https://www.elastic.co/): search engine based on the Lucene library. It provides a distributed, multitenant-capable full-text search engine with an HTTP web interface and schema-free JSON documents. `Apache 2.0 License`
  * [Kibana](https://www.elastic.co/fr/kibana/): source-available data visualization dashboard software for Elasticsearch. 

**License issue**: "(i) a dual license under the Server Side Public License, v 1 and the Elastic License 2.0 or (ii) an Apache License 2.0 compatible license or (iii) solely under the Elastic License 2.0, in each case, as noted in the applicable header." => Avoid as `⚠ Proprietary`

#### OpenSearch (fork) ####
Following the license change of ELK, the project has been forked.

[OpenSearch](https://opensearch.org/) is a community-driven, `Apache 2.0-licensed` open source search and analytics suite that makes it easy to ingest, search, visualize, and analyze data. Developers build with OpenSearch for use cases such as application search, log analytics, data observability, data ingestion, and more
  * OpenSearch: distributed search and analytics engine based on Apache Lucene.
  * OpenSearch Dashboards : default visualization tool for data in OpenSearch. It also serves as a user interface for many of the OpenSearch plugins, including security, alerting, Index State Management, SQL, and more.
  * Ingest Tools: compatible with a variety of ingestion and processing tools including beats, fluentbit and fluentd.

## Ingestion and processing tools ###
**[`^        back to top        ^`](#)**
[Fluentd](https://www.fluentd.org/): Unified logging layer. open source data collector, which lets you unify the data collection and consumption [CNCF graduated project](https://www.cncf.io/projects/fluentd/) - [Github Repo](https://github.com/fluent/fluentd) - Cross-platform `Apache 2.0 License`
- [500+ plugins](https://www.fluentd.org/plugins/all)
- [Inputs / Sources](https://www.fluentd.org/datasources) include: 
  * SNMP
  * syslog 
  * Apache / Nginx logs
  * Mobile / Webapp logs
  * Sensors / IoT (RaspberryPi)
  * MQTT (plugin)
  * UFW logs (plugin)
  * MYSQL / Postgre Slow query logs (plugin)
  * Zabbix agent (plugin)
  * SQL (plugin)
  * Twitter (plugin)
  * RSS (plugin), Feedly (plugin)
- [Outputs](https://www.fluentd.org/dataoutputs) include:
  * Log Management: Elastic Search + Kibana, Splunk, opensearch (plugin) 
  * Big Data: Hadoop, Mongodb, InfluxDB (plugin), Redis
  * Data Archiving: File, Amazon AWS S3, Azure storage (plugin), Google cloud storage (plugin)
  * Pub/Sub Queue: RabbitMQ, Kafka, nats (plugin)
  * DataWareHouse: BigQuery, MySQL, PostGresql, SQL (plugin)
  * Monitoring : Zabbix, Graphite, Statsd, Datadog, nagios (plugin), prometheus (plugin)
  * Notification : Email, Slack, Hipchat, IRC, Twilio, Jabber(plugin), Twitter (plugin) 
  * Other processor: beats (plugin)

## Databases ##
[My databases section on time series databases](databases.md#time-series)

## Dashboard ##
**[`^        back to top        ^`](#)**
- [Graphite](https://graphiteapp.org/): Monitoring tool that runs equally well on cheap hardware or Cloud infrastructure. Teams use Graphite to track the performance of their websites, applications, business services, and networked servers. Store numeric time-series data. Render graphs of this data on demand. Not a collecting agent. [Github repo](https://github.com/tmm1/graphite) `Apache License 2.0`
- [Grafana](https://grafana.com/): multi-platform open source analytics and interactive visualization web application. `AGPLv3`

## Tracing ##
[Top distributed tracing tools](https://signoz.io/blog/distributed-tracing-tools/)
[Zipkin vs. Jaeger (2019)](https://epsagon.com/observability/zipkin-or-jaeger-the-best-open-source-tools-for-distributed-tracing/)

[Jaeger](https://www.jaegertracing.io/): Monitor and troubleshoot transactions in complex distributed systems - [CNCF Graduated project](https://www.cncf.io/projects/jaeger/) - [Github repo](https://github.com/jaegertracing/jaeger) `Apache 2.0 License`

## Monitoring as a service ##
**[`^        back to top        ^`](#)**
- [Splunk](https://www.splunk.com/): log management and monitoring solution.
- [Datadog](https://www.datadoghq.com/): monitoring and analytics tool for information technology (IT) and DevOps teams that can be used to determine performance metrics as well as event monitoring for infrastructure and cloud services.