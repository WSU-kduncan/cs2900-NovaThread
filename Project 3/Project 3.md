# Project 3

## Available Mounts
## Docker

In Docker there are 3 types of mounts. Volumes, Bind Mounts and tmpfs (temporary). 
* Volumes are managed by the docker engine and can be shared between multiple docker containers.
* Bind Mounts are files on the host macchine that "bind" to the containers
* tmpfs is a temporary files only used until the container is stopped.

### Volume
To create a Volume,"sudo docker volume create NAME".
to start the container with a volume:

docker run -d
--name devtest
--mount type=bind,source=NAME,target= /app
nginx:latest

After running that you can inspect using 
"docker inspect NAME"

### Bind Mount
To start a container with Bind:

docker run -d
-it
--name devtest
--mount type=bind,source=path/to/file/,target=path/to/container/file
busybox

After running that inspect it with the same comand as for a Volume
"docker inspect NAME"

### tmpfs

in order to make a file a tmpfs you just need to add the "-tmpfs" flag

## Podman

Podman has the option for Bind mounts and Volumes. In order to choose which one you want all you would have to change in the command from Docker to work in Podman is
"type=bind/or/volume

## Building Images for the Container Engine

## Docker

Docker has included a command to build an image. 

"docker build [OPTIONS] PATH [URL]"

OPTIONS include FROM, RUN, COPY, WORKDIR I think there are more too.

## Podman

Podman has included a command to buid an image as well.

"podman image build [OPTIONS] PATH [URL]"

OPTIONS include FROM, RUN, COPY, WORKDIR. There are more aswell.






