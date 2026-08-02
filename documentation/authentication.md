# 🔐 Authentication

Esta documentação descreve como funciona a autenticação utilizada neste projeto utilizando a **Fake Store API**.

---

# 🎯 Objetivo

Demonstrar o fluxo de autenticação utilizando um endpoint de login que retorna um **JWT (JSON Web Token)** para fins de estudo.

Embora este projeto utilize uma API pública, a documentação segue o mesmo padrão utilizado em projetos reais de testes de APIs REST.

---

# 🔗 Endpoint

**Método HTTP**

```http
POST
```

**URL**

```text
{{base_url}}/auth/login
```

---

# 📦 Request Body

```json
{
  "username": "mor_2314",
  "password": "83r5^_"
}
```

Essas credenciais são disponibilizadas oficialmente pela Fake Store API para demonstração.

---

# ✅ Resposta esperada

Status Code

```text
200 OK
```

Exemplo

```json
{
  "token":"eyJhbGciOiJIUzI1NiIsInR..."
}
```

---

# ✔️ O que é validado

- Status Code 200
- Presença da propriedade `token`
- Token retornado como String
- Tempo de resposta

---

# 💻 Script de validação (Postman)

```javascript
pm.test("Status Code é 200", function () {
    pm.response.to.have.status(200);
});

pm.test("Token retornado", function () {
    const body = pm.response.json();
    pm.expect(body).to.have.property("token");
});

pm.test("Token é String", function () {
    const body = pm.response.json();
    pm.expect(body.token).to.be.a("string");
});

pm.test("Tempo de resposta menor que 2000 ms", function () {
    pm.expect(pm.response.responseTime).to.be.below(2000);
});
```

---

# 🔒 Armazenando o Token

Após a autenticação, o token pode ser armazenado automaticamente em uma variável de ambiente do Postman.

Exemplo:

```javascript
const body = pm.response.json();

pm.environment.set("token", body.token);
```

Posteriormente, basta utilizar:

```
{{token}}
```

nas requisições autenticadas.

---

# 📌 Utilização no Header

```http
Authorization: Bearer {{token}}
```

---

# ✅ Boas práticas

- Nunca armazenar Tokens reais no GitHub.
- Utilizar variáveis de ambiente para credenciais.
- Renovar Tokens quando expirarem.
- Nunca compartilhar credenciais em repositórios públicos.

---

# 📝 Observações

- A Fake Store API disponibiliza credenciais apenas para fins de estudo.
- O JWT retornado é utilizado somente para demonstração do fluxo de autenticação.
- Nenhuma credencial real é utilizada neste projeto.
