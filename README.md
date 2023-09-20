# Huggingface text-generation-inference and ChatUI in Docker Compose

## Docker Setup

- Docker and Docker compose
- NVIDIA Container Toolkit

## Build and Run

```bash
# pull chat-ui
$ git submodule update

# copy .env.local
$ cp ./chat-ui/.env ./env.local

# configuration
# point to docker compose server name
MONGODB_URL=mongodb://db:27017

# .env.local will only be used in the build phase and must be repackaged after each modification.
$ docker compose build --no-cache

# If there is a key in .env.local, please remember to edit or delete it after the build phase
# rm .env.local

$ docker compose up -d --force-recreate
```