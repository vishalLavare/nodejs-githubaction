# Dockerized Node.js Application

This is a simple Node.js application that serves "Hello World" on port 3000, running inside a Docker container.

## Prerequisites

- Docker installed on your system.
- Basic understanding of Docker commands.

## Docker Installation Commands for Ubuntu  

1. **Update the Package List:**  
   ```bash
   sudo apt update
   ```
2. **Install the docker:**
   ```bash
    sudo apt install docker.io -y
   ```
3. **Start the Service:**
   ```bash
    sudo service docker start
   ```
4. **Check status of service:**
   ```bash
    sudo service docker status
    sudo systemctl enable docker.service
   ```

## Setting Up the Application

### 1. Create the Project Directory
Create a directory for your project and navigate into it:
```bash
mkdir docker-node-app
cd docker-node-app
```
2. Create the package.json File

```bash
nano package.json
```

3. Create the index.js File

```bash
nano index.js
```
4.Create a Dockerfile to define the Docker image:

```bash
nano Dockerfile
```

5. Build the Docker image for your application:

```bash
docker build -t node-app .
```
6. Run the Docker Container

```bash
docker run -d -p 3000:3000 --name my-node-app node-app
```
# Accessing the Application
Open a browser and go to http://your-public-ip-address:3000 to see your Node.js application running. If running on a remote server, replace localhost with the server's IP address.

## Stopping and Removing the Container
#To stop the container:

```bash
docker stop my-node-app
```
# To remove the container:

```bash
docker rm my-node-app
```
## License
This project is licensed under the MIT License.
