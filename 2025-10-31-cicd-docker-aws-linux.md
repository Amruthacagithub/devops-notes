### Docker & Containers

* Docker bundles applications along with their dependencies
* A Docker image is a read-only build artifact
* Images are created using layered architecture
* Layer caching helps reduce build time
* Images are stored in container registries

---

### Deployment & Networking

* Public IP addresses can change after instance restart
* Elastic IP remains constant
* Elastic IP is preferred for production environments
* Ensures consistent and reliable access

---

### AWS Basics

* **Region** → Physical geographic location
* **Availability Zone (AZ)** → Data center within a region
* **VPC** → Isolated virtual private network
* **Subnet** → Smaller network inside a VPC
* Each subnet is associated with a single AZ
* Using multiple AZs improves fault tolerance

---

### EC2 Configuration Parameters

* **Name & Tags** → Resource identification
* **AMI** → Operating system image
* **Instance Type** → CPU and memory configuration
* **Key Pair** → Secure login access
* **Networking** → VPC, subnet, security group
* **Storage** → EBS volumes
* **IAM Role** → Access permissions
* **User Data** → Initialization scripts
* **Monitoring** → CloudWatch integration

---

### Linux Basics

* Linux is an open-source operating system
* Kernel controls system operations
* Shell acts as an interface to the kernel
* Bash is the most widely used shell

---

### Essential Linux Commands

* `pwd` → Display current directory
* `cd` → Navigate directories
* `mkdir` → Create directories
* `touch` → Create files
* `cat` → View file contents
* `echo` → Display or write text
* `history` → View command history

---

### File Handling Commands

* `ls` → List files and directories
* `cp` → Copy files
* `mv` → Move or rename files
* `rm` → Remove files or directories
* `find` → Search files
* `du` → Check disk usage
* `df` → Display available disk space

---

### Process Management

* `ps` → Display running processes
* `top` / `htop` → Real-time system monitoring
* `kill` → Terminate processes
* `jobs` → List background tasks
* `fg` / `bg` → Manage foreground/background jobs

---

### File Permissions

* `chmod` → Modify permissions
* `chown` → Change file owner
* `chgrp` → Change file group

---

## Key Takeaways

* CI/CD is the foundation of automation
* Artifacts are build outputs
* Docker enables consistent deployments
* Elastic IP provides stable connectivity
* VPC ensures network isolation
* Subnets help manage traffic flow
* Linux is core to DevOps practices
* Use `rm` carefully
* Monitor system processes regularly
* Proper permissions enhance security
