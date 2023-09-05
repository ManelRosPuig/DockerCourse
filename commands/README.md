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

## Docker run
Docker run is a command that simplifies the actions required to download an image, create a container and run it by unifying it into a single command called docker run. It is the fastest way to create a container. The steps of docker run are the following:
1. Searches the image
- 1.1. If the image is not downloaded, it searches it in the Docker Hub and downloads it.
2. Create a container
3. Start the container

```bash
ㅤ
docker run mongo
ㅤ
```
This command creates a container with a random name and no port mapped, it runs it automatically and show the logs of this command attached to the terminal. If we exit the logs process, the 
container stops.
<br><br>

```bash
ㅤ
docker run -d mongo
ㅤ
```
This -d option is "dettached", so it doesn't show the logs after running the container.
<br><br>

```bash
ㅤ
docker run --name monguito -p27017:27017 -d mongo
ㅤ
```
We can apply all the previous command options to this run command.
<br><br>
