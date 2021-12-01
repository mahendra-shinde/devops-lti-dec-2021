## Git Merge Conflict

Merge conflict occurs when both parent branch and child brach have NEW COMMITs that are trying to change the same line in code.

What can I do?

Open the file with conflict and delete the unwanted code while keeping the one you want!

## Demo
1. Lets create a new repository with HTML page

    cd \repos
    git init project3
    cd project3
    notepad index.html

2. Contents of index.html

    ```html
    <html>
    <head>
    <style>
    h1 {
    color: darkred;
    }
    </style>
    </head>
    <body>
    <h1>Hello World</h1>
    </body>
    </html>
    ```

3.  Now Save the file and make a new commit

    git add .
    git commit -m "Home page"

4.  Create a new branch

    git checkout -b dev

5.  Edit the index.html `notepad index.html`

    ```html
    <html>
    <head>
    <title>MySite : Home Page</title>
    <style>
    h1 {
    color: darkred;
    }
    </style>
    </head>
    <body>
    <h1>Hello WOrld</h1>
    </body>
    </html>
    ```

6.  Make a new commit

    git add .
    git commit -m "Title Added"

7.  Go back to master branch to add another title.

    git checkout master

    Modify the index.html

    ```html
    <html>
    <head>
    <title>MySite : Welcome </title>
    <style>
    h1 {
    color: darkred;
    }
    </style>
    </head>
    <body>
    <h1>Hello WOrld</h1>
    </body>
    </html>
    ```

8.  Make a new commit and then view differences

    git add .
    git commit -m "Title Updated"
    git diff dev master

9.  Try the merge (which should fail)

    git checkout master
    git merge dev

10. Open the index.html and make this changes:

    ```html
    <html>
    <head>
    <title>MySite : Welcome Page</title>
    <style>
    h1 {
    color: darkred;
    }
    </style>
    </head>
    <body>
    <h1>Hello WOrld</h1>
    </body>
    </html>
    ```

11. Now make a commit to fix the merge

    git add .
    git commit -m "Merge Fixed"
    git log --oneline --graph
