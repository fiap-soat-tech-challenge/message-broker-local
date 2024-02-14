# Message broker local

Este repositório mantem o setup do nosso message broker local para ambiente de desenvolvimento.
Como estamos utilizando o RabbitMQ, esse repositório contém toda a configuração necessária para
iniciar e configurar as filas necessárias.

Importante: Sempre que for desenvolver os microsserviços, você precisa subir o message broker local.
Porque os serviços dependem do mesmo para comuninicação e uso das sagas do SAGA Pattern.

### Pré-requisitos

* Docker com compose
  Veja a [documentação](https://docs.docker.com/engine/install/) para instalar o docker no seu sistema se ainda não tiver instalado.

### Instalação

A instalação é bem simples, siga as seguintes etapas:

1. Clone o repositório
   ```sh
   git clone https://github.com/fiap-soat-tech-challenge/message-broker-local
   ```
2. Entre na pasta do projeto
   ```sh
   cd message-broker-local
   ```
4. Agora execute o projeto usando o docker compose
   ```sh
   docker compose up -d
   ```

Nesse ponto tudo deve estar funcionando, se quiser pode acessar o painel de administração do RabbitMQ
no seguinte endereço http://localhost:15672 e para login use:

- Username: `admin`
- Password: `pass`

### Queues

Acessando a aba **Queues and Streams**, você verá as filas criadas pelo arquivo `definitions.json`, 
fique a vontande para alterar este arquivo conforme a necessidade!
