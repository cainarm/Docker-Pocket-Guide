# Docker Pocket Guide 📒

List of useful commands for docker, making life easier for beginners.

`docker version` - Display docker version.

`docker inspect CONTAINER_ID` - Display information about the container.

`docker ps` - Displays all executing containers.

`docker ps -a` - Displays all containers.

#### Execution

`docker run IMAGE_NAME` - Runs a container based on an image.

`docker run -it IMAGE_NAME` - Runs the container in Interactive Terminal mode.

`docker run -d -P --name NAME dockersamples/static-site` - Runs the container with a specific name given by the user.

`docker run -d -p 12345:80 dockersamples/static-site` - Defines a specific port to represent the container's virtual port, in this case port **12345** will access the container's port 80.

`docker run -v "VOLUME_PATH" IMAGE_NAME` - Creates a volume inside the container, given the path.

`docker run -it --name CONTAINER_NAME --network NETWORK_NAME IMAGE_NAME` - Creates a container with a specific name and network.

#### Start/interruption

`docker start CONTAINER_ID` - Start a container.

`docker start -a -i CONTAINER_ID` - Start the contrainer in interactive mode.

`docker stop CONTAINER_ID` - Stop the container.

#### Removal

`docker rm CONTAINER_ID` - Remove the container.

`docker container prune` - Remove all containers that are not executing.

`docker rmi IMAGE_NAME` - Remove a container based on a name.

#### Build

`docker build -f Dockerfile` - Build an image based on a Dockerfile.

`docker build -f Dockerfile -t USER_NAME/IMAGE_NAME` - Build and name an unofficial image.

`docker build -f Dockerfile -t USER_NAME/IMAGE_NAME DOCKERFILE_PATH` - Build and name an unofficial image based on a dockerfile given the path.

#### Network

`hostname -i` - Show container network data.
`docker network create --driver bridge NETWORK_NAME` - Creates a new network, given the name and driver.
