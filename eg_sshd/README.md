# Dockerfile SSH service
The following Dockerfile sets up a SSHd service in a container that you can use to connect to and inspect other container's volumes, or to get access a quick test container.

## Build
```
$ docker build -t eg_sshd .
```

## Run
```
$ docker run -d -P --name test_sshd eg_sshd
$ docker port test_sshd 22
```

## Connection
```
$ ssh root@192.168.1.2 -p 49154
# or
$ ssh root@localhost -p 49154
# The password is ``root``.
root@f38c87f2a42d:/#
```

### More information
* [SSH Service](https://docs.docker.com/engine/examples/running_ssh_service/) - Tutorial labs from [Docker Docs](https://docs.docker.com/).
