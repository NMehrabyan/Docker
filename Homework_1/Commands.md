## Homework
* create bridge network named MyNetwork
* create docker file for Nginx based on ubuntu image
* build image
* run container from that image in  MyNetwork  to listen port 8080
* run ubuntu container from ubuntu image in MyNetwork 
* try to reach Nginx container by hostname

### Create a Bridge Network
  ```sh
    docker network create MyNetwork
  ```

### Build the Docker Image
  ```sh
    docker build -t my-nginx .
  ```
### Run the Nginx Container
  ```sh
    docker run -d --name nginx-container --network MyNetwork -p 8080:80 my-nginx
  ```
###  Run an Ubuntu Container

```sh
   docker run -it --name ubuntu-container --network MyNetwork ubuntu
```	

### Try to Reach Nginx Container by Hostname
```sh
	apt-get update && apt-get install -y dnsutils nslookup nginx-container
```












