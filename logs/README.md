## Logs
If we want to read the logs of a container, we can do it with the command:
```bash
ㅤ
docker logs [container_id/container_name]
ㅤ
```
Returns a list of the images that are installed on the system.
<br><br>

```bash
ㅤ
docker logs --follows [container_id/container_name]
ㅤ
```
We can specify the "--follows" option, the terminal will keep listening for the logs until the process is cancelled.
<br><br>

<img src="https://raw.githubusercontent.com/ManelRosPuig/DockerCourse/main/logs/docker%20logs.png">
