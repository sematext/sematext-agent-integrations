This directory contains the Sematext metrics definition YAMLs for Apache Solr & SolrCloud. 

Refer to [Monitoring Apache Solr](https://sematext.com/docs/integration/solr/) for an overview of 
Apache Solr monitoring integration. Go to [https://apps.sematext.com/ui/howto/Solr/overview](https://apps.sematext.com/ui/howto/MySQL/overview) for instructions to install & set up Sematext Agent to monitor Apache Solr.

Refer to [Monitoring Apache SolrCloud](https://sematext.com/docs/integration/solrcloud/) for an overview of 
Apache Solr monitoring integration. Go to [https://apps.sematext.com/ui/howto/SolrCloud/overview](https://apps.sematext.com/ui/howto/SolrCloud/overview) for instructions to install & set up Sematext Agent to monitor Apache Solr.

## Solr 10

Solr 10 has no JMX metrics, so the `json-*-solr10*.yml` files read `/solr/admin/metrics` in Prometheus format and
`/solr/admin/info/system` for the version and mode. The agent finds Solr's HTTP endpoint on its own, from the system
properties of Solr's JVM (`solr.port.listen`, `solr.host.bind`, and `--module=https` for TLS), over the same JMX
connection it uses for JVM metrics.

Set these in the monitor properties file only when needed:

- `ST_MONITOR_SOLR_NODE_HOSTPORT`: Solr's endpoint without the `/solr` path, e.g. `https://solr-1:8984`. Needed when the agent can't reach
  Solr's JVM over JMX, or Solr is behind a proxy.
- `ST_MONITOR_SOLR_NODE_BASICAUTH_USERNAME` and `ST_MONITOR_SOLR_NODE_BASICAUTH_PASSWORD`: when Solr requires basic
  authentication.

Learn more:
- [eBook: Solr Monitoring - The Complete Guide](https://sematext.com/resources/solr-monitoring-ebook/)
- [Solr Monitoring with Sematext](https://sematext.com/blog/solr-monitoring-made-easy-with-sematext/)
- [Key Solr Metrics to Monitor](https://sematext.com/blog/solr-key-metrics-to-monitor/)
- [Open Source Monitoring Tools for Monitoring Solr](https://sematext.com/blog/solr-open-source-monitoring-tools/)
