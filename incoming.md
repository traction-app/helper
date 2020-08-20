# Entrada de Leads

## API com autenticação

Lorem ipsum dolor sit amet

## Endpoint Público de Formulário

Uma das formas de enviar um lead para o Traction é através de uma requisição HTTP para um endpoint de um formulário previamente criado.

Para copiar um endpoint de formulário, acesse a página "Formulários", escolha um dos formulários existentes, abra a opção "Endpoint" e copie a URL disponível lá.

| **Parametro** | **Tipo** |
| :-----------: | :------: |
|     name      |  String  |
|     email     |  String  |
|     phone     |  String  |


### Exemplo de Payload

```JSON
{
	"name": "John Doe",
	"email": "john@example.com",
	"phone": "+551199999999",
}
```


### Exemplo de um POST Request

#### HTTP

```HTTP
POST /webhook/lead/2hiqisdhm1g4 HTTP/1.1
Host: traction.to
Content-Type: application/json
cache-control: no-cache
{
	"name": "John Doe",
	"email": "john@example.com",
	"phone": "+551199999999",
}
```

#### cURL

```cURL
curl -X POST \
  https://new-traction.test/webhook/lead/2hiqisdhm1g4 \
  -H 'Content-Type: application/json' \
  -d '{
	"name": "John Doe",
	"email": "john@example.com",
	"phone": "+551199999999",
}'
```

