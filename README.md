Servidor de Usuários em Node.js

Este é um servidor simples em Node.js que permite armazenar e listar usuários em memória. Ele utiliza apenas o módulo nativo http, sem frameworks adicionais.

Funcionalidades

Listar todos os usuários cadastrados.

Adicionar novos usuários com nome e email.

Retorna mensagens de erro para dados inválidos ou rotas inexistentes.

Requisitos

Node.js (versão 14 ou superior recomendada)

Instalação

Clone o repositório ou baixe o arquivo server.js.

Abra o terminal na pasta do projeto.

Execute o servidor:

node server.js


O servidor estará rodando em: http://localhost:3000

Rotas
1. Listar usuários

URL: /usuarios

Método: GET

Descrição: Retorna todos os usuários cadastrados.

Exemplo de resposta:

[
  {
    "id": 1,
    "nome": "João",
    "email": "joao@email.com"
  }
]

2. Adicionar usuário

URL: /usuarios

Método: POST

Descrição: Adiciona um novo usuário com nome e email.

Exemplo de requisição (JSON no body):

{
  "nome": "Maria",
  "email": "maria@email.com"
}


Exemplo de resposta:

{
  "mensagem": "Usuário adicionado com sucesso"
}


Erros possíveis:

400 – Caso o JSON enviado seja inválido ou não contenha nome e email.

404 – Rota não encontrada.

Observações

Os usuários são armazenados apenas em memória; ao reiniciar o servidor, todos os dados são perdidos.

Para testes, você pode usar ferramentas como Postman
 ou curl.
