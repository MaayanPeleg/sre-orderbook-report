# SLI's, SLO's and SLA's Within Our orderbook Application
When we were first given the application, there were no **SLI's** or **SLO's**, We had to create these through our activities, and even come up with some within our team. Within the activities, and through our learning, we discovered that **SLI's** are dirrectly correlated to **user satisfaction**, and therefore we need to identify the metrics to use as **SLI's** and a bassis for our **SLO's** and **Error budgets**.
### SLI's
Through the activities we identfied the following **SLI's**:
- **Availability of buy Requests Thorugh */buy* path** - The number of successful requests (status 200) / total number of requests
- **Latency of buy Requests Thorugh */buy* path** - The number of requests under 0.3s / total number of requests
- **Availability of sell Requests Thorugh */sell* path** - The number of successful requests (status 200) / total number of requests
- **Latency of sell Requests Thorugh */sell* path** - The number of requests under 0.3s / total number of requests
- **Availability of NGINX Controller** - The number of successful requests (status 200) / total number of requests
- **Latency of orderbooks history page** - The number of requests under 0.3s / total number of requests

All of which were displayed through grafana using prometheus as the data source. 
### SLO's

With these we could then start to set **SLO's** and **Error budgets** as a team, so we sat down in a meeting scenario and we decided to set our **SLO's** to be:
- X
- Y
- Z

### SLA's

Next I Decided to have a meeting with a client of the application, and we discussed the **SLI's** and **SLO's** and how they would affect the client, and we decided to set the **SLA's** to be:
- X
- Y
- Z

We wanted the SLA's to have a greater **Error budget** than the SLO's, as with that the client would be more willing to accept a greater downtime, and then we could experiment and innovate more, and therefore improve the application at a faster pace, making the end user happier.

## How we used the SLI's, SLO's and SLA's
From the SLI's and SLO's created, we discovered that our application would not be meeting our targets for Latency within a 90 day period. The latency of both the application and the NGINX controller were too low, around (50%), there are no further metrics that can help us figure out the cause of this, Therefore we declare that an incident has occurd and investage and diagnose the root cause of this.