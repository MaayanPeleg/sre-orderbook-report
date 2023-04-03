# SLI/SLO/SLA
An ***SLI*** Is the Metric behind the SLO, and the ***SLO*** is the internal team objective for a **service**, and ***SLA's*** are the promised **service** uptime and **Availability** to a customer. The SLI is the metric that is measured, the SLO is the metric that is agreed upon within the team/ company, and the SLA is the metric that is promised to the customer.

## SLI

The SLI as mentioned is the metric behind the SLO, and is measured from our application and typically displayed in a **dashboard**. 
It has a dirrect correlation to customer and user *Happiness*, And SLI's should be chosen based on that fact. For Example
 - **Availability** is the number of successful requests / total number of requests, And when a site is up and available our user is happy, so this is an appropriate SLI.
 - **Memory Usage** would be the percentage of memory being used, and when a site is using too much memory, our uiser may notice drops in ***Latency***, however this is a seperate metric, so this is not an appropriate SLI, as it does not directly correlate to our users happiness, but through another metric, therefore this can be used for diagnostics.