## Build
```
$ docker build -t eg_sshd .
```

## Run
```
$ docker run -d -P --name test_sshd eg_sshd
$ docker port test_sshd 22
```
