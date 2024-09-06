## Run a Container
To run a Docker container, use the docker run command

- **Run a Container in the Background**
```bash
docker run -d IMAGE
```

- **Run a Container with Port Mapping**
```bash
docker run -d -p 80:80 IMAGE
```
This maps port 80 on the host to port 80 in the container.

- **Run a Container with a Specific Name**
```bash
docker run --name my-container IMAGE

```

- **Run a Container with Environment Variables**
```bash
docker run -d -e MY_ENV_VAR=value IMAGE
```
This sets an environment variable MY_ENV_VAR inside the container.


- Example

```bash
docker run --name my-mysql-container -e MYSQL_ROOT_PASSWORD=my-secret-pw -d mysql
```
`-e MYSQL_ROOT_PASSWORD=my-secret-pw`: Sets an environment variable inside the container (in this case, the MySQL root password).
`mysql`: The image name for MySQL.



- **Run a Container and Automatically Remove It After Exit**
```bash
docker run --rm IMAGE
```
This will remove the container once it exits.

Replace IMAGE with the name of the Docker image you want to use. If you need to specify a command to run inside the container, include it after the image name.


## Check Running Containers

- **To verify that your container is running, use**
```bash
docker ps
```

- **This will list all running containers. To list all containers (including stopped ones)**
```bash
docker ps -a
```

## Stopping and Removing the Container

- **To stop a running container:**
```bash
docker stop <container-name or container-id>

```

- **To remove a container**
```bash
docker rm <container-name or container-id>
```

### Exit from terminal but run container in backend
clt pq


### start a new Ubuntu container and get a shell immediately:
```bash
docker run -it ubuntu /bin/bash
```

### Start the stopped container
```bash
docker start f0de0b3f73bf
```

### Attach to the container interactively with Bash
```bash
docker exec -it f0de0b3f73bf /bin/bash
```