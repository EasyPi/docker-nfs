nfs
===

[NFS-Ganesha][1] is an NFSv3,v4,v4.1 fileserver that runs in user mode on most UNIX/Linux systems.

> :warning: ~90 seconds to sync.

```bash
# server
$ mkdir data
$ docker-compose up -d
$ echo hello > data/hello.txt

# client
$ sudo mkdir /mnt/data
$ sudo mount.nfs4 -v 127.0.0.1:/mnt/data
$ cat /mnt/data/hello.txt
```

[1]: https://github.com/nfs-ganesha/nfs-ganesha
