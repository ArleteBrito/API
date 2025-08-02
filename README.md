# API de Gerenciamento de Usuários com Express.js e Prisma

Este é um projeto simples de API REST criada com **Express.js** e **Prisma**, que permite realizar operações CRUD em uma tabela de usuários.

## 🧰 Tecnologias Utilizadas

- Node.js
- Express.js
- Prisma ORM
- SQLite/PostgreSQL/MySQL (dependendo da configuração do seu `schema.prisma`)

## 🚀 Instalação e Execução

### 1. Clone o repositório
```bash
git clone https://github.com/seu-usuario/seu-repositorio.git
cd seu-repositorio

### 2. Instale as depedências
```bash
npm install

### 3. Configure o banco de dados
Edite o arquivo .env com sua URL de conexão, por exemplo:
```bash
DATABASE_URL="file:./dev.db" # para SQLite

### 4. Gere os artefatos do Prisma
```bash
npx prisma generate

### 5. Rode as migrações (caso use SQLite, PostgreSQL ou MySQL)
```bash
npx prisma migrate dev --name init

###6. Inicie o servidor
```bash
npm start

📬 Rotas da API
POST /usuarios
Cria um novo usuário.

Body:

json
Copiar
Editar
{
  "email": "exemplo@email.com",
  "name": "Fulano",
  "age": 25
}

GET /usuarios
Retorna todos os usuários cadastrados.

PUT /usuarios/:id
Atualiza um usuário existente com base no ID.

Body:

json
Copiar
Editar
{
  "email": "novo@email.com",
  "name": "Novo Nome",
  "age": 30
}

DELETE /usuarios/:id
Remove um usuário pelo ID.

📁 Estrutura de Diretórios (Essencial)
pgsql
Copiar
Editar
.
├── generated/
│   └── prisma/
│       └── index.js     # Cliente Prisma gerado
├── index.js             # Código principal da API
├── package.json
├── prisma/
│   └── schema.prisma    # Definição do modelo do banco de dados
└── README.md

✅ Requisitos
Node.js v18+

npm

Banco de dados compatível com Prisma (SQLite, PostgreSQL, MySQL, etc)

📄 Licença

Este projeto está licenciado sob a licença MIT. Veja o arquivo LICENSE para mais detalhes.