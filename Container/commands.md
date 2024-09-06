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

- **Run a Container and Automatically Remove It After Exit**
```bash
docker run --rm IMAGE
```
This will remove the container once it exits.

Replace IMAGE with the name of the Docker image you want to use. If you need to specify a command to run inside the container, include it after the image name.