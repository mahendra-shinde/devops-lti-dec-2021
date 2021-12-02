## CI/CD Orchestrator 
Take a task, identify which extension or plugin will do?
Then request the extension/plugin to do the task.
Collect the logs and update the build status.

Jenkins, Bamboo Server, TeamCity, Azure DevOps, Travis CI, ...


### Jenkins:
- Free and Open Source Tool.
- Large collection of extensions & plugins available.
- Jenkins is Language neutral (Build any code !)
- Jenkins is cloud agnostic ( Integrate with Azure, Google, AWS, IBM, Oracle ... )

Hudson CI : Parent project, still in use !


### Jenkins : System Requirement
- Build in Java, You need Java installed ( Java 11 LTS )
- Jenkins UI is Web Application listening on port "8080"
   When it running on LOCAL machine, url is "http://localhost:8080"
   When it runs on REMOTE machine, url is "http://REMOTE_SERVER:8080"
	Just replace "REMOTE_SERVER" with IP Address.

### Jenkins need to know?
- Where is JDK ?
- Where is GIT ?
- Where is Maven ?
- Where is MSBuild (.net build tool)
- Where is Python & PIP
- Where is Node & NPM 
- Where is <Add-any-other-build-tool>



## CRON TAB for Scheduling

Example:  `*/2 * * * *`

*/2	Every TWO Minutes
*	Every Hour (0-23)  
* 	Every Day of Month (1-31)
* 	Every Month  (1-12)
*	Every Weekday (0-6)

30 	5 	10 	2 *	
Minutes Hours  Date Month WeekDay

On Feb 10th at 5:30 AM

## Build Triggers

Build Periodically :  Build on certain intervals

Poll SCM:	      On Certain intervals, check with SCM (git) if a new COMMIT	
			has been introuced.
		      	YES ==> Start new build
			NO  ==> Skip	

http://jenkins-zh7axxxpznqko.southeastasia.cloudapp.azure.com:8080/


Trigger build remotely

You need 
1. JENKINS URL (Your jenkins must be accessible from internet )
2. AUTHENTICATION TOKEN 
3. JOB_NAME

The actual url to launch new build would be:
[JENKINS_URL]/job/[JOB_NAME]/build?token=[AUTH_TOKEN]

JENKINS_URL => http://jenkins-zh7axxxpznqko.southeastasia.cloudapp.azure.com:8080/
JOB_NAME    => Greetings
AUTH_TOKEN  => RUNNOW

http://jenkins-zh7axxxpznqko.southeastasia.cloudapp.azure.com:8080/job/Greetings/build?token=RUNNOW&Cause=mahendra+shinde


