![Integrating your React project with APIs](thumbnail.png)

# AluraBooks

AluraBooks is an online store that sells books from Casa do Código.  
It is an MVP in its early stages, with many new features yet to be developed.

# JSONServer + JWT Auth

This is a mocked REST API using json-server and JWT.

## 🛠️ Installation

```bash
$ npm install
$ npm run start-auth
```

## 🛠️ How to register?

You can do this by making a POST request to:

```
POST http://localhost:8000/public/registrar
```

With the following data:

```
{
    "nome": "vinicios neves",
    "email": "vinicios@alura.com.br",
    "senha": "123456",
    "endereco": "Rua Vergueiro, 3185",
    "complemento": "Vila Mariana",
    "cep": "04101-300"
}
```

Note that the email is a unique field and users with duplicate emails will not be saved.

## 🛠️ How to log in?

You can do this by making a POST request to:

```
POST http://localhost:8000/public/login
```

With the following data:

```
{
  "email": "vinicios@alura.com.br",
  "senha":"123456"
}
```

You will receive a token in the following format:

```
{
   "access_token": "<ACCESS_TOKEN>",
   "user": { ... user data ... }
}
```

## Authenticate subsequent requests?

Then, add this same token to the header of the next requests:

```
Authorization: Bearer <ACCESS_TOKEN>
```

## 📚 More course information

AluraBooks is the project used throughout the entire training, and this API will be used in various different courses :)