# Logging App

Good Articles
- [Reference : Centralized Logging Architecture](http://jasonwilder.com/blog/2013/07/16/centralized-logging-architecture/)

The main aspects you will need to address are: collection, transport, storage, and analysis. In some special cases, you may also want to have an alerting capability as well.

|stages -> | collection | transport | storage | analysis |  alerting | 
| --- | --- | --- | --- | --- |  --- | 
||  |Scribe, nsq and Kafka, require clients to log data via their API. Logstash, Heka, fluentd and Flume provide a number of input sources but also support natively tailing files and transporting them reliably. These are a better fit for more general log collection. While rsyslog and Syslog-ng are typically thought of as the defacto log collector, not all applications use syslog.| transport | Storing Logs depends on: how long, volume, how you need to access | analysis |
|| collection | transport | storage | analysis |  alerting | 
