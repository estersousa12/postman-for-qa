# 🌐 GET Request — Listar Produtos

## 📌 Objetivo

Recuperar a lista de produtos cadastrados na **Fake Store API**.

Esta requisição é utilizada para validar o retorno dos recursos disponíveis, o status da resposta, o tempo de resposta e a estrutura dos dados retornados pela API.

---

## 🔗 Endpoint

```http
GET {{base_url}}/products
```

---

## 📄 Método HTTP

**GET**

---

## 📑 Headers

| Header | Valor |
|--------|-------|
| Accept | application/json |

---

## 🔎 Query Parameters

| Parâmetro | Obrigatório | Exemplo | Descrição |
|-----------|-------------|---------|-----------|
| `limit` | Não | `5` | Limita a quantidade de produtos retornados |
| `sort` | Não | `desc` | Define a ordenação dos produtos como `asc` ou `desc` |

### Exemplo com parâmetros

```http
GET {{base_url}}/products?limit=5&sort=desc
```

---

## 🧩 Path Parameters

Não utilizados nesta requisição.

---

## ✅ Resposta esperada

### Status Code

```text
200 OK
```

### Exemplo de resposta

```json
[
  {
    "id": 1,
    "title": "Fjallraven - Foldsack No. 1 Backpack",
    "price": 109.95,
    "description": "Your perfect pack for everyday use and walks in the forest.",
    "category": "men's clothing",
    "image": "https://fakestoreapi.com/img/81fPKd-2AYL._AC_SL1500_.jpg",
    "rating": {
      "rate": 3.9,
      "count": 120
    }
  }
]
```

---

## 🎯 Resultado esperado

- Retornar Status Code **200 OK**
- Retornar uma lista de produtos
- Retornar o corpo da resposta no formato **JSON**
- Retornar pelo menos um produto
- Cada produto deve possuir os campos esperados
- O tempo de resposta deve permanecer abaixo do limite definido

---

## 🧪 Validações realizadas

- Status Code igual a **200**
- Corpo da resposta é um **array**
- Resposta não está vazia
- Presença dos campos obrigatórios:
  - `id`
  - `title`
  - `price`
  - `category`
- Tempo de resposta inferior a **2000 ms**

---

## 💻 Script de validação no Postman

```javascript
pm.test("Status Code é 200", function () {
    pm.response.to.have.status(200);
});

pm.test("Resposta é um array", function () {
    const responseBody = pm.response.json();

    pm.expect(responseBody).to.be.an("array");
});

pm.test("Resposta não está vazia", function () {
    const responseBody = pm.response.json();

    pm.expect(responseBody.length).to.be.above(0);
});

pm.test("Produtos possuem os campos obrigatórios", function () {
    const products = pm.response.json();

    products.forEach(function (product) {
        pm.expect(product).to.have.property("id");
        pm.expect(product).to.have.property("title");
        pm.expect(product).to.have.property("price");
        pm.expect(product).to.have.property("category");
    });
});

pm.test("Tempo de resposta menor que 2000 ms", function () {
    pm.expect(pm.response.responseTime).to.be.below(2000);
});
```

---

## 📝 Observações

- Esta requisição utiliza a variável de ambiente `{{base_url}}`, permitindo sua reutilização em diferentes ambientes.
- Os parâmetros `limit` e `sort` são opcionais.
- A **Fake Store API** é utilizada exclusivamente para fins de estudo e demonstração de testes de APIs REST.
- Nenhum dado sensível ou credencial real é armazenado neste projeto.
- Os scripts apresentados podem ser executados diretamente na aba **Scripts → Post-response** do Postman.

---

## 📚 Referência

**Fake Store API**

<https://fakestoreapi.com/docs>
