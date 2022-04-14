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
