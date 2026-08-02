# 🌎 DEV Environment

## 🎯 Objetivo

Este ambiente é utilizado para executar a Collection do Postman durante os estudos de testes de APIs REST.

Todas as requisições utilizam variáveis de ambiente, permitindo reutilização da Collection sem necessidade de alterar URLs ou parâmetros manualmente.

---

# 📋 Informações do ambiente

| Item | Valor |
|------|------|
| Ambiente | Development |
| API utilizada | Fake Store API |
| Base URL | https://fakestoreapi.com |
| Formato das respostas | JSON |
| Autenticação | Não obrigatória |

---

# 🔧 Variáveis do ambiente

| Variável | Valor de exemplo | Descrição |
|-----------|-----------------|-----------|
| base_url | https://fakestoreapi.com | URL base da API |
| product_id | 1 | ID utilizado nas requisições |
| content_type | application/json | Header Content-Type |
| token | {{token}} | Token JWT (quando necessário) |

---

# 🚀 Utilização no Postman

Após importar o ambiente:

1. Selecione o ambiente **DEV**.
2. Execute a Collection.
3. Todas as requisições utilizarão automaticamente as variáveis.

Exemplo:

```http
GET {{base_url}}/products

GET {{base_url}}/products/{{product_id}}

POST {{base_url}}/products
```

---

# 📁 Variáveis utilizadas pelas requisições

| Requisição | Variáveis |
|------------|-----------|
| GET | {{base_url}} |
| POST | {{base_url}} |
| PUT | {{base_url}}, {{product_id}} |
| DELETE | {{base_url}}, {{product_id}} |

---

# 🔒 Boas práticas

- Utilizar variáveis de ambiente para URLs.
- Nunca armazenar Tokens reais.
- Evitar alterar endpoints diretamente nas requisições.
- Utilizar variáveis para IDs reutilizáveis.
- Manter um ambiente para cada etapa (DEV, HML e PROD).

---

# 📌 Observações

- Este ambiente utiliza apenas dados públicos da Fake Store API.
- Nenhuma credencial real está armazenada neste projeto.
- O arquivo serve exclusivamente para fins de estudo e demonstração de testes de APIs REST.
