## 🔐 JWT Auth com Prisma & Express
Este projeto é uma API RESTful robusta desenvolvida com Node.js, utilizando Express para roteamento e Prisma ORM para uma integração eficiente com o banco de dados. O foco principal é fornecer um sistema seguro de autenticação baseado em tokens (JWT).
## 🚀 Funcionalidades Registro de Usuários: 
- Armazenamento seguro de senhas com bcrypt.Autenticação JWT:
- Geração de tokens para sessões seguras e stateless.Gerenciamento de DB:
- Schema declarativo e migrações automatizadas via Prisma.
- Proteção de Rotas:
- Middleware pronto para validar o acesso a recursos privados.
## 🛠️ Tecnologias Utilizadas
Node.js Ambiente de execução JavaScript.
ExpressFramework web para APIs rápidas.
PrismaORM de última geração para Node.js e TypeScript.
JWTPadrão para transmissão segura de informações.
Bcrypt
Algoritmo de hashing para proteção de senhas.
## ⚙️ Configuração do Ambiente
1. Clonagem e Dependências
```js
git clone https://github.com/seu-usuario/seu-repositorio.git
cd Auth-Node
npm install
```

2. Variáveis de AmbienteCrie um arquivo `.env ` na raiz do projeto e configure suas credenciais:
```js
// Conexão com o banco (PostgreSQL, MySQL, SQLite, etc.)
DATABASE_URL="postgresql://user:password@localhost:5432/mydb"
// Chave secreta para assinar os tokens JWT
JWT_SECRET="sua_chave_secreta_super_segura"
```
4. Banco de Dados
5. Sincronize seu modelo do Prisma com o banco de dados:
```js
npx prisma migrate dev --name init
```
## 🛣️ API Endpoints
| Método | Endpoint | Descrição | Acesso |
| :--- | :--- | :--- | :--- |
| `POST` | `/register` | Cria um novo usuário | 🟢 Público |
| `POST` | `/login` | Autentica e retorna o JWT | 🟢 Público |
| `GET` | `/profile` | Retorna dados do usuário | 🔴 Privado |

Para acessar rotas privadas, envie o token no header:Authorization: Bearer <seu_token_aqui>
## 🛡️ Segurança AplicadaHashing: 
Nunca armazenamos senhas em texto puro.
Expiração: Tokens configurados com tempo de vida limitado.
Environment Safety: 
Chaves sensíveis isoladas em variáveis de ambiente.

<img width="1024" height="1024" alt="Image" src="https://github.com/user-attachments/assets/6c0b8e47-26ef-4d13-99b6-36b8d03f0c24" />

