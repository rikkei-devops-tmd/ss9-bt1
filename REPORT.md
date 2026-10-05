BAI 1: KIEM TRA CAI DAT DOCKER ENGINE VA CHAY CONTAINER HELLO-WORLD

1. MUC TIEU
- Thuc hanh chay cac lenh kiem tra phien ban Docker CLI va Docker Server.
- Kiem tra ket noi toi Docker Daemon khong can tien to sudo.
- Khoi chay container dau tien tren may ca nhan bang image hello-world.

2. BOI CANH VA CAU HINH PHAN QUYEN DOCKER
- Neu user hien tai chua co quyen goi Docker Daemon truc tiep:
```bash
sudo usermod -aG docker $USER && newgrp docker
```
- Kiem tra ket noi Docker Daemon khong can quyen root / sudo:
```bash
docker info
```

3. CAC LENH THUC HIEN VA KET QUA TERMINAL

3.1. Kiem tra phien ban Docker CLI va Server (docker version)
Lenh thuc hien:
```bash
docker version
```
Ket qua dau ra Terminal:
```text
Client: Docker Engine - Community
 Version:           27.3.1
 API version:       1.47
 Go version:        go1.22.7
 Git commit:        ce12230
 Built:             Fri Sep 20 11:41:00 2024
 OS/Arch:           linux/amd64
 Context:           default

Server: Docker Engine - Community
 Engine:
  Version:          27.3.1
  API version:      1.47 (minimum version 1.24)
  Go version:       go1.22.7
  Git commit:       4123218
  Built:            Fri Sep 20 11:41:00 2024
  OS/Arch:          linux/amd64
  Experimental:     false
 containerd:
  Version:          1.7.22
  GitCommit:        7f7fdf5fed64eb6a7caf99b3e12efcf9d60e311c
 runc:
  Version:          1.1.14
  GitCommit:        v1.1.14-0-g2c9f560
 docker-init:
  Version:          0.19.0
  GitCommit:        de40ad0
```

3.2. Kiem tra thong tin chi tiet he thong Docker (docker info)
Lenh thuc hien:
```bash
docker info
```
Ket qua dau ra Terminal:
```text
Client: Docker Engine - Community
 Version:    27.3.1
 Context:    default
 Debug Mode: false

Server:
 Containers: 0
  Running: 0
  Paused: 0
  Stopped: 0
 Images: 1
 Server Version: 27.3.1
 Storage Driver: overlay2
  Backing Filesystem: extfs
  Supports d_type: true
  Using metacopy: false
 Logging Driver: json-file
 Cgroup Driver: systemd
 Cgroup Version: 2
 Plugins:
  Volume: local
  Network: bridge host ipvlan macvlan null overlay
  Log: awslogs fluentd gcplogs gelf journald json-file local splunk syslog
 Operating System: Ubuntu 22.04.5 LTS
 OSType: linux
 Architecture: x86_64
 CPUs: 4
 Total Memory: 7.742GiB
 Docker Root Dir: /var/lib/docker
 Live Restore Enabled: false
```

3.3. Khoi chay container dau tien (docker run hello-world)
Lenh thuc hien:
```bash
docker run hello-world
```
Ket qua dau ra Terminal:
```text
Unable to find image 'hello-world:latest' locally
latest: Pulling from library/hello-world
c1ec31eb5944: Pull complete 
Digest: sha256:305243d734571da2d100c8c8b3c3140a61152246bea3963d60b01b49ecf277e0
Status: Downloaded newer image for hello-world:latest

Hello from Docker!
This message shows that your installation appears to be working correctly.

To generate this message, Docker took the following steps:
 1. The Docker client contacted the Docker daemon.
 2. The Docker daemon pulled the "hello-world" image from the Docker Hub.
    (amd64)
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
```

4. KET LUAN
- Docker Engine da duoc cai dat dung cach va Docker Daemon dang hoat dong binh thuong.
- User da co the tuong tac voi Docker CLI khong can sudo.
- Container hello-world da tai thanh cong va in ra chuoi xac nhan hoat dong chinh xac.
