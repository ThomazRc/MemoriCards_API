# MemoriCards API

<a href= "https://insomnia.rest/run/?label=memori-cards-api&uri=https%3A%2F%2Fmemori-cards-api.onrender.com" target="_blank"><img src="https://insomnia.rest/images/run.svg" alt="Run in Insomnia"></a>

<blockquote> Para importar o JSON no Insomnia é só clicar no botão "Run in Insomnia".
</blockquote>
<br>

A url base da API é https://memori-cards-api.onrender.com

## Endpoints que não necessitam de token

### Cadastro de usuário

`POST /signup - FORMATO DA REQUISIÇÃO`

```json
{
  "email": "kenzinho2@mail.com",
  "password": "$2a$10$inkMXFPw2KJWb.DbLA/I5ujgwZxQW5buCxUUxblE5OuMHPtDcSnnm",
  "id": 1,
}
```

<br>

### Login

`POST /signin - FORMATO DA REQUISIÇÃO`

```json
{
  "email": "kenzinho2@mail.com",
  "password": "$2a$10$inkMXFPw2KJWb.DbLA/I5ujgwZxQW5buCxUUxblE5OuMHPtDcSnnm",
}
```

## Endpoints que necessitam de token

### flashcards

`GET /flashcards/:userId - FORMATO DA REQUISIÇÃO`

```json
[
	{
	  "question":"Quem descobriu a ámerica",
	  "answer":"Cristovão colombo",
	  "userId":1
	},
	{
	  "question":"Qual a formula da agua?",
	  "answer":"H2O",
	  "userId":2
	}

    {...}
]
```

### Criar flashcard

`POST /flashcards/:userId - FORMATO DA REQUISIÇÃO`

```json
{
  "question":"Qual a capital do japão?",
  "answer":"Tokyo",
  "userId":3
}
```

### Excluir flashcard

`DELETE /flashcards/:userId - FORMATO DA REQUISIÇÃO`


### Editar flashcard

`PATCH /flashcards/:userId - FORMATO DA REQUISIÇÃO`

```json
{
  "question":"teste2",
  "answer": "12356"
}
```



