# DEV Environment

## Objetivo

Exemplo de configuração de ambiente para testes de APIs no Postman.

## Variáveis

| Variável | Valor de exemplo |
|---|---|
| base_url | https://fakestoreapi.com |
| product_id | 1 |
| content_type | application/json |
| token | não informado |

## Uso no Postman

As variáveis podem ser utilizadas nas requisições desta forma:

```text
{{base_url}}/products/{{product_id}}
