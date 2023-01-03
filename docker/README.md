# Docker

<p align="center">
<img src="../assets/docker-logo.png" width=50% height=30%>
</p>

### What is Docker?
> Docker is an open platform for developing, shipping, and running applications. Docker enables you to separate your applications from your infrastructure so you can deliver software quickly. With Docker, you can manage your infrastructure in the same ways you manage your applications. By taking advantage of Docker’s methodologies for shipping, testing, and deploying code quickly, you can significantly reduce the delay between writing code and running it in production.

### What is Docker Hub?
> Docker Hub is the world’s largest repository of container images with an array of content sources including container community developers, open source projects and independent software vendors (ISV) building and distributing their code in containers. Users get access to free public repositories for storing and sharing images or can choose subscription plan for private repos.

### Download Docker on your machine from this [link](https://docs.docker.com/get-docker/)

### You can play with Docker; without downloading it on your machine using this [link](https://labs.play-with-docker.com/)

### How to pull a Docker image on your machine form Docker Hub:
```docker
docker pull [IMAGE]
```

Example: _(pulling [redis](https://hub.docker.com/_/redis) image from Docker hub)_
```docker
docker pull redis
```

### How to run a Docker container from an image:
```docker
docker run [IMAGE]
```

Example: _(running a container using [redis](https://hub.docker.com/_/redis) image)_
```docker
docker run redis
```

### How to run a Docker container from an image and assign it a name:
```docker
docker run --name CONTAINER [IMAGE]
```

Example: _(running a container using [redis](https://hub.docker.com/_/redis) image with 'myredis' name)_
```docker
docker run --name myredis redis
```

### How to show a list of the downloaded Docker images on your machine:
```docker
docker images
```

### How to show a list of running Docker containers:
```docker
docker ps
```

### How to show a list of all Docker containers:
```docker
docker ps -a
```

### How to stop a running Docker container:
```docker
docker stop CONTAINER
```

Example: _(stopping a container named 'myredis')_
```docker
docker stop myredis
```

### How to start a stopped Docker container:
```docker
docker start CONTAINER
```

Example: _(starting a stopped container named 'myredis')_
```docker
docker start myredis
```

### How to run a Docker container and mapping it to a port:
```docker
docker run -p HOSTPORT:CONTAINERPORT IMAGE
```

Example: _(running and mapping a container to the port 5000 on the container side, and 8080 on the host side)_
```docker
docker run -p 8080:5000 redis
```

### How to run and detach a Docker container: _(running it in the background)_
```docker
docker run -d CONTAINER
```

Example: _(running and detaching a redis container)_
```docker
docker run -d redis
```


More will be added soon...