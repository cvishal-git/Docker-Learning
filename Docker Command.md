# Docker Commands Reference

## Level 1: Essential Basic Commands

### Container Basics

- `docker run <image_name>` - Create and start a new container from an image
- `docker ps` - List running containers
- `docker ps -a` - List all containers (including stopped ones)
- `docker stop <container_id>` - Stop a running container
- `docker start <container_id>` - Start a stopped container
- `docker rm <container_id>` - Remove a stopped container

### Image Basics

- `docker pull <image_name>` - Download an image from Docker Hub
- `docker images` - List all local images
- `docker rmi <image_name>` - Remove a Docker image

## Level 2: Container Interaction & Management

### Container Interaction

- `docker exec -it <container_id> <command>` - Execute a command in a running container
- `docker logs <container_id>` - View container logs
- `docker inspect <container_id>` - View detailed container information
- `docker cp <container_id>:<src_path> <dest_path>` - Copy files between container and host

### Advanced Container Management

- `docker run -d <image_name>` - Run container in detached mode
- `docker run -p <host_port>:<container_port> <image_name>` - Port mapping
- `docker run -v <host_path>:<container_path> <image_name>` - Volume mounting
- `docker run --name <container_name> <image_name>` - Name your container

## Level 3: Image Building & Management

### Image Creation

- `docker build -t <image_name> .` - Build an image from a Dockerfile
- `docker commit <container_id> <new_image_name>` - Create image from container
- `docker tag <image_name> <new_tag>` - Tag an image

### Image Sharing

- `docker push <image_name>` - Push an image to a registry
- `docker save <image_name> > backup.tar` - Save image to tar file
- `docker load < backup.tar` - Load image from tar file

## Level 4: Network & Volume Management

### Networking

- `docker network ls` - List networks
- `docker network create <network_name>` - Create a network
- `docker network connect <network_name> <container_id>` - Connect container to network
- `docker network inspect <network_name>` - Inspect a network

### Volume Management

- `docker volume ls` - List volumes
- `docker volume create <volume_name>` - Create a volume
- `docker volume inspect <volume_name>` - Inspect a volume

## Level 5: System & Maintenance

### System Commands

- `docker system df` - Show docker disk usage
- `docker system prune` - Remove unused data
- `docker stats` - Show container resource usage statistics

### Maintenance

- `docker events` - Get real-time events from the server
- `docker info` - Display system-wide information
- `docker version` - Show Docker version information

## Level 6: Docker Compose (Multi-Container Applications)

### Docker Compose Basics

- `docker-compose up` - Create and start containers
- `docker-compose down` - Stop and remove containers
- `docker-compose ps` - List containers
- `docker-compose logs` - View output from containers
