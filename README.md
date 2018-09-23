# Sematext Agent Integrations
Sematext Agent integrations are built, contributed, and maintained by both the community and Sematext.  Like its integrations the [Sematext Agent](https://github.com/sematext/sematext-agent-java) is open-source as well.

# Data Sources
Sematext Agent supports collecting data from the following sources.
* JMX
* SQL databases
* REST APIs

Support for additional data sources can be contributed to the [Sematext Agent repo](https://github.com/sematext/sematext-agent-java).

# Data Outputs
Sematext Agent uses Influx Line Protocol to ship the collected metrics via HTTPS.  Thus, the collected data can be sent to [Sematext Cloud](https://sematext.com/cloud) (or [Sematext Enterprise](https://sematext.com/enterprise)), or your own InfluxDB.

# Contributing
Adding a new integration that collects data from one of the available sources is easy and involves no coding.  To add a new integration only a set of configuration (YML) files is needed.  These config files specify the data source, as well as individual metrics to collect.  For more information see [Adding New Sematext Agent Integrations](CONTRIBUTING.md).

# Documentation
Each integration has its own README.  More documentation is available in [Sematext integrations docs](https://sematext.com/docs/integration).
