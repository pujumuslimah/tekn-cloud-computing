Mulai dengan Susunan Docker

Langkah 1: Pengaturan 🔗
Buat direktori untuk proyek

Starting "default"...
(default) Check network to re-create if needed...
(default) Windows might ask for the permission to configure a dhcp server. Sometimes, such confirmation window is minimized in the taskbar.
(default) Waiting for an IP...
Machine "default" was started.
Waiting for SSH to be available...
Detecting the provisioner...
Started machines may have new IP addresses. You may need to re-run the `docker-machine env` command.
Regenerate TLS machine certs?  Warning: this is irreversible. (y/n): Regenerating TLS certificates
Waiting for SSH to be available...
Detecting the provisioner...
Copying certs to the local machine directory...
Copying certs to the remote machine...
Setting Docker configuration on the remote daemon...



                        ##         .
                  ## ## ##        ==
               ## ## ## ## ##    ===
           /"""""""""""""""""\___/ ===
      ~~~ {~~ ~~~~ ~~~ ~~~~ ~~~ ~ /  ===- ~~~
           \______ o           __/
             \    \         __/
              \____\_______/

docker is configured to use the default machine with IP 192.168.99.100
For help getting started, check out the docs at https://docs.docker.com


Start interactive shell

Lenovo@DESKTOP-RC8LHGO MINGW64 /c/Program Files/Docker Toolbox
$ docker --version
Docker version 19.03.1, build 74b1e89e8a

Lenovo@DESKTOP-RC8LHGO MINGW64 /c/Program Files/Docker Toolbox
$ docker run hello-world

Hello from Docker!
This message shows that your installation appears to be working correctly.

To generate this message, Docker took the following steps:
 1. The Docker client contacted the Docker daemon.
 2. The Docker daemon pulled the "hello-world" image from the Docker Hub.    (amd64)
 3. The Docker daemon created a new container from that image which runs the
    executable that produces the output you are currently reading.
 4. The Docker daemon streamed that output to the Docker client, which sent it
    to your terminal.

To try something more ambitious, you can run an Ubuntu container with:
 $ docker run -it ubuntu bash

Share images, automate workflows, and more with a free Docker ID:
 https://hub.docker.com/

For more examples and ideas, visit:
 https://docs.docker.com/get-started/


Lenovo@DESKTOP-RC8LHGO MINGW64 /c/Program Files/Docker Toolbox
$ docker image ls
REPOSITORY          TAG                 IMAGE ID            CREATED             SIZE
<none>              <none>              de108dc4f937        5 days ago          64.2MB
figletku            latest              40fe66c660de        5 days ago          64.2MB
nginx               latest              ed21b7a8aee9        2 weeks ago         127MB
alpine              latest              a187dde48cd2        3 weeks ago         5.6MB
ubuntu              latest              4e5021d210f6        3 weeks ago         64.2MB
hello-world         latest              fce289e99eb9        15 months ago       1.84kB

Lenovo@DESKTOP-RC8LHGO MINGW64 /c/Program Files/Docker Toolbox
$ hello-world
bash: hello-world: command not found

Lenovo@DESKTOP-RC8LHGO MINGW64 /c/Program Files/Docker Toolbox
$ docker container run hello-world

Hello from Docker!
This message shows that your installation appears to be working correctly.

To generate this message, Docker took the following steps:
 1. The Docker client contacted the Docker daemon.
 2. The Docker daemon pulled the "hello-world" image from the Docker Hub.    (amd64)
 3. The Docker daemon created a new container from that image which runs the
    executable that produces the output you are currently reading.
 4. The Docker daemon streamed that output to the Docker client, which sent it
    to your terminal.

To try something more ambitious, you can run an Ubuntu container with:
 $ docker run -it ubuntu bash

Share images, automate workflows, and more with a free Docker ID:
 https://hub.docker.com/

For more examples and ideas, visit:
 https://docs.docker.com/get-started/


















