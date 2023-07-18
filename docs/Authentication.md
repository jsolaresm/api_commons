---
stoplight-id: pmh4yfvpg058e
---

# Authenticar las Apis

Las apis que usan el core COBIS requiere de un header de autorizacion, para el cual se debe invocar el servicio de autorización con las credenciales suministradas, a continuacion un ejemplo:

```http
POST v1/token
Content-Type: application/json
Accept: application/json

{
    "login": "admuser",
    "password": "123789",
    "office": "16",
    "role": "12",
    "server": "CTSSRV",
    "terminal": "TERMINAL1"
}
```

### Probar

Puede probar a continuacion la autenticacion, recuerde editar los valores en la pestana Body:

```yaml http
{
  "method": "post",
  "url": "https://lmdtei9tj5.execute-api.us-east-1.amazonaws.com/prod/v1/token",
  "headers":{
    "Content-Type": "application/json"
  },
  "body":{
  "login": "admuser",
  "password": "123789",
  "office": "16",
  "role": "12",
  "server": "CTSSRV",
  "terminal": "TERMINAL1"
}
}
\```