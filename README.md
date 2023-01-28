# H1-Information-security
This is the homework 1 for information security lesson
________________________________________________________________________________________________
x) Read and summarize. (This subtask x does not require tests with a computer. Some bullets per article is enough for your summary)
- Hutchins et al 2011: Intelligence-Driven Computer Network Defense Informed by Analysis of Adversary Campaigns and Intrusion Kill Chains, chapters Abstract, 
3.2 Intrusion Kill Chain and 
3.3 Courses of Action
- Karvinen 2020: Command Line Basics Revisited
________________________________________________________________________________________________

2. Related work 

Here are described other phase based models for the defensive and countermeasure strategies. 
- United States Department of Defence Joint Staff describes a kill chain as:
find, fix, target, engage, and assess (U.S. Department of Defence,2007)
- Similar phase based models have been used for antiterrorism planning, the U.S. Army describes the terrorist planning cycle as a seven step process that works as a base to assess the terrorist organizations. 
- Phase-based approaches to cybercrime, insider threats and countermeasure strategies are essential for CND against APT actors. One such approach is the Attack-Based Sequential Analysis of Countermeasures (ABSAC) which aligns types of countermeasures along the time phase of an attack. The ABSAC approach includes more reactive post-compromise countermeasures rather than early detection capability to uncover persistent adversaries.

3. Intelligence-driven Computer Network Defense

- Intelligence-driven computer network defense is a risk management strategy that addresses the threat component of risk, incorporating analysis of adversaries, their capabilities, objectives, doctrine and limitations.


3.1 Indicators and the Indicator Life Cycle
- The fundamental element of the intelligence in this model is the indicator. 
- Indicator is any piece of information that objectivelly describes an intrusion. There are three types of indicators:
      - Atomic indicators, are those which can not be broken down to smaller parts like IP addresses, email addresses and vulnerability identifiers. 
      - Computed indicators, are derived from data involved in an incident, like hash values and regular expressions. 
      - Behavioral indicators,  are collections of computed and atomic indicators. 
- This cycle of actions, and the corresponding indicator states, form the indicator life cycle:
      - Report -> Revealed -> Leverage -> Mature -> Discover -> Utilized -> Analyze ->
__________________________________________________________________________________________________________________
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
__________________________________________________________________________________________________________________
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

Then for the final task 6 we must clear all the network requests and then press the GO! button so that we can easily check which is the right one. From the file we can easily read the random number written there. 
![developer tools](https://user-images.githubusercontent.com/113516460/215217979-37439730-f8f3-445a-869d-e04c3c33a03a.JPG)

________________________________________________________________________________________________________________________
Voluntary bonus:

Banditry. Solve over the wire: Bandit 5-7.
________________________________________________________________________________________________________________________
-- Level 5 --

Open a new session with same host name and port. U: bandit5 and password the one that we found. 
When we are at the home directory:

      ls -la
      cd inhere
      find /home/bandit5/inhere -type f -size 1033c 
And it writes the exact file which meets the requirements we asked it for. 

      cd maybehere07
      cat .file2
And we get the password. 

-- Level 6 --

Open a new session with same host name and port. U: bandit6 and password the one that we found. 
When we are at the home directory since the password is hidden somewhere in the server we will search the entire server and set the requirments. 
So:

      find / -type f -size 33c -user bandit7 -group bandit6 2>/dev/null
we search the entire server for a file which is 33bytes owned by user bandit7 (which can be replaced by the numerical 11007) and owned by group bandit 6 ( 11006). with the 2>/dev/null we are asking it to drop the files we dont have access to a blackhole so that our terminal is not full of errors. 

The search returns one result which we open it and the password is there. 

-- Level 7 -- 

Open a new session with same host name and port. U: bandit7 and password the one that we found. 
When we are at the home directory since the password is hidden in the data.txt file we will use the grep.
So:

      grep 'millionth' data.txt
And the password is printed there. 
____________________________________________________________________________________________

o) Voluntary bonus: My fundaments. What do you consider the fundamentals of security? What would you teach the first day?
____________________________________________________________________________________________

      
      



      


      
      
      
      
      



         




