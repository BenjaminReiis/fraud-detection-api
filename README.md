# 🚨 Real-Time Fraud Detection API

<p align="center">

<img src="https://img.shields.io/badge/Python-3.11+-3776AB?style=for-the-badge&logo=python&logoColor=white"/>
<img src="https://img.shields.io/badge/FastAPI-Framework-009688?style=for-the-badge&logo=fastapi&logoColor=white"/>
<img src="https://img.shields.io/badge/JWT-Authentication-000000?style=for-the-badge&logo=jsonwebtokens"/>
<img src="https://img.shields.io/badge/Uvicorn-ASGI_Server-499848?style=for-the-badge"/>
<img src="https://img.shields.io/badge/Render-Cloud-46E3B7?style=for-the-badge&logo=render"/>
<img src="https://img.shields.io/badge/License-MIT-success?style=for-the-badge"/>

</p>

---

# 🚀 Overview

**Real-Time Fraud Detection API** é uma API REST desenvolvida para simular sistemas modernos de **detecção de fraude financeira em tempo real**.

O projeto reproduz conceitos encontrados em plataformas bancárias e fintechs, utilizando autenticação segura, análise inteligente de transações, versionamento de API e arquitetura backend escalável.

Foi desenvolvido com foco em **boas práticas de Engenharia de Software**, organização de código e construção de APIs profissionais.

---

# 🌐 Live Demo

## 🚀 API Online

> https://fraud-detection-api-jvwk.onrender.com

## 📖 Swagger Documentation

> https://fraud-detection-api-jvwk.onrender.com/docs

## 💻 Website

> https://benjaminreiis.github.io/fraud-detection-api/

---

# ✨ Principais Recursos

## 🔐 Segurança

* Autenticação JWT
* Rotas protegidas
* Validação de tokens
* Controle de acesso
* Middleware de autenticação

---

## 🚨 Detecção de Fraude

* Análise de transações em tempo real
* Score de risco
* Classificação automática
* Regras inspiradas em Machine Learning
* Identificação de comportamento suspeito

---

## 📊 Monitoramento

* Consulta por usuário
* Histórico de análises
* Status das transações
* Health Check
* API Versioning

---

## ⚙ Backend

* Tratamento global de exceções
* Arquitetura modular
* Validação de dados
* Respostas padronizadas
* Código escalável

---

# 🛠 Stack Tecnológica

## Backend

* Python
* FastAPI
* Uvicorn

## Segurança

* JWT
* PyJWT

## Deploy

* Render

## Documentação

* Swagger UI
* OpenAPI

---

# 🧠 Como Funciona a Detecção de Fraude

Cada transação enviada para a API passa por um mecanismo de análise baseado em regras inspiradas em sistemas de Machine Learning.

São avaliados diversos fatores para determinar o nível de risco da operação:

* 💰 Valor da transação
* ⏱ Frequência de operações
* 🌍 Localização geográfica
* 🕒 Horário da transação
* 👤 Comportamento do usuário
* 📈 Padrões de movimentação financeira

Após a análise, a API retorna uma classificação indicando se a transação apresenta baixo, médio ou alto risco de fraude.

---

# 🔐 Fluxo de Autenticação

## 1️⃣ Login

```http
POST /v1/auth/login
```

```json
{
  "username": "usuario",
  "password": "senha"
}
```

---

## 2️⃣ Resposta

```json
{
  "token": "jwt_token"
}
```

---

## 3️⃣ Utilização

Envie o token em todas as requisições protegidas.

```http
Authorization: Bearer <jwt_token>
```

---

# 📡 Endpoints

## 🔐 Autenticação

```http
POST /v1/auth/login
```

Realiza o login do usuário e retorna um token JWT.

---

## 💳 Transações

```http
POST /v1/transactions
```

Analisa uma nova transação em tempo real.

---

```http
GET /v1/transactions/status/{user_id}
```

Consulta todas as análises realizadas para um usuário.

---

## ❤️ Monitoramento

```http
GET /health
```

Retorna o status da aplicação.

---

# 🏗 Arquitetura

```text
fraud-detection-api
│
├── app/
│
├── api/
│   └── v1/
│       ├── auth.py
│       └── transactions.py
│
├── core/
│   ├── security.py
│   ├── fraud_rules.py
│   └── exceptions.py
│
├── models/
├── schemas/
├── services/
├── utils/
│
├── main.py
├── requirements.txt
└── README.md
```

---

# 🚀 Como Executar

## 1️⃣ Clonar o projeto

```bash
git clone https://github.com/benjaminreiis/fraud-detection-api.git
```

---

## 2️⃣ Entrar na pasta

```bash
cd fraud-detection-api
```

---

## 3️⃣ Criar ambiente virtual

### Linux / macOS

```bash
python -m venv venv
source venv/bin/activate
```

### Windows

```bash
venv\Scripts\activate
```

---

## 4️⃣ Instalar dependências

```bash
pip install -r requirements.txt
```

---

## 5️⃣ Executar a aplicação

```bash
uvicorn main:app --reload
```

---

## 6️⃣ Acessar

API

```
http://localhost:8000
```

Swagger

```
http://localhost:8000/docs
```

---

# 📁 Estrutura do Projeto

```text
fraud-detection-api/
│
├── app/
│   ├── api/
│   │   └── v1/
│   │       ├── auth.py
│   │       └── transactions.py
│   │
│   ├── core/
│   │       ├── security.py
│   │       ├── fraud_rules.py
│   │       └── exceptions.py
│   │
│   ├── models/
│   ├── schemas/
│   ├── services/
│   └── utils/
│
├── main.py
├── requirements.txt
└── README.md
```

---

# ☁ Deploy

O projeto está publicado na plataforma **Render**, utilizando deploy automático sempre que uma nova versão é enviada para a branch principal.

### 🌍 API

https://fraud-detection-api-jvwk.onrender.com

### 📖 Swagger

https://fraud-detection-api-jvwk.onrender.com/docs

---

# 🧠 Conceitos de Engenharia Aplicados

* REST API Design
* FastAPI Architecture
* JWT Authentication
* API Versioning
* Rule-Based Fraud Detection
* Request Validation
* Exception Handling
* Dependency Injection
* Layered Architecture
* Clean Code
* SOLID Principles
* Health Monitoring
* OpenAPI Specification
* Secure API Development
* Backend Best Practices

---

# 🎯 Objetivos do Projeto

Este projeto foi desenvolvido para demonstrar conhecimentos em:

* Desenvolvimento Backend com Python
* APIs REST de alta performance
* Sistemas Financeiros
* Segurança com JWT
* Arquitetura Escalável
* Engenharia de Software
* Organização de código profissional
* Documentação automática de APIs

---

# 👨‍💻 Autor

## Benjamin Dos Reis

**Backend Engineer**

Especializado em:

* Python
* Java
* FastAPI
* Spring Boot
* Sistemas Financeiros
* APIs REST
* Microsserviços
* Cloud Computing
* Docker
* PostgreSQL
* Redis

---

# 📄 Licença

Distribuído sob a licença **MIT**.

Sinta-se livre para utilizar, estudar e contribuir com este projeto.

---

<div align="center">

### ⭐ Se este projeto foi útil, considere deixar uma estrela no repositório!

**Construído com foco em arquitetura backend moderna e sistemas financeiros de alta confiabilidade. 🚀**

</div>
