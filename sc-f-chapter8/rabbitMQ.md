# docker 提供RabbitMQ

+ 检索
```shell
$ docker search rabbitMQ
INDEX       NAME                                                     DESCRIPTION                                     STARS     OFFICIAL   AUTOMATED
docker.io   docker.io/rabbitmq                                       RabbitMQ is an open source multi-protocol ...   2048      [OK]
docker.io   docker.io/tutum/rabbitmq                                 Base docker image to run a RabbitMQ server      17
docker.io   docker.io/frodenas/rabbitmq                              A Docker Image for RabbitMQ                     12                   [OK]
docker.io   docker.io/bitnami/rabbitmq                               Bitnami Docker Image for RabbitMQ               11                   [OK]
docker.io   docker.io/kbudde/rabbitmq-exporter                       rabbitmq_exporter for prometheus                6                    [OK]
docker.io   docker.io/sysrun/rpi-rabbitmq                            RabbitMQ Container for the Raspberry Pi 2 ...   6
docker.io   docker.io/arm32v7/rabbitmq                               RabbitMQ is an open source multi-protocol ...   5
docker.io   docker.io/gonkulatorlabs/rabbitmq                        DEPRECATED: See maryville/rabbitmq              5                    [OK]
docker.io   docker.io/aweber/rabbitmq-autocluster                    RabbitMQ with the Autocluster Plugin            4
docker.io   docker.io/cyrilix/rabbitmq-mqtt                          RabbitMQ MQTT Adapter                           4                    [OK]
docker.io   docker.io/luiscoms/openshift-rabbitmq                    RabbitMQ docker image to use on Openshift ...   3                    [OK]
docker.io   docker.io/mikaelhg/docker-rabbitmq                       RabbitMQ in Docker.                             3                    [OK]
docker.io   docker.io/authentise/rabbitmq                            A RabbitMQ image that will run a bash scri...   2                    [OK]
docker.io   docker.io/gavinmroy/alpine-rabbitmq-autocluster          Minimal RabbitMQ image with the autocluste...   2
docker.io   docker.io/pivotalrabbitmq/rabbitmq-autocluster           RabbitMQ with the rabbitmq-autocluster plu...   2
docker.io   docker.io/pivotalrabbitmq/rabbitmq-server-buildenv       Image used to build and test RabbitMQ serv...   2
docker.io   docker.io/cvtjnii/rabbitmq                                                                               1
docker.io   docker.io/henrylv206/rabbitmq-autocluster                RabbitMQ Cluster                                1                    [OK]

```
+ 下载

```sh
$ docker pull docker.io/rabbitmq
Using default tag: latest
Trying to pull repository docker.io/library/rabbitmq ...
latest: Pulling from docker.io/library/rabbitmq
be8881be8156: Pull complete
ab96a756674d: Pull complete
1afa3c8b1ac8: Pull complete
206747bbae88: Pull complete
db561c34b75c: Pull complete
a7bbdae386f6: Pull complete
97b38f15a89e: Pull complete
584757cbee20: Pull complete
0647a1654785: Pull complete
4b8b27ad9bb3: Pull complete
d7fca0df083a: Pull complete
f4dee21e0995: Pull complete
Digest: sha256:9bc0b4d778f9839930bf7098bbab5fc427cc2e71f21e70ff6000f41c3ffdd90a
Status: Downloaded newer image for docker.io/rabbitmq:latest
```
+ 创建镜像

```sh
$ docker images
REPOSITORY                         TAG                 IMAGE ID            CREATED             SIZE
docker.io/rabbitmq                 latest              dc1744b237f9        3 days ago          125 MB

$ docker run -d  -p 5671:5671 -p 5672:5672  -p 15672:15672 -p 15671:15671  -p 25672:25672  -v /data/rabbitmq-data/:/var/rabbitmq/lib  --name rabbitmq   dc1744b237f9
3cbfcc92631e3a467bb72979ad7bb770d28c25848fb83e45dcee18519d028771

```