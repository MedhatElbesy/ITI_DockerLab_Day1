# ITI - Docker Lab 🐋

## Task 1: Working with Docker Hello-world Image
### Objective
Learn how to run a container using the hello-world image and manage containers and images.

### Steps
#### 1. Run a Container with hello-world Image
```bash
docker pull hello-world
```
#### 2. Check Container Status and Explain
```bash
stoped because it didnot do any process
```
#### 3. Start the Stopped Container
```bash
docker start relaxed_elbakyan
```
#### 4. Remove the Container
```bash
docker rm relaxed_elbakyan
```
#### 5. Remove the Image
```bash
 docker rmi d2c94e258dcb
```
---

## Task 2: Running Container with Ubuntu Image
### Objective
Run an Ubuntu container in interactive mode, create a file inside it, and manage containers.

### Steps
#### 1. Run Ubuntu Container in Interactive Mode
```bash
docker run -it 7af9ba4f0a47
```
#### 2. Create a File inside the Container
```bash
touch task
```
#### 3. Stop and Remove the Container
```bash
exit
docker rm intelligent_pare

```
#### 4. Check File Status
```bash
removed
```
#### 5. What happened to hello-docker file?
```bash
removed
```
#### 6. Remove All Stopped Containers
```bash
docker container prune
```
#### 7. Bonus: Remove All Containers in One Command
```bash
docker rm $(docker ps -aq)
```

---
## Task 3: Creating a Custom Nginx Docker Image
### Objective
Create a custom Docker image using Nginx and a local HTML file.

### Steps
#### 1. Create a Local HTML File
```bash
touch file.html
```
#### 2. Write Dockerfile and Copy the HTML file to the Docker Image
```bash
touch Dockerfile
FROM nginx
COPY file.html /usr/share/nginx/html/file.html

docker build -t custom-nginx .
```
#### 3. Run Container with New Image
```bash
docker run -d -p 80:8088 custom-nginx
```

#### 4. Test the Container, open your browser and navigate to http://localhost:8088 to check if everything is okay
```bash
done successfully
```

