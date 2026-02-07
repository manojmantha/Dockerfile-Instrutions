# Dockerfile Instructions Repository 🐳

This repository is a collection of examples and explanations for the most commonly used **Dockerfile instructions**. Each instruction demonstrates how to build and configure Docker images effectively.  

---

## Table of Contents
1. [FROM](#from)  
2. [RUN](#run)  
3. [CMD](#cmd)  
4. [COPY](#copy)  
5. [ADD](#add)  
6. [LABEL](#label)  
7. [EXPOSE](#expose)  
8. [ENV](#env)  
9. [ENTRYPOINT](#entrypoint)  
10. [USER](#user)  
11. [WORKDIR](#workdir)  
12. [ARG](#arg)  

---

## 1. FROM
**Description:** Sets the base image for your container.  
**Last Updated:** 3 hours ago  
**Usage:**  
```dockerfile
FROM ubuntu:20.04
```

2. RUN

Description: Installs packages or executes commands during the build. Each RUN creates a new image layer.
Last Updated: 3 hours ago
Usage:

```dockerfile
RUN apt-get update && apt-get install -y curl
```

3. CMD

Description: Specifies the default command to run when the container starts. Can be overridden during docker run.
Last Updated: 3 hours ago
Usage:

```dockerfile
CMD ["node", "app.js"]
```

4. COPY

Description: Copies files or directories from the host system to the container.
Last Updated: 2 hours ago
Usage:

```dockerfile
COPY ./app /usr/src/app
```

5. ADD

Description: Similar to COPY, but also supports URLs and automatic extraction of tar files.
Last Updated: 2 hours ago
Usage:

```dockerfile
ADD https://example.com/file.tar.gz /usr/src/app/
```

6. LABEL

Description: Adds metadata to an image (author, version, description, etc.) for documentation and automation.
Last Updated: 2 hours ago
Usage:

```dockerfile
LABEL maintainer="yourname@example.com"
```

7. EXPOSE

Description: Documents which port the container listens on. Does not actually publish the port.
Last Updated: 2 hours ago
Usage:

```dockerfile
EXPOSE 80
```

8. ENV

Description: Sets environment variables inside the container, available during build and runtime.
Last Updated: 2 hours ago
Usage:

```dockerfile
ENV NODE_ENV=production
```

9. ENTRYPOINT

Description: Configures a container to run as an executable, making CMD arguments optional.
Last Updated: Not specified
Usage:

```dockerfile
ENTRYPOINT ["python3", "app.py"]
```

10. USER

Description: Sets the user to use when running the container.
Last Updated: 52 minutes ago
Usage:

```dockerfile
USER appuser
```

11. WORKDIR

Description: Sets the working directory inside the container.
Last Updated: 46 minutes ago
Usage:

```dockerfile
WORKDIR /usr/src/app
```

12. ARG

Description: Defines a build-time variable that can be passed to the Docker build process.
Last Updated: 35 minutes ago
Usage:

```dockerfile
ARG VERSION=1.0
```