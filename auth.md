# Autenticacion

<a id="opIdtoken"></a>

## POST Obtener tokens para autorizar el acceso a las Apis.

POST /api/auth/token

> Body Parameters

```json
{
  "username": "admin",
  "password": "abcd1234"
}
```

### Params

|Name|Location|Type|Required|Description|
|---|---|---|---|---|
|body|body|[LoginRequest](#schemaloginrequest)| no |none|

> Response Examples

> 200 Response

```json
{
  "id": "b331336a-46f4-4fe4-a850-3208bfc2c398",
  "username": "admin",
  "role": "ADMIN",
  "accessToken": {
    "token": "3L3DBnz4d8T8bMAEkX8uityJEDZKXoucVa2Ynde6bdX8nhN8kfbJq8GSTLyY9QfJCwMeZnQSL1kt4EXoxD",
    "expiresIn": 3600
  },
  "contentToken": {
    "token": "3L3DBnz4d8T8bMAEkX8uityJEDZKXoucVa2Ynde6bdX8nhN8kfbJq8GSTLyY9QfJCwMeZnQSL1kt4EXoxD",
    "expiresIn": 3600
  },
  "refreshToken": {
    "token": "3L3DBnz4d8T8bMAEkX8uityJEDZKXoucVa2Ynde6bdX8nhN8kfbJq8GSTLyY9QfJCwMeZnQSL1kt4EXoxD",
    "expiresIn": 3600
  }
}
```

### Responses

|HTTP Status Code |Meaning|Description|Data schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|[LoginResponse](#schemaloginresponse)|

<a id="opIdrefreshtoken"></a>

## POST Obtener un token de acceso para autorizar el acceso a las Apis usando el token de refresco.

POST /api/auth/refreshtoken

> Body Parameters

```json
{
  "refreshToken": "3L3DBnz4d8T8bMAEkX8uityJEDZKXoucVa2Ynde6bdX8nhN8kfbJq8GSTLyY9QfJCwMeZnQSL1kt4EXoxD"
}
```

### Params

|Name|Location|Type|Required|Description|
|---|---|---|---|---|
|body|body|[TokenRefreshRequest](#schematokenrefreshrequest)| no |none|

> Response Examples

> 200 Response

```json
{
  "accessToken": {
    "token": "3L3DBnz4d8T8bMAEkX8uityJEDZKXoucVa2Ynde6bdX8nhN8kfbJq8GSTLyY9QfJCwMeZnQSL1kt4EXoxD",
    "expiresIn": 3600
  },
  "contentToken": {
    "token": "3L3DBnz4d8T8bMAEkX8uityJEDZKXoucVa2Ynde6bdX8nhN8kfbJq8GSTLyY9QfJCwMeZnQSL1kt4EXoxD",
    "expiresIn": 3600
  }
}
```

### Responses

|HTTP Status Code |Meaning|Description|Data schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|[TokenRefreshResponse](#schematokenrefreshresponse)|

# Data Schema

<h2 id="tocS_TokenRefreshResponse">TokenRefreshResponse</h2>

<a id="schematokenrefreshresponse"></a>
<a id="schema_TokenRefreshResponse"></a>
<a id="tocStokenrefreshresponse"></a>
<a id="tocstokenrefreshresponse"></a>

```json
{
  "accessToken": {
    "token": "3L3DBnz4d8T8bMAEkX8uityJEDZKXoucVa2Ynde6bdX8nhN8kfbJq8GSTLyY9QfJCwMeZnQSL1kt4EXoxD",
    "expiresIn": 3600
  },
  "contentToken": {
    "token": "3L3DBnz4d8T8bMAEkX8uityJEDZKXoucVa2Ynde6bdX8nhN8kfbJq8GSTLyY9QfJCwMeZnQSL1kt4EXoxD",
    "expiresIn": 3600
  }
}

```

### Attribute

|Name|Type|Required|Restrictions|Title|Description|
|---|---|---|---|---|---|
|accessToken|[TokenResponse](#schematokenresponse)|false|none||none|
|contentToken|[TokenResponse](#schematokenresponse)|false|none||none|

<h2 id="tocS_TokenResponse">TokenResponse</h2>

<a id="schematokenresponse"></a>
<a id="schema_TokenResponse"></a>
<a id="tocStokenresponse"></a>
<a id="tocstokenresponse"></a>

```json
{
  "token": "3L3DBnz4d8T8bMAEkX8uityJEDZKXoucVa2Ynde6bdX8nhN8kfbJq8GSTLyY9QfJCwMeZnQSL1kt4EXoxD",
  "expiresIn": 3600
}

```

### Attribute

|Name|Type|Required|Restrictions|Title|Description|
|---|---|---|---|---|---|
|token|string|false|none||token|
|expiresIn|integer(int64)|false|none||duracion del token|

<h2 id="tocS_TokenRefreshRequest">TokenRefreshRequest</h2>

<a id="schematokenrefreshrequest"></a>
<a id="schema_TokenRefreshRequest"></a>
<a id="tocStokenrefreshrequest"></a>
<a id="tocstokenrefreshrequest"></a>

```json
{
  "refreshToken": "3L3DBnz4d8T8bMAEkX8uityJEDZKXoucVa2Ynde6bdX8nhN8kfbJq8GSTLyY9QfJCwMeZnQSL1kt4EXoxD"
}

```

### Attribute

|Name|Type|Required|Restrictions|Title|Description|
|---|---|---|---|---|---|
|refreshToken|string|true|none||token de refresco|

<h2 id="tocS_LoginResponse">LoginResponse</h2>

<a id="schemaloginresponse"></a>
<a id="schema_LoginResponse"></a>
<a id="tocSloginresponse"></a>
<a id="tocsloginresponse"></a>

```json
{
  "id": "b331336a-46f4-4fe4-a850-3208bfc2c398",
  "username": "admin",
  "role": "ADMIN",
  "accessToken": {
    "token": "3L3DBnz4d8T8bMAEkX8uityJEDZKXoucVa2Ynde6bdX8nhN8kfbJq8GSTLyY9QfJCwMeZnQSL1kt4EXoxD",
    "expiresIn": 3600
  },
  "contentToken": {
    "token": "3L3DBnz4d8T8bMAEkX8uityJEDZKXoucVa2Ynde6bdX8nhN8kfbJq8GSTLyY9QfJCwMeZnQSL1kt4EXoxD",
    "expiresIn": 3600
  },
  "refreshToken": {
    "token": "3L3DBnz4d8T8bMAEkX8uityJEDZKXoucVa2Ynde6bdX8nhN8kfbJq8GSTLyY9QfJCwMeZnQSL1kt4EXoxD",
    "expiresIn": 3600
  }
}

```

### Attribute

|Name|Type|Required|Restrictions|Title|Description|
|---|---|---|---|---|---|
|id|string(uuid)|false|none||id del usuario|
|username|string|false|none||nombre del usuario|
|role|string|false|none||rol del usuario|
|accessToken|[TokenResponse](#schematokenresponse)|false|none||none|
|contentToken|[TokenResponse](#schematokenresponse)|false|none||none|
|refreshToken|[TokenResponse](#schematokenresponse)|false|none||none|

<h2 id="tocS_LoginRequest">LoginRequest</h2>

<a id="schemaloginrequest"></a>
<a id="schema_LoginRequest"></a>
<a id="tocSloginrequest"></a>
<a id="tocsloginrequest"></a>

```json
{
  "username": "admin",
  "password": "abcd1234"
}

```

### Attribute

|Name|Type|Required|Restrictions|Title|Description|
|---|---|---|---|---|---|
|username|string|true|none||nombre de usuario|
|password|string|true|none||contraseña|

