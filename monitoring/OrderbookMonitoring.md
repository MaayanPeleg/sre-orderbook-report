# Monitoring:

## Slide 1:
### What is Monitoring:

Monitoring is used in everyday life, as well as across the technology industry.
It is used across nearly diciplines everyday from smartwatches and thermostats, but is even found in human activities like checking the time and platform for a train, or checking you have enough milk in the fridge.

## Slide 2:
### How is monitoring used in tech?

In the technology sector, monitoring is vital to collect information, which enables engineers to avoid downtime, look for trends where issues do arise, and keep uptime as high as possible.
It is also used to measure things like latency and time taken for requests to be completed, which can help to provide engineers with information related to user experience, which can be passed on to help with development.


## Slide 3:
### Monitoring within the orderbook application

In our dev environment, there is monitoring in place for multiple metrics, from a range of sources, including Prometheus and Loki.

These cover most metrics that are useful for error resolution, and can be easily interpreted by engineers to form a picture of what the current state of the application is. There are too many to go into detail for each one, but metrics like Total requests in last hour and Orderbook API CPU usage in last 10 minutes are essential, as these let engineers know how well the application is performing, and if any measures are needed to be taken to help the application with a particularly high load. 

We have other metrics built into our monitoring system which help keep track of how we are performing in terms of SLOs, and if we are on track to meet these in the current period. For example, we are keeping track of latency times, and can easily see what the latency was at any point in time, and if SLOs were met in that period. 

## Slide 4:
### Monitoring within the orderbook application - Continued
These have all been built into a dashboard in Grafana so can be easily read at a glance. Prometheus will query the information from the application hosts, and this is then fed to Grafana. Grafana then will hold the data and visualise it, allowing it to build in depth graphs, charts and visuals for engineers to work from. Grafana will also store this information, so previous events and incidents are acessible in the same way. This can enable engineers to identify long term trends, as well as compare incidents which can help reduce resolution time and prevent similar incidents in the future.

These dashboards can be further improved still, by organising metrics in terms of importance, with critical information, for example total requests in last hour at the top, and information which is less critical further down, such as deployments in last day, however these are simply quality of life upgrades that can be amended as time goes on.

I believe there are no more metrics or rules that need to be added, however the dashboards we have built in Grafana are a fluid system, so these can easily be added, changed or removed as time goes on. In the future, it may also be beneficial to build a similar system using a different platfrom, for example Zabbix, so that the data and monitoring has no single point of failure.

## Conclusion: 
From the monitoring that is in place we have been able to build a picture of how the Orderbook application should perform consistently. Using this we can spot issues and take action before they can spiral out of control, and threaten to stop the application from working entirely. This monitoring data has also helped to shape our SLOs, which Maayan will be able to talk you through now.


**Lead into MPs section on SLI/SLO**
