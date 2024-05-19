# Docker Basics
**Login to the docker**
```
docker login
```

**Check Docker Version**
```
docker –version
```

**Check Docker Version**
```
docker --version
```

**Check Docker Version**
```
docker –version
```
**List all images**
```
docker images
 ```

**List Running Containers**
```
docker ps
```
 
**To stop any running container**
```
docker stop CONTAINER_ID
```
 
**Start a Stopped Container**
```
docker start CONTAINER_ID
```
 
**Remove a Container**
```
docker rm CONTAINER_ID
```


# Docker Images

**List Docker Images**
```
docker images
 ```

**Pull an Image from Docker Hub**
```
docker pull IMAGE_NAME
```
Ex.  docker pull aniketandhale08/book-recommendation-system:myfirstimagepush

**Build an Image from a Dockerfile**
```
docker build -t IMAGE_NAME .
```
EX.  docker build -t bookrecommendationsystem .
 
**Run the Docker Container**
```
docker run -p localport:containerport aniketandhale08/book-recommendation-system:tagname
```
Ex.  docker run -p 8501:8501 bookrecommendationsystem:latest

**Remove an Image**
```
docker rmi IMAGE_NAME
```



# Docker Hub

**Login to Docker Hub**
```
docker login
```
```
docker logout
```

**Pull an Image from Docker Hub**

- Pulls an image from Docker Hub to your local machine
```
docker pull IMAGE_NAME[:TAG]
```

**Push an Image to Docker Hub**

- Pushes an image from your local machine to Docker Hub.
```
docker push IMAGE_NAME[:TAG]
```


# Tag an Image

 ```
docker tag SOURCE_IMAGE[:TAG] TARGET_IMAGE[:TAG]
```
Ex. docker tag book-recommendation-system:latest aniketandhale08/book-recommendation-system:myfirstimagepush

**Delete an Image from Local Machine**
```
docker rmi IMAGE_NAME[:TAG]
```

# Azure Cloud

## push local image to ACR ##

```
az acr login -n ACRname
```
EX. az acr login -n aniketandhale08

```
docker tag imgname ACRname.azurecr.io/futureimgname:tag
```
Ex. docker tag nginx-simple-website vtechboxacr.azurecr.io/nginx-simple-website:v1

```
docker push ACRname.azurecr.io/futureimgname:tag
```
Ex. docker push vtechboxacr.azurecr.io/nginx-simple-website:v1


## push image docker hub to ACR ##

```
docker login
```

- If you haven't pulled the image yet, you can pull it first to your local machine
```
docker pull IMAGE_NAME[:TAG]
```

- Tag the Image
```
docker tag IMAGE_NAME[:TAG] <ACR_NAME>.azurecr.io/IMAGE_NAME[:TAG]

<ACR_NAME>.azurecr.io/<IMAGE_NAME>:<TAG>
```

```
az acr login --name myacr
```

```
docker push myacr.azurecr.io/myapp:latest
```

**Startup Command**
```
python -m streamlit run app.py --server.port 8000 --server.address 0.0.0.0
```

**The az acr import command allows you to import Docker images from another registry, such as Docker Hub, into your Azure Container Registry. Make sure you have the necessary permissions and credentials to perform this action on Azure.**
```
az acr import -n bookrecommendationsystem --source docker.io/aniketandhale08/book-recommendation-system:myfirstimagepush --image book-recommendation-system:myfirstimagepush

az acr import -n <ACRname> --source docker.io/dockerhubusername/imgname:tag --image imgname:tag
```



# GitHub

## for new project ##
```
git init
```
```
git add .
```
```
git commit -m "Initial commit"
```
```
git remote add origin https://github.com/your-username/your-repository.git
```
```
git push -u origin master
```


## After making changes follow this commands ##
```
git add.
```
```
git commit -m "changes name"
```
```
git push -u origin master
```








