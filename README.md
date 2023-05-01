# ids-final-demo
This project is for duke ids final demo of our game project hosted in AWS-ECR. We really wanted to build a game, so we used Java instead of Python. The project involved creating a customized Docker container from a version of Java to deploy a Harry Potter themed game. The container image was pushed to AWS ECR and players could connect to the game using a client software from their local machines. The game allows 2-4 players to assign "students" to different territories in Hogwarts and engage in battles using unique abilities and spells. 

We deployed the server in AWS-ECR, and players could connect to the server by downloading the client software and run from local. Each game can hold 2-4 players, and they identify each other by a unique Room ID.


## Project Goal
```
Project: Docker and Kubernetes Container Project
Many cloud solutions involve Docker format containers. Let’s leverage Docker format containers in the following project:

Create a customized Docker container from the current version of Python that deploys a Python ML application.

Push the image to DockerHub, Amazon ECR, Google Container Registry, or some other Cloud Container Registry.

Pull the image down and run it on a cloud platform cloud shell: Google Cloud Shell or AWS Cloud9.

Deploy an application to a cloud-managed Kubernetes cluster, like GKE (Google Kubernetes Engine), or EKS (Elastic Kubernetes Service), etc.

```


## Architectural Diagram
![Architecture](https://github.com/yikai-Liu/ids-final-demo/blob/master/AWS.jpg)


## How to Run the Game
1. Start up the server in the docker

`docker pull public.ecr.aws/r9c5u1t7/finalproj`

`docker run -d --name citest-651 -p 1651:1651 -p 4321:4321 -t public.ecr.aws/r9c5u1t7/finalproj ./gradlew run-server`

2. git clone our project to your folder and run

`./gradlew run-client`

## Game Server in AWS ECR
Steps
1. Create a public ECR repo
![ECR Repo](https://github.com/yikai-Liu/ids-final-demo/blob/master/ECR_createRepo.png)
2. Clone our project to AWS Cloud9 and follow the ECR push commands
![ECR Push](https://github.com/yikai-Liu/ids-final-demo/blob/master/ECR_push.png)

## Game Logic 
### Game Login
![Login](https://github.com/yikai-Liu/ids-final-demo/blob/master/login.png)

### Game Start Game
![start game](https://github.com/yikai-Liu/ids-final-demo/blob/master/startGame.png)

### Game Join Room
![join room](https://github.com/yikai-Liu/ids-final-demo/blob/master/joinRoom.png)

### Game Choose Group
![Choose Group](https://github.com/yikai-Liu/ids-final-demo/blob/master/waitingRoom.png)

### Game Assign Units
![Choose Group](https://github.com/yikai-Liu/ids-final-demo/blob/master/AssignUnits.png)

### Game GamePlay
![Choose Group](https://github.com/yikai-Liu/ids-final-demo/blob/master/GamePlay.png)
