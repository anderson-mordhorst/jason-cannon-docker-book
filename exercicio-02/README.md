### Exercício 02: Usando o **docker run**

Iniciar um container (fazendo o pull caso não exista)
>docker run -d -it redis
>
>![](/exercicio-02/images/docker-run-daemon-redis.png "docker run -d -it redis")

Verificando os containers em execução
>docker ps
>
>![](/exercicio-02/images/docker-ps.png "docker ps")

Iniciando um novo container com nome específico
>docker run -d -it --name redis_teste redis
>
>![](/exercicio-02/images/docker-run-daemon-redis-with-name.png "docker run -d -it --name redis_teste redis")

Verificando os containers em execução
>docker ps
>
>![](/exercicio-02/images/docker-ps-redis.png "docker ps")

Parando o container com novo definido
>docker stop redis_teste
>
>![](/exercicio-02/images/docker-stop-redis-teste.png "docker stop redis_teste")

Verificando os containers em execução
>docker ps
>
>![](/exercicio-02/images/docker-ps-redis-again.png "docker ps")

Excluir automaticamente um container parado
>docker run --rm hello-world
>
>![](/exercicio-02/images/docker-run-remove-hello-workld.png "docker run --rm hello-world")

Verificando se o container foi removido
>docker ps -a
>
>![](/exercicio-02/images/docker-ps--a.png "docker ps -a")

Rodando o container sem a opção **--rm** para validar se não exclui
>docker run hello-world
>
>![](/exercicio-02/images/docker-run-hello-world.png "docker run hello-world")

>docker ps -a
>
>![](/exercicio-02/images/docker-ps--a-again.png "docker ps -a")

Visualizando logs de um container
>docker run --name teste hello-world
>
>![](/exercicio-02/images/docker-run--name-hello-world.png "docker run --name teste hello-world")

>docker ps
>
>![](/exercicio-02/images/docker-ps-hello-world.png "docker ps")

O motivo de não haver um container chamado teste é porque não foi iniciado em modo daemon, portanto ao terminar o container é terminado

Para visualizar as informações do container acima, precisa rodar o comando
>docker ps -a
>
>![](/exercicio-02/images/docker-ps--a-hello-world.png "docker ps -a")

Visualizando os logs do container
>docker logs teste
>
>![](/exercicio-02/images/docker-logs-teste.png "docker logs teste")

Para visualizar os logs com timestamp
>docker logs -t teste
>
>![](/exercicio-02/images/docker-logs--t-teste.png "docker logs -t teste")