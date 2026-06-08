# Create a docker network using below command so that all the craeted communicate using same network which is bridge network

docker network create roboshop

*******************************************************************************************************************************
# Build the docker images from dockerfile

docker build -t backend:1.0.0 .

*******************************************************************************************************************************

# Once image is created use below command to run the images

docker run -d -p 8080:8080 --name node-app --network roboshop -e DB_HOST="mysql" backend:1.0.0
