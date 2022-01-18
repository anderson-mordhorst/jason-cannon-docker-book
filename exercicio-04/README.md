### Exercício 04: Acessando um container em execução

Acessando um container em tempo de execução
>docker run -it --name redis_teste redis /bin/bash
> 
>![](/exercicio-04/images/docker-run-bash.png "docker run -it --name redis_teste redis /bin/bash")

Verificando se o comando bash executa corretamente
>bash --version
> 
>![](/exercicio-04/images/docker-bash-version.png "bash --version")

Verificando se depois do comando **exit** o container continua rodando
>docker ps -a
> 
>![](/exercicio-04/images/docker-ps-a.png "docker ps -a")


Acessando um container já executado
>docker run -dit --name redis_teste redis
> 
>![](/exercicio-04/images/docker-run-redis.png "docker run -dit --name redis_teste redis")

>docker ps
> 
>![](/exercicio-04/images/docker-ps-again.png "docker ps")


Executando comando **bash** no container já iniciado

>docker exec -it redis_teste /bin/bash
> 
>![](/exercicio-04/images/docker-exec-bash.png "docker exec -it redis_teste /bin/bash")

>exit
> 
>![](/exercicio-04/images/exit.png "exit")

>docker ps
> 
>![](/exercicio-04/images/docker-ps-redis.png "docker ps")