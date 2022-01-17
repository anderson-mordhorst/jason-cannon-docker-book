### Exercício 01: **Fazer download e remover docker images**

Fazer download de duas imagens: memcached e httpd  
>docker pull memcached:latest
>
>![](/exercicio-01/images/docker-pull-memcached.png "docker pull memcached")

>docker pull httpd:2-alpine
> 
>![](/exercicio-01/images/docker-pull-httpd:2-alpine.png "docker pull httpd:2-alpine")

Verificar as imagens
>docker images
>
>![](/exercicio-01/images/docker-images.png "docker images")

Verificar espaço em disco
>docker system df
>
>![](/exercicio-01/images/docker-system-df.png "docker system df")


Excluir as imagens
>docker rmi memcached
>
>![](/exercicio-01/images/docker-rmi-memcached.png "docker rmi memcached")

>docker rmi httpd:2-alpine
>
>![](/exercicio-01/images/docker-rmi-httpd:2-alpine.png "docker rmi httpd:2-alpine")

Listar as imagens novamente
>docker images
>
>![](/exercicio-01/images/docker-images-final.png "docker images")