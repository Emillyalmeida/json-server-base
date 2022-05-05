# json-server-base

Esse é o repositório com a base de JSON-Server + JSON-Server-Auth já configurada, feita para ser usada no desenvolvimento das API's nos Capstones do Q2.

## Endpoints

Assim como a documentação do JSON-Server-Auth traz (https://www.npmjs.com/package/json-server-auth), existem 3 endpoints que podem ser utilizados para cadastro e 2 endpoints que podem ser usados para login.

### Cadastro

POST /register <br/>
POST /signup <br/>
POST /users

Qualquer um desses 3 endpoints irá cadastrar o usuário na lista de "Users", sendo que os campos obrigatórios são os de email e password.
Você pode ficar a vontade para adicionar qualquer outra propriedade no corpo do cadastro dos usuários.

### Login

POST /login <br/>
POST /signin

Qualquer um desses 2 endpoints pode ser usado para realizar login com um dos usuários cadastrados na lista de "Users"

### Tech

GET /tech

- Retorna todas as tecnologias cadastradas pelos usuarios.
- Todos podem ter acesso a essa rota, não é necessario login.

Post /tech

- È necessario o usuario está logado poder adicionar tecnologias
- È obrigatorio conter o "userId" do usuario
- O usuario poderá adicionar as suas tecnologias
  --Exemplo:
  ```{
        "tech": "react",
        "level": "iniciante"
        "userId": 1
  }
  ```

## Info

GET /info

--É preciso o usuario está logado para ter acesso a essa rota
--Retorna as informações dos usuarios

Post /info

-- È necessario o usuario está logado poder adicionar as informações
-- È obrigatorio conter o "userId" do usuario
-- O usuario poderá adicionar as suas informações
--Exemplo:

```
{
    "telefone": "7599999978",
    "linkedin": "https://www.linkedin.com/in/nome",
    "github": "https://github.com/nome",
    "userId": 2
}

```
