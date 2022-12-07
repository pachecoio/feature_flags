# feature_flags
Feature flag manager application


## Get started

### Requirements

- Docker
- Kubernetes (optional)

### Running the application

Create a .env file with the following content:

```
MONGODB_URI=<YOUR MONGODB URI>
DATABASE_NAME=<YOUR DB NAME>
```

The application can be executed with docker by using the existing docker-compose.yaml file

```
docker compose up
```

It can also be executed on kubernetes using skaffold

```
skaffold dev
or
skaffold debug
or
skaffold run --port-forward
```

The above will execute the application with a mongo db locally, but if you'd like to connect to a remote MongoDB instance you can simply remove the mongo service from the docker-compose.yaml file and modify the MONGODB_URI and DATABASE_NAME environment variables.
