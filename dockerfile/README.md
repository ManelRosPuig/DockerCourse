## Dockerfile

### Environment variables

When creating a container from an image, we can set some environment variables. Each image is unique and  has its specific environment variables. For example mongo has the MONGO_INITDB_ROOT_USERNAME variable. To set this environment variable we can set the value in the container creation command. Like this:

```bash
ㅤ
docker create -e MONGO_INITDB_ROOT_USERNAME=manel -e MONGO_INITDB_ROOT_PASSWORD=12345aA mongo
ㅤ
```
Creates a container from the image "mongo" with two environment variables, MONGO_INITDB_ROOT_USERNAME and MONGO_INITDB_ROOT_PASSWORD.
<br><br>

### What is the Dockerfile?
Dockerfile is a file that contains the commands that the new containers have to execute when they're being created. We need to create a file called Dockerfile on the project root folder. In the Dockerfile we can write the commands for our future container. In this file must be all the required commands needed to successfully start our application. With this Dockerfile we're creating our unique image. To then be able to create a container with it. Once is created, we'll be able to share this image between the development team as needed.

### 1. FROM
If we want to create an image, first we need to come from another created image, for example, node.

<img src="https://raw.githubusercontent.com/ManelRosPuig/DockerCourse/main/dockerfile/1.png" width=450 height=575>

### 2. RUN
Then, we need to create a folder for our application. Every code file will be located below /home/app. This location is within the container, NOT the host.

<img src="https://raw.githubusercontent.com/ManelRosPuig/DockerCourse/main/dockerfile/2.png" width=450 height=575>

### 3. COPY
Now we need to copy the file to the folder that we just created with the previous command.

<img src="https://raw.githubusercontent.com/ManelRosPuig/DockerCourse/main/dockerfile/3.png" width=450 height=575>

### 4. EXPOSE
After that, we need to open the port that the app will need to receive the requests.

<img src="https://raw.githubusercontent.com/ManelRosPuig/DockerCourse/main/dockerfile/4.png" width=450 height=575>

### 5. CMD
Finally, to start the app, we need to set the command to run the program. For example:

<img src="https://raw.githubusercontent.com/ManelRosPuig/DockerCourse/main/dockerfile/5.png" width=450 height=575>

<br><br>

## Docker build
Once we have done the Dockerfile we now can create the actual image with the command docker build:

<img src="https://raw.githubusercontent.com/ManelRosPuig/DockerCourse/main/dockerfile/docker%20build.png" width=650 height=325>
