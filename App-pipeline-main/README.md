# Project Description

Dockerize a full application Spring boot Angular with SQL and orchestrate it with kubernetes and using sonarqube for vurnebililities and code analysis
## Table of Contents

- [Dockerizing the application](#about)
- [Set up a CI/CD pipeline](#features)
- [Orchestration](#technologies)
- [Sonarqube](#getting-started)
- [Technologies](#technologies)


## Dockerizing the application

I have used docker-compose file that will :
- Create image for my backend and sql app
- Create image for my frontend app
Docker compose will create both images based on dockerfile in backend and frontend folders and it will setup database configuration and run 3 containers:backend ,frontend and sql
  

## Set up a CI/CD pipeline

I have created webhook between jenkins and my github repository that will triigeer my commits and start build my app based on Jenkinsfile instructions:
- Check some versions and do some analysis
- Create containers for my app
- Connect to my docker hub and push images

## Orchestration

I have used Kubernetes to orchestrate my containers because docker-compose work only locally:
- Create service and deploy files for backend
- Create service and deploy files for sql
I have used images already deployed in the CI/CD pipeline then setup a configuration to connect with sql and expose my application

## Sonarqube

I integrate sonarqube in my CI/CD pipeline for code analysis and vulnerabilities 
I pull its official image then add step in Jenkinsfile

## Technologies

List the major technologies, frameworks, and tools used in this project:
- App: Angular / Spring Boot .
- Database:  SQL 
- DevOps: Docker, Kubernetes, CI/CD tools, Jenkins,Sonarqube.



