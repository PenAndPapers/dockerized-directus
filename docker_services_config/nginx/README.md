#### Configurations for nginx

#### It's not necessary to add self signed certificate in local development

#### Follow this tutorial for generating self signed certificates for nginx
[How to created self signed ssl certificate for nginx](https://www.digitalocean.com/community/tutorials/how-to-create-a-self-signed-ssl-certificate-for-nginx-in-ubuntu-16-04)

#### Generate self signed certificate
```sudo openssl req -x509 -nodes -days 365 -newkey rsa:2048 -keyout docker_services_config/nginx/cert/nginx-selfsigned.key -out docker_services_config/nginx/cert/nginx-selfsigned.crt```

#### Generate Diffie-Hellman
```sudo openssl dhparam -dsaparam -out docker_services_config/nginx/cert/dhparam.pem 2048```