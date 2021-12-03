Job : azurewebapp (or anyother name!)
Source code management:
  Git : https://github.com/mahendra-shinde/sample-aspnet
  Branch:  */main

Build:
  .NET Build Project
  .NET Publish Project
  More Options...
     Output Directory: Publish

Post Build:
  Send build artifacts over FTP
	FTP Server: azure-webapp
    Transfer fileset: 
	Source: Publish/**    (** refers to files and sub-directories)

	Remove Prefix : Publish/

Continuous Integration & Deployment

Source Repo ---> Building --> Deploying Azure App Service

Modify certain files in Source repo, the build and deploy should get triggered.

Goto https://github.com/mahendra-shinde/sample-aspnet and create a "FORK"


Modify your jenkins job:
 1. Build Triggers, use Poll SCM with Schedule "*/1 * * * *"
 2. Change the GIT Repo to https://github.com/YOURNAME/sample-aspnet
	Replace YOURNAME with your github-id
 3. Build Environment, use "Delete Workspace before build starts"
 4. Post Build, "send build artifacts over FTP" use "Advanced" and check "Clean Remote"
 5. Save the configuration.

Goto https://github.com/YOURNAME/sample-aspnet and edit this file
  Views/Shared/_Layout.cshtml 
  Line #6 Replace " Sample ASP.NET Website" with your name
  Line #14 Replace the Sample WebSite to My Sample Website

Goto Azure portal and stop the app service