"# rocklov-api-tests" 
# 🔥 Testes de API - Rocklov

Este repositório contém a automação de testes de API do projeto Rocklov, desenvolvido com Ruby, RSpec e HTTParty.

---

## 🚀 Tecnologias

- 💎 Ruby
- 📦 HTTParty
- ✅ RSpec
- 🗂️ YAML (fixtures)
- 🐳 Docker (opcional)

---

## 📄 Descrição dos Testes

### ✅ Cenários de Login

- **Login com sucesso:**  
  Garante que um usuário pode fazer login com um email e senha válidos, validando:
  - Status code 200
  - Retorno do ID do usuário (24 caracteres)

- **Cenários negativos:**  
  Valida comportamentos quando:
  - Senha incorreta
  - Email inválido
  - Campos obrigatórios ausentes  
  As mensagens de erro e os status code são validados contra os dados no arquivo `login.yml`.

---

## 🗂️ Estrutura do Projeto

├── spec/
│ ├── fixtures/
│ │ └── login.yml # Dados para testes negativos de login
│ ├── login_spec.rb # Arquivo de testes de login
│ └── spec_helper.rb # Configurações globais do RSpec
├── .gitignore
├── Gemfile
├── Gemfile.lock
└── README.md

## ⚙️ Como executar

### 🔧 Instalação de dependências:

```bash
bundle install

Executar os Testes :
rspec
ou um arquivo específico : rspec spec/login_spec.rb

🔗 Endpoints utilizados:
POST /signup — Criação de usuários para garantir pré-condições.

POST /sessions — Realiza o login dos usuários.
