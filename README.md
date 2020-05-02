# postgres11_SR

## Docker build
```
docker build -t centos76_base .
```

## Docker run
```
docker run --privileged \
     -h manager \
     --net=user_defined_nw \
     --ip=192.168.56.100 \
     -d \
     -p 10022:22 \
     -p 10080:80 \
     -p 19100:9100 \
     -p 19090:9090 \
     -p 19187:9187 \
     -p 13000:3000 \
     -p 15432:5432 \
     -v /Users/mitsuo3/repository/postgres/docker_work:/db/work \
     --name manager \
     centos76_base \
     /sbin/init
```
