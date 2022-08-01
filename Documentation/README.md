### Hosting a Full-Stack Application

## Udagram project deployment
>> After installing the required dependencies I run the frontend and backend locally and making sure that they perform the tasks correctly
I added the scripts for installation, build and deployment for bothe the backend and the frontend to automate all the steps.
I linked the project in github to circleci and added the config.yml file of the circleci containing all the orbs and jobs for running the scripts automatically.
For accessing the application: http://zayedcamp2.s3-website-us-east-1.amazonaws.com/home
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