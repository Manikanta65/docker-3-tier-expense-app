# Create a docker network using below command so that all the craeted communicate using same network which is bridge network

docker network create roboshop

*************************************************************************************************************************

# build the docker images from dockerfile

docker build -t frontend:1.0.0 .

**********************************************************************************************************************
# once image is created use below command to run the images

docker run -d -p 80:80 --network roboshop --name frontend frontend:1.0.0
