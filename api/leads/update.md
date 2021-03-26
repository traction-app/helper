# Update

Atualiza um Lead

**Endpoint** : `/leads/:uuid`

**Parâmetro** : `uuid`

**Método** : `PUT|PATCH`

**Modelo**

```json
{
    "name": "string",
    "email": "string|required",
    "phone": "string",
    "campaign": "string",
    "form": "string",
    "channel": "string",
    "status": "string",
    "extra_fields": "array/object"
}
```

**Exemplo**

## Alterando o status de um lead para "Venda Fechado".

```json
{
    "status": "acquired"
}
```

## Alterando o telefone e campos extras.

```json
{
    "phone": "+5511100000000",
    "extra_fields": [
      {
        "key": "city",
        "value": "Araraquara"
      },
      {
        "key": "state",
        "value": "SP"
      }
    ]
}
```

## Resposta de Sucesso

**Code** : `200 OK`

**Exemplo de Resposta**

```json
{
    "uuid": "2f114dec-74bf-8c9a-8cb8-1ebbfb716ced",
    "name": "John Doe",
    "email": "john@traction.to",
    "phone": "+5511100000000",
    "campaign": null,
    "form": null,
    "channel": "Indicação",
    "status": "acquired",
    "extra_fields": [
        {
            "key": "city",
            "value": "Araraquara"
        },
        {
            "key": "state",
            "value": "SP"
        }
    ]
}
```