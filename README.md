# Microserviços com Node.js - Rocketseat

Este projeto foi desenvolvido durante o evento de Microserviços da Rocketseat, onde exploramos conceitos avançados de arquitetura distribuída e comunicação entre serviços.

## 🚀 Sobre o Projeto

Este é um projeto de estudo que implementa uma arquitetura de microserviços utilizando Node.js. O sistema é composto por diferentes serviços que se comunicam entre si através de mensageria (RabbitMQ) e são gerenciados por um API Gateway (Kong).

## 🏗️ Arquitetura

O projeto é composto pelos seguintes serviços:

- **API Gateway (Kong)**: Gerencia o roteamento e as requisições entre os serviços
- **Serviço de Pedidos (app-orders)**: Gerencia os pedidos do sistema
- **Serviço de Faturas (app-invoices)**: Processa as faturas dos pedidos
- **Message Broker (RabbitMQ)**: Gerencia a comunicação assíncrona entre os serviços
- **Jaeger**: Sistema de tracing distribuído para monitoramento

## 🛠️ Tecnologias Utilizadas

- Node.js
- TypeScript
- Docker
- Docker Compose
- RabbitMQ
- Kong API Gateway
- Jaeger (OpenTelemetry)

## 📋 Pré-requisitos

Para executar este projeto, você precisará ter instalado:

- Docker
- Docker Compose
- Node.js (versão 22 ou superior)
- npm ou yarn

## 🔧 Instalação e Execução

1. Clone o repositório:
```bash
git clone [https://github.com/GabrielVitorSilva/microservice_node_rocketseat]
cd microservice_node_rocketseat
```

2. Inicie os serviços de infraestrutura:
```bash
docker-compose up -d
```

3. Instale as dependências dos serviços:
```bash
# No diretório app-orders
cd app-orders
npm install

# No diretório app-invoices
cd ../app-invoices
npm install
```

4. Inicie os serviços:
```bash
# Em um terminal, inicie o serviço de pedidos
cd app-orders
npm run dev

# Em outro terminal, inicie o serviço de faturas
cd app-invoices
npm run dev
```

## 🌐 Acessando os Serviços

- API Gateway: http://localhost:8000
- Kong Admin UI: http://localhost:8002
- RabbitMQ Management: http://localhost:15672
- Jaeger UI: http://localhost:16686

## 📚 Aprendizados

Durante o desenvolvimento deste projeto, foram abordados conceitos importantes como:

- Arquitetura de Microserviços
- Comunicação Assíncrona
- API Gateway
- Message Broker
- Distributed Tracing
- Containerização
- Orquestração de Containers

## 🤝 Contribuindo

Este é um projeto de estudo, mas sinta-se à vontade para contribuir com melhorias através de Pull Requests.

## 📝 Licença

Este projeto foi desenvolvido como parte do evento de Microserviços da Rocketseat e está sob a licença MIT. 