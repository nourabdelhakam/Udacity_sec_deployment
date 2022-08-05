### Hosting a Full-Stack Application

## Infrastructure:
>>>  Services (from AWS Cloud)

> RDS - Database Host: database-1.cxxuxsnvwohp.us-east-1.rds.amazonaws.com

> RDS - Database Port: 3010

> RDS - Database Name: udagram

> S3 Endpoint - Frontend: http://zayedcamp2.s3-website-us-east-1.amazonaws.com/
- for accessing please make sure It may not work because it is being blocked because of "cors policy"

> Elastic Beanstalk URL - Backend: http://zayedcamp5-env.eba-v3igzbbm.us-east-1.elasticbeanstalk.com/

>>> CircleCi
>> jobs :
> Setting Env Variables.
> Install NodeJS.
> Checkout Code & Cloning the Repo.
> Install AWS CLI v2.
> Configure AWS AccessKeyID.
> Configure AWS Region.
--> Frontend:
> Install dependencies.
> Build angular.
> Deploy the site to AWS S3.
--> Backend:
> Install dependencies.
> Change The main entry point in package.json.
> Transpile the typescript/ build the app.
> Install AWS Elastic Beanstalk CLI.
> Deploy the app to AWS Elastic Beanstalk.

## App dependencies: 
>> The dependencies required to run the project :

--> Frontend:
> Node 14.15.0
> npm 6.14.8 (LTS)
> Angular 8.2.14
> core-js 2.5.4
> rxjs 6.5.4
> Zone.js ~0.9.1
--> Backend:
> bcryptjs 2.4.3
> body-parser 1.18.3
> cors 2.8.5
> dotenv 8.2.0
> email-validator 2.0.4
> express 4.16.4
> jsonwebtoken 8.5.1
> pg 8.7.1
> reflect-metadata 0.1.13
> sequelize 5.21.4

## Pipeline process: 

>> After installing the required dependencies I run the frontend and backend locally and making sure that they perform the tasks correctly
I added the scripts for installation, build and deployment for bothe the backend and the frontend to automate all the steps.
I linked the project in github to circleci and added the config.yml file of the circleci containing all the orbs and jobs for running the scripts automatically.
## Pipeline process
# Continuous integration:
>> First I added all the commands needed for installing and building the application in the package.json files in the frontend and the backend then called these scripts inside the package.json file of the main application.
>> I added the jobs inside circleci yml file for installing all the dependencies on both the frontend and backend of the application using the : npm install command inside package.json files.
>> Then I added the jobs for building the frontend and the backend by calling the corresponding scripts.
# Continuous Deployment:
>> First I added all the commands needed deploying the application in the package.json files in the frontend and the backend then called these scripts inside the package.json file of the main application.
>> I added the Elastic Beanstalk and aws in the circleci orbs for setting them up and installing them for the deployment.
>> I added the jobs inside circleci yml file for deploying the frontend and the backend just by calling the deploy scripts added to the main package.json file which correspondingly calls the deploy commands added to the package.json file of both the frontend and the backend.
>> I linked my github application to the circleci so the pipeline automatically run after every application update.



>>> All the screenshots for the EB and S3 and DB and circleci are added .
I also added the diagram showing the architecture and another diagram showing the pipeline relationships and the communication between the different services.