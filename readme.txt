First refer the jenkinsfile and then the script.sh file in repo. 
The Repository is an example for the Building, Testing and deploying of the code. which has a Jenkinsfile which has stages of Building the code where it Compiles the code.
Then it test the code using junit plugin which is a second stage. 
After that it builds the build file that is war file. Then it moves the build files to the target machine that is the tomcat machine. 
The next stage triggers the deploy script that is kept in the tomcat server.
