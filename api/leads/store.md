# Login

Cadastra um Lead

**Endpoint** : `/leads`

**Método** : `POST`

**Modelo**

```json
{
    "name": "string",
    "email": "string|required",
    "password": "string"    
}
```

**Exemplo**

```json
{
    "name": "John Doe",
    "email": "john@traction.to",
    "phone": "+551111111111"    
}
```

## Resposta de Sucesso

**Code** : `201 Created`

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
    "status": null,
    "extra_fields": null
}
```