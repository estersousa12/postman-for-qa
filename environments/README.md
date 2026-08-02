# 🌎 Environments

Esta pasta contém os ambientes utilizados pela Collection do Postman durante a execução dos testes de API REST.

Os ambientes permitem reutilizar variáveis, facilitando a troca entre diferentes APIs ou ambientes (Desenvolvimento, Homologação e Produção) sem alterar as requisições.

---

# 📁 Arquivos

| Arquivo | Descrição |
|----------|-----------|
| dev-environment.md | Documentação do ambiente de desenvolvimento utilizado neste projeto |

---

# 🔧 Variáveis utilizadas

| Variável | Descrição |
|-----------|-----------|
| {{base_url}} | URL base utilizada por todas as requisições |
| {{token}} | Token JWT retornado após autenticação (quando necessário) |

---

# 🚀 Vantagens do uso de Environments

- Evita repetir URLs em todas as requisições.
- Facilita a troca entre diferentes ambientes.
- Centraliza configurações da Collection.
- Permite reutilizar Tokens automaticamente.
- Mantém o projeto organizado.

---

# 🔒 Boas práticas

- Nunca armazenar Tokens reais no repositório.
- Utilizar variáveis para URLs e credenciais.
- Não compartilhar ambientes contendo dados sensíveis.
- Utilizar variáveis Secret sempre que possível.

---

# 📌 Observação

Este projeto utiliza apenas dados públicos da Fake Store API para fins de estudo, portanto nenhuma informação sensível é armazenada neste repositório.
