# Sample dotnet application
A sample dotnet application built on version 6.0. The web application displays the hosting environment.

```bash
# Build the application using dotnet version 6.0
cd src
dotnet build
# Run the application
dotnet run
```
Dockerize the application.
```bash
# Build the docker image
docker build -t dotnetapp:v1.0.0 .
# Run the docker container locally
docker run --name dotnetapp-container -d -p 8002:80 dotnetapp:v1.0.0
# Test the app
curl http://localhost:8002
# log into the running container 
docker exec -it dotnetapp-container /bin/bash
docker exec -it <container-name> <command>
# Remove the container
docker rm dotnetapp-container -f 
# Remove the image
docker rmi dotnetapp:v1.0.0
```

![alt txt](/images/dotnetapp.jpg)
