### Exercício 05: Construir e enviar uma imagem

Criar uma conta em https://hub.docker.com/

Usuário criado: https://hub.docker.com/u/amordhorst

Depois, criar o arquivo Dockerfile com o seguinte conteúdo

>FROM debian:stable
>
>LABEL maintainer="Anderson Mordhorst"
>
>RUN apt update && apt install -y nano && apt clean
>
>CMD ["/bin/bash"]

Depois construir a imagem no diretório do arquivo dockerfile

>docker build -t amordhorst/nanotest:latest .
> 
>![](/exercicio-05/images/docker-build.png "docker build -t amordhorst/nanotest:latest .")

Listar as imagens
>docker images
> 
>![](/exercicio-05/images/docker-images.png "docker images")

Criar o container docker
>docker run --name nanotest -it amordhorst/nanotest
> 
>![](/exercicio-05/images/docker-run-nano.png "docker run --name nanotest -it amordhorst/nanotest")

Efetuar login no docker hub
>docker login
> 
>![](/exercicio-05/images/docker-login.png "docker login")

Enviar a imagem para a conta do docker hub
>docker push amordhorst/nanotest:latest
> 
>![](/exercicio-05/images/docker-push.png "docker push amordhorst/nanotest:latest")