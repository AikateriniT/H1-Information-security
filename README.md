# H1-Information-security
This is the homework 1 for information security lesson

a) Bandit (solve the first 5 levels)
__________________________________________________________________________________________________________________
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

b) Bullseye. Install Debian 11-Bullseye virtual machine in VirtualBox. (See also: Karvinen 2021: Install Debian on VirtualBox)
__________________________________________________________________________________________________________________

We install Debian linux on OracleVM and then following the steps we install the WebGoat 8 on the linux. 
We open the command line and type the following commands.
Prerequisites:

          $sudo apt-get update
          $sudo apt-get -y install openjdk-11-jre ufw wget bash-completion
          $sudo ufw enable ( to enable the firewall)

To install the webgoat: 

            $ wget https://terokarvinen.com/2020/install-webgoat-web-pentest-practice-target/webgoat-server- 8.0.0.M26.jar
            $ java -jar webgoat-server-8.0.0.M26.jar

After the installation is done we open the browser and register at the website for an account. 
For the exersices we have to do : 
1. HTTP Basics.
__________________________________________________________________________________________________________________

- GET request 
- POST request

First we write our name and the server will accept the request, then reverse it and print it again. 
For the magic number we should search at the second page for the magic_num.
![Magic_num](https://user-images.githubusercontent.com/113516460/215193220-5b8a99f3-bb78-4930-90bc-822be55a424e.JPG)

2. Developer tools.
__________________________________________________________________________________________________________________
For the developer tools there is introduction about how the developer tools is working (HTML, CSS etc). For the first assignment we have to open the console and type a function that shows a random number which must be written to the empty field of the input. 
![Console](https://user-images.githubusercontent.com/113516460/215195606-2c5626c7-dee2-4b4e-a115-660d22a12ade.JPG)




Voluntary bonus:

Banditry. Solve over the wire: Bandit 5-7.

-- Level 5 --
Open a new session with same host name and port. U: bandit5 and password the one that we found. 
When we are at the home directory:

      ls -la
      cd inhere
      
      
      
      



         




