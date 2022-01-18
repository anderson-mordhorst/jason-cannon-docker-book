### Exercício 02: Expondo portas do container

Rodar o docker mapeando a porta 9900 para 80
>docker run --name apache -d -p 9900:80 httpd:latest
> 
>![](/exercicio-03/images/docker-run-apache.png "docker run --name apache -d -p 9900:80 httpd:latest")

Verificando se a porta foi especificada corretamente
>docker ps
> 
>![](/exercicio-03/images/docker-ps-check-port.png "docker ps")

Verificar se a aplicação atende na porta especificada
>curl http://localhost:9900
> 
>![](/exercicio-03/images/curl-localhost-9900.png "curl http://localhost:9900")
>![](/exercicio-03/images/acessing-web-page.png "Acessando pelo navegador")
