# Desafio de Automação de Testes de API

Projeto de automação de testes da API ServeRest utilizando Postman + Newman.

## 📌 Contexto

Testes automatizados para operações de CRUD de usuários:
- GET /usuarios
- POST /usuarios
- GET /usuarios/{id}
- PUT /usuarios/{id}
- DELETE /usuarios/{id}

Autenticação via token JWT.

---

## ✅ Cobertura dos Testes

### Fluxo Positivo
- Criar usuário administrador
- Login com JWT
- Criar usuário comum
- Buscar usuário por ID
- Atualizar usuário
- Deletar usuário

### Fluxos Negativos
- Criar usuário sem token
- Criar usuário sem campo obrigatório
- Criar usuário com email duplicado
- Buscar usuário inexistente
- Atualizar usuário inexistente
- Deletar usuário inexistente



