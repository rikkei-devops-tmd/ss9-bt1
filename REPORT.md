BAI 1: KIEM TRA CAI DAT DOCKER ENGINE VA CHAY CONTAINER HELLO-WORLD

1. MUC TIEU
- Thuc hanh chay cac lenh kiem tra phien ban Docker CLI va Docker Server.
- Kiem tra ket noi toi Docker Daemon khong can tien to sudo.
- Khoi chay container dau tien tren may ca nhan bang image hello-world.

2. BOI CANH VA CAU HINH PHAN QUYEN DOCKER
- Bối cảnh thực tế trên máy chủ Ubuntu 24.04 LTS (User duc_devops).
- Neu user hien tai chua co quyen goi Docker Daemon truc tiep:
```bash
sudo usermod -aG docker $USER && newgrp docker
```
- Kiem tra ket noi Docker Daemon khong can quyen root / sudo:
```bash
docker info
```

3. CAC LENH THUC HIEN VA KET QUA TERMINAL THUC TE

3.1. Kiem tra phien ban Docker CLI va Server (docker version)
Lenh thuc hien:
```bash
docker version
```
Ket qua dau ra Terminal:
```text
Client: Docker Engine - Community
 Version:           29.9.0
 API version:       1.56
 Go version:        go1.26.9
 Git commit:        f415da8
 Built:             Thu Oct  8 20:38:42 2026
 OS/Arch:           linux/amd64
 Context:           default

Server: Docker Engine - Community
 Engine:
  Version:          29.9.0
  API version:      1.56 (minimum version 1.40)
  Go version:       go1.26.9
  Git commit:       a5b58c9
  Built:            Thu Oct  8 20:38:42 2026
  OS/Arch:          linux/amd64
  Experimental:     false
 containerd:
  Version:          v2.4.1
  GitCommit:        f2551031d7276a770f65f98c9b52e57e7dad07e8
 runc:
  Version:          1.5.2
  GitCommit:        v1.5.2-0-g29dd3dc2
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
 Version:    29.9.0
 Context:    default
 Debug Mode: false
 Plugins:
  buildx: Docker Buildx (Docker Inc.)
    Version:  v0.38.0
    Path:     /usr/libexec/docker/cli-plugins/docker-buildx
  compose: Docker Compose (Docker Inc.)
    Version:  v5.6.0
    Path:     /usr/libexec/docker/cli-plugins/docker-compose

Server:
 Containers: 1
  Running: 0
  Paused: 0
  Stopped: 1
 Images: 4
 Server Version: 29.9.0
 Storage Driver: overlayfs
  driver-type: io.containerd.snapshotter.v1
 Logging Driver: json-file
 Cgroup Driver: systemd
 Cgroup Version: 2
 Plugins:
  Volume: local
  Network: bridge host ipvlan macvlan null overlay
  Log: awslogs fluentd gcplogs gelf journald json-file local splunk syslog
 CDI spec directories:
  /etc/cdi
  /var/run/cdi
 Swarm: inactive
 Runtimes: runc io.containerd.runc.v2
 Default Runtime: runc
 Init Binary: docker-init
 containerd version: f2551031d7276a770f65f98c9b52e57e7dad07e8
 runc version: v1.5.2-0-g29dd3dc2
 init version: de40ad0
 Security Options:
  apparmor
   Profile: default
  seccomp
   Profile: builtin
  cgroupns
 Kernel Version: 6.8.0-31-generic
 Operating System: Ubuntu 24.04.5 LTS
 OSType: linux
 Architecture: x86_64
 CPUs: 2
 Total Memory: 1.875GiB
 Name: 10320102126523343
 ID: 8aa8d2a9-12ab-4752-b4c4-b5a317c76e97
 Docker Root Dir: /var/lib/docker
 Debug Mode: false
 Experimental: false
 Insecure Registries:
  127.0.0.0/8
  ::1/128
 Live Restore Enabled: false
 Firewall Backend: iptables
  EnableUserlandProxy: true
  UserlandProxyPath: /usr/bin/docker-proxy
```

3.3. Khoi chay container dau tien (docker run hello-world)
Lenh thuc hien:
```bash
docker run hello-world
```
Ket qua dau ra Terminal:
```text
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
- User duc_devops da duoc gan vao nhom docker va tuong tac truc tiep khong can sudo.
- Container hello-world chay thanh cong va in ra chuoi xac nhan hoat dong chinh xac.
