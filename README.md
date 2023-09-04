# Docker Course
This repository is created for **docker learning purposes**. It contains notes and code examples. The course is available for free in youtube: https://www.youtube.com/watch?v=4Dko5W96WHg

## What is docker?
Docker is a software platform that allows you to build, test, and deploy applications quickly. Docker packages software into standardized units called containers that have everything the software needs to run including libraries, system tools, code, and runtime.

### Containers
Containers are a way to package our applications with all the **dependencies** it contains. Containers are very portable. Easy to share between devs and ops.

<img src="https://raw.githubusercontent.com/ManelRosPuig/DockerCourse/main/notes/Container.png" width=400 height=325>

### Docker Hub
Containers are hosted on **private** or **public** repositories. The most famous public repository is Docker Hub where there are over 100,000 container images from software vendors, open-source projects, and the community. In the docker hub, there are hosted images for example like python, mysql, node and many many more.

<img src="https://raw.githubusercontent.com/ManelRosPuig/DockerCourse/main/notes/Docker%20hub.png" width=400 heigth=650>

### Docker WorkFlow
The way of work with docker is to **download images** that are based on linux, those images have all the necessary dependencies or configuration files that are needed to be able to run. **The biggest problem that docker solves is the dependency problem**. It is very common to have errors or conflicts with other developers over the versions of the dependencies or technologies that are required to run an app. With Docker that problem is completely solved. Even on the same machine, several containers with the same technology in different versions can be run, without having any conflict.
<br><br>
When it's time to deploy an application, developers create an image. This image just needs docker runtime to be able to run propperly. The
cool thing about this is that this can be completely automated with a **pipeline**. A pipeline is a set of automated processes and tools that allows
devs and ops to collaborate on building and deploying code to a production environment provided by version control service providers like GitHub, GitLab or many others.

### Container layers
Containers are created from images. Containers multiple layers of images. Each layer is an actual image. The bottom layer is the linux distribution. The top image is the technology one (ex: python, mysql, node).

<img src="https://raw.githubusercontent.com/ManelRosPuig/DockerCourse/main/notes/Layers.png" width=400 heigth=650>

### Virtual Machine vs Container
Virtual machines (VMs) and Docker containers are both technologies used in the field of virtualization, but they serve different purposes and have distinct characteristics. Here's a comparison of VMs and Docker containers:

<img src="https://raw.githubusercontent.com/ManelRosPuig/DockerCourse/main/notes/VMvsContainer.png" width=400 heigth=650>

## Summary

![](https://raw.githubusercontent.com/ManelRosPuig/DockerCourse/main/notes/Docker%20drawio.png)
