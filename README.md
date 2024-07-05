# Projeto iCasei

Este projeto engloba o frontend e o backend da aplicação iCasei, utilizando Docker Compose para facilitar a execução dos serviços.

## Pré-requisitos

Antes de começar, certifique-se de ter instalado o seguinte:
- Docker: [Instalação do Docker](https://docs.docker.com/get-docker/)
- Node.js e npm (opcional, para desenvolvimento local): [Instalação do Node.js](https://nodejs.org/)

## Configuração do Ambiente

1. Clone o repositório:

    ```bash
    git clone https://github.com/juulioclf/teste_icasei
    cd teste_icasei
    ```

2. Inicialize e atualize os submódulos:

    ```bash
    git submodule update --init --recursive
    ```

3. Crie um arquivo `.env` na raiz do projeto `backend` com as seguintes variáveis de ambiente:

    ```bash
    PORT=3000
    YOUTUBE_API_KEY=sua_api_key_do_youtube
    ```

## Instalação e Execução

1. Construa e inicie os contêineres com Docker Compose:

    ```bash
    docker-compose up --build
    ```

2. Acesse a aplicação:
   - Frontend: [http://localhost:9000](http://localhost:9000)
   - Backend: [http://localhost:3000](http://localhost:3000)

## Estrutura do Projeto

- `frontend`: Submódulo do repositório de frontend.
- `backend`: Submódulo do repositório de backend.
- `docker-compose.yml`: Arquivo de configuração do Docker Compose.

## Comandos Úteis (mas não necessários com docker compose)

### No Diretório `frontend`

- Instalar dependências:
    ```bash
    npm install
    ```

- Executar localmente:
    ```bash
    npm start
    ```

### No Diretório `backend`

- Instalar dependências:
    ```bash
    npm install
    ```

- Executar localmente:
    ```bash
    npm start
    ```

- Executar testes:
    ```bash
    npm test
    ```

## Notas

- Certifique-se de que as portas `9000` e `3000` estão disponíveis no seu ambiente local.
- O banco de dados SQLite está configurado para persistir os dados no diretório `backend/database`.
