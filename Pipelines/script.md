Pipeline script

Slide 1 - What is a pipeline?

A pipeline is a series of automated steps, each step must be completed and passed through before being deployed and released to production
These steps include building, testing and deploying the code
This is done by using various tools in order to build our pipeline - 
- So usually we first commit out changes to a source code management system
- Then we use a pipeline tool to receive these changes, there a number of tools we can use for this, some of them are:
  - Jenkins - a popular open source automation server that can be used for pipelines
  - Gitlab CI/CD - web based way to simply create and manage pipelines
  - CircleCi - a cloud based platform used for pipelines
 and there are many other tools that can be used.
- This pipeline tool will then build the code and run the tests, if these tests pass then the changes will be deployed

Benefits of Pipelines:
- Pipelines allows automated, faster and consistent releases, having a set way how to do deploy your application can signifcantly increase efficiency and allow changes to be released quickly
- It also allows bugs and erros to be caught early in development process, ensuring a more relibable application when deployed.
- Pipelines also enhance team collaboration as it can provide a standardised process for code review, testing and deployment making it easier for the team to work on problems together

Slide 2 - Pipelines within Orderbook
- Currently on the orderbook application we have to pipelines - one that creates the dev environment and one that prmotes to production.
- The initial pipeline will build our code and then publish them as docker images by using the Kaniko container
- These docker images are then pushed to the AWS ECR repository, ready to be promoted into production
- The second pipeline will define the Kubernetes pod specification, so our production environment can be set up correctly
- It then checks if the production images exist already, if it doesnt, it will promote the images add the production tags

Slide 3 - What can we improve?

Going through our pipeline there are many thins we can improve:
- Firstly 
