### Exercício 06: Gerenciando volumes no docker

Criar um volume no docker
>docker volume create local_volume
> 
>![](/exercicio-06/images/docker-create-volume.png "docker volume create local_volume")

Inspecionar o volume criado
>docker volume inspect local_volume
> 
>![](/exercicio-06/images/docker-volume-inspect.png "docker volume inspect local_volume")

Criar um arquivo de exemplo e salvar no local do volume criado (usar usuário **root**)
>echo "This file exists" > ../var/lib/docker/volumes/local_volume/_data/file.txt 
> 
>![](/exercicio-06/images/criar-arquivo-volume.png)

Rodar um container e associar ao volume criado na pasta /data do container
>docker run -d --name teste_volume --mount src=local_volume,dst=/data httpd 
> 
>![](/exercicio-06/images/docker-run-mount.png "docker run -d --name teste_volume --mount src=local_volume,dst=/data httpd")

Executar o bash no container para acessar o arquivo
>docker exec -it teste_volume /bin/bash
> 
>![](/exercicio-06/images/docker-exec.png "docker exec -it teste_volume /bin/bash")

Acessar o arquivo
>
> df -h
>
> cat /data/file.txt
> 
>![](/exercicio-06/images/cat-file.png)

Criando um arquivo de dentro do container
>echo "Created from  inside de container" > /data/from-container.txt
>
>![](/exercicio-06/images/create-file-from-container.png)


Acessando o arquivo criado de fora do container
>sudo -i
>
>cat ../var/lib/docker/volumes/local_volume/_data/from-container.txt
> 
>![](/exercicio-06/images/access-other-file-outside-container.png)

Criando outros tipos de volumes
>docker run -d --name temp_volume --mount type=tmpfs,dst=/temp_data httpd
> 
>![](/exercicio-06/images/docker-run-other-volume.png)

Analisando o volume criado
>docker inspect temp_volume | grep Mounts -A10
> 
>![](/exercicio-06/images/docker-inspect.png)