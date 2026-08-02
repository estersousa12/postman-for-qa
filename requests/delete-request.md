# DELETE Request

## Objetivo

Exemplo de requisição DELETE utilizada para remover um produto de uma API pública.

## Endpoint

DELETE https://fakestoreapi.com/products/1

## Headers

| Chave | Valor |
|--------|-------|
| Content-Type | application/json |

## Request Body

Não possui.

## Resposta esperada

Status Code:

```text
200 OK
```

Exemplo de resposta:

```json
{
  "id": 1
}
```

## Resultado esperado

- Retornar status **200 OK**
- Excluir o produto informado
- Retornar confirmação da exclusão
