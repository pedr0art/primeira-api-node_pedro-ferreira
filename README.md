Perfeito! Aqui está uma versão pronta em Markdown, pronta para colar direto no **Add README** do GitHub:

````markdown
# Servidor de Usuários em Node.js

Este é um servidor simples em Node.js que permite armazenar e listar usuários em memória.  
Ele utiliza apenas o módulo nativo `http`, sem frameworks adicionais.

## Funcionalidades

- Listar todos os usuários cadastrados.
- Adicionar novos usuários com `nome` e `email`.
- Retorna mensagens de erro para dados inválidos ou rotas inexistentes.

## Requisitos

- Node.js (versão 14 ou superior recomendada)

## Instalação e execução

1. Clone o repositório ou baixe o arquivo `server.js`.
2. Abra o terminal na pasta do projeto.
3. Execute o servidor:

```bash
node server.js
````

4. O servidor estará rodando em: `http://localhost:3000`

## Rotas

### 1. Listar usuários

* **URL:** `/usuarios`
* **Método:** `GET`
* **Descrição:** Retorna todos os usuários cadastrados.

**Exemplo de resposta:**

```json
[
  {
    "id": 1,
    "nome": "João",
    "email": "joao@email.com"
  }
]
```

### 2. Adicionar usuário

* **URL:** `/usuarios`
* **Método:** `POST`
* **Descrição:** Adiciona um novo usuário com `nome` e `email`.

**Exemplo de requisição (JSON no body):**

```json
{
  "nome": "Maria",
  "email": "maria@email.com"
}
```

**Exemplo de resposta:**

```json
{
  "mensagem": "Usuário adicionado com sucesso"
}
```

**Erros possíveis:**

* `400` – JSON inválido ou dados incompletos (`nome` ou `email` ausentes).
* `404` – Rota não encontrada.

## Observações

* Os usuários são armazenados apenas em memória; ao reiniciar o servidor, todos os dados são perdidos.
* Para testes, você pode usar ferramentas como [Postman](https://www.postman.com/) ou `curl`.

```

Se você quiser, posso também criar **uma versão ainda mais enxuta**, ótima para quem só quer instruções rápidas para rodar e testar. Quer que eu faça?
```
