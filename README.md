# CI-CD Pipeline with Jenkins Shared Libraries using Groovy | Advanced DevSecOps Project
This is a real time end to end CI-CD pipeline project. In this we will learn about multiple tools.
Lets understand and implement it and make a step-by-step notes of each and every steps.

Credits: Mr. DevOps Youtube Channel

We are implement this CI-CD Pipeline with Jenkins Shared Libraries. Purpose Shared Libraries is it makes the code re-usable.

### CI-CD Pipeline Project Architecture
![image](https://github.com/snbdevops/1-DevOps-Project/assets/83505877/90399cbf-206b-4769-88b6-f32240b23f80)

###Creating Jenkins Server.
As we are going to use sonarqube in this server itself so we should take a bigger resource server. Here we will be taking t2.medium(2vCPU & 4GB RAM). Also, use EBS volume of 30GB.
**Note - Here we will be installing sonarqube as a docker container.**

