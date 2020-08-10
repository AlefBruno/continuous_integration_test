# continuous_integration_test

## Pré-Requisitos
* Docker-ce Instalado

### Imagens Docker customizada para o projetos
[DockerHub - Jenkins](https://hub.docker.com/repository/docker/alefbruno/jenkins)
[DockerHub - automation_ruby](https://hub.docker.com/repository/docker/alefbruno/automation_ruby)

### Utilização
* Execute o comando abaixo, para criar um container customizado Jenkins, com alguns pipelines criados e configurados, prontos para execução dos testes.

```
docker container run --name jenkins_default --detach \
   -v jenkins_home:/var/jenkins_home \
   -v jenkins_bkp:/srv/backup \
   -v /var/run/docker.sock:/var/run/docker.sock \
   -p 8080:8080 -p 50000:50000 alefbruno/jenkins:1.0.0

```
  * Após executar o comando, acesse pelo navegador o [Link](localhost:8080)
  
  * Usuário e Senha para acessar o Jenkins
    * User: admin
    * Passwd: admin
    
    * Agora só clicar em Schecule a build do projeto desejado.
    
    
    ### Repositórios associados nos pipelines do Jenkins
    
    [automation_web](https://github.com/AlefBruno/automation_web)
    [automation_api](https://github.com/AlefBruno/automation_api)
    
    
    ## TO DO
    * Incluir testes mobile no pipeline
      [automation_app](https://github.com/AlefBruno/automation_app)

    

