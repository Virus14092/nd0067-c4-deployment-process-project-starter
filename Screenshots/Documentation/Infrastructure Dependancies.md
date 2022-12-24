# Infrastructure Dependencies for Deploying on AWS:

### RDS :

A database with DB identifier postgres was created by RDS and with the username and password given in the environmental variables file, the RDS database instance is running and I used the link and put it in the sequelize function.

### Elastic Beanstalk:

First I installed AWS CLI and EB CLI so that I can write commands on the terminal, I started with `eb init` that made me enter the desired environment and app name and the platform which was Node Js 14, I used nvm and downgraded my node and npm to match the package.json file, then I made a new environment using `eb create`, before that I made sure that the app was build and ready for production, in the build folder I used the command `eb use udagramapi-env` to use this environment for finally the `eb deploy` command and you can see the screenshot of the health ok and the working server on the chrome with the elastic beanstalk link.

### S3 Buckets

There were 2 buckets available, one that was made automatically when I deployed the api to elastic beanstalk and the other one I made and uploaded the frontend build and made sure to make the index.html is window for our deploy, you can find the screenshot of the link provided by s3 bucket.

### Circle Ci:

The config Yaml file in the circle ci folder has workflows to build and deploy the application with chronological order.
