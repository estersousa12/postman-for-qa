# 🔄 PUT Request — Atualizar Produto

## 📌 Objetivo

Atualizar um produto existente na **Fake Store API** utilizando o método HTTP **PUT**.

Esta requisição demonstra como alterar completamente um recurso existente, enviando um novo corpo (Body) em formato JSON e validando a resposta retornada pela API.

---

## 🔗 Endpoint

```http
PUT {{base_url}}/products/1
```

---

## 📄 Método HTTP

**PUT**

---

## 📑 Headers

| Header | Valor |
|--------|-------|
| Content-Type | application/json |
| Accept | application/json |

---

## 🛣️ Path Parameters

| Parâmetro | Valor | Descrição |
|-----------|-------|-----------|
| `id` | `1` | Identificador do produto que será atualizado |

---

## 📦 Request Body

```json
{
  "title": "Notebook Gamer Atualizado",
  "price": 5299.90,
  "description": "Notebook atualizado para estudos e jogos",
  "image": "https://i.pravatar.cc",
  "category": "electronics"
}
```

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
  "title": "Notebook Gamer Atualizado",
  "price": 5299.90,
  "description": "Notebook atualizado para estudos e jogos",
  "image": "https://i.pravatar.cc",
  "category": "electronics"
}
```

---

## 🎯 Resultado esperado

- Retornar Status Code **200 OK**
- Atualizar o recurso informado
- Retornar o objeto atualizado
- Manter o mesmo ID informado na URL
- Retornar os novos dados enviados na requisição

---

## 🧪 Validações realizadas

- Status Code igual a **200**
- Corpo da resposta no formato **JSON**
- Campo **id** igual ao informado na URL
- Campo **title** atualizado corretamente
- Campo **price** atualizado corretamente
- Campo **category** atualizado corretamente
- Tempo de resposta inferior a **2000 ms**

---

## 💻 Script de validação (Postman)

```javascript
pm.test("Status Code é 200", function () {
    pm.response.to.have.status(200);
});

pm.test("Resposta é um objeto", function () {
    pm.expect(pm.response.json()).to.be.an("object");
});

pm.test("ID retornado é igual ao informado na URL", function () {
    const product = pm.response.json();

    pm.expect(product.id).to.eql(1);
});

pm.test("Título atualizado corretamente", function () {
    const product = pm.response.json();

    pm.expect(product.title).to.eql("Notebook Gamer Atualizado");
});

pm.test("Preço atualizado corretamente", function () {
    const product = pm.response.json();

    pm.expect(product.price).to.eql(5299.90);
});

pm.test("Categoria atualizada corretamente", function () {
    const product = pm.response.json();

    pm.expect(product.category).to.eql("electronics");
});

pm.test("Tempo de resposta menor que 2000 ms", function () {
    pm.expect(pm.response.responseTime).to.be.below(2000);
});
```

---

## 📝 Observações

- Esta requisição utiliza a variável de ambiente `{{base_url}}`.
- O parâmetro **id** identifica qual recurso será atualizado.
- A Fake Store API simula a atualização do recurso para fins de estudo.
- Nenhum dado sensível ou credencial real é utilizado neste projeto.
- Os scripts apresentados podem ser executados diretamente na aba **Scripts → Post-response** do Postman.

---

## 📚 Referência

**Fake Store API**

<https://fakestoreapi.com/docs>
