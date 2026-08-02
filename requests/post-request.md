# POST Request

## Objetivo

Exemplo de requisição POST utilizada para cadastrar um novo produto em uma API pública.

## Endpoint

POST https://fakestoreapi.com/products

## Headers

| Chave | Valor |
|--------|-------|
| Content-Type | application/json |

## Request Body

```json
{
  "title": "Notebook Gamer",
  "price": 4999.90,
  "description": "Notebook para estudos e jogos",
  "image": "https://i.pravatar.cc",
  "category": "electronics"
}
```

## Resposta esperada

Status Code:

```text
200 OK
```

Exemplo de resposta:

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

## Resultado esperado

- Retornar status **200 OK**
- Criar um novo produto
- Retornar o objeto criado em formato **JSON**
