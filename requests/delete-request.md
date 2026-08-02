# 🗑️ DELETE Request — Remover Produto

## 🎯 Objetivo

Remover um produto existente na **Fake Store API**, simulando uma operação de exclusão.

Embora a API retorne sucesso, a exclusão **não é persistida**, pois a Fake Store API é destinada apenas para estudos.

---

## 🔗 Endpoint

**Método HTTP**

```http
DELETE
```

**URL**

```text
{{base_url}}/products/1
```

---

## 📋 Headers

| Header | Valor |
|---------|-------|
| Content-Type | application/json |
| Accept | application/json |

---

## 📌 Path Parameter

| Parâmetro | Valor | Descrição |
|-----------|-------|-----------|
| id | 1 | Identificador do produto que será removido |

---

## 📦 Request Body

Esta requisição **não possui Body**, pois apenas identifica o recurso através do ID informado na URL.

---

## ✅ Resposta esperada

### Status Code

```text
200 OK
```

### Exemplo de resposta

```json
{
  "id": 1,
  "title": "Fjallraven - Foldsack No. 1 Backpack",
  "price": 109.95,
  "description": "Your perfect pack for everyday use and walks in the forest.",
  "category": "men's clothing",
  "image": "https://fakestoreapi.com/img/81fPKd-2AYL._AC_SL1500_.jpg"
}
```

---

## ✔️ Resultado esperado

- Retornar **Status Code 200**
- Retornar o objeto correspondente ao produto removido
- Confirmar que o ID retornado corresponde ao ID informado na URL
- Resposta em formato JSON

---

## 💻 Script de validação (Postman)

```javascript
pm.test("Status Code é 200", function () {
    pm.response.to.have.status(200);
});

pm.test("Resposta possui ID", function () {
    const body = pm.response.json();
    pm.expect(body).to.have.property("id");
});

pm.test("ID retornado corresponde ao produto removido", function () {
    const body = pm.response.json();
    pm.expect(body.id).to.eql(1);
});

pm.test("Tempo de resposta menor que 2000 ms", function () {
    pm.expect(pm.response.responseTime).to.be.below(2000);
});
```

---

## 📝 Observações

- Esta requisição utiliza a variável de ambiente **{{base_url}}**, permitindo reutilização da Collection em diferentes ambientes.
- A **Fake Store API** apenas simula a exclusão de registros; nenhuma informação é realmente removida do banco de dados.
- O objetivo desta requisição é validar o comportamento esperado do método HTTP **DELETE** e o contrato da resposta.
- Nenhum dado sensível é utilizado neste projeto.
