To push built images to remote registry:

If not logged in:

$ docker login registry.lil.tools

Build and push multiplatform images in docker-compose.yml:

$ docker buildx bake -f docker-compose.yml -f docker-compose.override.yml --push