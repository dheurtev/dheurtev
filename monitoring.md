# My picks for monitoring

Tools and packages I am using are marked `in use`.
Tools and packages I used are marked as `past`.

- [Introduction](#introduction)
- [Basic Monitoring](#basic-monitoring)
- [Event monitoring, Agent and metrics (ELK Stack and alternatives)](#event-monitoring-agent-and-metrics)
- [Event Logging - Dashboard](#event-logging---dashboard)
- [Monitoring as a service](#monitoring-as-a-service)

## Introduction ##
- [Comparison](https://prometheus.io/docs/introduction/comparison/)
- [ELK stack alternatives](https://betterstack.com/community/comparisons/elk-stack-alternatives/)
- [Kubernetes monitoring tools](https://medium.com/codex/5-top-kubernetes-log-monitoring-tools-d8c0494deb30)

## Basic Monitoring ##
**[`^        back to top        ^`](#)**
- [SNMP](https://en.wikipedia.org/wiki/Simple_Network_Management_Protocol): Simple Network Management Protocol (SNMP) is an IP-based application layer protocol that exchanges information between a network management solution and any SNMP-enabled device. `in use`
- [Syslog](https://en.wikipedia.org/wiki/Syslog): standard for message logging. `in use`
- [Nagios Core - Nagios](https://www.nagios.org/): free and open-source computer-software application that monitors systems, networks and infrastructure. `GPLv2` `past`
- [RRDtool (round-robin database tool)](https://oss.oetiker.ch/rrdtool/): RRDtool aims to handle time series data such as network bandwidth, temperatures or CPU load. The data is stored in a circular buffer based database, thus the system storage footprint remains constant over time. `GPLv2`

## Event monitoring, Agent and metrics ##
**[`^        back to top        ^`](#)**
- [Jabbix](https://www.zabbix.com/): open-source software tool to monitor IT infrastructure such as networks, servers, virtual machines, and cloud services. Zabbix collects and displays basic metrics. Agent. `GPLv2` `past`
- [Collectd](https://collectd.org/): very popular collection agent. Unix daemon that collects, transfers and stores performance data of computers and network equipment. Used by Graphite and in Prometheus. `MIT License` and `GPLv2`
- [StatsD](https://github.com/statsd/statsd): A network daemon that runs on the Node.js platform and listens for statistics, like counters and timers, sent over UDP or TCP and sends aggregates to one or more pluggable backend services (e.g., Graphite). [Also used in Datadog](https://www.datadoghq.com/blog/statsd/). `MIT License`
- [Prometheus](https://prometheus.io/): free software application used for event monitoring and alerting. It records real-time metrics in a time series database built using a HTTP pull model, with flexible queries and real-time alerting. `Apache License 2.0`

### ELK Stack ###
- [ELK](https://www.elastic.co/fr/elastic-stack/): Elasticsearch, Kibana, Beats et Logstash
  * [Beats](https://www.elastic.co/fr/beats/): Beats is a free and open platform for single-purpose data shippers. `Apache 2.0 License` 
  * [Logstash](https://www.elastic.co/fr/logstash/): free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to an Elasticsearch data warehouse. `Apache 2.0 License`
  * [Elasticsearch](https://www.elastic.co/): search engine based on the Lucene library. It provides a distributed, multitenant-capable full-text search engine with an HTTP web interface and schema-free JSON documents. `Apache 2.0 License`
  * [Kibana](https://www.elastic.co/fr/kibana/): source-available data visualization dashboard software for Elasticsearch. 
**License**: "(i) a dual license under the Server Side Public License, v 1 and the Elastic License 2.0 or (ii) an Apache License 2.0 compatible license or (iii) solely under the Elastic License 2.0, in each case, as noted in the applicable header." => Avoid as `⚠ Proprietary`

Fork : 
- [OpenSearch](https://opensearch.org/) is a community-driven, `Apache 2.0-licensed` open source search and analytics suite that makes it easy to ingest, search, visualize, and analyze data. Developers build with OpenSearch for use cases such as application search, log analytics, data observability, data ingestion, and more
  * OpenSearch: distributed search and analytics engine based on Apache Lucene.
  * OpenSearch Dashboards : default visualization tool for data in OpenSearch. It also serves as a user interface for many of the OpenSearch plugins, including security, alerting, Index State Management, SQL, and more.
  * Ingest Tools: compatible with a variety of ingestion and processing tools including beats, fluentbit and fluentd.

## Event Logging - Dashboard ##
**[`^        back to top        ^`](#)**
- [Graphite](https://graphiteapp.org/): Monitoring tool that runs equally well on cheap hardware or Cloud infrastructure. Teams use Graphite to track the performance of their websites, applications, business services, and networked servers. Store numeric time-series data. Render graphs of this data on demand. Not a collecting agent. [Github repo](https://github.com/tmm1/graphite) `Apache License 2.0`
- [InfluxDB](https://www.influxdata.com/): open-source time series database. `MIT License`
- [Grafana](https://grafana.com/): multi-platform open source analytics and interactive visualization web application. `AGPLv3`

## Monitoring as a service ##
**[`^        back to top        ^`](#)**
- [Splunk](https://www.splunk.com/): log management and monitoring solution.
- [Datadog](https://www.datadoghq.com/): monitoring and analytics tool for information technology (IT) and DevOps teams that can be used to determine performance metrics as well as event monitoring for infrastructure and cloud services.
