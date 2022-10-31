# README
Final project
DFE Cloud Specialism-Final Project

Student Enrolment Application






Contents
Introduction	2
Technical Detail of App	2
Infrastructure	2
Azure Infrastructure	3
Infrastructure Diagram	3
Applications/Frameworks & Libraries	3
Languages, Scripting & Commands	4
Methodology	5
CI/CD Stack	6
Crud	7
App Design…………………………………………………………………………………………………………………………………….8
Risk-Assessment……………………………………………………………………………………………………………………….9-11
Testing……………………………………………………………………………………………………………………………………12-13
Summary…………………………………………………………………………………………………………………………………….14
Improvements……………………………………………………………………………………………………………………………15




Introduction
The aim of the project is to develop and deploy a student enrolment application. The purpose of the application is to help students to enrol on courses and then once assigned the student can select classes they wish to attend. 
I will demonstrate using a variety of methodologies, technologies & tools for the Project that all serve a unique purpose and work in synergy to deliver a functioning application. 

Technical Detail of App
The application will be a web facing application, it will use Crud (create, read, update and delete) functionality for the user to get requests and responses from the backend and DB. The Flask micro-framework was used for this project and all the information was stored in a MYSQL database which comprised of a minimum of two tables sharing a one-to many relationship. This structure is shown in the diagram below:
 
 ![image](https://user-images.githubusercontent.com/111758676/199000233-eb5db325-04aa-4516-878c-1a9c5740de25.png)


Azure will host Linux which will sit on a VM, the VM will host Docker and Jenkins and receive code commits from GitHub, bash will be used to command Azure and the Linux OS.
Docker Swarm will be deployed for load balancing.  
A docker container will hold the Flask APP which will be accessible by users via public facing IP/URL (HTTP)
 
![image](https://user-images.githubusercontent.com/111758676/199000362-b9fb42f3-e44a-4ec4-a077-c0eae124253d.png)

Infrastructure

Appliction
![image](https://user-images.githubusercontent.com/111758676/199003960-196dbcdc-297e-437c-99d6-220e64ce47b3.png)


Environment	Description	Purpose
Microsoft Azure	Cloud computing environment that often services scenarios of IaaS & PaaS	Azure will be hosting the Virtual Machines that will host the application and provide the network connectivity & functionality 
Linux	Host Operating System	The docker Swam will sit on 3 Linux hosts
Docker	OS virtualisation that delivers containers for applications	The application will exist inside the docker containers. Docker swarm will demonstrate load balancing for the application platform
SQL Database	Database	This will hold all the data for the applications. Details like student, teachers and courses

Environment	Description	Purpose
Microsoft Azure	Cloud computing environment that often services scenarios of IaaS & PaaS	Azure will be hosting the Virtual Machines that will host the application and provide the network connectivity & functionality 
Linux	Host Operating System	The docker Swam will sit on 3 Linux hosts
Docker	OS virtualisation that delivers containers for applications	The application will exist inside the docker containers. Docker swarm will demonstrate load balancing for the application platform
SQL Database	Database	This will hold all the data for the applications. Details like student, teachers and courses

Azure Infrastructure
Microsoft Azure is a cloud hosting environment. For this project I will be running VMs, and Databases on MS Azure and I will be following the IaaS model for hosting my application. 
 ![image](https://user-images.githubusercontent.com/111758676/199000826-8ad49425-5a32-4df3-b840-96c408f39d0f.png)


	Infrastructure Diagram
  Linux (OS)
![image](https://user-images.githubusercontent.com/111758676/199000889-e672ebfa-7d5d-41dc-bf2c-50ebf8ee6499.png)

 
Applications/Frameworks & Libraries 
Application	Description	Purpose
SQL Workbench	Database design tool	I will be using SQL Workbench to design my database structure and write SQL
Flask	Flask is a python web framework	I will be using python in flask to build up my webapp. This will mainly cover the front end.
GitHub	GitHub is used to host coding and track changes and version. It’s also collaborative	I will be using Git to do commits and pull requests for my code. GitHub repositories will host my code and versions of my code
JIRA	JIRA is used as ticketing system, change control, knowledge base and bug tracking	I will use Jira to function inside the agile project management framework. 
Jenkins	Jenkin offers a simple way to set up continuous integration/continuous delivery. It offers automation to software development	Jenkins will play an important role in my development process. It enables me to quickly test code changes on my app using CI/CD pipeline. Jenkins will integrate with GitHub and my infrastructure and application layer. Changes committed to GitHub will reflect on my test environments and development environments
Pytest	Pytest is a software test framework.	I will be using pytest alongside pycharm when writing my python code. Pytest will play a role in my testing process.
Pycharm	Pycharm is a python IDE which provides a range of tools for python development	Pycharm will be the main place where I will write my python code for my app. Pycharm will also allow me to connect to github
SQLAlchemy	SQLAlchemy is an open-source SQL toolkit and object-relational mapper for the Python programming language	SQL Alchemy will help my app written in python work with sql for storing and recalling data and carrying out queries against the databases


Languages, Scripting & Commands
Language	Description	Purpose
SQL	Structured Query Language (SQL) is a standardized programming language that is used to manage relational databases and perform various operations on the data in them.	I will use SQL to query my databases and the tables in my databases
Python	Python is a high-level programming language	I will be using Python 3.11 to develop my application. Python will be used to develop the functionality of my app
Bash	Bash is a command-line interface shell program used extensively in Linux	I will be using Bash to command and manage azure CLI/ Azure Cloud shell as well as my virtual machine which will host Linux.
Git	Git is a DevOps tool used for source code management. It is a free and open-source version control system used to handle small to very large projects efficiently.	Git commands will be used to manage versions of my source code.
HTML/CSS/JS – FRONT END	All used for front end development. HTML will make the webpage up while CSS will be responsible for styling and looks. Js will be used for dynamically updating content	All three will be used for the front end of my application. The HTML code will sit in my templates folder in my flask environment. The HTML file will link to the python file (typically the header). CRUD will be the method for the transport mechanism from front end to back end

Methodology
Methodology	Description	Purpose
CI/CD	A continuous integration and continuous deployment (CI/CD) pipeline is a series of steps that must be performed in order to deliver a new version of software. CI/CD pipelines are a practice focused on improving software delivery throughout the software development life cycle via automation	I will be using CI/CD pipeline managed by Jenkins through GitHub to commit change and test.
CRUD	CRUD refers to the four basic operations a software application should be able to perform – Create, Read, Update, and Delete.

In such apps, users must be able to create data, have access to the data in the UI by reading the data, update or edit the data, and delete the data.

In full-fledged applications, CRUD apps consist of 3 parts: an API (or server), a database, and a user interface (UI).
	I will use a CRUD app to link my front-end environment to backend and database.

The API contains the code and methods, the database stores and helps the user retrieve the information, while the user interface helps users interact with the app. The user will make a HTTP request through the web browser will work with my CRUD app.



Agile Scrum	Agile scrum methodology is a sprint-based project management system with the goal of delivering the highest value to stakeholders.	SCRUM would be the methodology I use in a team working environment. I would use techniques like sprints and stand-up meetings to help deliver complex projects with multiple teams involved.

CI/CD Stack

This project required the implementation of several stages of a CI Pipeline. These were project tracking, version control, development environment and build server.
Git was used for version control, with the project repository hosted on GitHub. Version control via git allows changes to the project to be made and committed whilst keeping the commit history for access to earlier versions. GitHub as a repository hosting service permits the repository to be stored away from the development environment, as well as providing webhooks, which send http POST requests to the build server to automate building and testing.
The development environment used was a python3 virtual environment (venv) hosted on a virtual machine. Python is used as Flask is a python-based framework. A venv allows pip installs to be performed and the app to be run without affecting any conflicting pip installs on the same machine.
Jenkins was used as a build server, providing automation of building and testing. This automation is accomplished by setting up a freestyle project which executes the test.sh script when it receives a webhook from GitHub upon pushing a commit. Jenkins is also used to run the app via gunicorn once testing is complete. The diagram below describes the CI/CD Pipeline.
 
So, I will be writing code in python from my local machine, from here I will update my repositories, then through webhooks Jenkins will pull code & run test & build. The images will be sent to docker which will have the testing and live environments.
 


Crud
Crud will operate as a function in my application, it will get the data from the api url. 
 

APP Design

I have chosen to build an application which allows users once completed the enrolment process are able to view the options to select what course they would like to enrol into which will include availability of an advisor to assist them in selecting the suitable course for them. The ERD for this MVP is shown below which shows a one-to-many relationship.

 

The goal for future iterations of this project will be to add categorisation of questions by topic via a quizzes table, and to make results specific to specific quizzes. For example, a quiz about each course and questions based on student’s experiences.

Risk Assessment
Prior to building the app, a risk assessment was undertaken to identify risks and propose measures to control these risks. These measures could then be implemented in the app. The diagram below shows the initial risk assessment:


 

Some of the control measures implemented in the project as a result of the risk assessment are as follows:
•	User profiles were not applied, as this would demand sending some form of authentication over unsecured HTTP connection.
•	SQL Alchemy was applied with Flask to prevent SQL commands being sent directly to the database.
•	Credentials stored as secret texts on Jenkins VM and exported as environment variables to prevent accidentally publishing confidential details.
Brief risk description: -
Confidentiality Risks
•	Supplier looking at sensitive data
•	Disclosure of data by the provider
•	Disclosure of internal system data
Integrity Risks
•	Manipulation of transferred data
•	Data manipulation at provider side
•	Accidental modification of transferred data
•	Accidental data modification at provider side
•	Data modification in internal systems
Availability Risks
•	Discontinuity of the service
•	Unintentional downtime
•	Attacks against availability
•	Loss of data access
•	Data loss at provider side
•	Insufficient availability of internal systems
Performance Risks
•	Network performance problems
•	Limited scalability
•	Deliberate underperformance
•	Performance issues of internal system
Accountability Risks
•	Identity theft
•	Insufficient user separation
•	Insufficient logging of actions
•	Access without authorisation
•	Missing logging of actions in internal systems
Maintainability Risks
•	Limited customisation possibilities
•	Incompatible business processes
•	Incompatible with new technologies
•	Limited data import
•	Proprietary technologies
•	Insufficient maintenance
•	Unfavourably timed updates 

The diagram below demonstrates the different types of risk assessments that may well be conducted.



 

Testing


 

Testing is a continuous and automated process that enables continuous and faster delivery of software. Testing spans every stage of the software development lifecycle. In this project we merged the code to a central repository on GitHub. This meant that the code updated continuously through continuous integration (CI). To prevent the risk of errors, we had to continuously test the code through different types of tests, the one we used for this project was unit test. Unit tests were written for create, read, update and delete functionality. These tests are automated using Jenkins via webhooks. A successful build, in which only one test passed, is shown below:

Started by user admin
Obtained Jenkinsfile from git https://github.com/Nazmeena/final-project.git
[Pipeline] Start of Pipeline
[Pipeline] node
Running on Jenkins in /home/jenkins/.jenkins/workspace/final-project-inital
[Pipeline] {
[Pipeline] stage
[Pipeline] { (Declarative: Checkout SCM)
[Pipeline] checkout
Selected Git installation does not exist. Using Default
The recommended git tool is: NONE
No credentials specified
 > git rev-parse --resolve-git-dir /home/jenkins/.jenkins/workspace/final-project-inital/.git # timeout=10
Fetching changes from the remote Git repository
 > git config remote.origin.url https://github.com/Nazmeena/final-project.git # timeout=10
Fetching upstream changes from https://github.com/Nazmeena/final-project.git
 > git --version # timeout=10
 > git --version # 'git version 2.34.1'
 > git fetch --tags --force --progress -- https://github.com/Nazmeena/final-project.git +refs/heads/*:refs/remotes/origin/* # timeout=10
 > git rev-parse refs/remotes/origin/main^{commit} # timeout=10
Checking out Revision dc8f8e386889d8c98ffa489585f66eff6ff00339 (refs/remotes/origin/main)
 > git config core.sparsecheckout # timeout=10
 > git checkout -f dc8f8e386889d8c98ffa489585f66eff6ff00339 # timeout=10
Commit message: "Update index.html"
 > git rev-list --no-walk 028c62aad7a0c02c5150e865d3f0219e4f6213f4 # timeout=10
[Pipeline] }
[Pipeline] // stage
[Pipeline] withEnv
[Pipeline] {
[Pipeline] stage
[Pipeline] { (Tests)
[Pipeline] dir
Running in /home/jenkins/.jenkins/workspace/final-project-inital/flask-app
[Pipeline] {
[Pipeline] sh
+ echo this is a test
this is a test
[Pipeline] }
[Pipeline] // dir
[Pipeline] }
[Pipeline] // stage
[Pipeline] stage
[Pipeline] { (docker-compose build and run)
[Pipeline] sh
+ docker-compose up -d
Container mysql Running
Container flask-app Created
Container nginx Recreate
Container nginx Recreated
Container flask-app Starting
Container flask-app Started
Container nginx Starting
Container nginx Started
[Pipeline] }
[Pipeline] // stage
[Pipeline] }
[Pipeline] // withEnv
[Pipeline] }
[Pipeline] // node
[Pipeline] End of Pipeline
Finished: SUCCESS


Pipeline steps for the above build that was successful.
Step	Arguments			Status
Start of Pipeline - (2.8 sec in block)
			
node - (2.5 sec in block)
			
node block - (2.5 sec in block)
			
stage - (0.38 sec in block)
Declarative: Checkout SCM			
stage block (Declarative: Checkout SCM) - (0.32 sec in block)
			
checkout - (0.29 sec in self)
			
withEnv - (2 sec in block)
GIT_BRANCH, GIT_COMMIT, GIT_PREVIOUS_COMMIT, GIT_PREVIOUS_SUCCESSFUL_COMMIT, GIT_URL			
withEnv block - (2 sec in block)
			
stage - (0.47 sec in block)
Tests			
stage block (Tests) - (0.4 sec in block)
			
dir - (0.34 sec in block)
flask-app			
dir block - (0.3 sec in block)
			
sh - (0.28 sec in self)
echo this is a test			
stage - (1.4 sec in block)
docker-compose build and run			
stage block (docker-compose build and run) - (1.4 sec in block)
			
sh - (1.3 sec in self)
docker-compose up -d			







Summary
In my project I was successful in running my first build up to the stage of docker-compose and run. Unfortunately, I had to face many challenges after this stage. Two virtual machines were created on Azure, one was swarm-master and the other swarm-worker, running the appropriate commands allowed me to connect with both worker and master. We also had to create images by installing the correct packages i.e., pip3/python and Jenkins. I received the code for Jenkins but was unable to login and proceed with my next build. When I realised, I created both swarm-master and swarm-worker on different virtual machines, I decided to delete one virtual machine and create it again making sure its under the same resource group. However whilst doing that I was facing further more challenges, in which I was unable to locate the public ip address and hence it would not allow me to connect to Azure cloud shell on bash. I managed to fix the issue by searching it on google, which took a great length of time. Once this issue was resolved I was unable to proceed on cloud shell. I was receiving error messages for the commands I was running for adding a service. Hence, I was unable to complete the deployment. I made several attempts to troubleshoot Jenkins pipeline failure issues, by referring to the console output page, check the logs to find the reason for the failure however I was unsuccessful.

Improvement

I would improve on the following, due to experiencing my project failing, I would have to certainly backup the data stores immediately. I would write down the sequence of activities I took. There would be a need to action the report explaining all the challenges experienced during deployment of the project. Also, to communicate the issue quickly and honestly is important. For the deployment process to be improved I would do the following:
-	Plan early 
-	Release regularly
-	Always strive for continuous improvement
-	Don’t ignore the basics
-	Do more regression testing
The primary objectives of the Devops methodology are to speed up the time to market, apply incremental improvements in response to the changing environment, and create a more streamlined development process. I hope in the future I  have the opportunity to apply these skills and manage to experience a successful deployment process.


