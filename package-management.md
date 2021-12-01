DevOps What & Why?
Workflows:
  Continuous Integration and Continuous Delivery & Deployment

Jenkins CI/CD 
Bamboo Server
Azure DevOps (TFS)
Travis CI
GitHub Actions

=============================
Version Control System			GIT, TFVC, SVN
CI / CD Orchestrator			
Package management tool			NPM, NuGET, PIP, Maven
Static Code Analysis			SonarQube
Unit Testing				JUNit, TestNG, VSTest
System Testing, UI Testing, .... 	
Deployment tools			

-------------------------------------------
Package Management

1. Download the package and all it's dependencies.
2. All the downloads should be verified. File Finger-prints "checksums" 
3. Resolves the conflicts
	Lib-A depends on lib-b-version1.0 and Lib-X depends on lib-b-version2.0
	Solution 1: Use only latest version of lib-b-version2.0
	Solution 2: Use both versions of "lib-b"


CI Pipeline:

get source 
download / install dependencies
build app 
run unit tests
scan the code for quality

