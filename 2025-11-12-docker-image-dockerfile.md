# Docker Image & Dockerfile – Short Notes

## Docker Image

* Docker image = **Read-only template** of an app
* Contains code, runtime, libraries, configs
* Built using a **Dockerfile**
* Stored in **layers**
* Image → blueprint
* Container → running image

```bash
docker run image_name
```

* Container = Image + writable layer

---

## Dockerfile

* Dockerfile = **instructions to build an image**

Example:

```dockerfile
FROM python:3.12-slim
WORKDIR /app
COPY . .
RUN pip install -r requirements.txt
CMD ["python","app.py"]
```

---

## Important Instructions

* **FROM** → base image (mandatory, first)
* **RUN** → build-time commands (creates layers)
* **CMD** → default start command (overrideable)
* **ENTRYPOINT** → fixed main command
* **COPY** → copy files (preferred)
* **ADD** → URL / tar extract (use only if needed)
* **ENV** → environment variables

---

## ENTRYPOINT + CMD

* ENTRYPOINT = program
* CMD = arguments

```dockerfile
ENTRYPOINT ["echo"]
CMD ["Hello"]
```

---

## Best Practices

* Use `slim/alpine` images
* Combine RUN commands
* Pin versions
* Copy dependencies first
* Run as non-root user
* Use ENV for configs
* Use multi-stage builds

---

## Inspect & Scan

```bash
docker history image
docker inspect image
docker scan image
trivy image image
```

---

## Key Points

* Image = template
* Container = running image
* Dockerfile builds images
* FROM is required
* RUN creates layers
* CMD & ENTRYPOINT control startup
