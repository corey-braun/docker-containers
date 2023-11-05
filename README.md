# Corey Braun's Docker Containers
The `Dockerfile` and `docker-compose.yml` files in this repository define the docker containers I currently run at home.

## Compose environment variables
A [.env file](https://docs.docker.com/compose/environment-variables/set-environment-variables/#substitute-with-an-env-file) is used for environment variable subsitution in Docker Compose files. Additionally, some environment variables are passed directly to containers by listing them under the service's `environment:` key without specifying a value.

Environment variable `BIND_IP` is a host IP to bind container port mappings to, followed by a colon. If set, this overrides [Docker's default behavior](https://docs.docker.com/network/) of binding port mappings to all host IPs/interfaces.

Aside from environment variables, [Docker secrets](https://docs.docker.com/compose/use-secrets/) are used for supplying containers sensitive information, such as passwords.
