## Container Networking for Docker

* Bridged: DEFAULT MODE, Namespace isn't shared with host. Used for standalone containers. these containers can communicate with one another.

* Host: Uses the hosts networking directly. Doesn't isolate btween the container and the host.

* None: Does not attach the container to a network. Completely isolated.

### How to run the container and bind a host port to the container port

docker run -dit -p HOST_PORT:CONTAINER_PORT IMAGE_NAME

This is the most generic way to write the command, names and ports will be replaced and filled in respectively.

## Container Networking for Podman

* Bridged: DEFAULT MODE, Same functionality as Docker. Can forward single/multiple ports between the host network and container network. The ports may have different numbers depending on your usecase/setup.

* Host: Uses the network of the host, doesn't isolate between container network and host network.

* NONE: same as Docker. Completely isolated and is not connected to a network.

### How to run the container and bind a host port to the container port

podman run -dit -p HOST_PORT:CONTAINER_PORT IMAGE_NAME

## Investigate Vulnerability Scanners

* Hadolint. This is a pretty popular open source tool. You can get it for VSCode as well as run it command line. https://github.com/hadolint/hadolint
Hadolint can help a bit with syntax. removing spaces after = signs when trying to assign a value.
Removes the apt-get lists after installing something.

* Aqua Trivy
Trivy can only scan docker images that have a recognised distro like from dockerhub. The process of running this can sometimes be slow, this should be brought into consideration for business related deployments. Can scan for misconfigurations, general software vulnerabilities like dependencies and general filesystems.


