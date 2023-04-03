# This is a repository for our SRE report
This is what I would suggest for the structure, beggining from the flow of the activities we did of the SRE [report](https://docs.google.com/presentation/d/1-NWifK1iWYW1R6WIJ-O10OCrbUyNuTlIage0yU1Cz_g/edit?usp=sharing):
## Pipelines
> Talk about piplines first as they are the first thing we worked on
> - Talk about the different **pipelines** we have and how they work
> - Talk about how we can improve them, eg, **integration and unit tests** as this is manual **toil** that can be automated
> - Talk about how we we manually run the **promotion pipeline** and how we can **automate** this
> - Emphasize how important having included tests are and create a calculation and /or talk about ROI of having tests automated

## Environments

> We can talk about how we dont have a **test/ stage environment**, and we deploy to production after we test in dev
> - We can talk about how we can improve this by having a **test/ stage environment**
> - emphasize how want to add this whilst maintaining **simplicity** and not adding too much complexity

## Deployment

> We can talk about how we next **manually** had to to depoly to Kubernets
> - But we can idenifty that this is overhead and we cannot automate this
> - And that this is similar to a developer commiting changes to a pipeline, so this does not classify as toil
> - We had to asmually make a production release, and this is toil, we can create a pipline and or a jenkins job to automate this

## SLI/ SLO/ SLA

> Talk about how we have **SLI/ SLO/ SLA** and how we can improve them
> - Talk about the SLI's we have in our moniutoring system, and were we get them, Prometheus and Grafana
> - Talk about the SLI's we currently have, eg, **Availability** and **Latency**
> - Talk about the actual calculations behind the SLI's, eg, **Availability** is the number of successful requests / total number of requests and **Latency** is number of requests under 0.3s / total number of requests
> - Talk about how we can improve them by adding more SLI's, eg, **latency** of the actual functions within our applications to help whith dioagnosing issues
> - talk about the acctual bad latency we have, how the latency of our orderbook is less than 50%.
> - Talk to our clinet to agree on SLA's for our applications, eg, **Availability** of 99.9% and **Latency** of 95% for our orderbook
> - Agree as a **Team** on SLO's for our application

## Monitoring

> This directly ties into the SLI/ SLO/ SLA
> - Talk about how we have **monitoring** and how we can improve it
> - Talk about how we can improve it by adding more **SLI's** to our monitoring system
> - Talk about how we can improve it by adding more **alerts** to our monitoring system, what are **alerts** and why do we need them
> - Talk about how we can improve it by adding more **dashboards** to our monitoring system, what are **dashboards** and why do we need them

## incidents
>Do we currently have any protocols for **incidents**?
> - Talk about how we can improve it by having a **protocol** for **incidents**
> - Create a central location for **postmortems** and logging of **incidents** and doccumentation of **incidents**
> - create an example incident and create a runthrough of how we would handle it creating the example around the team
>    - Then create a **postmortem** and explain why we use **postmortems** and how they are useful more in future **incidents** as they explain what went wrong and ow to improve **MTTR**
>    - What is **MTTR** and why is it important