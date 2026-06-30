🚨 Real-Time Fraud Detection API
API de detecção de fraude em tempo real desenvolvida com foco em arquitetura de backend profissional.

PythonFastAPIJWTRender

🔗 API Online: https://fraud-detection-api-jvwk.onrender.com
📄 Documentação (Swagger): https://fraud-detection-api-jvwk.onrender.com/docs
🌐 Site do Projeto: https://benjaminreiis.github.io/fraud-detection-api/

💡 Sobre o Projeto
Este projeto simula como sistemas financeiros analisam transações bancárias para detectar possíveis fraudes em tempo real.

A aplicação foi construída utilizando boas práticas de desenvolvimento backend, incluindo autenticação segura com JWT, versionamento de API e tratamento global de erros — reproduzindo o comportamento de plataformas financeiras utilizadas em produção.

🚀 Funcionalidades
Funcionalidade	Descrição
🔐 Autenticação JWT	Login seguro com geração e validação de tokens
💳 Análise de transações	Processamento e análise de transações em tempo real
🚨 Detecção de fraude	Motor de regras para identificação de transações suspeitas
📊 Consulta por usuário	Endpoint para consultar o status das transações de um usuário
🧠 Lógica inspirada em ML	Regras de detecção baseadas em padrões de Machine Learning
🛠️ Tratamento de erros	Handler global padronizado para todos os erros da API
❤️ Health Check	Endpoint de monitoramento para verificar a disponibilidade da API
🔄 Versionamento de API	Rotas organizadas sob /v1 para controle de versão
🧱 Tecnologias Utilizadas
Tecnologia	Finalidade
Python	Linguagem principal do projeto
FastAPI	Framework web para construção da API REST
Uvicorn	Servidor ASGI de alta performance
PyJWT	Geração e validação de tokens JWT
Render	Plataforma de deploy em cloud
🔐 Como Funciona a Autenticação
A API utiliza autenticação baseada em JWT (JSON Web Token). Siga os passos abaixo para autenticar-se:

1. Faça login para obter o token
http 
POST /v1/auth/login
json 
{
  "username": "seu_usuario",
  "password": "sua_senha"
}
2. Receba o token JWT
json 
{
  "token": "seu_token_aqui"
}
3. Use o token nos endpoints protegidos
Envie o token via header em todas as requisições autenticadas:

http 
authorization: seu_token_aqui
📡 Endpoints Principais
Autenticação
http 
POST /v1/auth/login
Realiza o login do usuário e retorna um token JWT.

Transações
http 
POST /v1/transactions
Submete uma transação para análise de fraude em tempo real.

http 
GET /v1/transactions/status/{user_id}
Consulta o status das transações de um usuário específico.

Monitoramento
http 
GET /health
Verifica a disponibilidade e saúde da aplicação.

📄 Consulte a documentação completa no Swagger para ver todos os endpoints, parâmetros e exemplos de resposta.

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
source venv/bin/activate  # Linux/Mac
venv\Scripts\activate     # Windows

# Instale as dependências
pip install -r requirements.txt
Executando a API
bash 
uvicorn main:app --reload
A API estará disponível em: http://localhost:8000
Documentação Swagger em: http://localhost:8000/docs

🧠 Como Funciona a Detecção de Fraude
O sistema analisa cada transação em tempo real com base em um conjunto de regras inspiradas em modelos de Machine Learning, avaliando fatores como:

Valor da transação — montantes incomuns ou fora do padrão do usuário
Frequência — múltiplas transações em curto intervalo de tempo
Localização — origem geográfica inconsistente com o histórico
Horário — transações em horários atípicos
Cada transação recebe uma classificação de risco e, quando identificada como suspeita, é marcada como potencial fraude.

📁 Estrutura do Projeto
fraud-detection-api/
│
├── app/
│   ├── api/
│   │   └── v1/
│   │       ├── auth.py          # Endpoints de autenticação
│   │       └── transactions.py  # Endpoints de transações
│   ├── core/
│   │   ├── security.py          # Lógica JWT
│   │   └── fraud_rules.py       # Regras de detecção de fraude
│   ├── models/                  # Modelos de dados (Pydantic)
│   └── schemas/                 # Schemas de request/response
│
├── main.py                      # Ponto de entrada da aplicação
├── requirements.txt             # Dependências do projeto
└── README.md
🌐 Deploy
A aplicação está hospedada na plataforma Render com deploy automático a cada push na branch principal.

API: https://fraud-detection-api-jvwk.onrender.com
Docs: https://fraud-detection-api-jvwk.onrender.com/docs
👨‍💻 Autor
Desenvolvido com foco em arquitetura backend profissional, boas práticas de Engenharia de Software e simulação de sistemas financeiros reais.

📄 Licença
Este projeto está sob a licença MIT. Consulte o arquivo LICENSE para mais detalhes.
