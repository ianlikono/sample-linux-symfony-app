# Sample Linux Symfony App

This repository contains source for a Symfony Application built on Azure AppService. 

- A Docker file - `Dockerfile`
- Symfony web application
- A supervisor configuration  - `supervisord.conf`

## Docker

The docker container is running multiple services: ngnix and php-fpm. php-fpm is necessary
for performance because the defualy apache php configuration does not function efficiently
for a symfony application. This is configured to run in a single container and deployed
to azure app service.

## Deployment

The general process is building the docker image in the root of the project and deploying it to
a container registry. This can be either in azure, or a local instance. Azure devops integrates
really well with azure and can be used to deploy to an azure registry. more information
can be found [here](https://docs.microsoft.com/en-us/azure/container-instances/container-instances-using-azure-container-registry).





