## Typical GIT Usage:

1. Developer edit few files.
2. Developer then add files to an INDEX
	git add <file>	## Add single file
	git add *.html	## Add HTML files
	git add .       ## Add ALL files & Subdirectories
	git add *	## Add ALL files but not subdirectories
3. Once ready, create new commit
	git commit -m "The Message"

4. Now check history ??
	git checkout master
	git log

5. Compare the changes in TWO commit
   
Use git log command to get commit history, copy FIRST FOUR chars for two commit
 git diff <COMMIT1> <COMMIT2>

## Git Commit (ROOT) Explained:
[master (root-commit) 11f6d9c] Added a html file
 --+--- ----+-------  --+----  ------+----------
   |        |           |            +------------- Commit Message
   |        |           +-------------------------- Unqiue Commit ID (First 7 chars)
   |        +-------------------------------------- First COMMIT is called "ROOT"
   +----------------------------------------------- Default branch

 1 file changed, 1 insertion(+)
 -----+-------- ------+--------
      |               +------------------ The number of lines CHANGED
      +---------------------------------- The number of FILES CHANGED
 create mode 100644 file2.html ---------- Creating a new ENTRY in LOCAL REPO
		              100644 is NORMAL file which is R/W Permissions	

## Git Commit History

commit 11f6d9c797363c86279b6a347475a269929b93cf (HEAD -> master)
--+--- ---------+------------------------------  -----+---------
  |             |				      +------------ You are on MASTER
  |             +---------------------------------------------- FULL COMMIT ID (GUID)
  +------------------------------------------------------------ Commit !
Author: Mahendra Shinde <MahendraShinde@synergetics-india.com>
        ---------+--------------------------------------------
                 +----- Picked from Git Config Global user.name & user.email

Date:   Wed Dec 1 10:24:29 2021 +0530	====> Date/Time when COMMIT command run !

    Added a html file			====> Commit message