# 📋 Sistema de Ordem de Serviço

Aplicação fullstack para gerenciamento de Ordens de Serviço (OS), permitindo o cadastro e acompanhamento de chamados.

> 🚧 **Projeto em desenvolvimento**

O projeto está sendo desenvolvido com foco em aprendizado prático de desenvolvimento fullstack, organização de código, criação de APIs REST e integração entre frontend, backend e banco de dados.

---

## 📌 Sobre o projeto

O sistema tem como objetivo permitir que usuários registrem Ordens de Serviço e acompanhem seu andamento.

A aplicação está sendo construída de forma incremental, começando pela API e persistência dos dados e posteriormente evoluindo para uma interface web completa.

### Fluxo planejado

```text
Cliente
   │
   ▼
Cria uma Ordem de Serviço
   │
   ▼
OS aberta
   │
   ▼
Técnico assume o chamado
   │
   ▼
OS em andamento
   │
   ▼
Técnico resolve
   │
   ▼
OS resolvida
   │
   ▼
OS fechada
```

---

## 🚀 Tecnologias utilizadas

### Backend

* Node.js
* Express
* MongoDB
* Mongoose
* dotenv
* Axios
* CORS

### Frontend

* React
* Vite
* JavaScript
* Axios

### Ferramentas

* Git
* GitHub
* VS Code
* Postman / Thunder Client

---

## 🏗️ Arquitetura

O projeto utiliza uma organização separando frontend e backend.

```text
os/
│
├── backend/
│   ├── src/
│   │   ├── controllers/
│   │   ├── models/
│   │   ├── routes/
│   │   └── server.js
│   │
│   ├── .env
│   └── package.json
│
└── frontend/
    ├── src/
    │   ├── components/
    │   ├── pages/
    │   ├── services/
    │   └── App.jsx
    │
    └── package.json
```

### Fluxo da aplicação

```text
Frontend
   │
   │ HTTP / JSON
   ▼
Express / API REST
   │
   ▼
Routes
   │
   ▼
Controllers
   │
   ▼
Models / Mongoose
   │
   ▼
MongoDB
```

---

## 📂 Estrutura do Backend

### Controllers

Responsáveis pela lógica das requisições e regras relacionadas às operações da aplicação.

### Models

Responsáveis pela definição dos schemas e comunicação dos dados através do Mongoose.

### Routes

Responsáveis por definir os endpoints da API e direcionar as requisições para os controllers.

---

## ⚙️ Como executar o projeto

### 1. Clone o repositório

```bash
git clone URL_DO_REPOSITORIO
```

### 2. Entre na pasta do projeto

```bash
cd os
```

### 3. Instale as dependências do backend

```bash
cd backend
npm install
```

### 4. Configure as variáveis de ambiente

Crie um arquivo `.env` dentro do backend:

```env
MONGO_URI=sua_string_de_conexao
PORT=3000
```

### 5. Execute o backend

```bash
npm run dev
```

ou:

```bash
node src/server.js
```

---

## 🖥️ Frontend

Em outro terminal:

```bash
cd frontend
npm install
npm run dev
```

O frontend será disponibilizado pelo Vite.

---

## 📡 API

### Criar Ordem de Serviço

```http
POST /ordens-servico
```

Exemplo de requisição:

```json
{
  "titulo": "Computador não liga",
  "descricao": "Computador do setor financeiro não está ligando.",
  "prioridade": "Alta",
  "cliente": {
    "nome": "João Silva",
    "email": "joao@email.com"
  }
}
```

### Listar Ordens de Serviço

```http
GET /ordens-servico
```

---

## 📝 Status da implementação

| Funcionalidade              | Status                |
| --------------------------- | --------------------- |
| Estrutura do backend        | ✅ Concluído           |
| Conexão com MongoDB         | ✅ Concluído           |
| Model de Ordem de Serviço   | ✅ Concluído           |
| POST de Ordem de Serviço    | ✅ Concluído           |
| GET de Ordens de Serviço    | ✅ Concluído           |
| Frontend React              | 🚧 Em desenvolvimento |
| Formulário de criação de OS | 🚧 Em desenvolvimento |
| Listagem de OS              | ⏳ Pendente            |
| Alteração de status         | ⏳ Pendente            |
| Técnico assumir OS          | ⏳ Pendente            |
| Autenticação JWT            | ⏳ Pendente            |

---

## 🔮 Próximos passos

* [ ] Finalizar interface de criação de OS
* [ ] Criar tela de listagem de OS
* [ ] Criar visualização detalhada da OS
* [ ] Implementar alteração de status
* [ ] Criar cadastro de técnicos
* [ ] Implementar técnico assumindo chamado
* [ ] Implementar autenticação com JWT
* [ ] Criar controle de acesso
* [ ] Melhorar validações da API
* [ ] Adicionar tratamento de erros
* [ ] Adicionar testes
* [ ] Publicar aplicação

---

## 🎯 Objetivos de aprendizado

Este projeto está sendo desenvolvido com o objetivo de praticar:

* Desenvolvimento de APIs REST
* Node.js e Express
* MongoDB e Mongoose
* React
* Integração frontend e backend
* CRUD
* Arquitetura e organização de projetos
* Variáveis de ambiente
* Git e GitHub
* Autenticação e autorização
* Regras de negócio

---

## 👨‍💻 Autor

**Matheus Cardozo**

Projeto desenvolvido para estudos e construção de portfólio em desenvolvimento fullstack.

