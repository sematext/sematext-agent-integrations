This directory contains the Sematext metrics definition YAMLs for Elastic Cloud

Refer to [Monitoring Elasticsearch](https://sematext.com/docs/integration/elasticsearch/) for an overview of 
Elasticsearch monitoring integration. Go to [https://apps.sematext.com/ui/howto/Elasticsearch/overview](https://apps.sematext.com/ui/howto/Elasticsearch/overview) for instructions to install & set up Sematext Agent to monitor Elasticsearch.

Learn more:
* [Elasticsearch Monitoring Guide](https://sematext.com/blog/elasticsearch-guide/)
* [Top 10 Elasticsearch Metrics To Monitor](https://sematext.com/blog/top-10-elasticsearch-metrics-to-watch/)
* [Open Source Monitoring Tools for Monitoring Elasticsearch](https://sematext.com/blog/elasticsearch-open-source-monitoring-tools/)
* [Monitoring Elasticsearch With Sematext](https://sematext.com/blog/monitoring-elasticsearch-with-sematext/)
* [eBook: Elasticsearch Monitoring - The Complete Guide](https://sematext.com/resources/elasticsearch-monitoring-ebook/)

Troubleshooting:

On large clusters, you can fetch metrics less often and give the agent more heap by putting this in the properties file:
```
# defaults to 10s
SPM_MONITOR_COLLECT_INTERVAL=60000
# replace the existing JAVA_DEFAULTS value
JAVA_DEFAULTS="-Xmx2g -Xms2g -XX:+ExitOnOutOfMemoryError -XX:+AlwaysPreTouch -XX:+UseG1GC -XX:GCTimeRatio=2 -Xss512k"
```
