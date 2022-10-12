# Demo : Git Branching

> Tool used: either Git Bash or Command prompt or Powershell 

1. Create a new repository with working directory \repos\webproject

   ```bash
   cd \repos
   git init webproject
   cd webproject
   ```

1. Create "index.html" with following contents. 

	> Use any text editor eg. Notepad or VSCode

	> Make sure when you save the changes, file is saved in \repos\webproject directory only !

	```html
	<html>
	<head>
	<title>Home Page</title>
	</head>
	<body>
	</body>
	</html>
	```

1. Commit the changes

	```bash
	git add .
	git commit -m "Home Page"
	```

1. List all branches

	```bash
	git branch
	```

1. Create a new "css" branch

	```bash
	git checkout -b css
	```

1. Go back to master branch and create "content" branch

	```bash
	git checkout master
	git checkoit -b content
	```

1. Edit "index.html" and replace old contents with this one:

	```html
	<html>
	<head>
	<title>Home Page</title>
	</head>
	<body>
	<h1>Hello World</h1>
	</body>
	</html>
	```

1. Commit these changes to "content" branch

	```bash
	git add .
	git commit -m "Heading added"
	```

1. Switch to Master branch once again and find the differences between master and content

	```bash
	git checkout master
	git diff content master
	```

1. Go back to "css" branch 

	```bash
	git checkout css
	```
	
1. and replace content of  index.html with following
	
	```html
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
	```

	```bash
	git add .
	git commit -m "Style added"
	```

11.	Compare all branches

	```bash
	git diff master css content
	```

12.	Go back to master branch and merge css and content into master

	```bash
	git checkout master
	git merge css
	git merge content
	```