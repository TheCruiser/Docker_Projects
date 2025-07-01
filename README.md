## Installation Process for Docker

https://github.com/iam-veeramalla/Docker-Zero-to-Hero?tab=readme-ov-file#install-docker

## Docker Networking Example:

### Created two containers in a single host, i.e. login and logout
![docker ps](./imgs/image.png)

### Now once I do 'docker inspect', the IPs assigned to these are 

![login](./imgs/image-1.png)
![logout](./imgs/image-2.png)

### Now went on to ping both containers from each other. They're accessible.
![pingable to self and other container](./imgs/image-3.png)

But this is a security risk if any sensitive information is stored in either of the containers.

### Let's imagine a 'Finance' container which has to be isolated from other containers

### Created a separate network first - default one will be bridge network
![alt text](./imgs/image-5.png)

![alt text](./imgs/image-6.png)

### Created a new container called 'finance' which need to be isolated
![alt text](./imgs/image-7.png)

### it will come up with different subnet of network + different network as we've set it
![alt text](./imgs/image-8.png)

### So now when I try to ping it from login or logout container, it won't be successful
![alt text](./imgs/image-9.png)

## This is the Docker networking in a secured way, summed up !!!