# DevSecOps-Pro
Notes for future / Exam
> Pull image from DockerHub
```bash
docker pull ubuntu
```
> Hide output using -q 
```bash
docker pull -q alpine
```

> Start container from docker image
```bash
docker run -d --name myubuntu ubuntu
```
> List docker container
```bash
docker ps
```

> to keep docker container running
```bash
docker run -d --name myubuntu -i ubuntu
```

> remove docker container 
```bash
docker rm myubuntu
```
> run command inside a container using exec
```bash
docker exec myubuntu whoami
docker exec -it myubuntu bash
docker exec myubuntu cat /etc/lsb-release
```
> Check Docker Status
```bash
docker ps -a
```
> Show processes running inside a container 
```bash
docker top myubuntu
```

