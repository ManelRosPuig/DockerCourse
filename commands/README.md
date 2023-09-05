## Commands
We can use docker with Docker Desktop with a GUI (Graphical User Interface) or we can use docker with the CLI (Command Line Interface). Here are explained the most common and used docker commands.
<br><br>
### Images
```bash
ㅤ
docker pull node:latest
ㅤ
```
Downloads the image from Docker Hub with the LATEST version. As it is not specified the verison. When the user executes this command, docker downloads all the layers that are on the image that is being downloaded. The images
can be shared, so, there's no need to download the linux layer twice.
<br><br>
```bash
ㅤ
docker images
ㅤ
```
Returns a list of the images that are installed on the system.
<br><br>

```bash
ㅤ
docker image rm node:latest
ㅤ
```
Deletes an image from the system.
<br><br>

## Commands
```bash
ㅤ
docker ps
ㅤ
```
Returns a list of the running containers.
<br><br>

```bash
ㅤ
docker create node
ㅤ
```
Create container from an image. Returns the id of the container that we just created.
<br><br>

```bash
ㅤ
docker create --name monguito mongo
ㅤ
```
Create a container with a name. If no name is specified, docker generates a random name.
<br><br>

```bash
ㅤ
docker start [container_id/container_name]
ㅤ
```
Start a container with a container id or container name. Returns the id or the name of the container.
<br><br>

```bash
ㅤ
docker stop [container_id/container_name]
ㅤ
```
Stop a running container with a container id or container name.
<br><br>

```bash
ㅤ
docker rm [container_id/container_name]
ㅤ
```
Deletes a container with a container id or container name.
<br><br>
