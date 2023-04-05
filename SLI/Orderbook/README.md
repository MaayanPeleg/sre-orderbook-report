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

With these we could then start to define **SLO's** and **Error budgets** as a team, where we began to discuss what we should set the SLO's to be, this became a debate within the team as if we set this high, our application will be extremely stable, but will restrict innovation and experimentation, as we will be afraid to change anything, and if we set it low, we will be able to experiment and innovate, and develop our application faster, but the application will be likley more unstable, and therefore the end user will be unhappy.


After some careful consideration within our team, we chose to be more reliable, as we are creating an application that deals with finacial transactions, than innovative. From this, we decided that we want the **SLO's** to be high, in the region of 4 nines, so that our apllication would remain reliable.

If we were within a team atually managing this application we would set actual targets, but giving a guideline is sufficient for this activity.

SlO's can also be setting improvement goals from one period to the next, For example, if we set our **SLO's** to be **100% availability**, and we are currently at **99%**, we can set an **SLO** to improve our application by 1% within a **timeframe**. The point I am trying to make is that SLO's can be used to set improvement goals, therefore the end user experience.

### Error Budgets

Based upon our **SLO's** we could then calculate our **Error budgets**. Which is the amount of downtime we can afford within a **timeframe**, calculated by 1 - **SLO**.

With an **Error budget** of 1%, for example, we can afford to have 1% **downtime** within a **timeframe**, and still be within our **Error budget**. This is important as it allows us to **experiment and innovate**, and therefore improve the application at a faster pace, making the end user happier, whist mainting and ensureing that our application is stable, and therefore **meeting our SLO's**.

### SLA's

As we do not have a client, we cannot set **SLA's** for our application, but as a guildine for setting SLO's when a client arises, we want the SLA's to have a greater **Error budget** than the SLO's, as with that the company is less likey to exceed the promised performance of our application, and nor risk facing fines.

## How we used the SLI's, SLO's and SLA's

Our SLI's informed us that our application seems to be meeting our availability SLO's, as it is consistantly 100% available, this goes for all of our path checks and the application itself.

However, we discovered that our application would not be meeting our targets for Latency within a 90 day period. The latency of both the application and the NGINX controller were too low, around (50%), there are no further metrics that can help us figure out the cause of this, Therefore we declare that an incident has occurd and investage and diagnose the root cause of this.
