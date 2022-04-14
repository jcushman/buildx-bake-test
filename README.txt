To push built images to remote registry:

If not logged in:

$ docker login registry.lil.tools

If you get "multiple platforms feature is currently not supported for docker driver", set up a builder:

$ docker buildx create --use --name my-builder

Build and push multiplatform images in docker-compose.yml:

$ docker buildx bake -f docker-compose.yml -f docker-compose.override.yml --push