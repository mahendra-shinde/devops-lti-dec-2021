# Jenkins Setup
Download the jenkins https://get.jenkins.io/war-stable/2.303.3/jenkins.war

Verify java version
java -version
cd downloads
java -jar jenkins.war

Jenkins log should now display the one time secret
Copy the password 
Visit "http://localhost:8080" using web browser.
And it should ask you for "InitialAdminPassword"
Paste password here

Now, click "Install Suggested Plugins"