# azurecontainerapps-helloworld
This repository is a fork from [https://github.com/mavilleg/azurecontainerapps-helloworld](https://github.com/mavilleg/azurecontainerapps-helloworld), part of the [Azure container apps Workshop](https://stoworkshopacastaging.z6.web.core.windows.net/)

This sample is a very simple NodeJS application used to demonstrate [Azure Container Apps](https://docs.microsoft.com/en-us/azure/container-apps/). The packaged version of the application is available on [Docker Hub](https://hub.docker.com/r/pinpindock/azconapps).

# Build the docker image
```sh
docker_usr="<Your Docker Hub Account>"
echo "Docker Hub user Name : " $docker_usr 

docker version
docker info
docker login
systeminfo
docker system df
docker container ls

docker build --no-cache -t "$docker_usr/azconapps:1.1" -f ".\Dockerfile" .
docker image list
docker image history "$docker_usr/azconapps:1.1"
docker image push "$docker_usr/azconapps:1.1"
docker scan --accept-license --file Dockerfile "$docker_usr/azconapps:1.1"
# docker image prune -a
# docker system prune -a
# docker container prune
# docker volume prune
# docker network prune
#docker container ls
```

## Push it to Docker Hub


## Contributing

This project welcomes contributions and suggestions.  Most contributions require you to agree to a
Contributor License Agreement (CLA) declaring that you have the right to, and actually do, grant us
the rights to use your contribution. For details, visit https://cla.microsoft.com.

When you submit a pull request, a CLA-bot will automatically determine whether you need to provide
a CLA and decorate the PR appropriately (e.g., label, comment). Simply follow the instructions
provided by the bot. You will only need to do this once across all repos using our CLA.

This project has adopted the [Microsoft Open Source Code of Conduct](https://opensource.microsoft.com/codeofconduct/).
For more information see the [Code of Conduct FAQ](https://opensource.microsoft.com/codeofconduct/faq/) or
contact [opencode@microsoft.com](mailto:opencode@microsoft.com) with any additional questions or comments.
