# API de Games
# ESta API é utilizada para tal tal..... 
## Endpoints
### GET /games
Esse endpoint é responsavel por  retornar a listagem de todos os games cadastrados no banco de dados.
#### Paremetros
Nenhum
#### Respostas
#####  OK 200
Caso essa respostas aconteça você vai receber a listagem de todos os games.
Exemplo de respostas:
```
[
    {
        "id": 23,
        "title": "Call of duty MW",
        "year": 2019,
        "price": 60
    },
    {
        "id": 65,
        "title": "Sea of thieves",
        "year": 2018,
        "price": 40
    },
    {
        "id": 2,
        "title": "Minecraft",
        "year": 2012,
        "price": 20
    }
]

``` 
##### Falha na autenticação! 401
Caso essa resposta aconteça isso significa que aconteceu alguma falha durante o processo de autenticação de requisição.
Motivos: Token inválido, Token Expirado.

Exemplo de respostas:

```
{
    "err": "token invalido"
}

```



### POST /auth
Esse endpoint é responsavel por  retornar fazer o processo de login 
#### Paremetros
email: E-mail do usuario cadastrado no sistema.

password: senha do usuario cadastrado no sistema com aquele deterninado  e-mail.

Exemplo:
```
{   
"email":"lucianogudas057@gmail.com",
"senha": "nodejs"    

}
    
```
#### Respostas
#####  OK 200
Caso essa respostas aconteça você vai receber o token JWT para conseguir acessar Endpoints protegidos na API.
Exemplo de respostas:
```
{
   "Token":
"eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpZCI6MSwiZW1haWwiOiJsdWNpYW5vZ3VkYXMwNTdAZ21haWwuY29tIiwiaWF0IjoxNjQ5OTAyODA5LCJleHAiOjE2NTAwNzU2MDl9.WouRMQkvZXxDSPOU_FS8rVh4j5kkUE-rZIYGwJmSH6Ajrkhgrio"
}
``` 
##### Falha na autenticação! 401
Caso essa resposta aconteça isso significa que aconteceu alguma falha durante o processo de autenticação de requisição.Motivos:
Senha ou E-mail incorretos.

Exemplode respostas:
```
Credenciais invalidas!
```
Motivos: Token inválido, Token Expirado.

Exemplo de respostas:

```
{
   ({err: "Credenciais invalidas!"})
}

```


