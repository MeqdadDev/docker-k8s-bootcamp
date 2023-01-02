# Docker

<p align="center">
<img src="../assets/docker-logo.png" width=30% height=10%>
</p>

### What is Docker?
> Docker is an open platform for developing, shipping, and running applications. Docker enables you to separate your applications from your infrastructure so you can deliver software quickly. With Docker, you can manage your infrastructure in the same ways you manage your applications. By taking advantage of Docker’s methodologies for shipping, testing, and deploying code quickly, you can significantly reduce the delay between writing code and running it in production.

### What is Docker Hub?
> Docker Hub is the world’s largest repository of container images with an array of content sources including container community developers, open source projects and independent software vendors (ISV) building and distributing their code in containers. Users get access to free public repositories for storing and sharing images or can choose subscription plan for private repos.

### Download Docker on your machine from this [link](https://docs.docker.com/get-docker/)

### You can play with Docker; without downloading it on your machine using this [link](https://labs.play-with-docker.com/)

### How to pull a Docker image on your machine form Docker Hub:
```
docker pull [IMAGE]
```

Example: _(pulling [redis](https://hub.docker.com/_/redis) image from Docker hub)_
```
docker pull redis
```

### How to run a Docker container from an image:
```
docker run [IMAGE]
```

Example: _(running a container using [redis](https://hub.docker.com/_/redis) image)_
```
docker run redis
```

### How to run a Docker container from an image and assign it a name:
```
docker run --name CONTAINER [IMAGE]
```

Example: _(running a container using [redis](https://hub.docker.com/_/redis) image with 'myredis' name)_
```
docker run --name myredis redis
```

More will be added soon...