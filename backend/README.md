# Video Manager API

Esta é uma API RESTful minimalista desenvolvida em **Node.js** utilizando o framework **Fastify**. O objetivo da aplicação é gerenciar um catálogo de vídeos, permitindo operações de criação, leitura, atualização e exclusão (CRUD).

## 🚀 Tecnologias

- **Node.js**: Runtime Javascript.
- **Fastify**: Framework web de alta performance.
- **Database Memory**: Estrutura de dados em memória (`Map`) para persistência volátil.
- **UUID**: Identificadores únicos universais para cada registro.

## 🛠️ Instalação e Execução

1. Instale as dependências:
   ```bash
   npm install
   ```
2. Inicie o servidor:
   ```bash
   node server.js
   ```
3. A API estará disponível em `http://localhost:3333`.

## 📝 Endpoints

### 1. Criar Vídeo
`POST /videos`

Cria um novo registro de vídeo.
- **Payload (JSON):**
  ```json
  { "title": "Node.js Tutorial", "description": "Aula sobre Fastify", "duration": 180 }
  ```
- **Resposta:** `201 Created`.

### 2. Listar Vídeos
`GET /videos`

Retorna a lista de todos os vídeos. Suporta filtragem por título via query string (se implementado).
- **Resposta:** `200 OK` com array de objetos contendo `id`.

### 3. Atualizar Vídeo
`PUT /videos/:id`

Atualiza integralmente os dados de um vídeo existente.
- **Parâmetros:** `id` (UUID).
- **Resposta:** `204 No Content`.

### 4. Deletar Vídeo
`DELETE /videos/:id`

Remove um vídeo do sistema.
- **Parâmetros:** `id` (UUID).
- **Resposta:** `204 No Content`.
