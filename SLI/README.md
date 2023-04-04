# SLI/SLO/SLA
An ***SLI*** Is the Metric behind the SLO, and the ***SLO*** is the internal team objective for a **service**, and ***SLA's*** are the promised **service** uptime and **Availability** to a customer. The SLI is the metric that is measured, the SLO is the metric that is agreed upon within the team/ company, and the SLA is the metric that is promised to the customer.

## SLI

The SLI as mentioned is the metric behind the SLO, and is measured from our application and typically displayed in a **dashboard**. 
It has a dirrect correlation to customer and user *Happiness*, And SLI's should be chosen based on that fact. For Example
> ### Good SLI:
> - **Availability** is the number of successful requests / total number of requests, And when a site is up and available our user is happy, so this is an appropriate SLI.
> ### Bad SLI:
>  - **Memory Usage** would be the percentage of memory being used, and when a site is using too much memory, our uiser may notice drops in ***Latency***, however this is a seperate metric, so this is not an appropriate SLI, as it does not directly correlate to our users happiness, but through another metric, therefore this can be used for diagnostics.

## SLO
An SLO is a Service Level Objective, and is the internal team objective for a service, and is typically displayed in a **dashboard**. SLO's cannot be decided by just upper managment and then observed by the team, as the team are the ones who work with the application on a day-to-day basis so truely understand the capabilities and targets the application can reach, *And with Devops/SRE concepts, this provides a sense of ownership and proudness of the application within the team*. Also With **SLO's** there must be a time ascociated with it, *Typically this is 90 days as an industry standard, but other time frames are not forbidden.* So for Example:
> ### Good SLO:
> - A team sitting down in a meeting with the past logs of the application and past metrics, *From the last year for example* and deciding that the application should have a **Latency** of less than 100ms ***99%*** of the time, and an **Availability** ***of 99.99% (4 nines)***, ***within 90 days***, and this is the **SLO** that the team will strive to achieve.
> ### Bad SLO:
> - Managment deciding that the application should have a **Latency** of less than 100ms ***99.99% (4 nines)*** of the time, and an **Availability** of ***99.9999% (6 nines)***, and this is the **SLO** that the team will strive to achieve, without any input from the team, and the team not understanding the capabilities of the application, and therefore not being able to achieve the **SLO**, This will in turn demotivate the team as they are provides targets that are virtually impossible, and there is no **time frame** as to when the **SLO** should be achieved, so the team will not know when to stop trying to achieve the **SLO**.

### Error Budget
SLO's leads into a concept of an **Error Budget**, which is the amount of service downtime, or unavailability, that the team is allowed to observe, which encourages **innovation and experimentation**, whilst a **"budget"** remains, within a **timeframe**. And when a **"budget"** is used up, the team must focus on **reliability and stability**, by for example not pushing out new features, but rather improving the reliability of those already implemented, and when the **budget** is replenished, by beggining a new timeframe, the team can focus on innovation and experimentation again. This is a good way to encourage innovation and experimentation, whilst still maintaining a **Reliable** service.

## SLA
An SLA in short is an agreement, or a promise, to or with a customer regarding the availability, latency or other SLI's to a customer. And this is typically displayed in a **contract**. And the SLA is the metric that is promised to the customer, and is observed and met with **fines and penalties** for the company. 
**SLA's** should be made after a meeting with the product owner and team of the application, or after the team has passed the **SLO's** decided by the team to those who will meet with the **customer**, as this allows the **SLA's** to be **Realistic, Achievable** and for te company to not be met with **Penalties**. For Example:
> ### Good SLA:
> - A company promises a customer that the application will have a **Latency** of less than 100ms ***99.99% (4 nines)*** of the time, and an **Availability** of ***99.9999% (6 nines)***, and this is the **SLA** that the company will strive to achieve.
> ### Bad SLA:
> - Creating an SLA with a customer before **SLO's** are made, or before consulting with the **team** of which work with the application day-to-day, as the application may not be able to reach **SLA** agreements, and therefore the customer will be dissapointed, and the company will be **fined and penalised**, and the **team** is ultimatley punished.