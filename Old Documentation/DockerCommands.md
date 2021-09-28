# Docker cheat sheet

## Dockerfile

A Dockerfile (no extension, just Dockerfile) is required for building docker images. It should be in the root directory of your folder. That is, parallel to your pom.xml and your src/ folder. If you're pulling from one of the GitHub repositories, they should already have a Dockerfile in them.

## Basic navigation & information commands

 * ```docker container ls | docker ps``` : Shows all currently running containers. Adding ```-a``` after either command will show stopped containers as well.
 * ```docker image ls``` : Shows all existing docker images on your local machine
 * ```docker rm [name | id] | docker rmi [name | id]``` : Removes the docker container from your machine | Removes the docker image from your machine.
   * ```[name]``` is the name of the container or image.
   * ```[id]``` is the id of the container or image. 
   * Either one (but not both) can be used. 
   * example: ```docker rmi quizzard-api``` will remove the image tagged 'quizzard-api'
 
## Building & running the image

Before the image is even built, make sure to ```mvn clean package``` first.

 * ```docker build [directory]``` : Builds a docker image using the Dockerfile found in the provided directory. If you are building inside a directory, use ```.``` (dot) to denote the current directory.
   * (Optional, but reccomended) ```-t [name]``` : This can be added after the directory to tag your image with a name, otherwise a random tag will be provided for your image. See example below for the reccomended way of building the quizzard-api.
   * example/recommended: ```docker build . -t quizzard-api``` : will create an image in the current folder and tag it 'quizzard-api'.
 * ```docker run [optionals] [image]:[version]``` : Spins up a docker container using the provided [image], at whatever version is specified with [version]. For our purposes this will usually be ```quizzard-api:latest``` but if you did not name the image, or wish to use other images, simply change 'quizzard-api' to whatever the image name is. If the image has no name, the id should also work. [optionals] are explained below
   * The following commands can be provided where the [optionals] tag is in the above command. You may add as many optionals as you want, provided they don't conflict with one another.
     * ```-d``` : detaches the container from your terminal so it does not log directly to it.
     * ```-i``` : makes the container 'interactive'. For quizzard this doesn't actually do anything besides allowing you to terminate the process from inside. Unless you're using powershell, in which case you're SoL and will have to open another terminal to stop the process.
     * ```-p [from]:[to]``` : maps the port [from] to the port [to]. example: ```-p 80:5000``` will map any incoming requests on port 80 to port 5000. This eliminates the need to suffix your localhost with :5000 before hitting endpoints.
     * ```--name [name]``` : provides a name for your container. If one is not provided, a random one will be picked out. example: ```--name quizzard-api``` Note you cannot have two containers with the same name. Trying to name your container the same name as an existing container will throw an error and fail to run.
     * example: ```docker run -d -p 80:5000 --name quizzard-api quizzard-api:latest``` : This will run a detached container forwarding port 80 to 5000 with the name quizzard-api using the image quizzard-api:latest. It is not recommended to add a name to your container, as you will have to remove the old container any time you want to run a new image.

## Starting/Stopping container

 * ```docker stop [name | id]``` : stops any currently running container that matches the name provided, or the id provided.
 * ```docker start [name | id]``` : starts any inactive container whose name matches the one provided. Ideally, you will be rebuilding the image running a new container and shouldn't need to use this very often.
 
## Bonus command

The below command combines ```mvn clean package``` and ```docker build```, but takes longer to execute the first time than if the two commands were run separately. This is because it is also building a buildpack image, however after the first run future runs should be quicker. If you are having problems building your docker image and you use this command, switch to just using ```mvn clean package``` and ```docker build```.

```mvn spring-boot:build-image```
