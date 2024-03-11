# Votação

## Configuração do Projeto

O projeto usa docker para criação do seu banco de dados Postgres, é necessária a instalação do docker CLI e docker compose. Para cria o container do banco basta executar: 

```docker compose up -d```

Obs.: Esse comando eve ser executado dentro do projeto voting-service.

### Configurando voting-service

1. ```cd voting-service```
2. ```npm i``` (O projeto foi desenvolvido em node v18.15)
3. Executa as migrations para montar a estrutura do banco: ```npm run migrate ```
4. Execute ```npm run seed``` para criar um usuário admin no banco de dados.
5. Execute ```npm run start:dev``` para iniciar o servidor.

Para executar os testes basta rodar:
``` npm run test```

Dentro da pasta raiz tem um arquivo com as collections do insominia com os endpoints do service:
`voting-service.json`

### Configurando voting-front

1. ```cd voting-front```
2. ```npm i``` (O projeto foi desenvolvido em node v18.15)
3. Será preciso instalar a CLI do angular: ```npm i -g @angular/cli@17.2.0```
4. Execute ```ng serve```  para iniciar o front.

Ao acessar o path raiz (http://localhost:4200/) do projeto front você será levado a tela de login, as credenciais de acesso são: 
``` 
username: admin 
password: admin
```