Removing Containers and Images
Stop and remove all containers:
Bash
docker stop $(docker ps -q)
docker rm $(docker ps -a -q)
Use code with caution.

Remove all images:
Bash
docker rmi -f $(docker images -q)
Use code with caution.

Remove a specific container:
Bash
docker rm <container_id_or_name>
Use code with caution.

Remove a specific image:
Bash
docker rmi <image_id>
Use code with caution.

Remove dangling images:
Bash
docker image prune -f
Use code with caution.

Remove all unused objects (images, containers, networks, volumes):
Bash
docker system prune -a
Use code with caution.

