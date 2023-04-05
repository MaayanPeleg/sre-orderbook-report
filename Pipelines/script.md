# Pipeline script

-------------

## Slide 1 - What is a pipeline?

A pipeline is a series of automated steps, each step must be completed and passed through successfully before being deployed and released to production
- These steps include building, testing and deploying the code
- In order to build our pipline we use various tools - 
- So usually we first commit out changes to a source code management system, for example GitHub
- Then we use a pipeline tool, for example Jenkins, to receive these changes,
- This pipeline tool will then build the code and run the relevant tests, if these tests pass then the changes will be deployed

Benefits of Pipelines:
- Pipelines allows automated, faster and consistent releases, having a set way how to do deploy your application can signifcantly increase efficiency and allow changes to be released quickly
- It also allows bugs and erros to be caught early in development process, ensuring a more relibable application when deployed.
- Pipelines also enhance team collaboration as it can provide a standardised process for code review, testing and deployment making it easier for the team to work on problems together

------------------------------------

## Slide 2 - Pipelines within Orderbook
- Currently on the orderbook application we have two pipelines - one that creates the dev environment and one that prmotes to production.
- The initial pipeline will build our code and then publish them as docker images by using the Kaniko container
- These docker images are then pushed to the AWS ECR repository, ready to be promoted into production
- The second pipeline will define the Kubernetes pod specification, so our production environment can be set up correctly
- It then checks if the production images exist already, if it doesnt, it will promote the images add the production tags

-----------------------------

## Slide 3 - What can we improve?

Going through our pipeline there are many thins we can improve:
- Firstly our pipeline is run every 10 minutes and our container are being rebuilt even if nothing has changed 
- This can be improved and made more efficient
  - This can be done by setting up a webhook so the pipeline is run when a change is made to the source code
- Within the pipeline there is currently no testing at all - obviously this a problem as it can hinder the flow of the pipeline and stop smooth and reliable releases, defeating the whol epurpose of the pipeline
  - We can add unit testing to firstly test individual components
  - Then integration testing can be added, so the overall application can be tested before being deployed production
    -Currently we have to manually test our on our dev environment, so having automated integration tests should solve this
- Right now to promote to production we have to manually deploy the promotion pipeline
  - After doing integration tests, we can also automate this promotion to production

---------------------

## Slide 4 - SRE in Pipelines

When implementing these changes we have to take into account the SRE principles and how we can implement them into our pipelines:
- Eliminating Toil 
  - We need to integrate tests into our pipeline, other this will be done manually, which is a repetitive tasks that would be classed as toil
- Automation
  - We can automate the promoting to production pipeline
  - Our unit tests and integration tests will be automated
- Release Engineering
  - Automating the release of the application, ensuring the release on a whole is efficient and automated
- Simplicity
  - We will automate where we need to and not over complicate and over do things
 
-------------------
  
  After deployment, monitoring the application is very important, and I'll pass it over to George to speak about it.
  
