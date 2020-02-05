Microservice Udagram App
Udagram is a simple cloud application developed alongside the Udacity Cloud Engineering Nanodegree. It allows users to register and log into a web client, post photos to the feed, and process photos using an image filtering microservice.

Tasks
Setup Docker Environment
You'll need to install docker https://docs.docker.com/install/. 
Open a new terminal within the project directory and run:

Switch the folder: cd udacity-c3-deployment/docker
Build the images: docker-compose -f docker-compose-build.yaml build --parallel
Push the images: docker-compose -f docker-compose-build.yaml push
Run the container: docker-compose up

Setup k8s Environment
Create the cluster: eksctl create cluster --name udagram
Create travis-user: eksctl create iamidentitymapping --name udagram --role arn:aws:iam::?:role/travis_eks --group system:masters --username travis_eks
Run the ci/cd-pipeline