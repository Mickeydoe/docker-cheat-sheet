
Here’s a README.md file with the Docker removal commands:

markdown
Copy code
# Docker Cleanup Commands Cheat Sheet

## Overview
This cheat sheet provides essential Docker commands for stopping and removing containers, images, and other related resources.

## Commands

### 1. Stop All Running Containers
```bash
docker stop $(docker ps -q)
Stops all running containers.

2. Remove All Containers (Running and Stopped)
bash
Copy code
docker rm -f $(docker ps -a -q)
Removes all containers, whether they are running or stopped.

3. Remove All Images
bash
Copy code
docker rmi -f $(docker images -q)
Forcefully removes all Docker images, regardless of dependencies.

4. Remove a Specific Container
bash
Copy code
docker rm <container_id_or_name>
Removes a specific container by its ID or name.

5. Remove a Specific Image
bash
Copy code
docker rmi <image_id>
Removes a specific image by its ID.

6. Remove Dangling Images
bash
Copy code
docker image prune -f
Removes all dangling images (those not tagged and not used by any container).

7. Remove All Unused Images, Networks, and Volumes
bash
Copy code
docker system prune -a
Cleans up your Docker system by removing all unused images, containers, networks, and optionally, volumes.

Quick Tips
Check Running Containers:

bash
Copy code
docker ps
Check All Containers (Including Stopped):

bash
Copy code
docker ps -a
Check Docker Images:

bash
Copy code
docker images
Remove Unused Volumes:

bash
Copy code
docker volume prune
