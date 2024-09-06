## Managing Docker Images

#### Listing All Docker Images on Your Local Machine
To list all Docker images currently stored on your local machine, use the following command:

```bash
docker images
```

#### Pulling an image without a tag (default to latest):

```bash
docker pull nginx
```


#### Pulling a specific version of an image:
```bash
docker pull mysql:8.0
``` 

#### Pulling from a different registry: By default, Docker pulls images from Docker Hub, but you can also pull images from other registries (e.g., AWS ECR, GCR, or private registries) by specifying the full registry URL.
```bash
docker pull myregistry.com/myimage:mytag
```