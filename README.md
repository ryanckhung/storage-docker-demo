1. Create the docker volume locally

### `docker volume create data_volume`

### `docker volume ls`

2. Create a nginx container (edit a file in the volume)

### `docker run -d -p 8080:80 --name nginx -v data_volume:/home nginx`

### `docker exec -it nginx bash`

### `cd home`

### `touch index.html`

### `exit`

3. delete the nginx container

### `docker stop nginx`

### `docker rm nginx`

4. Creaet a new nginx container and see if the /home/index.html exist

### `docker run -d -p 8080:80 --name nginx -v data_volume:/home nginx`

### `docker exec -it nginx bash`

### `cd home`

### 'ls'
