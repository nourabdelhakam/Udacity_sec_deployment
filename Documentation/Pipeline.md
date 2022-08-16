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