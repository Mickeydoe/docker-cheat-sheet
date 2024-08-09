# Stop all running containers
docker stop $(docker ps -q)

# Remove all containers (including stopped ones)
docker rm $(docker ps -a -q)

# Remove all images
docker rmi -f $(docker images -q)

# Remove a specific container (replace with container ID or name)
docker rm my_container

# Remove a specific image (replace with image ID)
docker rmi my_image

# Remove dangling images
docker image prune -f

# Remove all unused objects (images, containers, networks, volumes)
docker system prune -a

# Check running containers
docker ps

# Check all containers (including stopped)
docker ps -a

# Check Docker images
docker images

# Remove unused volumes
docker volume prune

Remove Unused Volumes:

bash
Copy code
docker volume prune
