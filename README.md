# ids-final-demo
This project is for duke ids final demo of our game project hosted in AWS-ECR



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

### Game Start Game

### Game Join Room

### Game Choose Group

### Game Assign Units

### Game GamePlay
