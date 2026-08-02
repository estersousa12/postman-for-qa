# 📤 POST Request — Criar Produto

## 📌 Objetivo

Criar um novo produto na **Fake Store API**, simulando uma operação de cadastro através do método HTTP **POST**.

Esta requisição demonstra como enviar informações para uma API REST utilizando um corpo (Body) no formato JSON, validando a resposta retornada pelo servidor.

---

## 🔗 Endpoint

```http
POST {{base_url}}/products
```

---

## 📄 Método HTTP

**POST**

---

## 📑 Headers

| Header | Valor |
|--------|-------|
| Content-Type | application/json |
| Accept | application/json |

---

## 📦 Request Body

```json
{
  "title": "Notebook Gamer",
  "price": 4999.90,
  "description": "Notebook para estudos e jogos",
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
  "id": 21,
  "title": "Notebook Gamer",
  "price": 4999.90,
  "description": "Notebook para estudos e jogos",
  "image": "https://i.pravatar.cc",
  "category": "electronics"
}
```

---

## 🎯 Resultado esperado

- Retornar Status Code **200 OK**
- Criar um novo produto (simulado pela API)
- Retornar o objeto criado
- Retornar os mesmos dados enviados na requisição
- Gerar um identificador (`id`) para o recurso criado

---

## 🧪 Validações realizadas

- Status Code igual a **200**
- Corpo da resposta no formato **JSON**
- Campo **id** retornado
- Campo **title** igual ao enviado
- Campo **price** igual ao enviado
- Campo **category** igual ao enviado
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

pm.test("Produto criado possui ID", function () {
    const product = pm.response.json();

    pm.expect(product).to.have.property("id");
});

pm.test("Título retornado é igual ao enviado", function () {
    const product = pm.response.json();

    pm.expect(product.title).to.eql("Notebook Gamer");
});

pm.test("Preço retornado é igual ao enviado", function () {
    const product = pm.response.json();

    pm.expect(product.price).to.eql(4999.90);
});

pm.test("Categoria retornada é igual à enviada", function () {
    const product = pm.response.json();

    pm.expect(product.category).to.eql("electronics");
});

pm.test("Tempo de resposta menor que 2000 ms", function () {
    pm.expect(pm.response.responseTime).to.be.below(2000);
});
```

---

## 📝 Observações

- Esta requisição utiliza a variável de ambiente `{{base_url}}`, permitindo reutilização em diferentes ambientes.
- A Fake Store API simula a criação do recurso, retornando um objeto como se ele tivesse sido persistido.
- O campo **id** é gerado automaticamente pela API de demonstração.
- Nenhum dado sensível ou credencial real é utilizado neste projeto.
- Os testes podem ser executados diretamente na aba **Scripts → Post-response** do Postman.

---

## 📚 Referência

**Fake Store API**

<https://fakestoreapi.com/docs>
