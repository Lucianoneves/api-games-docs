# API de Games
# ESta API é utilizada para tal tal..... 
## Endpoints
### GET /games
Esse endpoint é responsavel por  retornar a listagem de todos os games cadastrados no banco de dados.
#### Paremetros
Nenhum
#### Respostas
#####  OK 200
Caso essa respostas aconteça você vai receber a listagem de todos os games 
##### Falha na autenticação! 401
Caso essa resposta aconteça isso significa que aconteceu alguma falha durante o processo de autenticação de requisição.
Motivos: Token inválido, Token Expirado.
