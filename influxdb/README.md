login as docker

docker run --name influxdb -p 8086:8086 -v myInfluxVolume:/var/lib/influxdb2 --restart=always influxdb:latest

http://ip-addr:8086/

250MB RAM

50MB Swap

2GB HDD