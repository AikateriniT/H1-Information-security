# H1-Information-security
This is the homework 1 for information security lesson

a) Bandit (solve the first 5 levels)

-- Level 0 -- 
For the first exersice I worked with Putty SSH. Host name was bandit.labs.overthewire.org on port 2220. Use as u: bandit0 and p:bandit0.
Hint: When we write the password for the server it never shows. 
To get the password for the level 1 : 

      ls -la (list  -list all)
      To get the names of all the files in the directory listed.

In order to read the readme file:

      cat readme 
      And it writes the password written in the file readme.

-- Level 1 -- 
For the level 1 we use the command Ctrl + d to disconnect and we open a new session with the same host name and port. U: bandit1 and for password we use the password we found. From the notepad we had pasted the password we copy it and paste it by right clicking.

      ls -la 
      To list the names of the files.
The file has a "-" as a name so we must use 

      cat < -
In order to read the file. And the password is written there. 

      Ctrl + d
      
-- Level 2 --
Open a new session with same host name and port. U: bandit2 and password the one that we found. 

      ls -la
From the list we can see that the file with name "spaces in this filename" exists, and in order to read it we press "cat sp + Tab"

      cat spaces\ in\ this\ filename
And the password is written there. 

      Ctrl + d

-- Level 3 -- 
Open a new session with same host name and port. U: bandit3 and password the one that we found. 

      ls -la
      With the l"a" we are asking to get the names of all the files and directories even the hidden ones. The hidden names are marked with blue color. We can see that the blue "inhere" directory exists and then we use the:
      cd inhere ( change directory inhere)
      ls - la - To get list of files in this hidden directory.
      cat .hidden 
And the password is written there. 

-- Level 4 -- 
Open a new session with same host name and port. U: bandit4 and password the one that we found. 
When we are at the home directory:

      ls -la
      cd inhere
      ls -la
We start searching which is the correct file, and since there are files which are not human-redable they mess up the SSH and we need to reset. The password is found in the 8th file. 

Ctrl + d



