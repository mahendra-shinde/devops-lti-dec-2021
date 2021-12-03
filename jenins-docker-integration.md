IT Admin (Infra)
   Configuring Jenkins, Installation Plugins
   Managing credentials
   Integrating jenkins with cloud environment

Job Creation should be handled by Developers
   Each job is different.
	Java Developer should create JOB for building & deploying java application
	.net developer should create JOB for building & deploying .net application

-------------------------------
Containers & Docker 
Developers should create / write source code 
And, Should create "Dockerfile"

Building Container Images using Jenkins
+ You must have DOCKER installed on Jenkins machine.
+ Install "docker-build-step" plugin

Jenkins "System Configuration" then "Docker Builder" > "Docker URL
Docker for Unix/Linux/Mac ::> unix:///var/run/docker.sock
Docker for Windows        ::> tcp://127.0.0.1:2375