# docker-demo

```docker build -t colorapp . ```

```
port   -p your's:docker's
volume -v your's:docker's
```

```docker run --rm -it -p 8000:8080 --name blue-app -e APP_COLOR=blue colorapp```




Got permission denied while trying to connect to the Docker daemon socket at unix:///var/run/docker.sock: 

If want to run docker without using sudo everytime - you need to add your user (who has root privileges) to docker group.

For this run following command

```
sudo groupadd docker
sudo gpasswd -a $USER docker
newgrp docker or (logout/login your system)
docker run hello-world
```
[More Deep Info Here](https://askubuntu.com/questions/477551/how-can-i-use-docker-without-sudo)

## Few Other Important Commands 
---

```docker exec -it <container name> bash```
```docker exec -it <container name> python3```

```docker attach <container name>```
```docker cp mycontainer:/filename.txt filename.txt```
