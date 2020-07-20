# tas4_dy
HERE IS TASK Detail one By One !!! 

1. Create container image that’s has Linux and other basic configuration required to run Slave for Jenkins. ( example here we require kubectl to be configured ) 
Now you download the file of Dokcerfile_jenkins

2. Change the TCP settting on Docker HOST  . open the file  /usr/lib/systemd/system/docker.service with vi editor do change -H tcp://0.0.0.0:4243 in file . 
   Reload and restart the service of docker on Docker server.  

	systemctl daemon-reload
	systemctl restart docker.service

3. Now Move on your client End server where you have to install kubctl command and access your kubernetes server .
Run This commadn on your client end. (Make sure stop the minikube ) 

	export DOCKER_HOST=202.63.219.39:4243

Now we have to install some plugins for the docker , so that we can configure the docker cloud.

Now we will setup Dynamic Cloud on Jenkins by using the Docker.For this go to:

4. Now create two job : job1 & job2. 
	where job1 is duty to download the code form github with webhooks. 
	where job2 is duty to check the two things first complie the code with dokcer image . 
		upload the image on docker hub with new version . 
	Next thing in this task , code will check weather we have kubernets deployment have or not . 
	if we don't have then it will create new deployemnt with stable version from our the code and deploye the deployemnt.
	if we have already deployment then it just update the version of my code . update he my web without any downtime . 


