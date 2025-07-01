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