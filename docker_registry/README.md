login as dockerr

$ mkdir -p /docker_registry/data ==> Contents for data_dir will be autogenerated

$ cd docker_registry

$ nano compose.yml

$ docker-compose up #(autostart)

http://ip-addr:5000/v2/_catalog ## To view active repositories

200MB RAM

50MB Swap

1GB HDD