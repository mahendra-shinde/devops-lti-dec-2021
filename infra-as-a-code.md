## Infrastructure management
==> terraform  works with ANY Cloud providers 
	
	You create a configuration file
		define all the infra resources 
		define their dependence 
		Deploy them
	You can "delete" the deployment

==============================================================>
You are BUILDING a front-end, to TEST your front-end you need a MOCK back-end
and a database.
Now, challenge is:
  You need mock backend and database in "dev" , "qa" , "staging" environments.

Workflow (CD)
Get the artifact BUILD BY CI workflow
Dev/QA/Staging
 deploy the server env (prepared by infra automation like terraform)
 Run all tests
 delete the server env
--------------
On premise servers : no scalability
  Reusability:  Whenever project1 is built, use available resource to create the Dev/QA/Staging env, and once complete, delete the env.
     		project2 can re-use the resources later!

On Cloud:
  Azure / AWS/ Google
  Minimize Cost in CD workflow by deleting resources when NOT in use.

---------------------------
1. Infrastructure As A Code (IaaC)
      Create a document that "describes" and "defines" your infrastructure 
	Later use a tool (eg terraform) to create / manage the environment.
	
      Iaac treat your infrastructure as piece of code, which can be used to 
	create or destroy environment on demand.


2. Change Management (Desired State configuration)
	You define what packages to be installed, what configuration to be used
  	inside the individual servers.
	You can CHANGE that definition any time and apply it on all servers.
	Example: Ansible, Chef or Puppet

	It requires the environment to be already set.

