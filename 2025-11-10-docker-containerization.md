# Class Notes – Docker & Containerization (Today)

### Containers

* Lightweight and isolated runtime environments
* Package application code, libraries, runtime, and configuration
* Share the host operating system kernel (faster than virtual machines)
* More efficient and quicker compared to VMs

---

### Docker Images

* Images act as blueprints or templates
* Used to create containers
* Immutable (read-only)

Example:

```bash
docker run ubuntu
```

---

### Docker Architecture

* Docker uses a **client–server architecture**

Flow:
CLI → Docker Daemon → Containers → Host OS

* Client sends commands
* Daemon processes and executes them
* Container runtime manages running containers

---

### Common Docker Commands

| Purpose                 | Command         |
| ----------------------- | --------------- |
| Run a container         | `docker run`    |
| List running containers | `docker ps`     |
| List all containers     | `docker ps -a`  |
| List images             | `docker images` |
| Pull image              | `docker pull`   |
| Stop container          | `docker stop`   |
| Remove container        | `docker rm`     |
| Remove image            | `docker rmi`    |

---

### Running Containers

**Interactive mode**

```bash
docker run -it ubuntu bash
```

**Detached mode**

```bash
docker run -d nginx
```

Flags:

* `-i` → Interactive
* `-t` → Allocate terminal
* `-d` → Run in background

---

### Accessing a Running Container

* Used to enter an already running container

```bash
docker exec -it <container_id> bash
```

---

### Docker Hub

* Centralized online registry for Docker images
* Default source for pulling images
* Similar to GitHub, but for containers

Example:

```bash
docker pull nginx
docker push username/image
```

---

### Networking & Container Communication

* Each container is assigned an IP address
* Details can be viewed using:

```bash
docker inspect
```

* Containers communicate using APIs or tools like `curl`
* Commonly used in microservices architectures

---

### Dockerfile & Image Layers

* Dockerfile contains instructions to build an image
* Each instruction creates a separate layer

Example:

```bash
FROM ubuntu
RUN apt install nginx
COPY ./app
```

* More layers generally increase image size

---

### Layered File System

* Docker uses a Union File System
* Image layers are read-only
* Containers have a single writable layer

Layer structure:

* Base OS layer
* Application layers
* Configuration layers
* Writable container layer

---

### Copy-on-Write Mechanism

* Modified files are copied to the writable layer
* Original image layers remain unchanged
* Optimizes storage usage

---

### Image Storage on Linux

* Docker stores image data at:

```bash
/var/lib/docker/overlay2/
```

* Contains layer files and metadata

---

### Inspecting Image Layers

* View image build history:

```bash
docker history <image>
```

* Inspect image details:

```bash
docker image inspect <image>
```

---

### Layer Caching & Reuse

* Each layer is identified using a SHA256 hash
* Identical layers are reused across images
* Reduces disk usage and build time
* Enables faster image builds

---

### Virtual Machines vs Docker

| Aspect       | Virtual Machine | Docker    |
| ------------ | --------------- | --------- |
| OS           | Full OS         | Shared OS |
| Startup time | Slow            | Fast      |
| Size         | Large           | Small     |
| Boot time    | Minutes         | Seconds   |

* Docker is lightweight and faster

---

### Multi-Architecture Considerations

* ARM and AMD architectures are different
* Images must match system architecture
* Incorrect architecture may prevent image execution

---

## Key Takeaways

* Image acts as a template
* Container is a running instance of an image
* Docker daemon controls container operations
* Dockerfile is used to build images
* Layering improves performance and efficiency
* Volumes ensure data persistence
* Docker Hub hosts container images
* Containers are not virtual machines


