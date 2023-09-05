## Port mapping
By default, containers have a port created which typically is 27000+, but this is the port for the container, not the host machine, it is necessary to map a host port to the container port if we want to use the container. Even though the container is
running, if there's no port specified, it is not possible to connect to this instance. Containers can reach to each other without the need of a port mapping, but if the connection is from ouside of the containers network, a port mapping is needed.

### What is port mapping?
The port mapping concept is when we receive a connection from one of our local machine ports and we "redirect" this port to another, in this case, the container's port.

<img src="https://raw.githubusercontent.com/ManelRosPuig/DockerCourse/main/port_mapping/port%20mapping.png" with=550 height=475>

### Example:
| Container   | Inside Realm   | Outside Realm   |
|------------|------------|------------|
| monguito | 27017 | 3000 |
| app_database | 27041 | 3001 |
| nodito | 27014 | 3002 |
