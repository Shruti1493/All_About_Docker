# Docker Compose: Simplifying Multi-Container Applications

## What is Docker Compose?
Docker Compose is a powerful tool that simplifies the management of multi-container Docker applications. Instead of running and configuring containers individually using `docker run`, Docker Compose allows you to define and run multiple containers with a single command using a configuration file (`docker-compose.yml`).

---

## Key Features of Docker Compose:
1. **Multi-Container Orchestration:** Compose allows you to define all the services (containers) your application needs, such as databases, web servers, and background workers, in one file.
  
2. **Easy Configuration:** You define the containers, their configuration, networks, volumes, and environment variables in a simple YAML file (`docker-compose.yml`).

3. **Service Dependencies:** Specify dependencies between services. For example, if your web application depends on a database, Docker Compose ensures that the database starts before the web app.

4. **Networking:** Compose automatically creates a network so the services can communicate with each other using their service names as hostnames (e.g., `web` can communicate with `db`).

5. **Scaling:** Easily scale services by specifying how many instances of a container should run, making it useful for load testing or redundancy.

6. **One Command for Everything:** With a single command (`docker-compose up`), you can build, start, and run multiple containers and services.

---

## Example `docker-compose.yml` File:
Here’s a simple example of how a multi-container application can be configured using `docker-compose.yml`.

```yaml
version: '3'
services:
  web:
    image: my-web-app:latest
    ports:
      - "80:80"
    depends_on:
      - db
  db:
    image: postgres:latest
    environment:
      POSTGRES_USER: example
      POSTGRES_PASSWORD: example
