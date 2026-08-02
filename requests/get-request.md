# GET Request

## Objetivo

Exemplo de requisição GET utilizada para consultar informações de uma API pública.

## Endpoint

GET https://fakestoreapi.com/products

## Headers

| Chave | Valor |
|--------|-------|
| Content-Type | application/json |

## Parâmetros

Nenhum.

## Resposta esperada

Status Code:

```http
200 OK
```

Exemplo de resposta:

```json
[
  {
    "id": 1,
    "title": "Produto Exemplo",
    "price": 109.95
  }
]
```

## Resultado esperado

- Retornar status **200 OK**
- Listar os produtos cadastrados
- Resposta no formato JSON
