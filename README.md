🚨 Real-Time Fraud Detection API

API de detecção de fraude em tempo real desenvolvida com foco em arquitetura de backend profissional.

PythonFastAPIJWTRender

🔗 Links
API Online: https://fraud-detection-api-jvwk.onrender.com
Documentação (Swagger): https://fraud-detection-api-jvwk.onrender.com/docs
Site do Projeto: https://benjaminreiis.github.io/fraud-detection-api/

💡 Sobre o Projeto
Este projeto simula como sistemas financeiros analisam transações bancárias para detectar possíveis fraudes em tempo real.

A aplicação foi construída utilizando boas práticas de desenvolvimento backend, incluindo autenticação segura com JWT, versionamento de API e tratamento global de erros — reproduzindo o comportamento de plataformas financeiras utilizadas em produção.

🚀 Funcionalidades
🔐 Autenticação com JWT
💳 Análise de transações em tempo real
🚨 Detecção de fraude baseada em regras
📊 Consulta de status por usuário
🧠 Lógica inspirada em Machine Learning
🛠️ Tratamento global de erros
❤️ Health check para monitoramento
🔄 Versionamento de API (/v1)
🧱 Tecnologias Utilizadas
Python — linguagem principal do projeto
FastAPI — framework web para construção da API REST
Uvicorn — servidor ASGI de alta performance
PyJWT — geração e validação de tokens JWT
Render — plataforma de deploy em cloud
🔐 Como Funciona a Autenticação
1. Faça login para obter o token
http 
POST /v1/auth/login
json 
{
  "username": "seu_usuario",
  "password": "sua_senha"
}
2. A API retorna um token JWT
json 
{
  "token": "seu_token_aqui"
}
3. Use o token nos endpoints protegidos
Envie o token via header em todas as requisições autenticadas:

authorization: seu_token_aqui
📡 Endpoints Principais
Autenticação
POST /v1/auth/login
Realiza o login e retorna um token JWT.

Transações
POST /v1/transactions
Submete uma transação para análise de fraude em tempo real.

GET /v1/transactions/status/{user_id}
Consulta o status das transações de um usuário específico.

Monitoramento
GET /health
Verifica a disponibilidade e saúde da aplicação.

🧠 Como Funciona a Detecção de Fraude
O sistema analisa cada transação com base em regras inspiradas em modelos de Machine Learning, avaliando fatores como:

Valor da transação — montantes incomuns ou fora do padrão do usuário
Frequência — múltiplas transações em curto intervalo de tempo
Localização — origem geográfica inconsistente com o histórico
Horário — transações em horários atípicos
Cada transação recebe uma classificação de risco e, quando identificada como suspeita, é marcada como potencial fraude.

🚀 Como Executar Localmente
Pré-requisitos
Python 3.10+
pip
Instalação
bash 
# Clone o repositório
git clone https://github.com/benjaminreiis/fraud-detection-api.git
cd fraud-detection-api

# Crie e ative um ambiente virtual
python -m venv venv
source venv/bin/activate   # Linux/Mac
venv\Scripts\activate      # Windows

# Instale as dependências
pip install -r requirements.txt
Executando a API
bash 
uvicorn main:app --reload
Acesse a API em http://localhost:8000 e a documentação em http://localhost:8000/docs.

📁 Estrutura do Projeto
fraud-detection-api/
│
├── app/
│   ├── api/
│   │   └── v1/
│   │       ├── auth.py            # Endpoints de autenticação
│   │       └── transactions.py    # Endpoints de transações
│   ├── core/
│   │   ├── security.py            # Lógica JWT
│   │   └── fraud_rules.py         # Regras de detecção de fraude
│   ├── models/                    # Modelos de dados (Pydantic)
│   └── schemas/                   # Schemas de request/response
│
├── main.py                        # Ponto de entrada da aplicação
├── requirements.txt               # Dependências do projeto
└── README.md
🌐 Deploy
A aplicação está hospedada na plataforma Render com deploy automático a cada push na branch principal.

API: https://fraud-detection-api-jvwk.onrender.com
Docs: https://fraud-detection-api-jvwk.onrender.com/docs

👨‍💻 Autor
Desenvolvido com foco em arquitetura backend profissional, boas práticas de Engenharia de Software e simulação de sistemas financeiros reais.

📄 Licença
Este projeto está sob a licença MIT.
