## Readings: Django REST Framework & Docker


Docker is an open platform for developing, shipping, and running applications. Docker enables you to separate your applications from your infrastructure so you can deliver software quickly. With Docker, you can manage your infrastructure in the same ways you manage your applications

Install Docker
```
$ docker-compose --version

```

Images and Containers
Images and containers are the two fundamental concepts to grasp when you start with Docker. An image is a snapshot in time of what a project contains. A container is a running instance of the image.

When we ran hello-world we used an official Docker image. We did not have to create the image ourself. But typically we will create custom images and we do so using a Dockerfile. We also will use docker-compose.yml files to run the containers.

A baking analogy we can use here is as follows:

A Dockerfile is the recipe for a cake
An image is a snapshot of the recipe at a given time
A docker-compose.yml says how to make the cake
And the container is the actual, baked cake
