# 💳 Projeto POC - Consulta de Crédito Constituído

Este projeto é uma **Prova de Conceito (POC)** para uma aplicação de **consulta de crédito constituído**, totalmente conteinerizada utilizando **Docker**.

---

## 🚀 Tecnologias Utilizadas

### Backend
- **Java 21**
  - Spring Boot
  - Spring Data JPA
  - Lombok
  - ModelMapper
  - JUnit
  - Mockito
- **Banco de Dados**: PostgreSQL
- **Mensageria**: Apache Kafka

### Frontend
- **Angular 20**
- **Angular Material**

### Infraestrutura
- **Conteinerização**: Docker + Docker Compose

---

## ⚙️ Como Executar o Projeto

### 1. Clone o repositório

```bash
git clone https://github.com/DevGomes/credito-constiuido.git
cd credito-constiuido
```

### 2. Certifique-se de ter o Docker instalado e em execução

Caso ainda não tenha o Docker instalado, acesse: [https://www.docker.com/get-started](https://www.docker.com/get-started)

### 3. Suba a aplicação com Docker Compose

Na raiz do projeto, execute:

```bash
docker-compose up --build
```

### 4. Acessos disponíveis após inicialização

- **Frontend**: [http://localhost:4000/](http://localhost:4000/)
- **Backend (API REST)**: [http://localhost:8081/api/creditos](http://localhost:8081/api/creditos)

---

## 🔁 Monitoramento Kafka

Para visualizar as mensagens consumidas no tópico Kafka (`credito-consultado`), execute o comando:

```bash
docker exec -it kafka kafka-console-consumer --bootstrap-server kafka:9092 --topic credito-consultado --from-beginning
```

---

## 🗄️ Acesso ao Banco de Dados

Você pode acessar o banco de dados via **pgAdmin 4** configurando a conexão com os seguintes dados:

- **Host**: `localhost`
- **Porta**: `5432` (padrão do PostgreSQL)
- **Banco de dados**: `credito_db`
- **Usuário**: `postgres`
- **Senha**: `admin`

---

## 📦 Estrutura Conteinerizada

Todos os serviços (backend, frontend, banco de dados, Kafka, carga inicial no banco) são iniciados automaticamente via `docker-compose`.

---

## 📌 Observações

- Certifique-se de que as portas 4000, 8081 e 5432 estejam livres antes de iniciar a aplicação.
- O tempo de inicialização pode variar conforme a velocidade da sua máquina e internet.

---

## 🧑‍💻 Autor

Breno Gomes  
[LinkedIn](https://www.linkedin.com/in/breno-gomes-772a2431/)

---
