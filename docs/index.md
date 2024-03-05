## Introduction to Docker

### What is Docker?

Docker is a platform for developing, shipping, and running applications. It provides a way to package and distribute applications and their dependencies in a standardized format called containers.

### Key Concepts

- **Containers**: Lightweight, portable, and self-sufficient units that encapsulate application code and all its dependencies.
- **Images**: Read-only templates used to create containers.
- **Dockerfile**: Text document containing instructions for building a Docker image.
- **Docker Engine**: Core component responsible for building, running, and managing containers.

### Benefits of Docker

- **Portability**: Run applications on any platform supporting Docker.
- **Isolation**: Prevent conflicts and ensure consistency in deployment.
- **Efficiency**: Optimize resource usage and improve performance.
- **Scalability**: Lightweight and scalable containers for easy scaling based on demand.

---

## Getting Started with Docker

### Installation

Install Docker Engine on your system from the official Docker website.

### Docker Commands

- `docker pull <image>`: Pulls a Docker image from a registry.
- `docker build <path/to/Dockerfile>`: Builds a Docker image from a Dockerfile.
- `docker run <image>`: Runs a Docker container from an image.
- `docker ps`: Lists running containers.
- `docker images`: Lists Docker images.
- `docker stop <container>`: Stops a running container.
- `docker rm <container>`: Removes a container.
- `docker rmi <image>`: Removes an image.

### Dockerfile Example

```Dockerfile
# Use an official Python runtime as the base image
FROM python:3.9-slim

# Set the working directory in the container
WORKDIR /app

# Copy the current directory contents into the container at /app
COPY . /app

# Install any needed dependencies specified in requirements.txt
RUN pip install --no-cache-dir -r requirements.txt

# Make port 80 available to the world outside this container
EXPOSE 80

# Define environment variable
ENV NAME World

# Run app.py when the container launches
CMD ["python", "app.py"]
