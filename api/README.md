# API

RESTful API do Traction

## Entidades / Objetos

* [Leads](#api/README.md)

## URL Base

```
https://api.traction.to/v1/
```

## Autenticação

A autenticação é realizada por meio de um token simples que pode ser gerado no painel do Traction

O Token deve ser passado via cabeçalho da requisição com a chave "Api-Token".


### Exemplo cURL
```curl
POST /v1/leads HTTP/1.1
Host: api.traction.to
Api-Token: a79e524ac5cbfba1ae1e60a94fafa79e
Content-Type: application/json
Content-Length: 89

{
    "name": "John Doe",
    "email": "john@traction.to",
    "phone": "+551111111111"
}
```

### Exemplo HTTP
```
POST /v1/leads HTTP/1.1
Host: api.traction.to
Api-Token: a79e524ac5cbfba1ae1e60a94fafa79e
Content-Type: application/json
Content-Length: 89

{
    "name": "John Doe",
    "email": "john@traction.to",
    "phone": "+551111111111"
}
```

