# docker-command
目次
- [docker-command](#docker-command)
  - [image](#image)
  - [container](#container)
  - [compose](#compose)

## image

* build  
dockerfileからimageを作成する。  
```shell
# docker image build --tag {docker-image-name} {dockerfile-PATH}

docker image build --tag test_image .
```

## container

* run  
image から container を作成する。  
```shell
# docker container run -d -it --name {docker-container-name} {docker-image-name}

docker container run -d -it --name test_container test_image
```

* exec  
起動中の container に入る。  
```shell
docker container exec -it test_container /bin/bash
```

## compose

* up  
docker image と container を作成する。
```shell
docker compose up -d
```