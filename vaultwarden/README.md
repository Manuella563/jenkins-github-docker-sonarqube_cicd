Vaultwarden - still facing https problem with accessing Vaultwarden web-vault.

login as dockerr

mkdir vaultwarden

cd vaultwarden

docker run -d --name vaultwarden -v ./vw-data/:/data/ -p 8022:80 --restart=always vaultwarden/server:latest

http://ip-addr:8022/#/login

150MB RAM

50MB Swap

1GB HDD