# SLI/SLO/SLA
An ***SLI*** Is the Metric behind the SLO, and the ***SLO*** is the internal team objective for a **Service**, and ***SLA's*** are the promised **Service** uptime and **Availability** to a customer.

## SLI

The SLI as mentioned is the metric behind the SLO, and is measured from our application and typically displayed in a **dashboard**. 
It has a dirrect correlation to customer and user *Happiness* and *Satisfaction*, And SLI's should be chosen based on that fact. For Example
> ### Good SLI:
> - **Availability** is the number of successful requests / total number of requests, And when a site is up and available our user is happy, there is a direct relationship between availability and user satisfaction, so this is an appropriate SLI.
> ### Bad SLI:
>  - **Memory Usage** would be the percentage of memory being used, and when a site is using too much memory, our uiser may notice drops in ***Latency***, however this is a seperate metric, so this is not an appropriate SLI, as it does not directly correlate to our users happiness, but through another metric, therefore this can be used for diagnostics.

## SLO
An SLO is a Service Level Objective, and is the internal team objective for a service, and is typically displayed in a **dashboard**. SLO's cannot be decided by just upper managment and then observed by the team, as the team are the ones who work with the application on a day-to-day basis so truely understand the capabilities and targets the application can reach. Also With **SLO's** there must be a time ascociated with it, *Typically this is 90 days as an industry standard, but other time frames are not forbidden.*

### Error Budget
SLO's leads into a concept of an **Error Budget**, which is the amount of service downtime, or unavailability, that the team is allowed to observe, which encourages **innovation and experimentation**, whilst a **"budget"** remains, within a **timeframe**. And when a **"budget"** is used up, the team must focus on **reliability and stability**, by for example not pushing out new features, but rather improving the reliability of those already implemented, and when the **budget** is replenished, by beggining a new timeframe, the team can focus on innovation and experimentation again. This is a good way to encourage innovation and experimentation, whilst still maintaining a **Reliable** service.

## High vs Low SLO's
Within a team, a decision arises when it comes to deciding the **SLO's** for the application, and this decision is whether to set **High** or **Low** **SLO's**. And this decision is based on the **teams** lean towards availability or innovation.
### High SLO's
High **SLO's** are typically set by teams who lean towards **Availability** and **Reliability**, and those who want to ensure the application remains available as much as possible, and value reliabiliry over innovation.

### Low SLO's
Low **SLO's** are typically set by teams who lean towards **Innovation** and **Experimentation**, and those who want the application to develop faster and iclude experimental features, and are willing to sacrifice **Availability** for **Innovation**.

The choice a team decides is up to them, and is based on the teams **culture** and **values**, or maybe even influenced by the **Customer** or **Managment**
> ### Good SLO:
> - A team sitting down in a meeting with the past logs of the application and past metrics, *From the last year for example* and deciding that the application should have a **Latency** of less than 100ms ***99%*** of the time, and an **Availability** ***of 99.99% (4 nines)***, ***within 90 days***, and this is the **SLO** that the team will strive to achieve.
> ### Bad SLO:
> - Managment deciding that the application should have a **Latency** of less than 100ms ***99.99% (4 nines)*** of the time, and an **Availability** of ***99.9999% (6 nines)***, and this is the **SLO** that the team will strive to achieve, without any input from the team, and the team not understanding the capabilities of the application, and therefore not being able to achieve the **SLO**, This will in turn demotivate the team as they are provides targets that are virtually impossible, and there is no **time frame** as to when the **SLO** should be achieved, so the team will not know when to stop trying to achieve the **SLO**.


## SLA
An SLA in short is an agreement, or a promise, to or with a customer regarding the availability, latency or other SLI's to a customer. And this is typically outlined in a **contract**. And is observed and met with **fines and penalties** for the company, if not met. 
**SLA's** should be made after a meeting with the product owner and team of the application, or after the team has passed the **SLO's** decided to those who will meet with the **customer**, as this allows the **SLA's** to be **Realistic, Achievable** and for te company to not be met with **Penalties**.
