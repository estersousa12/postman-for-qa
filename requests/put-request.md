# PUT Request

## Objetivo

Exemplo de requisição PUT utilizada para atualizar um produto existente em uma API pública.

## Endpoint

PUT https://fakestoreapi.com/products/1

## Headers

| Chave | Valor |
|--------|-------|
| Content-Type | application/json |

## Request Body

```json
{
  "title": "Notebook Gamer Atualizado",
  "price": 5299.90,
  "description": "Notebook atualizado para estudos e jogos",
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
  "id": 1,
  "title": "Notebook Gamer Atualizado",
  "price": 5299.90,
  "description": "Notebook atualizado para estudos e jogos",
  "image": "https://i.pravatar.cc",
  "category": "electronics"
}
```

## Resultado esperado

- Retornar status **200 OK**
- Atualizar o produto existente
- Retornar o objeto atualizado em formato **JSON**
