# 📦 Collections

## 🎯 Objetivo

Esta pasta contém a Collection utilizada durante os estudos de testes de APIs REST com o Postman.

A Collection foi organizada para demonstrar boas práticas na construção, execução e validação de requisições HTTP, utilizando APIs públicas e dados fictícios.

---

# 📋 Collection disponível

| Collection | Descrição |
|------------|-----------|
| Lojinha_API_Postman_Collection.json | Collection principal utilizada durante os estudos |

---

# 🚀 O que esta Collection demonstra

- Organização das requisições por método HTTP
- Utilização de variáveis de ambiente
- Testes automatizados com JavaScript
- Validação de Status Codes
- Validação de Response Body
- Reutilização de endpoints
- Documentação das requisições
- Estrutura preparada para ambientes diferentes

---

# 📁 Estrutura da Collection

```
Collection

├── GET Products
├── POST Product
├── PUT Product
└── DELETE Product
```

---

# ▶ Como utilizar

### 1. Importe a Collection

No Postman:

File → Import

Selecione:

```
Lojinha_API_Postman_Collection.json
```

---

### 2. Importe o Environment

Importe também o ambiente disponível na pasta:

```
environments/
```

---

### 3. Selecione o ambiente

No canto superior direito do Postman:

```
DEV
```

---

### 4. Execute as requisições

Cada requisição já possui:

- Headers
- Variáveis
- Scripts de teste
- Validações
- Exemplos de resposta

---

# 🧪 Validações implementadas

A Collection executa automaticamente testes como:

- Status Code esperado
- Tempo de resposta
- Estrutura do JSON
- Campos obrigatórios
- Response Body
- Quantidade de registros
- Tipos de dados

---

# 📚 Tecnologias utilizadas

- Postman
- JavaScript
- REST API
- JSON
- Fake Store API
- Markdown

---

# 📌 Observações

- Todos os exemplos utilizam APIs públicas.
- Nenhum dado sensível está armazenado no projeto.
- A Collection possui finalidade exclusivamente educacional e faz parte do meu portfólio de QA.
