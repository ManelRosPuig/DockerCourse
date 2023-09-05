## Port mapping
By default, containers have a port created which typically is 27000+, but this is the port for the container, not the host machine, it is necessary to map a host port to the container port if we want to use the container. Even though the container is
running, if there's no port specified, it is not possible to connect to this instance. Containers can reach to each other without the need of a port mapping, but if the connection is from ouside of the containers network, a port mapping is needed.

<img src="https://raw.githubusercontent.com/ManelRosPuig/DockerCourse/main/port_mapping/container%20ports.png" width=650 height=275>

### What is port mapping?
The port mapping concept is when we receive a connection from one of our local machine ports and we "redirect" this port to another, in this case, the container's port.

<img src="https://raw.githubusercontent.com/ManelRosPuig/DockerCourse/main/port_mapping/port%20mapping.png" with=550 height=475>

### Example:
| Container   | Inside Realm   | Outside Realm   |
|------------|------------|------------|
| monguito | 27017 | 3000 |
| app_database | 27041 | 3001 |
| nodito | 27014 | 3002 |

### How to do this port mapping?
We can do this when we create the contianer. We need to add another flag called -p (publish) and then the local port of the machine outside realm, followed by a colon and then the contianer's port inside realm. So:

```bash
ㅤ
docker container create --name monguito -p27029:27029 mongo:latest
ㅤ
```
Creates a container from the image mongo:latest and maps the port 27029.
<br><br>

<img src="https://raw.githubusercontent.com/ManelRosPuig/DockerCourse/main/port_mapping/how%20to%20port%20mapping.png" width=550 height=275>
