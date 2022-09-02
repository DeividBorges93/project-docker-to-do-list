# Boas-vindas ao repositório do projeto Docker Todo List!

Neste projeto eu:

1. **_Conteinerizei_** aplicações;
1. Crei uma conexão entre elas;
1. Orquestrei seu funcionamento.

Temos uma aplicação full-stack neste repositório: um **aplicativo de tarefas**! Esta aplicação precisa ser conteinerizada para funcionar. Eu desenvolvi os arquivos de configuração para cada frente específica: `Front-end`, `Back-end` e, no nosso caso, para um aplicativo de `teste` que valida se as aplicações estão se comunicando.

Eu criei as imagens para as aplicações e configurei essas imagens com o `docker-compose`.

Para isto, utilizei uma série de comandos do `docker` com diferentes níveis de complexidade.

Para isto, segui os seguintes passos:

1. Criei um arquivo chamado `commandN.dc` no diretório `docker-commands`, onde `N` é o número do requisito. Por exemplo:

    ```text
    Requisito 1: ./docker/docker-commands/command01.dc
    Requisito 2: ./docker/docker-commands/command02.dc
    Requisito 3: ./docker/docker-commands/command03.dc
    ```

2. Escrevi neste arquivo o comando do CLI *(Interface de Linha de Comando)* do Docker que resolve o requisito. Um exemplo de como fica o arquivo:

    ```dc
    docker network inspect bridge
    ```

Os arquivos principais do projeto estão na pasta `docker`, na raiz do projeto. Nela estão contidos:

1. Pasta `docker-commands`: onde ficam os comandos;
   - Por exemplo, se você precisa referenciar um caminho em um comando, você deve assumir que sua pasta raiz esta partindo de `./docker`.
2. Pasta `todo-app`: onde fica a nossa **pseudo-aplicação**, que servirá como base para nossos `Dockerfile's` e `Compose`;
   - **⚠️ Essa aplicação conta com um [**README.md**](./docker/todo-app/README.md) próprio!**

</details>

### Comandos docker

#### 1. Cria um container em modo interativo, sem rodá-lo, nomeando-o como `01container` e utilizando a imagem `alpine` na versão `3.12`

#### 2. Inicia o container `01container`

#### 3. Lista os containers filtrando pelo nome `01container`

#### 4. Executa o comando `cat /etc/os-release` no container `01container` sem se acoplar a ele

#### 5. Remove o container `01container`

#### 6. Faz o download da imagem `nginx` com a versão `1.21.3-alpine` sem criar ou rodar um container

#### 7. Roda um novo container com a imagem  `nginx` com a versão `1.21.3-alpine` em segundo plano nomeando-o como `02images` e mapeando sua porta padrão de acesso para porta `3000` do sistema hospedeiro

#### 8. Para o container `02images` que está em andamento

### Dockerfile

**⚠️ As aplicações a seguir contam com um [**README.md**](./docker/todo-app/README.md) próprio!**

#### 9. Gera uma build a partir do Dockerfile do `back-end` do `todo-app` nomeando a imagem para `todobackend`

#### 10. Gera uma build a partir do Dockerfile do `front-end` do `todo-app` nomeando a imagem para `todofrontend`

#### 11. Gera uma build a partir do Dockerfile dos `testes` do `todo-app` nomeando a imagem para `todotests`

### Docker-compose

#### 12. Sobe uma orquestração em segundo plano com o docker-compose de forma que `backend`, `frontend` e `tests` consigam se comunicar


## O que eu aprendi com esse projeto?

- Além de fixar meus aprendizados em Docker, como seus conceitos e comandos de manipulação de containers e imagens, consigo ter uma noção mais aprofundada mesmo que introdutória sobre a comunicação entre serviços, como no caso, front-end e back-end.

## Novas habilidades adquiridas através do projeto

- Criar um container Docker para uma aplicação de front-end;
- Criar um container Docker para uma aplicação de back-end;
- Criar um container Docker para uma aplicação de testes;
- Orquestrar os três containers com o uso do Docker compose.
