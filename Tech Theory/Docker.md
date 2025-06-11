---
created: 2025-06-11T16:38:50+05:30
modified: 2025-06-11T16:39:28+05:30
---

# Docker

This is a simple docker command file

Follow below commands to run a Spring Boot jar file on a docker container using an OpenJDK image.

1. docker pull <any Open JDK container - eclipse-temurin for eg> #get the image from docker hub for an open JDK
2. docker run -it <openJDK container name> #it stands for iterative - so, run the OpenJDK container iteratively on the docker engine.
3. docker ps #check all running containers - your openJDK should be running and copy its container ID
4. docker exec <containerID of OpenJDK> ls -a #list all the directories under the OpenJDK foler to look for a place to paste your app's JAR file physically.
5. docker exec <containerID> ls tmp #choose and view the contents of the tmp folder of OpenJDK
6. docker cp <JAR file name> <containerID>/tmp #copy your JAR (remember to navigate to the source path of the JAR file - usually the target folder inisde your maven project) to the tmp folder inside the OpenJDK container.
7. docker exec <containerID> ls tmp #check if the JAR was correctly copied
8. docker commit <Container ID> <new Image name:v1> #do not run this - it's only to see that because OpenJDK doesn't run the JAR but runs only jShell
9. docker commit --change='CMD ["java","-jar","JAR file name"]' <ContainerID> <ImageName:V2> #this will create a new version with command arguments required to run the executable JAR package of your Spring Boot app
10. docker run <Image:V2> #This is not accessible locally as docker has its own network
11. docker run -p 8080:8080 <Image:V2> # The -p ports the network to the desired port, try different ports if an error message appears saying the port you mentioned is occupied.
