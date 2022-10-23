# mule-aws-ecs-app
Simple mule application to demonstrate the docker image deployment on AWS ECS Fargate instance. 

Build mule application from command line using below command -

`mvn clean package`

To build docker image, run below command -

`docker build . -t mule-aws-ecs-app:latest`

Run below command to deploy mule application inside docker container -

`docker run -it --rm -p 8080:8080 mule-aws-ecs-app:latest`

Once the application is deployed successfully, use below URLs to access Mule console -

http://localhost:8081/console
