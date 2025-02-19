# Flow-1: Pull Docker Image from Docker Hub and Run it

## Step-1: Verify Docker version and also login to Docker Hub
```
docker version
docker login
```

## Step-2: Pull Image from Docker Hub
```
docker pull stacksimplify/dockerintro-springboot-helloworld-rest-api:1.0.0-RELEASE
```

## Step-3: Run the downloaded Docker Image & Access the Application
- Copy the docker image name from Docker Hub
```
docker run --name app1 -p 80:8080 -d stacksimplify/dockerintro-springboot-helloworld-rest-api:1.0.0-RELEASE
http://localhost/hello
```

## Step-4: List Running Containers
```
docker ps
docker ps -a (lists stopped/Exited containers as well)
docker ps -a -q 
```

## Step-5: Connect to Container Terminal
```
docker exec -it <container-name> /bin/sh
```
## run commands without loggin into the container

By default docker exec command runs in the same working directory set when container was created.

```
docker exec -it <container-name> /bin/sh pwd
```
You can select working directory for the command to execute into
```
docker exec -it -w /root <container-name> /bin/sh ls
/root
```
  
  

## Step-6: Container Stop, Start 
```
docker stop <container-name>
docker start  <container-name>
```

## Step-7: Remove Container 
```
docker stop <container-name> 
docker rm <container-name>
```

## Step-8: Remove Image
```
docker images
docker rmi  <image-id>
```

