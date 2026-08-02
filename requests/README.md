# 📨 Requests

Esta pasta reúne a documentação das requisições HTTP implementadas na Collection do Postman.

Cada arquivo descreve detalhadamente como uma requisição foi construída, qual endpoint foi utilizado, quais parâmetros são enviados, quais respostas são esperadas e quais validações são executadas durante os testes.

---

# 📋 Métodos documentados

| Método | Descrição |
|---------|-----------|
| GET | Consulta de recursos |
| POST | Criação de recursos |
| PUT | Atualização completa de recursos |
| DELETE | Remoção de recursos |

---

# 📄 Estrutura de cada documentação

Cada documentação de requisição contém:

- Objetivo da requisição
- Endpoint utilizado
- Método HTTP
- Headers
- Query Parameters (quando aplicável)
- Path Parameters (quando aplicável)
- Request Body
- Exemplo de resposta
- Status Code esperado
- Scripts de validação do Postman
- Observações

---

# ✅ Boas práticas adotadas

- Utilização de variáveis de ambiente (`{{base_url}}`)
- Organização por método HTTP
- Documentação padronizada
- Validação automática utilizando `pm.test`
- Exemplos utilizando APIs públicas
- Nenhum dado sensível armazenado no repositório

---

# 📌 Próximos arquivos

Esta pasta será composta pelos seguintes documentos:

- `get-request.md`
- `post-request.md`
- `put-request.md`
- `delete-request.md`

Cada arquivo representa um estudo completo de um método HTTP utilizado em testes de APIs REST.
