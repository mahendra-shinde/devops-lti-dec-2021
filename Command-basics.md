cd : Change a Directory
cd <directory-name>

Windows ===> C:\A\B\C
Unix    ===> /A/B/C

C:\   is ROOT of filesystem
  COMMAND to go back to ROOT of filesystem:
	Windows cd \
	Unix    cd /

 Switch to "C"
	Windows cd \A\B\C
	Unix    cd /A/B/C

 What if you are inside directory "A"
	Windows cd B\C
	Unix    cd B/C

 What if you are inside directory "B"
	Windows/Unix  cd C

Path /A/B/C are called Absolute path
Path B/C or C are called Relative Path

   cd project1 # Result ERROR : there is no "project1" inside current directory
   cd /repos/projects 

Verify contents of current directory:
   dir

Check your current directory:
   pwd (Poweshell / Bash )
