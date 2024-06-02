login as docker

mkdir mysql

cd mysql

nano compose.yml

docker-compose up #(autostart)

http://ip-addr:8080/

login:

  server=db

  username=root 
   
  database=mysql
600MB RAM

100MB Swap

2GB HDD

LXC = true