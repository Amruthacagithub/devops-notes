# Class Notes – Docker & Containerization (Today)

### Docker Concept

* “Build once, run anywhere”
* If an application works inside a container, it will work across environments
* Eliminates environment-related issues

---

### Containers

* Lightweight isolated runtime environments
* Includes:

  * Application
  * Required libraries
  * Tools
  * Configuration
* Shares the host OS kernel (unlike virtual machines)
* Faster and more efficient than VMs

---

### Docker Images

* Image acts as a blueprint for containers
* Immutable (read-only) file
* Used to create running containers

Example:

```bash
docker run ubuntu
```

---

### Docker Client & Daemon

#### Docker Client

* Command-line interface (`docker`)
* Sends requests to Docker engine

#### Docker Daemon

* Runs in the background
* Builds, runs, and manages containers and images
* Receives commands from the client

---

### Storage & Networking

#### Volumes

* Used for persistent data storage
* Data remains even if the container stops or is removed

#### Networking

* Enables communication between containers
* Provides internet access to containers

---

### Running Containers

* Basic command:

```bash
docker run
```

* Interactive mode:

```bash
docker run -it ubuntu
```

Flags:

* `-i` → Interactive mode
* `-t` → Allocates terminal

---

### Docker Hub

* Central image registry
* Hosts public and private images
* Default source for pulling images

Example:

```bash
docker pull nginx
```

---

### Hands-on Practice

* Executed containers using Cloud Shell
* Pulled images from Docker Hub
* Practiced basic Docker commands
* Understood container deployment
* Emphasis on practical learning

---

### Docker in DevOps Today

* Core tool in DevOps ecosystem
* Commonly used alongside Kubernetes
* Direct production usage may be limited
* Still essential for learning and development

---

## Key Takeaways

* Docker is a containerization platform
* Image is a container blueprint
* Container is a running instance of an image
* Docker daemon manages containers
* Volumes provide persistent storage
* Docker Hub stores container images
* Containers are lightweight and fast
* Docker knowledge is required before Kubernetes
