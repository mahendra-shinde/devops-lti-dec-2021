Launch "local" jenkins on localhost:8080
Goto Manage Jenkins > Manage Plugins > Available
  Search & install docker-build-steps plugins
Manage Jenkins > Configure System > Docker Builder
  Docker URL: tcp://52.139.230.184:2375
Click "Test Connection"

Create new "Freestyle Project" "docker-demo1"
Git >>> https://github.com/mahendra-shinde/ci-servlet-demo
        branch : */master

Build:
  docker-command
     command: create/build image
     Build Context : $WORKSPACE
     Resulting docker image:  unlimited.azurecr.io/YOURNAME:$BUILD_NUMBER


   docker-command
     command: Push Image
	Repository: YOURNAME
	Tag : $BUILD_NUMBER
	Registry: unlimited.azurcr.io
	Registry URL: https://unlimited.azurecr.io
	
	Registry Credentials : <Add>
		Userid : unlimited
		Password: Vnosx1n8ggUe+BZ7FgKFCt5GVQrshHaM
		ID:  docker
	