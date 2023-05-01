# ids-final-demo
This project is for duke ids final demo of our game project hosted in AWS-ECR. This is a Harry-Potter themed 4-player game that allow each player to assign "students" to different territories in Hogwarts, then move / attack to different territories. Players take on the role of Hogwarts houses (colors), commanding armies to conquer territories while engaging in battles and strategic maneuvers using unique abilities and spells.

We deployed the server in AWS-ECR, and players could connect to the server by downloading the client software and run from local. Each game can hold 2-4 players, and they identify each other by a unique Room ID.

Please enjoy the advanture in HP magic world!


## Architectural Diagram
![Architecture](https://github.com/yikai-Liu/ids-final-demo/blob/master/AWS.jpg)


## How to Run the Game
1. Start up the server in the docker

docker pull public.ecr.aws/r9c5u1t7/finalproj

docker run -d --name citest-651 -p 1651:1651 -p 4321:4321 -t public.ecr.aws/r9c5u1t7/finalproj ./gradlew run-server

2. git clone our project to your folder and run

./gradlew run-client

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

### Game GamePlay
