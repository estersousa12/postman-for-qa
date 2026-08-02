# Authentication

## Objetivo

Apresentar os principais métodos de autenticação utilizados em APIs REST e como configurá-los no Postman.

---

# Basic Auth

Utiliza usuário e senha enviados na requisição.

### Exemplo

```text
Username: admin
Password: 123456
```

### Configuração no Postman

Authorization → Type → Basic Auth

Preencha:

- Username
- Password

---

# Bearer Token (JWT)

É o método mais utilizado atualmente.

O token é enviado no Header da requisição.

### Exemplo

```http
Authorization: Bearer eyJhbGciOiJIUzI1NiIsInR5cCI...
```

### Configuração no Postman

Authorization → Type → Bearer Token

Cole o Token no campo Token.

---

# API Key

Utilizada por diversas APIs públicas.

Pode ser enviada no Header ou na URL.

### Exemplo no Header

```http
x-api-key: SUA_API_KEY
```

### Configuração no Postman

Authorization → Type → API Key

Informe:

- Key
- Value
- Add to: Header

---

# OAuth 2.0

Utilizado em aplicações que exigem login do usuário.

Exemplos:

- Google APIs
- Microsoft Graph
- GitHub API

No Postman:

Authorization → OAuth 2.0

É possível gerar automaticamente o Access Token.

---

# Boas práticas

- Nunca compartilhar Tokens.
- Não salvar senhas em repositórios públicos.
- Utilizar variáveis de ambiente para credenciais.
- Renovar Tokens quando expirarem.
- Utilizar HTTPS em produção.

---

# Resumo

| Método | Mais utilizado |
|---------|----------------|
| Basic Auth | Sistemas internos |
| Bearer Token | APIs REST modernas |
| API Key | APIs públicas |
| OAuth 2.0 | Grandes aplicações |
