# Cloud-Computing-Docker-container-build
An attempt to create a docker container to deploy and run a sample web application

1. Install Docker on the system
2. Go to create a folder on system named Docker-testing. Create a Dockerfile with the name Dockerfile (exact name with no extension). Command line is better suited for this purpose. Tu run, download the file shared here with the same name.
3. Create your web application in the same folder. For web application, the web app given in this repo can also be used i.e. mywebapp.html. The below is a screenshot of mywebapp.html. It is a web based Calculator.

![image](https://user-images.githubusercontent.com/67788727/131698909-7d5ba3df-688a-41d2-ac59-a92ca14d5696.png)

5. The details of OS creation and supported specifications needs to be mentioned in the dockerfile so as to create docker image for docker containers.
6. To create docker image, the command to be run on command line is- docker build _pfilename_with_athname_ (here give- docker build ./sampleimage)
7. Cross check if docker image has been created or not by giving the command- docker images. A list should appear with at least your docker image's name as listed.
8. Now docker image is created. We need to create docker container from this image. Hence, run the command

	docker run -p 80:80 sampleimage:v1
	
	here, since we have nginx installed, it would act as server with port 80 to run the web app locally and display the calculator. v1 here is the nametag and sampleimage is the image name of docker.
	
	Now run the web app in the container just created. It can also be run through host machine with the localhost mentioning the port number and web app name.
	
	e.g.     http://localhost/mywebapp.html
