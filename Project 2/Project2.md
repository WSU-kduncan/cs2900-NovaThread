# INSTALLING DOCKER ENGINES
(source - https://docs.docker.com/engine/install/ubuntu/#install-from-a-package)
1. run "sudo apt-get update" to update everything.

2. run "sudo apt-get install \
    apt-transport-https \
    ca-certificates \
    curl \
    gnupg \
    lsb-release" to install the required programs

3. run "curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo gpg --dearmor -o /usr/share/keyrings/docker-archive-keyring.gpg" this will set up your gpg keys correctly.

4.run "sudo apt-get update" to update everything again

5.run "sudo apt-get install docker-ce docker-ce-cli containerd.io" to install the required docker engines and programs/files this downloads everything needed to run dockers succesfully.

6.run "sudo docker run hello-world" to verify that the instalation was successful, this will also install the hello-world docker from docker hub.

# PULLING A DOCKER 
(source - https://linuxhit.com/install-docker-on-ubuntu-20-04-run-container/)

1. run "sudo docker pull nginx" this will pull a small light weight web server docker.

2.run "sudo docker image ls" to see what dockers you have installed.
![image](https://github.com/WSU-kduncan/cs2900-NovaThread/edit/main/Project%202/Images/dockerimagels.jpg)

# RUNNING A CONTAINER 
(source - https://stackoverflow.com/questions/34782678/difference-between-running-and-starting-a-docker-container)

1. the difference between docker run and docker start; docker run will create a new container of an image and execute the container. docker start will start a previously stopped container.

2. running the docker in foreground mode "sudo docker run -p 80:80 ngnix"

3. running the docker in background/detached mode "sudo docker run -d -p 80:80 ngnix"
![image](https://github.com/WSU-kduncan/cs2900-NovaThread/edit/main/Project%202/Images/dockerterminal.jpg)

# LOGS AND STATUS
(source - https://www.cloudsavvyit.com/10953/how-to-monitor-docker-container-logs/)

1. "sudo docker ps" this will list information about the container as well as status.

2. "sudo docker logs my-container" (replace my-container with container id) this will display the entire container log into the terminal.


# STOPPING A CONTAINER

1. "sudo docker stop my-container" (replace my container with container id) stops the container
![image](https://github.com/WSU-kduncan/cs2900-NovaThread/edit/main/Project%202/Images/dockerstop.jpg)

2. "sudo docker pause my-container" (replace my container with container id) pauses the container in current state

3. "sudo docker restart my-container" (replace my container with container id) restarts container from last saved state

4. "sudo docker kill my-container" (replace my container with container id) terminates the container.

5. "sudo docker resume my-container" (replace my container with container id) resumes container from being paused or last save if stopped. 
