

![image](https://github.com/snbdevops/1-DevOps-Project/assets/83505877/b0e2070c-c8c6-4955-8a55-87a7b05b4a44)

![image](https://github.com/snbdevops/1-DevOps-Project/assets/83505877/5d609bdd-6334-4ef0-8523-c908d5f4cf95)

Flow -
**GIT > JENKIN > Maven(compiling, unit testing, Integration testing) > SonarQube(Static Code Analysis, Quality Gate status Check) > MAVEN BUILD > DOCKER IMAGE > Trivy(Scan the Image) > ECR > EKS**

unit testing, Integration testing, maven build will be done by shared library.

### Steps
1. Creating & setting up a Jenkins server.
Note: 1) This server will contain Jenkins as well as Sonarqube, so we will have to choose little bigger resource instance(like t2.medium)
      2) We will use docker container to host our Sonarqube setup.
Put below scripts in USERDATA while creating the EC2 and launch the instance.

a) Install Jenkins
![image](https://github.com/snbdevops/1-DevOps-Project/assets/83505877/cdc2a541-7c32-4339-a739-dbf1bd70aa38)

b) Install Docker
![image](https://github.com/snbdevops/1-DevOps-Project/assets/83505877/5ee154fa-31d7-4109-99cf-af6d122dbee5)


c) Installing Sonarqube inside docker.
![image](https://github.com/snbdevops/1-DevOps-Project/assets/83505877/a7ff94a7-83d4-4d94-8c5c-3d76a8cc807d)

USERDATA Screenshot:

![image](https://github.com/snbdevops/1-DevOps-Project/assets/83505877/a045d3f2-221f-4b9f-b5be-717bcbb72ec6)

Jekins is up and running as shown below:

![image](https://github.com/snbdevops/1-DevOps-Project/assets/83505877/c5c8a6a2-be24-45d2-84a7-95ceab132de7)

Now, when we chk docker, it will give below error -

![image](https://github.com/snbdevops/1-DevOps-Project/assets/83505877/a7ba6126-3599-434f-a0f9-d89dc7007e65)

to resolve this  we can change the permission of the file as shown below -

![image](https://github.com/snbdevops/1-DevOps-Project/assets/83505877/3c9b53da-437d-4939-ae1c-aa450d1ee3b9)

![image](https://github.com/snbdevops/1-DevOps-Project/assets/83505877/163dc4f2-cfdf-48c2-9761-9c33cf17d5bf)

**Starting sonarqube.**

![image](https://github.com/snbdevops/1-DevOps-Project/assets/83505877/55af8547-291a-4a5d-aa10-f704bfd3f419)

![image](https://github.com/snbdevops/1-DevOps-Project/assets/83505877/386d57da-4e9b-4d00-b354-c8adaae90510)

sonarqube default credentials is - admin/admin.

![image](https://github.com/snbdevops/1-DevOps-Project/assets/83505877/a5f18196-45ba-45b9-9140-5fd51efffeb4)

































