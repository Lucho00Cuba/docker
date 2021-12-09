

## Traefik v2.1 Proxy Inverso

Traefik en el docker compose ya viene configurado para levantar el servicio son SSL y redireccion de HTTP a HTTPS

En el archivo traefik.yml se encuentra la configuracion del servicio

**------------------------------------------------**

## Dependencias

- ### Crear una Red Docker
    **docker network create traefik_net**

- ### Modificacion de Archivos
    **.env** → Archivo donde se almacenan varibles de entorno. Se tiene que cambiar los "[]" por el Dominio (example.com)
    **user_credentails** → Archivo el cual contendra los usuario y contraseñas, para una implementacion de auth-middlewares

- ### DNS
    **__Tendrian que crear registros DNS "A/PTR" para cada servicio__**


En este caso solo habran tres servicios 

Apache → apache.example.com
Nginx → nginx.example.com
Traefik → traefik.example.com

## Certificado SSl por Lets Encrypt

Archivo autogenerado en la configuracion de traefik

[Documentacion Oficial Traefik](https://traefik.io/traefik/)