1. Create a new repository

   cd \repos
   git init webproject
   cd webproject

2. Create "index.html" with following contents
	<html>
	<head>
	<title>Home Page</title>
	</head>
	<body>
	</body>
	</html>
3. COmmit the changes
	git add .
	git commit -m "Home Page"

4.  List all branches
	git branch

5.  Create a new "css" branch
	git checkout -b css

6.  Go back to master branch and create "content" branch
	git checkout master
	git checkoit -b content

7.  Edit "index.html" and replace old contents with this one:
	<html>
	<head>
	<title>Home Page</title>
	</head>
	<body>
	<h1>Hello World</h1>
	</body>
	</html>

8.  Commit these changes to "content" branch
	git add .
	git commit -m "Heading added"
9.  Switch to Master branch once again and find the differences between master and content
	git checkout master
	git diff content master

10.  Go back to "css" branch 
	git checkout css
	
and replace content of  index.html with following
	<html>
	<head>
	<title>Home Page</title>
	<style>
	h1 {
	  color: darkred;
	}
	</style>
	</head>
	<body>
	</body>
	</html>


	git add .
	git commit -m "Style added"
11.	Compare all branches
	git diff master css content
12.	Go back to master branch and merge css and content into master
	git checkout master
	git merge css
	git merge content