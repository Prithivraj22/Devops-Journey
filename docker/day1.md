
# Docker Learning Log - Day 1 🐳

## 1. What is a Docker Image and How is it Created?

**Question**: Can you tell me how a Docker image is created?

**Answer**:  
Docker images are built using a `Dockerfile`, which is a text file containing a set of instructions to build the image layer by layer. Each layer represents a change in the filesystem (like installing packages or copying files). Docker caches each layer, making builds faster and more efficient.

**Key Command**:
```bash
docker build -t myapp:1.0 .
```
- `-t myapp:1.0`: Tags the image with a name and version
- `.`: Specifies the build context (current directory)

---

## 2. What is `docker run` and its Options?

**Question**: How do you run a Docker container with various options?

**Answer**:  
The `docker run` command is used to start a container from an image. It can be customized with flags like `-it`, `--name`, `-p`, and more.

**Key Command**:
```bash
docker run -it alpine sh
```
- `-i`: Keep STDIN open
- `-t`: Allocate pseudo-TTY
- `alpine`: Lightweight image
- `sh`: Shell inside the container

**Common Attributes**:
- `--name`: Name the container
- `-p host:container`: Port mapping
- `-v host:path:container:path`: Volume mount
- `--cpus` / `--memory`: Limit CPU/memory
- `--env`: Set environment variables
- `--privileged`: Give extended privileges
- `--rm`: Remove after exit

---
