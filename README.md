# Todos os livres

Boas vindas a API do AllBooks!

O AllBooks é uma loja virtual que vende livros da Casa do Código. 
É um MVP que só veio e ainda tem muitas funções novas para serem desenvolvidas.

# JSONServer + JWT Auth

Essa é ma API Rest mockada, utilizando json-server e JWT.

## ?? ️ Instalação

`bash
$ npm instalar
$ npm execute start-auth
`
## ?? ️ Como se registrador?

Você pode fazer isso efetuando uma requisição post para:

`
POSTAGEM http://localhost:8000/public/registrar
`

Com os seguintes dados:


`
{
 "nome": "vinicios neves",
 "e-mail": "vinicios@alura.com.br",
 "senha": "123456",
 "endereco": "Rua Vergueiro, 3185",
 "complemento": "Vila Mariana",
 "cep": "04101-300"
}
`

Repare que o e-mail é um campo único e usuários com e-mails duplicados não serão persistidos.

## ?? ️ Como fazer login?

Você pode fazer isso efetuando uma requisição post para:

`
POSTAGEM http://localhost:8000/public/login
`

Com os seguintes dados:


`
{
 "e-mail": "vinicios@alura.com.br",
 "senha":"123456"
}
`

Você vai receber um token no segundo formato:

`
{
 "acesso_token": "<ACESSO_TOKEN>",
 "usuário": { ... dados do usuário... }
}
```

## Autenticar próximas requests?

E então, adicionar este mesmo token ao header das próximas requisições:

```
Authorization: Bearer <ACCESS_TOKEN>
```
