# Login

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
    "extra_fields": "object"
}
```

**Exemplo**

```json
{
    "status": "acquired"
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
    "phone": "+551111111111",
    "campaign": null,
    "form": null,
    "channel": "Direto",
    "status": "acquired",
    "extra_fields": null
}
```