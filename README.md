# singularity-docker-centos7-calibre
calibre singularity container on CentOS-7

```
singularity run shub://truatpasteurdotfr/singularity-docker-centos7-calibre
or ln -s truatpasteurdotfr-singularity-docker-centos7-calibre,img ~/bin/calibre
```

Since calibre version 4.x, the requirements for running calibre are no longer met on CentOS-7 :(
```
`You need GLIBC 2.18 or higher and libstdc++.so.6.0.21 (from gcc 5.4.0) or higher to run calibre`.
```

You will only be able to get version 3.x starting from 2019/12.
