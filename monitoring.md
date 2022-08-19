# My picks for monitoring

Technologies I use, I have used or consider using.

-[Comparison](https://prometheus.io/docs/introduction/comparison/)
- [Kubernetes monitoring tools](https://medium.com/codex/5-top-kubernetes-log-monitoring-tools-d8c0494deb30)

## Basic Monitoring ##
- [SNMP](https://en.wikipedia.org/wiki/Simple_Network_Management_Protocol): Simple Network Management Protocol (SNMP) is an IP-based application layer protocol that exchanges information between a network management solution and any SNMP-enabled device. [using]
- [Nagios Core - Nagios](https://www.nagios.org/): free and open-source computer-software application that monitors systems, networks and infrastructure. GPLv2 [considering]

## Event monitoring, Agent and metrics ##
- [Jabbix](https://www.zabbix.com/): open-source software tool to monitor IT infrastructure such as networks, servers, virtual machines, and cloud services. Zabbix collects and displays basic metrics. Agent. GPLv2. [used]
- [Collectd](https://collectd.org/): very popular collection agent. Unix daemon that collects, transfers and stores performance data of computers and network equipment. Used by Graphite and in Prometheus. MIT License & GNU General Public License, version 2. [considering]
- [StatsD](https://github.com/statsd/statsd): A network daemon that runs on the Node.js platform and listens for statistics, like counters and timers, sent over UDP or TCP and sends aggregates to one or more pluggable backend services (e.g., Graphite). [Also used in Datadog](https://www.datadoghq.com/blog/statsd/). [considering]
- [Prometheus](https://prometheus.io/): free software application used for event monitoring and alerting. It records real-time metrics in a time series database built using a HTTP pull model, with flexible queries and real-time alerting. Apache License 2.0 [considering]

## Event Logging - Dashboard ##
- [Graphite](https://graphiteapp.org/): Monitoring tool that runs equally well on cheap hardware or Cloud infrastructure. Teams use Graphite to track the performance of their websites, applications, business services, and networked servers. Store numeric time-series data. Render graphs of this data on demand. Not a collecting agent [considering]
- [InfluxDB](https://www.influxdata.com/): open-source time series database. MIT Licensed
- [Grafana](https://grafana.com/): multi-platform open source analytics and interactive visualization web application. GNU Affero General Public License, version 3.0 [Considering]

## Monitoring as a service ##
- [Splunk](https://www.splunk.com/): log management and monitoring solution [considering]
- [Datadog](https://www.datadoghq.com/): monitoring and analytics tool for information technology (IT) and DevOps teams that can be used to determine performance metrics as well as event monitoring for infrastructure and cloud services. [considering]
