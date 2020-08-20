# Entrada de Leads

## API com autenticação

Lorem ipsum dolor sit amet

## Endpoint Público de Formulário

Uma das formas de enviar um lead para o Traction é através de uma requisição HTTP para um endpoint de um formulário previamente criado.

Para copiar um endpoint de formulário, acesse a página "Formulários", escolha um dos formulários existentes, abra a opção "Endpoint" e copie a URL disponível lá.

| **Parametros** | **Tipo** |
| :------------: | :------: |
|      name      |  String  |
|     email      |  String  |
|     phone      |  String  |

**Campos Adicionais**

É possível enviar campos adicionais além dos campos primários (name, email e phone). Todos os campos adicionais serão convertidos em um novo objeto específico de campos adicionais e poderão ser alterados ou removidos dentro da ferramenta.

### Exemplo de endpoint

```
https://app.traction.to/webhook/lead/n01tc4rt20
```

### Exemplo de Payload

O payload deve ser do tipo JSON.

```JSON
{
  "name": "John Doe",
  "email": "john@example.com",
  "phone": "+551199999999",
}
```

Enviando parâmetros adicionais

```JSON
{
  "name": "John Doe",
  "email": "john@example.com",
  "phone": "+551199999999",
  "company": "Google",
  "city": "São Paulo",
  "state": "SP"
}
```

### Exemplo de um POST Request

#### Text-based (Raw)

```HTTP
POST /webhook/lead/n01tc4rt20 HTTP/1.1
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
  https://app.traction.to/webhook/lead/n01tc4rt20 \
  -H 'Content-Type: application/json' \
  -d '{
	"name": "John Doe",
	"email": "john@example.com",
	"phone": "+551199999999",
}'
```

### Retorno

```
Status 201 OK
```

```JSON
{
  "name": "John Doe",
  "email": "john@example.com",
  "phone": "+551199999999",
  "campaign": "Campanha de teste",
  "forms": "Formulário de teste",
  "channel": "Chatbot",
  "status": "qualified"
}
```
