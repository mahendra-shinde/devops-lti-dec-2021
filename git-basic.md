# Demo: Git Basics

1. Create a new repo inside `C:\repos` with Name `project2`

   ```bash
   cd \repos\ 	         ###Windows
   cd ~/repos/          ###Mac
   git init project2
   cd project2
   ```

1. Create a new file `App.java` inside project2

   ```bash
   notepad App.java  
   ## You can use code / vim / nano editor instead !
   ```

1. Add few lines of text inside "App.java" using notepad (or text editor you chose earlier)

1. Save the changes

1. Using Git ADD command add this file to INDEX
   
   ```bash
   git add App.java
   ```

1. Create Another file `Config.java` inside project2 

   ```bash
   notepad Config.java
   ```

1. Using Notepad add few lines inside `Config.java`
   Click YES to Create file and add few lines then save & close. 

1. Commit both changes using message `Created App and Config`
   
   ```bash
   git commit -m "Created App and Config"
   ```

1. View the commit history
   
   ```bash
   git log
   ```