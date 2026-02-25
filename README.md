# 🚀 Desafio de Automação de Testes de API

Projeto de automação de testes da API **ServeRest**, desenvolvido utilizando **Postman**, **Newman** e **GitHub Actions**, com foco em testes de API REST e integração contínua (CI).

---

## 📌 Contexto

Este projeto tem como objetivo validar os principais endpoints de uma API REST responsável pelo gerenciamento de usuários, garantindo o correto funcionamento das operações de **CRUD** (Create, Read, Update e Delete).

API utilizada:  
👉 https://serverest.dev

---

## 🔧 Tecnologias Utilizadas

- Postman  
- Newman  
- Newman Reporter HTML Extra  
- Node.js  
- GitHub Actions (CI)  

---

## 📂 Estrutura do Projeto


📁 desafio-automacao-api
├── 📄 Desafio Automacao API.postman_collection.json
├── 📄 README.md
└── 📁 .github
└── 📁 workflows
└── 📄 ci.yml


---

## 🧪 Testes Implementados

Os testes automatizados cobrem os seguintes cenários:

### ✔️ Testes Positivos
- Criar usuário administrador
- Login com usuário administrador
- Criar usuário comum autenticado
- Buscar usuário por ID
- Atualizar usuário
- Deletar usuário

### ❌ Testes Negativos
- Criar usuário sem campos obrigatórios
- Login com credenciais inválidas
- Validação de respostas inválidas da API

Os testes validam principalmente:
- Status code das respostas
- Estrutura do retorno da API
- Fluxo de autenticação via token JWT

---

## ▶️ Como Executar os Testes Localmente

### 1️⃣ Pré-requisitos

- Node.js instalado  
👉 https://nodejs.org

- Newman e reporter HTML instalados globalmente:

```bash
npm install -g newman newman-reporter-htmlextra
2️⃣ Executar a Collection

Na pasta onde está o arquivo da collection, execute:

newman run "Desafio Automacao API.postman_collection.json" \
-r htmlextra \
--env-var baseUrl=https://serverest.dev \
--reporter-htmlextra-export report.html

Após a execução, será gerado um relatório HTML (report.html) com o resultado dos testes.

🔄 Integração Contínua (CI)

Este projeto utiliza GitHub Actions para execução automática dos testes.

✔️ Como funciona:

A cada push na branch main, a pipeline é acionada automaticamente

A collection é executada via Newman

Um relatório HTML é gerado

O relatório é disponibilizado como artefato da pipeline

Arquivo da pipeline:

.github/workflows/ci.yml
📊 Relatórios

Os relatórios de execução são gerados no formato HTML, permitindo fácil visualização dos resultados, incluindo:

Total de testes executados

Testes aprovados e reprovados

Detalhes de cada request

⚠️ Observação Importante

A API ServeRest é uma API pública e pode apresentar instabilidade ocasional.
Por esse motivo, a pipeline foi configurada para não interromper a execução em caso de falhas pontuais, garantindo a geração do relatório completo para análise dos resultados.

✅ Conclusão

Este projeto demonstra a automação de testes de API REST com integração contínua, cobrindo cenários positivos e negativos, geração de relatórios e execução automatizada via CI.

👩‍💻 Desenvolvido por: Ingrid Pursch Barbosa
