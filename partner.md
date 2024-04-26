# Partner

<a id="opIdpostReserva"></a>

## POST Crear una reserva de boletas para un cliente, registrar visitantes, reservar parqueaderos y lockers.

POST /api/partner/reserva

> Body Parameters

```json
{
  "fecha": "26-04-2024",
  "tipoIdentificacion": "CC",
  "numeroIdentificacion": "1111222333",
  "nombre": "Juan",
  "apellido": "Perez",
  "email": "example@email.com",
  "telefono": "3005557777",
  "enviarCorreos": false,
  "boletas": [
    {
      "idTipoBoleta": 1,
      "visitante": {
        "tipoIdentificacion": "CC",
        "numeroIdentificacion": "1111222333",
        "nombre": "nombre 1",
        "apellido": "apellido 1",
        "email": "example@email.com",
        "telefono": "3005557777",
        "paisProcedencia": "Colombia",
        "ciudadProcedencia": "Bogota",
        "fechaNacimiento": "26-04-2024",
        "estaturaMayor145": true,
        "genero": "M"
      },
      "idTipoCasilla": 1
    }
  ],
  "vehiculos": [
    {
      "idTipoServicio": 1,
      "idTipoVehiculo": 1,
      "placa": "AAA111"
    }
  ]
}
```

### Params

|Name|Location|Type|Required|Description|
|---|---|---|---|---|
|body|body|[PostReservaPartner](#schemapostreservapartner)| no |none|

> Response Examples

> 200 Response

```json
{
  "message": "respuesta",
  "id": "1"
}
```

### Responses

|HTTP Status Code |Meaning|Description|Data schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|[IdMessageResponse](#schemaidmessageresponse)|

<a id="opIdpostReservaBoleta"></a>

## POST Reserva una boleta para un cliente.

POST /api/partner/reservaBoleta

> Body Parameters

```json
{
  "fecha": "26-04-2024",
  "tipoIdentificacion": "CC",
  "numeroIdentificacion": "1111222333",
  "nombre": "Juan",
  "apellido": "Perez",
  "email": "example@email.com",
  "telefono": "3005557777",
  "tarifa": "Adulto",
  "barcode": "1234567890123456789012",
  "orderId": 1
}
```

### Params

|Name|Location|Type|Required|Description|
|---|---|---|---|---|
|body|body|[PostReservaBoletaPartner](#schemapostreservaboletapartner)| no |none|

> Response Examples

> 200 Response

```json
{
  "message": "respuesta",
  "id": "1"
}
```

### Responses

|HTTP Status Code |Meaning|Description|Data schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|[IdMessageResponse](#schemaidmessageresponse)|

<a id="opIdgetPartnerInfo"></a>

## GET Obtener informacion del partner de la cuenta de usuario actual.

GET /api/partner/partnerInfo

> Response Examples

> 200 Response

```json
{
  "fechaCreado": "26-04-2024 12:37:36",
  "creadoPor": "string",
  "fechaModificado": "26-04-2024 12:37:36",
  "modificadoPor": "string",
  "id": "e3617a05-6e65-433f-b0db-c2a8747f3314",
  "nombre": "Partner 1",
  "boletasMax": 0,
  "boletasRest": 0,
  "account": {
    "fechaCreado": "26-04-2024 12:37:36",
    "creadoPor": "string",
    "fechaModificado": "26-04-2024 12:37:36",
    "modificadoPor": "string",
    "id": "23d4c71f-dc56-4d1e-b2b0-d64110d778ca",
    "name": "admin",
    "email": "example@email.com",
    "role": {
      "fechaCreado": "26-04-2024 12:37:36",
      "creadoPor": "string",
      "fechaModificado": "26-04-2024 12:37:36",
      "modificadoPor": "string",
      "id": 1,
      "name": "ADMIN",
      "urlInicio": "/index.html",
      "menus": [
        {
          "fechaCreado": "[",
          "creadoPor": "string",
          "fechaModificado": "[",
          "modificadoPor": "string",
          "role": {},
          "menu": {}
        }
      ],
      "estado": "ADMIN"
    },
    "estado": "ACTIVO"
  },
  "canal": {
    "fechaCreado": "26-04-2024 12:37:36",
    "creadoPor": "string",
    "fechaModificado": "26-04-2024 12:37:36",
    "modificadoPor": "string",
    "id": 1,
    "nombre": "Canal A"
  },
  "tarifas": [
    {
      "id": 1,
      "nombre": "TARIFA 1",
      "tipoBoleta": {
        "fechaCreado": "26-04-2024 12:37:36",
        "creadoPor": "string",
        "fechaModificado": "26-04-2024 12:37:36",
        "modificadoPor": "string",
        "id": 1,
        "producto": {
          "fechaCreado": "[",
          "creadoPor": "string",
          "fechaModificado": "[",
          "modificadoPor": "string",
          "id": "[",
          "codigo": "string",
          "nombre": "[",
          "descripcion": "[",
          "valorVariable": true,
          "valor": "[",
          "imagenId": "[",
          "tipo": "[",
          "productosCombo": [
            null
          ],
          "ventaFechaInicio": "[",
          "ventaFechaFin": "[",
          "consumoFechaInicio": "[",
          "consumoFechaFin": "[",
          "excepcionesDiasSemana": [
            null
          ],
          "activacionDesactivacionAutomatica": true
        },
        "categoriaEdad": {
          "fechaCreado": "[",
          "creadoPor": "string",
          "fechaModificado": "[",
          "modificadoPor": "string",
          "id": "[",
          "nombre": "[",
          "edadInicial": "[",
          "edadFinal": "["
        },
        "categoriaEstatura": {
          "fechaCreado": "[",
          "creadoPor": "string",
          "fechaModificado": "[",
          "modificadoPor": "string",
          "id": "[",
          "nombre": "[",
          "estaturaCmMin": "[",
          "estaturaCmMax": "["
        },
        "hikcentralPrivilegeGroupId": "1"
      }
    }
  ],
  "estado": "INACTIVO"
}
```

### Responses

|HTTP Status Code |Meaning|Description|Data schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|[Partner](#schemapartner)|

<a id="opIdgenerarQRBoleta"></a>

## GET Generar imagen del codigo QR de la boleta especificada.

GET /api/partner/generarQRBoleta

### Params

|Name|Location|Type|Required|Description|
|---|---|---|---|---|
|idBoleta|query|string(uuid)| yes |none|

> Response Examples

> 200 Response

```json
{
  "mimeType": "string",
  "imageBase64": "/9j/4AAQSkZJRgABAgAAAQABAAD/7QCEUGhvdG9zaG9wIDMuMAA4QklNBAQAAAAAAGccAigAYkZCTUQwMTAwMGFhNjAzMDAwMDY5MD"
}
```

### Responses

|HTTP Status Code |Meaning|Description|Data schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|[ImageBase64Response](#schemaimagebase64response)|

<a id="opIdgetBuscarVentaPartner"></a>

## GET Buscar ventas realizadas por el partner de la cuenta actual usando filtros de busqueda.

GET /api/partner/buscarVentaPartner

### Params

|Name|Location|Type|Required|Description|
|---|---|---|---|---|
|filter|query|string| no |none|
|page|query|integer(int32)| no |none|
|size|query|integer(int32)| no |none|
|sort|query|string| no |none|

> Response Examples

> 200 Response

```json
{
  "totalPages": 0,
  "totalElements": 0,
  "size": 0,
  "content": [
    {
      "fechaCreado": "26-04-2024 12:37:36",
      "creadoPor": "string",
      "fechaModificado": "26-04-2024 12:37:36",
      "modificadoPor": "string",
      "id": 1,
      "reservaId": "e4b3b3b3-4b3b-4b3b-4b3b-4b3b4b3b4b3b",
      "cliente": {
        "fechaCreado": "26-04-2024 12:37:36",
        "creadoPor": "string",
        "fechaModificado": "26-04-2024 12:37:36",
        "modificadoPor": "string",
        "identificacion": {
          "tipo": "[",
          "numero": "["
        },
        "primerNombre": "Nombre 1",
        "segundoNombre": "Nombre 2",
        "primerApellido": "Apellido 1",
        "segundoApellido": "Apellido 2",
        "nombreCompleto": "Nombre 1 Nombre 2 Apellido 1 Apellido 2",
        "email": "example@email.com",
        "telefono": "3005557777",
        "genero": "M",
        "fechaNacimiento": "26-04-2024",
        "ciudad": "11001.11.Co",
        "direccion": "Calle 1 # 1 - 1"
      },
      "registroTaquillaId": "b3b3b3b3-4b3b-4b3b-4b3b-4b3b4b3b4b3b",
      "reciboTaquilla": {
        "fechaCreado": "26-04-2024 12:37:36",
        "creadoPor": "string",
        "fechaModificado": "26-04-2024 12:37:36",
        "modificadoPor": "string",
        "id": 0,
        "numero": 0,
        "ultimoRegistroImpresion": {
          "fechaCreado": "[",
          "creadoPor": "string",
          "fechaModificado": "[",
          "modificadoPor": "string",
          "id": 0,
          "tipoImpresion": "[",
          "impresora": {},
          "identificador": "string",
          "estado": "[",
          "mensajeError": "["
        }
      },
      "recepcionPago": "TAQUILLA",
      "detallesVentaProductos": {
        "fechaCreado": "26-04-2024 12:37:36",
        "creadoPor": "string",
        "fechaModificado": "26-04-2024 12:37:36",
        "modificadoPor": "string",
        "id": 0,
        "clienteTipoIdentificacion": "CC",
        "clienteNumeroIdentificacion": "1111222333",
        "clienteNombre": "Nombre 1 Nombre 2 Apellido 1 Apellido 2",
        "reservaId": "dd36d635-3836-499b-b9e8-a21f7b8f8d99",
        "productoId": "facf4a34-c5cd-4888-bb4d-b65af8ae4dd9",
        "productoCodigo": "string",
        "productoTipo": "BOLETA",
        "productoNombre": "string",
        "productoValor": 0,
        "descuentoValor": 0,
        "valor": 0,
        "boletaId": "1bdd62d6-cfe6-46e0-9d28-6efc9e2d97ee",
        "reservaCasillaId": "ffa80c2d-a380-4e24-8b51-81cc376fde36",
        "reservaVehiculoId": "e3e6894b-2f0a-4368-ab7e-d7263f01cea3",
        "espacioParqueaderoId": 0,
        "reservaServicioAdicionalId": "e2db60eb-fe50-40b8-8bf7-7fd2f4953292",
        "reservaComboId": "b5015fcd-c071-4677-a321-3ff1e45a389a",
        "descuento": {
          "fechaCreado": "[",
          "creadoPor": "string",
          "fechaModificado": "[",
          "modificadoPor": "string",
          "id": "[",
          "nombre": "[",
          "tiposProducto": [
            null
          ],
          "aplicarConCodigo": "[",
          "codigo": "[",
          "aplicarConVigencia": "[",
          "vigenciaInicio": "[",
          "vigenciaFin": "[",
          "tipo": "[",
          "valor": "[",
          "consumoMax": "[",
          "consumoMaxCliente": "[",
          "consumo": "[",
          "estado": "[",
          "clientesObjetivo": "[",
          "clientesCompraronEnFechas": "[",
          "ccefFechaInicio": "[",
          "ccefFechaFin": "[",
          "clientesEspecificos": "["
        },
        "estadoPago": "APROBADO",
        "reservaFecha": "26-04-2024"
      },
      "transaccionesPago": {
        "fechaCreado": "26-04-2024 12:37:36",
        "creadoPor": "string",
        "fechaModificado": "26-04-2024 12:37:36",
        "modificadoPor": "string",
        "id": 0,
        "recepcionPago": "TAQUILLA",
        "metodoPago": {
          "fechaCreado": "[",
          "creadoPor": "string",
          "fechaModificado": "[",
          "modificadoPor": "string",
          "id": "[",
          "nombre": "[",
          "cuentaDestino": "[",
          "tipo": "[",
          "requiereDatosAutorizacion": "[",
          "recepcionesPago": [
            null
          ],
          "estado": "["
        },
        "valor": 50000,
        "transaccionTaquilla": {
          "fechaCreado": "[",
          "creadoPor": "string",
          "fechaModificado": "[",
          "modificadoPor": "string",
          "id": "[",
          "reservaId": "dd36d635-3836-499b-b9e8-a21f7b8f8d99",
          "metodoPago": {},
          "valor": "[",
          "numeroAutorizacion": "[",
          "ultimosDigitos": "[",
          "registroTaquillaId": "aded13d6-1970-4003-aa21-1f29fc5692a9",
          "cambioEfectivo": {},
          "reciboTaquillaNumero": 0,
          "taquillaId": 0,
          "taquillaNombre": "string"
        },
        "transaccionPasarela": {
          "fechaCreado": "[",
          "creadoPor": "string",
          "fechaModificado": "[",
          "modificadoPor": "string",
          "id": "[",
          "reservaId": "[",
          "tipoIdentificacionCliente": "[",
          "numeroIdentificacionCliente": "[",
          "valor": "[",
          "origen": "[",
          "ip": "[",
          "metodoPago": {},
          "fechaHoraInicio": "[",
          "fechaHoraFin": "[",
          "estado": "["
        },
        "transaccionParqueadero": {
          "fechaCreado": "[",
          "creadoPor": "string",
          "fechaModificado": "[",
          "modificadoPor": "string",
          "id": "[",
          "metodoPago": {},
          "valor": "[",
          "numeroAutorizacion": "[",
          "ultimosDigitos": "[",
          "zonaParqueaderoId": 0,
          "placa": "string",
          "fechaParqueo": "[",
          "cambioEfectivo": {}
        },
        "transaccionPartner": {
          "fechaCreado": "[",
          "creadoPor": "string",
          "fechaModificado": "[",
          "modificadoPor": "string",
          "id": "[",
          "partnerId": "bf408d53-df49-40a6-8455-a34bd4360901",
          "reservaId": "[",
          "tipoIdentificacionCliente": "[",
          "numeroIdentificacionCliente": "[",
          "valor": "[",
          "barcode": "string",
          "orderId": 0
        }
      },
      "valorSinDescuento": 100000,
      "valorPagoTotal": 100000,
      "canal": {
        "fechaCreado": "26-04-2024 12:37:36",
        "creadoPor": "string",
        "fechaModificado": "26-04-2024 12:37:36",
        "modificadoPor": "string",
        "id": 1,
        "nombre": "Canal A"
      },
      "reservaFecha": "26-04-2024",
      "taquilla": {
        "fechaCreado": "26-04-2024 12:37:36",
        "creadoPor": "string",
        "fechaModificado": "26-04-2024 12:37:36",
        "modificadoPor": "string",
        "id": 1,
        "nombre": "Taquilla 1",
        "conteoRecibos": 0,
        "estado": "ACTIVO",
        "impresoras": [
          {
            "fechaCreado": null,
            "creadoPor": null,
            "fechaModificado": null,
            "modificadoPor": null,
            "id": null,
            "nombre": null,
            "direccionIp": null,
            "estado": null,
            "marca": null,
            "referencia": null,
            "serial": null,
            "tipoImpresora": null
          }
        ]
      },
      "facturaVentaNumero": 1,
      "reservaDescuento": {
        "fechaCreado": "26-04-2024 12:37:36",
        "creadoPor": "string",
        "fechaModificado": "26-04-2024 12:37:36",
        "modificadoPor": "string",
        "id": "6ae369b6-847e-446a-a096-06e589c63db7",
        "nombre": "Descuento A",
        "tiposProducto": [
          {
            "fechaCreado": null,
            "creadoPor": null,
            "fechaModificado": null,
            "modificadoPor": null,
            "tipoProducto": null,
            "cantidadMax": null
          }
        ],
        "aplicarConCodigo": true,
        "codigo": "D1AHF524A0",
        "aplicarConVigencia": true,
        "vigenciaInicio": "26-04-2024 12:37:36",
        "vigenciaFin": "26-04-2024 12:37:36",
        "tipo": "PORCENTAJE",
        "valor": 20,
        "consumoMax": 100,
        "consumoMaxCliente": 1,
        "consumo": 5,
        "estado": "ACTIVO",
        "clientesObjetivo": true,
        "clientesCompraronEnFechas": true,
        "ccefFechaInicio": "26-04-2024 12:37:36",
        "ccefFechaFin": "26-04-2024 12:37:36",
        "clientesEspecificos": false
      }
    }
  ],
  "number": 0,
  "sort": {
    "empty": true,
    "sorted": true,
    "unsorted": true
  },
  "first": true,
  "pageable": {
    "offset": 0,
    "sort": {
      "empty": true,
      "sorted": true,
      "unsorted": true
    },
    "pageNumber": 0,
    "pageSize": 0,
    "unpaged": true,
    "paged": true
  },
  "numberOfElements": 0,
  "last": true,
  "empty": true
}
```

### Responses

|HTTP Status Code |Meaning|Description|Data schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|[PageVenta](#schemapageventa)|

<a id="opIdgetBuscarTipoVehiculo"></a>

## GET Buscar tipos de vehiculo usando filtros.

GET /api/partner/buscarTipoVehiculo

### Params

|Name|Location|Type|Required|Description|
|---|---|---|---|---|
|filter|query|string| no |none|
|page|query|integer(int32)| no |none|
|size|query|integer(int32)| no |none|
|sort|query|string| no |none|

> Response Examples

> 200 Response

```json
{
  "totalPages": 0,
  "totalElements": 0,
  "size": 0,
  "content": [
    {
      "fechaCreado": "26-04-2024 12:37:36",
      "creadoPor": "string",
      "fechaModificado": "26-04-2024 12:37:36",
      "modificadoPor": "string",
      "id": 1,
      "nombre": "AUTOMOVIL"
    }
  ],
  "number": 0,
  "sort": {
    "empty": true,
    "sorted": true,
    "unsorted": true
  },
  "first": true,
  "pageable": {
    "offset": 0,
    "sort": {
      "empty": true,
      "sorted": true,
      "unsorted": true
    },
    "pageNumber": 0,
    "pageSize": 0,
    "unpaged": true,
    "paged": true
  },
  "numberOfElements": 0,
  "last": true,
  "empty": true
}
```

### Responses

|HTTP Status Code |Meaning|Description|Data schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|[PageTipoVehiculo](#schemapagetipovehiculo)|

<a id="opIdgetBuscarTipoServicio"></a>

## GET Buscar tipos de servicio usando filtros.

GET /api/partner/buscarTipoServicio

### Params

|Name|Location|Type|Required|Description|
|---|---|---|---|---|
|filter|query|string| no |none|
|page|query|integer(int32)| no |none|
|size|query|integer(int32)| no |none|
|sort|query|string| no |none|

> Response Examples

> 200 Response

```json
{
  "totalPages": 0,
  "totalElements": 0,
  "size": 0,
  "content": [
    {
      "fechaCreado": "26-04-2024 12:37:36",
      "creadoPor": "string",
      "fechaModificado": "26-04-2024 12:37:36",
      "modificadoPor": "string",
      "id": 1,
      "producto": {
        "fechaCreado": "26-04-2024 12:37:36",
        "creadoPor": "string",
        "fechaModificado": "26-04-2024 12:37:36",
        "modificadoPor": "string",
        "id": "6c872a0f-4e21-460a-ae3d-2f3994f73dc6",
        "codigo": "string",
        "nombre": "Producto A",
        "descripcion": "Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua",
        "valorVariable": true,
        "valor": 30000,
        "imagenId": "644176ac-41f6-48ac-a4ef-3db5eb09fbf9",
        "tipo": "BOLETA",
        "productosCombo": [
          {
            "fechaCreado": null,
            "creadoPor": null,
            "fechaModificado": null,
            "modificadoPor": null,
            "producto": null,
            "cantidad": null
          }
        ],
        "ventaFechaInicio": "26-04-2024",
        "ventaFechaFin": "26-04-2024",
        "consumoFechaInicio": "26-04-2024",
        "consumoFechaFin": "26-04-2024",
        "excepcionesDiasSemana": [
          {
            "id": null,
            "tipo": null,
            "lunes": null,
            "martes": null,
            "miercoles": null,
            "jueves": null,
            "viernes": null,
            "sabado": null,
            "domingo": null
          }
        ],
        "activacionDesactivacionAutomatica": true
      },
      "tiposVehiculo": [
        {
          "fechaCreado": "26-04-2024 12:37:36",
          "creadoPor": "string",
          "fechaModificado": "26-04-2024 12:37:36",
          "modificadoPor": "string",
          "id": 1,
          "nombre": "AUTOMOVIL"
        }
      ],
      "estado": "ACTIVO"
    }
  ],
  "number": 0,
  "sort": {
    "empty": true,
    "sorted": true,
    "unsorted": true
  },
  "first": true,
  "pageable": {
    "offset": 0,
    "sort": {
      "empty": true,
      "sorted": true,
      "unsorted": true
    },
    "pageNumber": 0,
    "pageSize": 0,
    "unpaged": true,
    "paged": true
  },
  "numberOfElements": 0,
  "last": true,
  "empty": true
}
```

### Responses

|HTTP Status Code |Meaning|Description|Data schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|[PageTipoServicioParqueadero](#schemapagetiposervicioparqueadero)|

<a id="opIdgetBuscarTipoCasilla"></a>

## GET Buscar tipo de casilla usando filtros de busqueda.

GET /api/partner/buscarTipoCasilla

### Params

|Name|Location|Type|Required|Description|
|---|---|---|---|---|
|filter|query|string| no |none|
|page|query|integer(int32)| no |none|
|size|query|integer(int32)| no |none|
|sort|query|string| no |none|

> Response Examples

> 200 Response

```json
{
  "totalPages": 0,
  "totalElements": 0,
  "size": 0,
  "content": [
    {
      "fechaCreado": "26-04-2024 12:37:36",
      "creadoPor": "string",
      "fechaModificado": "26-04-2024 12:37:36",
      "modificadoPor": "string",
      "id": 1,
      "producto": {
        "fechaCreado": "26-04-2024 12:37:36",
        "creadoPor": "string",
        "fechaModificado": "26-04-2024 12:37:36",
        "modificadoPor": "string",
        "id": "6c872a0f-4e21-460a-ae3d-2f3994f73dc6",
        "codigo": "string",
        "nombre": "Producto A",
        "descripcion": "Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua",
        "valorVariable": true,
        "valor": 30000,
        "imagenId": "644176ac-41f6-48ac-a4ef-3db5eb09fbf9",
        "tipo": "BOLETA",
        "productosCombo": [
          {
            "fechaCreado": null,
            "creadoPor": null,
            "fechaModificado": null,
            "modificadoPor": null,
            "producto": null,
            "cantidad": null
          }
        ],
        "ventaFechaInicio": "26-04-2024",
        "ventaFechaFin": "26-04-2024",
        "consumoFechaInicio": "26-04-2024",
        "consumoFechaFin": "26-04-2024",
        "excepcionesDiasSemana": [
          {
            "id": null,
            "tipo": null,
            "lunes": null,
            "martes": null,
            "miercoles": null,
            "jueves": null,
            "viernes": null,
            "sabado": null,
            "domingo": null
          }
        ],
        "activacionDesactivacionAutomatica": true
      },
      "estado": "ACTIVO"
    }
  ],
  "number": 0,
  "sort": {
    "empty": true,
    "sorted": true,
    "unsorted": true
  },
  "first": true,
  "pageable": {
    "offset": 0,
    "sort": {
      "empty": true,
      "sorted": true,
      "unsorted": true
    },
    "pageNumber": 0,
    "pageSize": 0,
    "unpaged": true,
    "paged": true
  },
  "numberOfElements": 0,
  "last": true,
  "empty": true
}
```

### Responses

|HTTP Status Code |Meaning|Description|Data schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|[PageTipoCasilla](#schemapagetipocasilla)|

<a id="opIdgetBuscarTipoBoleta"></a>

## GET Buscar tipo de boleta usando filtros de busqueda.

GET /api/partner/buscarTipoBoleta

### Params

|Name|Location|Type|Required|Description|
|---|---|---|---|---|
|filter|query|string| no |none|
|page|query|integer(int32)| no |none|
|size|query|integer(int32)| no |none|
|sort|query|string| no |none|

> Response Examples

> 200 Response

```json
{
  "totalPages": 0,
  "totalElements": 0,
  "size": 0,
  "content": [
    {
      "fechaCreado": "26-04-2024 12:37:36",
      "creadoPor": "string",
      "fechaModificado": "26-04-2024 12:37:36",
      "modificadoPor": "string",
      "id": 1,
      "producto": {
        "fechaCreado": "26-04-2024 12:37:36",
        "creadoPor": "string",
        "fechaModificado": "26-04-2024 12:37:36",
        "modificadoPor": "string",
        "id": "6c872a0f-4e21-460a-ae3d-2f3994f73dc6",
        "codigo": "string",
        "nombre": "Producto A",
        "descripcion": "Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua",
        "valorVariable": true,
        "valor": 30000,
        "imagenId": "644176ac-41f6-48ac-a4ef-3db5eb09fbf9",
        "tipo": "BOLETA",
        "productosCombo": [
          {
            "fechaCreado": null,
            "creadoPor": null,
            "fechaModificado": null,
            "modificadoPor": null,
            "producto": null,
            "cantidad": null
          }
        ],
        "ventaFechaInicio": "26-04-2024",
        "ventaFechaFin": "26-04-2024",
        "consumoFechaInicio": "26-04-2024",
        "consumoFechaFin": "26-04-2024",
        "excepcionesDiasSemana": [
          {
            "id": null,
            "tipo": null,
            "lunes": null,
            "martes": null,
            "miercoles": null,
            "jueves": null,
            "viernes": null,
            "sabado": null,
            "domingo": null
          }
        ],
        "activacionDesactivacionAutomatica": true
      },
      "categoriaEdad": {
        "fechaCreado": "26-04-2024 12:37:36",
        "creadoPor": "string",
        "fechaModificado": "26-04-2024 12:37:36",
        "modificadoPor": "string",
        "id": 1,
        "nombre": "Categoria de edad A",
        "edadInicial": 8,
        "edadFinal": 60
      },
      "categoriaEstatura": {
        "fechaCreado": "26-04-2024 12:37:36",
        "creadoPor": "string",
        "fechaModificado": "26-04-2024 12:37:36",
        "modificadoPor": "string",
        "id": 1,
        "nombre": "Categoria de estatura A",
        "estaturaCmMin": 120,
        "estaturaCmMax": 180
      },
      "hikcentralPrivilegeGroupId": "1"
    }
  ],
  "number": 0,
  "sort": {
    "empty": true,
    "sorted": true,
    "unsorted": true
  },
  "first": true,
  "pageable": {
    "offset": 0,
    "sort": {
      "empty": true,
      "sorted": true,
      "unsorted": true
    },
    "pageNumber": 0,
    "pageSize": 0,
    "unpaged": true,
    "paged": true
  },
  "numberOfElements": 0,
  "last": true,
  "empty": true
}
```

### Responses

|HTTP Status Code |Meaning|Description|Data schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|[PageTipoBoleta](#schemapagetipoboleta)|

<a id="opIdgetBuscarReserva"></a>

## GET Buscar reserva usando filtros de busqueda.

GET /api/partner/buscarReserva

### Params

|Name|Location|Type|Required|Description|
|---|---|---|---|---|
|filter|query|string| no |none|
|page|query|integer(int32)| no |none|
|size|query|integer(int32)| no |none|
|sort|query|string| no |none|

> Response Examples

> 200 Response

```json
{
  "totalPages": 0,
  "totalElements": 0,
  "size": 0,
  "content": [
    {
      "fechaCreado": "26-04-2024 12:37:36",
      "creadoPor": "string",
      "fechaModificado": "26-04-2024 12:37:36",
      "modificadoPor": "string",
      "id": "c42f2c16-13e8-4d95-af60-134881bfbba7",
      "codigo": "Q6ASG1",
      "cliente": {
        "fechaCreado": "26-04-2024 12:37:36",
        "creadoPor": "string",
        "fechaModificado": "26-04-2024 12:37:36",
        "modificadoPor": "string",
        "identificacion": {
          "tipo": "[",
          "numero": "["
        },
        "primerNombre": "Nombre 1",
        "segundoNombre": "Nombre 2",
        "primerApellido": "Apellido 1",
        "segundoApellido": "Apellido 2",
        "nombreCompleto": "Nombre 1 Nombre 2 Apellido 1 Apellido 2",
        "email": "example@email.com",
        "telefono": "3005557777",
        "genero": "M",
        "fechaNacimiento": "26-04-2024",
        "ciudad": "11001.11.Co",
        "direccion": "Calle 1 # 1 - 1"
      },
      "fecha": "26-04-2024",
      "canal": {
        "fechaCreado": "26-04-2024 12:37:36",
        "creadoPor": "string",
        "fechaModificado": "26-04-2024 12:37:36",
        "modificadoPor": "string",
        "id": 1,
        "nombre": "Canal A"
      },
      "serviciosAdicionales": [
        {
          "fechaCreado": "26-04-2024 12:37:36",
          "creadoPor": "string",
          "fechaModificado": "26-04-2024 12:37:36",
          "modificadoPor": "string",
          "id": "497f6eca-6276-4993-bfeb-53cbbbba6f08",
          "servicioAdicional": {
            "fechaCreado": null,
            "creadoPor": null,
            "fechaModificado": null,
            "modificadoPor": null,
            "id": null,
            "producto": null,
            "categoriaServicio": null
          },
          "visitanteId": "8c06e1d1-3f95-45bd-b423-7fe0ab137edf",
          "consumido": false,
          "estadoPago": "APROBADO"
        }
      ],
      "casillas": [
        {
          "fechaCreado": "26-04-2024 12:37:36",
          "creadoPor": "string",
          "fechaModificado": "26-04-2024 12:37:36",
          "modificadoPor": "string",
          "id": "e3617a05-6e65-433f-b0db-c2a8747f3314",
          "casilla": {
            "fechaCreado": null,
            "creadoPor": null,
            "fechaModificado": null,
            "modificadoPor": null,
            "id": null,
            "hid": null,
            "nombre": null,
            "casillero": null,
            "tipo": null,
            "clave": null
          },
          "visitanteId": "71b09bc0-f6f6-4f86-b937-6c6689187632",
          "codigo": "6A5SD",
          "fechaPrimeraApertura": "26-04-2024 12:37:36",
          "estadoPago": "APROBADO"
        }
      ],
      "vehiculos": [
        {
          "fechaCreado": "26-04-2024 12:37:36",
          "creadoPor": "string",
          "fechaModificado": "26-04-2024 12:37:36",
          "modificadoPor": "string",
          "id": "df668ac0-9ea6-4772-b396-ed7e4b6e11fb",
          "vehiculo": {
            "fechaCreado": null,
            "creadoPor": null,
            "fechaModificado": null,
            "modificadoPor": null,
            "id": null,
            "placa": null,
            "tipo": null,
            "hikcentralVehicleId": null
          },
          "zonaParqueadero": {
            "fechaCreado": null,
            "creadoPor": null,
            "fechaModificado": null,
            "modificadoPor": null,
            "id": null,
            "nombre": null,
            "aforoMax": null,
            "reservaMax": null,
            "tiempoMaxSalidaSinCobro": null,
            "tipoServicio": null,
            "camarasPlaca": null,
            "parkingLotIndexCode": null,
            "listaNegraEntradaIndexCode": null,
            "listaBlancaSalidaIndexCode": null,
            "estado": null
          },
          "visitanteId": "df668ac0-9ea6-4772-b396-ed7e4b6e11fb",
          "estadoPago": "APROBADO"
        }
      ],
      "combos": [
        {
          "fechaCreado": "26-04-2024 12:37:36",
          "creadoPor": "string",
          "fechaModificado": "26-04-2024 12:37:36",
          "modificadoPor": "string",
          "id": "df668ac0-9ea6-4772-b396-ed7e4b6e11fb",
          "combo": {
            "fechaCreado": null,
            "creadoPor": null,
            "fechaModificado": null,
            "modificadoPor": null,
            "id": null,
            "codigo": null,
            "nombre": null,
            "descripcion": null,
            "valorVariable": null,
            "valor": null,
            "imagenId": null,
            "tipo": null,
            "productosCombo": null,
            "ventaFechaInicio": null,
            "ventaFechaFin": null,
            "consumoFechaInicio": null,
            "consumoFechaFin": null,
            "excepcionesDiasSemana": null,
            "activacionDesactivacionAutomatica": null
          },
          "reservaProducto": [
            {}
          ],
          "estadoPago": "APROBADO"
        }
      ],
      "descuento": {
        "fechaCreado": "26-04-2024 12:37:36",
        "creadoPor": "string",
        "fechaModificado": "26-04-2024 12:37:36",
        "modificadoPor": "string",
        "id": "6ae369b6-847e-446a-a096-06e589c63db7",
        "nombre": "Descuento A",
        "tiposProducto": [
          {
            "fechaCreado": null,
            "creadoPor": null,
            "fechaModificado": null,
            "modificadoPor": null,
            "tipoProducto": null,
            "cantidadMax": null
          }
        ],
        "aplicarConCodigo": true,
        "codigo": "D1AHF524A0",
        "aplicarConVigencia": true,
        "vigenciaInicio": "26-04-2024 12:37:36",
        "vigenciaFin": "26-04-2024 12:37:36",
        "tipo": "PORCENTAJE",
        "valor": 20,
        "consumoMax": 100,
        "consumoMaxCliente": 1,
        "consumo": 5,
        "estado": "ACTIVO",
        "clientesObjetivo": true,
        "clientesCompraronEnFechas": true,
        "ccefFechaInicio": "26-04-2024 12:37:36",
        "ccefFechaFin": "26-04-2024 12:37:36",
        "clientesEspecificos": false
      },
      "cortesia": {
        "fechaCreado": "26-04-2024 12:37:36",
        "creadoPor": "string",
        "fechaModificado": "26-04-2024 12:37:36",
        "modificadoPor": "string",
        "id": 0,
        "fechaExpiracion": "26-04-2024"
      },
      "registroVentaMasivaId": 1,
      "historialVentaMasivaId": 1
    }
  ],
  "number": 0,
  "sort": {
    "empty": true,
    "sorted": true,
    "unsorted": true
  },
  "first": true,
  "pageable": {
    "offset": 0,
    "sort": {
      "empty": true,
      "sorted": true,
      "unsorted": true
    },
    "pageNumber": 0,
    "pageSize": 0,
    "unpaged": true,
    "paged": true
  },
  "numberOfElements": 0,
  "last": true,
  "empty": true
}
```

### Responses

|HTTP Status Code |Meaning|Description|Data schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|[PageReserva](#schemapagereserva)|

# Data Schema

<h2 id="tocS_PageReserva">PageReserva</h2>

<a id="schemapagereserva"></a>
<a id="schema_PageReserva"></a>
<a id="tocSpagereserva"></a>
<a id="tocspagereserva"></a>

```json
{
  "totalPages": 0,
  "totalElements": 0,
  "size": 0,
  "content": [
    {
      "fechaCreado": "26-04-2024 12:37:36",
      "creadoPor": "string",
      "fechaModificado": "26-04-2024 12:37:36",
      "modificadoPor": "string",
      "id": "c42f2c16-13e8-4d95-af60-134881bfbba7",
      "codigo": "Q6ASG1",
      "cliente": {
        "fechaCreado": "26-04-2024 12:37:36",
        "creadoPor": "string",
        "fechaModificado": "26-04-2024 12:37:36",
        "modificadoPor": "string",
        "identificacion": {
          "tipo": "[",
          "numero": "["
        },
        "primerNombre": "Nombre 1",
        "segundoNombre": "Nombre 2",
        "primerApellido": "Apellido 1",
        "segundoApellido": "Apellido 2",
        "nombreCompleto": "Nombre 1 Nombre 2 Apellido 1 Apellido 2",
        "email": "example@email.com",
        "telefono": "3005557777",
        "genero": "M",
        "fechaNacimiento": "26-04-2024",
        "ciudad": "11001.11.Co",
        "direccion": "Calle 1 # 1 - 1"
      },
      "fecha": "26-04-2024",
      "canal": {
        "fechaCreado": "26-04-2024 12:37:36",
        "creadoPor": "string",
        "fechaModificado": "26-04-2024 12:37:36",
        "modificadoPor": "string",
        "id": 1,
        "nombre": "Canal A"
      },
      "serviciosAdicionales": [
        {
          "fechaCreado": "26-04-2024 12:37:36",
          "creadoPor": "string",
          "fechaModificado": "26-04-2024 12:37:36",
          "modificadoPor": "string",
          "id": "497f6eca-6276-4993-bfeb-53cbbbba6f08",
          "servicioAdicional": {
            "fechaCreado": null,
            "creadoPor": null,
            "fechaModificado": null,
            "modificadoPor": null,
            "id": null,
            "producto": null,
            "categoriaServicio": null
          },
          "visitanteId": "8c06e1d1-3f95-45bd-b423-7fe0ab137edf",
          "consumido": false,
          "estadoPago": "APROBADO"
        }
      ],
      "casillas": [
        {
          "fechaCreado": "26-04-2024 12:37:36",
          "creadoPor": "string",
          "fechaModificado": "26-04-2024 12:37:36",
          "modificadoPor": "string",
          "id": "e3617a05-6e65-433f-b0db-c2a8747f3314",
          "casilla": {
            "fechaCreado": null,
            "creadoPor": null,
            "fechaModificado": null,
            "modificadoPor": null,
            "id": null,
            "hid": null,
            "nombre": null,
            "casillero": null,
            "tipo": null,
            "clave": null
          },
          "visitanteId": "71b09bc0-f6f6-4f86-b937-6c6689187632",
          "codigo": "6A5SD",
          "fechaPrimeraApertura": "26-04-2024 12:37:36",
          "estadoPago": "APROBADO"
        }
      ],
      "vehiculos": [
        {
          "fechaCreado": "26-04-2024 12:37:36",
          "creadoPor": "string",
          "fechaModificado": "26-04-2024 12:37:36",
          "modificadoPor": "string",
          "id": "df668ac0-9ea6-4772-b396-ed7e4b6e11fb",
          "vehiculo": {
            "fechaCreado": null,
            "creadoPor": null,
            "fechaModificado": null,
            "modificadoPor": null,
            "id": null,
            "placa": null,
            "tipo": null,
            "hikcentralVehicleId": null
          },
          "zonaParqueadero": {
            "fechaCreado": null,
            "creadoPor": null,
            "fechaModificado": null,
            "modificadoPor": null,
            "id": null,
            "nombre": null,
            "aforoMax": null,
            "reservaMax": null,
            "tiempoMaxSalidaSinCobro": null,
            "tipoServicio": null,
            "camarasPlaca": null,
            "parkingLotIndexCode": null,
            "listaNegraEntradaIndexCode": null,
            "listaBlancaSalidaIndexCode": null,
            "estado": null
          },
          "visitanteId": "df668ac0-9ea6-4772-b396-ed7e4b6e11fb",
          "estadoPago": "APROBADO"
        }
      ],
      "combos": [
        {
          "fechaCreado": "26-04-2024 12:37:36",
          "creadoPor": "string",
          "fechaModificado": "26-04-2024 12:37:36",
          "modificadoPor": "string",
          "id": "df668ac0-9ea6-4772-b396-ed7e4b6e11fb",
          "combo": {
            "fechaCreado": null,
            "creadoPor": null,
            "fechaModificado": null,
            "modificadoPor": null,
            "id": null,
            "codigo": null,
            "nombre": null,
            "descripcion": null,
            "valorVariable": null,
            "valor": null,
            "imagenId": null,
            "tipo": null,
            "productosCombo": null,
            "ventaFechaInicio": null,
            "ventaFechaFin": null,
            "consumoFechaInicio": null,
            "consumoFechaFin": null,
            "excepcionesDiasSemana": null,
            "activacionDesactivacionAutomatica": null
          },
          "reservaProducto": [
            {}
          ],
          "estadoPago": "APROBADO"
        }
      ],
      "descuento": {
        "fechaCreado": "26-04-2024 12:37:36",
        "creadoPor": "string",
        "fechaModificado": "26-04-2024 12:37:36",
        "modificadoPor": "string",
        "id": "6ae369b6-847e-446a-a096-06e589c63db7",
        "nombre": "Descuento A",
        "tiposProducto": [
          {
            "fechaCreado": null,
            "creadoPor": null,
            "fechaModificado": null,
            "modificadoPor": null,
            "tipoProducto": null,
            "cantidadMax": null
          }
        ],
        "aplicarConCodigo": true,
        "codigo": "D1AHF524A0",
        "aplicarConVigencia": true,
        "vigenciaInicio": "26-04-2024 12:37:36",
        "vigenciaFin": "26-04-2024 12:37:36",
        "tipo": "PORCENTAJE",
        "valor": 20,
        "consumoMax": 100,
        "consumoMaxCliente": 1,
        "consumo": 5,
        "estado": "ACTIVO",
        "clientesObjetivo": true,
        "clientesCompraronEnFechas": true,
        "ccefFechaInicio": "26-04-2024 12:37:36",
        "ccefFechaFin": "26-04-2024 12:37:36",
        "clientesEspecificos": false
      },
      "cortesia": {
        "fechaCreado": "26-04-2024 12:37:36",
        "creadoPor": "string",
        "fechaModificado": "26-04-2024 12:37:36",
        "modificadoPor": "string",
        "id": 0,
        "fechaExpiracion": "26-04-2024"
      },
      "registroVentaMasivaId": 1,
      "historialVentaMasivaId": 1
    }
  ],
  "number": 0,
  "sort": {
    "empty": true,
    "sorted": true,
    "unsorted": true
  },
  "first": true,
  "pageable": {
    "offset": 0,
    "sort": {
      "empty": true,
      "sorted": true,
      "unsorted": true
    },
    "pageNumber": 0,
    "pageSize": 0,
    "unpaged": true,
    "paged": true
  },
  "numberOfElements": 0,
  "last": true,
  "empty": true
}

```

### Attribute

|Name|Type|Required|Restrictions|Title|Description|
|---|---|---|---|---|---|
|totalPages|integer(int32)|false|none||none|
|totalElements|integer(int64)|false|none||none|
|size|integer(int32)|false|none||none|
|content|[[Reserva](#schemareserva)]|false|none||[reserva asociada a la boleta]|
|number|integer(int32)|false|none||none|
|sort|[SortObject](#schemasortobject)|false|none||none|
|first|boolean|false|none||none|
|pageable|[PageableObject](#schemapageableobject)|false|none||none|
|numberOfElements|integer(int32)|false|none||none|
|last|boolean|false|none||none|
|empty|boolean|false|none||none|

<h2 id="tocS_PageableObject">PageableObject</h2>

<a id="schemapageableobject"></a>
<a id="schema_PageableObject"></a>
<a id="tocSpageableobject"></a>
<a id="tocspageableobject"></a>

```json
{
  "offset": 0,
  "sort": {
    "empty": true,
    "sorted": true,
    "unsorted": true
  },
  "pageNumber": 0,
  "pageSize": 0,
  "unpaged": true,
  "paged": true
}

```

### Attribute

|Name|Type|Required|Restrictions|Title|Description|
|---|---|---|---|---|---|
|offset|integer(int64)|false|none||none|
|sort|[SortObject](#schemasortobject)|false|none||none|
|pageNumber|integer(int32)|false|none||none|
|pageSize|integer(int32)|false|none||none|
|unpaged|boolean|false|none||none|
|paged|boolean|false|none||none|

<h2 id="tocS_SortObject">SortObject</h2>

<a id="schemasortobject"></a>
<a id="schema_SortObject"></a>
<a id="tocSsortobject"></a>
<a id="tocssortobject"></a>

```json
{
  "empty": true,
  "sorted": true,
  "unsorted": true
}

```

### Attribute

|Name|Type|Required|Restrictions|Title|Description|
|---|---|---|---|---|---|
|empty|boolean|false|none||none|
|sorted|boolean|false|none||none|
|unsorted|boolean|false|none||none|

<h2 id="tocS_Reserva">Reserva</h2>

<a id="schemareserva"></a>
<a id="schema_Reserva"></a>
<a id="tocSreserva"></a>
<a id="tocsreserva"></a>

```json
{
  "fechaCreado": "26-04-2024 12:37:36",
  "creadoPor": "string",
  "fechaModificado": "26-04-2024 12:37:36",
  "modificadoPor": "string",
  "id": "c42f2c16-13e8-4d95-af60-134881bfbba7",
  "codigo": "Q6ASG1",
  "cliente": {
    "fechaCreado": "26-04-2024 12:37:36",
    "creadoPor": "string",
    "fechaModificado": "26-04-2024 12:37:36",
    "modificadoPor": "string",
    "identificacion": {
      "tipo": "CC",
      "numero": "1111111111"
    },
    "primerNombre": "Nombre 1",
    "segundoNombre": "Nombre 2",
    "primerApellido": "Apellido 1",
    "segundoApellido": "Apellido 2",
    "nombreCompleto": "Nombre 1 Nombre 2 Apellido 1 Apellido 2",
    "email": "example@email.com",
    "telefono": "3005557777",
    "genero": "M",
    "fechaNacimiento": "26-04-2024",
    "ciudad": "11001.11.Co",
    "direccion": "Calle 1 # 1 - 1"
  },
  "fecha": "26-04-2024",
  "canal": {
    "fechaCreado": "26-04-2024 12:37:36",
    "creadoPor": "string",
    "fechaModificado": "26-04-2024 12:37:36",
    "modificadoPor": "string",
    "id": 1,
    "nombre": "Canal A"
  },
  "serviciosAdicionales": [
    {
      "fechaCreado": "26-04-2024 12:37:36",
      "creadoPor": "string",
      "fechaModificado": "26-04-2024 12:37:36",
      "modificadoPor": "string",
      "id": "497f6eca-6276-4993-bfeb-53cbbbba6f08",
      "servicioAdicional": {
        "fechaCreado": "26-04-2024 12:37:36",
        "creadoPor": "string",
        "fechaModificado": "26-04-2024 12:37:36",
        "modificadoPor": "string",
        "id": 1,
        "producto": {
          "fechaCreado": "[",
          "creadoPor": "string",
          "fechaModificado": "[",
          "modificadoPor": "string",
          "id": "[",
          "codigo": "string",
          "nombre": "[",
          "descripcion": "[",
          "valorVariable": true,
          "valor": "[",
          "imagenId": "[",
          "tipo": "[",
          "productosCombo": [
            null
          ],
          "ventaFechaInicio": "[",
          "ventaFechaFin": "[",
          "consumoFechaInicio": "[",
          "consumoFechaFin": "[",
          "excepcionesDiasSemana": [
            null
          ],
          "activacionDesactivacionAutomatica": true
        },
        "categoriaServicio": {
          "fechaCreado": "[",
          "creadoPor": "string",
          "fechaModificado": "[",
          "modificadoPor": "string",
          "id": "[",
          "nombre": "["
        }
      },
      "visitanteId": "8c06e1d1-3f95-45bd-b423-7fe0ab137edf",
      "consumido": false,
      "estadoPago": "APROBADO"
    }
  ],
  "casillas": [
    {
      "fechaCreado": "26-04-2024 12:37:36",
      "creadoPor": "string",
      "fechaModificado": "26-04-2024 12:37:36",
      "modificadoPor": "string",
      "id": "e3617a05-6e65-433f-b0db-c2a8747f3314",
      "casilla": {
        "fechaCreado": "26-04-2024 12:37:36",
        "creadoPor": "string",
        "fechaModificado": "26-04-2024 12:37:36",
        "modificadoPor": "string",
        "id": 1,
        "hid": "1527-1",
        "nombre": "226",
        "casillero": {
          "fechaCreado": "[",
          "creadoPor": "string",
          "fechaModificado": "[",
          "modificadoPor": "string",
          "id": "[",
          "hid": "[",
          "nombre": "[",
          "hikcentralPrivilegeGroupId": "[",
          "ubicacion": {},
          "prioridad": "["
        },
        "tipo": {
          "fechaCreado": "[",
          "creadoPor": "string",
          "fechaModificado": "[",
          "modificadoPor": "string",
          "id": "[",
          "producto": {},
          "estado": "["
        },
        "clave": "F457U"
      },
      "visitanteId": "71b09bc0-f6f6-4f86-b937-6c6689187632",
      "codigo": "6A5SD",
      "fechaPrimeraApertura": "26-04-2024 12:37:36",
      "estadoPago": "APROBADO"
    }
  ],
  "vehiculos": [
    {
      "fechaCreado": "26-04-2024 12:37:36",
      "creadoPor": "string",
      "fechaModificado": "26-04-2024 12:37:36",
      "modificadoPor": "string",
      "id": "df668ac0-9ea6-4772-b396-ed7e4b6e11fb",
      "vehiculo": {
        "fechaCreado": "26-04-2024 12:37:36",
        "creadoPor": "string",
        "fechaModificado": "26-04-2024 12:37:36",
        "modificadoPor": "string",
        "id": "a90fbb8e-6318-4d52-812b-2b98018460c5",
        "placa": "AAA111",
        "tipo": {
          "fechaCreado": "[",
          "creadoPor": "string",
          "fechaModificado": "[",
          "modificadoPor": "string",
          "id": "[",
          "nombre": "["
        },
        "hikcentralVehicleId": "1"
      },
      "zonaParqueadero": {
        "fechaCreado": "26-04-2024 12:37:36",
        "creadoPor": "string",
        "fechaModificado": "26-04-2024 12:37:36",
        "modificadoPor": "string",
        "id": 1,
        "nombre": "Zona de paqueadero A",
        "aforoMax": 40,
        "reservaMax": 30,
        "tiempoMaxSalidaSinCobro": 15,
        "tipoServicio": {
          "fechaCreado": "[",
          "creadoPor": "string",
          "fechaModificado": "[",
          "modificadoPor": "string",
          "id": "[",
          "producto": {},
          "tiposVehiculo": [
            null
          ],
          "estado": "["
        },
        "camarasPlaca": [
          {
            "fechaCreado": null,
            "creadoPor": null,
            "fechaModificado": null,
            "modificadoPor": null,
            "id": null,
            "nombre": null,
            "tipo": null,
            "zonaParqueadero": null,
            "cameraIndexCode": null,
            "estado": null
          }
        ],
        "parkingLotIndexCode": "1",
        "listaNegraEntradaIndexCode": "1",
        "listaBlancaSalidaIndexCode": "1",
        "estado": "ACTIVO"
      },
      "visitanteId": "df668ac0-9ea6-4772-b396-ed7e4b6e11fb",
      "estadoPago": "APROBADO"
    }
  ],
  "combos": [
    {
      "fechaCreado": "26-04-2024 12:37:36",
      "creadoPor": "string",
      "fechaModificado": "26-04-2024 12:37:36",
      "modificadoPor": "string",
      "id": "df668ac0-9ea6-4772-b396-ed7e4b6e11fb",
      "combo": {
        "fechaCreado": "26-04-2024 12:37:36",
        "creadoPor": "string",
        "fechaModificado": "26-04-2024 12:37:36",
        "modificadoPor": "string",
        "id": "6c872a0f-4e21-460a-ae3d-2f3994f73dc6",
        "codigo": "string",
        "nombre": "Producto A",
        "descripcion": "Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua",
        "valorVariable": true,
        "valor": 30000,
        "imagenId": "644176ac-41f6-48ac-a4ef-3db5eb09fbf9",
        "tipo": "BOLETA",
        "productosCombo": [
          {
            "fechaCreado": null,
            "creadoPor": null,
            "fechaModificado": null,
            "modificadoPor": null,
            "producto": null,
            "cantidad": null
          }
        ],
        "ventaFechaInicio": "26-04-2024",
        "ventaFechaFin": "26-04-2024",
        "consumoFechaInicio": "26-04-2024",
        "consumoFechaFin": "26-04-2024",
        "excepcionesDiasSemana": [
          {
            "id": null,
            "tipo": null,
            "lunes": null,
            "martes": null,
            "miercoles": null,
            "jueves": null,
            "viernes": null,
            "sabado": null,
            "domingo": null
          }
        ],
        "activacionDesactivacionAutomatica": true
      },
      "reservaProducto": [
        {
          "fechaCreado": "26-04-2024 12:37:36",
          "creadoPor": "string",
          "fechaModificado": "26-04-2024 12:37:36",
          "modificadoPor": "string",
          "id": 0,
          "tipoProducto": "BOLETA",
          "reservaProductoId": "839d0ba2-4b42-487d-b280-4c3ba14bac66"
        }
      ],
      "estadoPago": "APROBADO"
    }
  ],
  "descuento": {
    "fechaCreado": "26-04-2024 12:37:36",
    "creadoPor": "string",
    "fechaModificado": "26-04-2024 12:37:36",
    "modificadoPor": "string",
    "id": "6ae369b6-847e-446a-a096-06e589c63db7",
    "nombre": "Descuento A",
    "tiposProducto": [
      {
        "fechaCreado": "26-04-2024 12:37:36",
        "creadoPor": "string",
        "fechaModificado": "26-04-2024 12:37:36",
        "modificadoPor": "string",
        "tipoProducto": "BOLETA",
        "cantidadMax": 0
      }
    ],
    "aplicarConCodigo": true,
    "codigo": "D1AHF524A0",
    "aplicarConVigencia": true,
    "vigenciaInicio": "26-04-2024 12:37:36",
    "vigenciaFin": "26-04-2024 12:37:36",
    "tipo": "PORCENTAJE",
    "valor": 20,
    "consumoMax": 100,
    "consumoMaxCliente": 1,
    "consumo": 5,
    "estado": "ACTIVO",
    "clientesObjetivo": true,
    "clientesCompraronEnFechas": true,
    "ccefFechaInicio": "26-04-2024 12:37:36",
    "ccefFechaFin": "26-04-2024 12:37:36",
    "clientesEspecificos": false
  },
  "cortesia": {
    "fechaCreado": "26-04-2024 12:37:36",
    "creadoPor": "string",
    "fechaModificado": "26-04-2024 12:37:36",
    "modificadoPor": "string",
    "id": 0,
    "fechaExpiracion": "26-04-2024"
  },
  "registroVentaMasivaId": 1,
  "historialVentaMasivaId": 1
}

```

reserva asociada a la boleta

### Attribute

|Name|Type|Required|Restrictions|Title|Description|
|---|---|---|---|---|---|
|fechaCreado|string|false|none||none|
|creadoPor|string|false|none||none|
|fechaModificado|string|false|none||none|
|modificadoPor|string|false|none||none|
|id|string(uuid)|false|none||id de la reserva|
|codigo|string|false|none||codigo de la reserva|
|cliente|[Cliente](#schemacliente)|false|none||cliente asociado con esta reserva|
|fecha|string|false|none||fecha de la reserva|
|canal|[Canal](#schemacanal)|false|none||canal asociado con esta reserva|
|serviciosAdicionales|[[ReservaServicioAdicional](#schemareservaservicioadicional)]|false|none||[servicios adicionales asociados con esta reserva]|
|casillas|[[ReservaCasilla](#schemareservacasilla)]|false|none||[reserva de casilla asociada al visitante]|
|vehiculos|[[ReservaVehiculo](#schemareservavehiculo)]|false|none||[vehiculos asociados con esta reserva]|
|combos|[[ReservaCombo](#schemareservacombo)]|false|none||[combos de productos asociados con esta reserva]|
|descuento|[Descuento](#schemadescuento)|false|none||descuento asociado con esta reserva|
|cortesia|[ReservaCortesia](#schemareservacortesia)|false|none||cortesia asociada con esta reserva|
|registroVentaMasivaId|integer(int64)|false|none||id de la bolsa de ventas masivas asociada con esta reserva|
|historialVentaMasivaId|integer(int64)|false|none||id del historial de ventas masivas asociado con esta reserva|

<h2 id="tocS_ReservaCortesia">ReservaCortesia</h2>

<a id="schemareservacortesia"></a>
<a id="schema_ReservaCortesia"></a>
<a id="tocSreservacortesia"></a>
<a id="tocsreservacortesia"></a>

```json
{
  "fechaCreado": "26-04-2024 12:37:36",
  "creadoPor": "string",
  "fechaModificado": "26-04-2024 12:37:36",
  "modificadoPor": "string",
  "id": 0,
  "fechaExpiracion": "26-04-2024"
}

```

cortesia asociada con esta reserva

### Attribute

|Name|Type|Required|Restrictions|Title|Description|
|---|---|---|---|---|---|
|fechaCreado|string|false|none||none|
|creadoPor|string|false|none||none|
|fechaModificado|string|false|none||none|
|modificadoPor|string|false|none||none|
|id|integer(int64)|false|none||none|
|fechaExpiracion|string|false|none||none|

<h2 id="tocS_Descuento">Descuento</h2>

<a id="schemadescuento"></a>
<a id="schema_Descuento"></a>
<a id="tocSdescuento"></a>
<a id="tocsdescuento"></a>

```json
{
  "fechaCreado": "26-04-2024 12:37:36",
  "creadoPor": "string",
  "fechaModificado": "26-04-2024 12:37:36",
  "modificadoPor": "string",
  "id": "6ae369b6-847e-446a-a096-06e589c63db7",
  "nombre": "Descuento A",
  "tiposProducto": [
    {
      "fechaCreado": "26-04-2024 12:37:36",
      "creadoPor": "string",
      "fechaModificado": "26-04-2024 12:37:36",
      "modificadoPor": "string",
      "tipoProducto": "BOLETA",
      "cantidadMax": 0
    }
  ],
  "aplicarConCodigo": true,
  "codigo": "D1AHF524A0",
  "aplicarConVigencia": true,
  "vigenciaInicio": "26-04-2024 12:37:36",
  "vigenciaFin": "26-04-2024 12:37:36",
  "tipo": "PORCENTAJE",
  "valor": 20,
  "consumoMax": 100,
  "consumoMaxCliente": 1,
  "consumo": 5,
  "estado": "ACTIVO",
  "clientesObjetivo": true,
  "clientesCompraronEnFechas": true,
  "ccefFechaInicio": "26-04-2024 12:37:36",
  "ccefFechaFin": "26-04-2024 12:37:36",
  "clientesEspecificos": false
}

```

descuento asociado con esta reserva

### Attribute

|Name|Type|Required|Restrictions|Title|Description|
|---|---|---|---|---|---|
|fechaCreado|string|false|none||none|
|creadoPor|string|false|none||none|
|fechaModificado|string|false|none||none|
|modificadoPor|string|false|none||none|
|id|string(uuid)|false|none||id del descuento|
|nombre|string|false|none||nombre del descuento|
|tiposProducto|[[DescuentoTipoProducto](#schemadescuentotipoproducto)]|false|none||[Tipos de producto a los cuales se aplica este descuento, vacio para aplicar a todos]|
|aplicarConCodigo|boolean|false|none||determina si el descuento se aplica usando el codigo, de lo contrario se aplicara a todas las compras de productos que cumplan con las condiciones|
|codigo|string|false|none||codigo del descuento|
|aplicarConVigencia|boolean|false|none||determina si el descuento se aplica usando vigencia de tiempo, de lo contrario se aplicara a todas las compras de productos sin importar la fecha|
|vigenciaInicio|string|false|none||fecha de inicio de vigencia del descuento|
|vigenciaFin|string|false|none||fecha de finalizacion de vigencia del descuento|
|tipo|string|false|none||tipo de descuento|
|valor|number(double)|false|none||valor del descuento|
|consumoMax|integer(int32)|false|none||numero de consumos maximo del descuento, 0 para consumo ilimitado|
|consumoMaxCliente|integer(int32)|false|none||numero de consumos maximo por cliente, 0 para consumo ilimitado|
|consumo|integer(int32)|false|none||numero de consumos realizados hasta el momento|
|estado|string|false|none||estado del descuento|
|clientesObjetivo|boolean|false|none||determina si el descuento se aplica a los clientes objetivo, de lo contrario se aplicara a todos los clientes|
|clientesCompraronEnFechas|boolean|false|none||determina si los clientes objetivo seran los que hayan comprado dentro de el rango de fechas especificado tener compras en fechas especificas (si/no)|
|ccefFechaInicio|string|false|none||fecha de inicio en la que los clientes objetivo compraron|
|ccefFechaFin|string|false|none||fecha de finalizacion en la que los clientes objetivo compraron|
|clientesEspecificos|boolean|false|none||determina si los clientes objetivo seran clientes especificos (si/no)|

#### Enum

|Name|Value|
|---|---|
|tipo|PORCENTAJE|
|tipo|MONTO_FIJO|
|estado|INACTIVO|
|estado|ACTIVO|

<h2 id="tocS_DescuentoTipoProducto">DescuentoTipoProducto</h2>

<a id="schemadescuentotipoproducto"></a>
<a id="schema_DescuentoTipoProducto"></a>
<a id="tocSdescuentotipoproducto"></a>
<a id="tocsdescuentotipoproducto"></a>

```json
{
  "fechaCreado": "26-04-2024 12:37:36",
  "creadoPor": "string",
  "fechaModificado": "26-04-2024 12:37:36",
  "modificadoPor": "string",
  "tipoProducto": "BOLETA",
  "cantidadMax": 0
}

```

Tipos de producto a los cuales se aplica este descuento, vacio para aplicar a todos

### Attribute

|Name|Type|Required|Restrictions|Title|Description|
|---|---|---|---|---|---|
|fechaCreado|string|false|none||none|
|creadoPor|string|false|none||none|
|fechaModificado|string|false|none||none|
|modificadoPor|string|false|none||none|
|tipoProducto|string|false|none||none|
|cantidadMax|integer(int32)|false|none||none|

#### Enum

|Name|Value|
|---|---|
|tipoProducto|BOLETA|
|tipoProducto|PARQUEADERO|
|tipoProducto|CASILLA|
|tipoProducto|SERVICIO_ADICIONAL|
|tipoProducto|COMBO|

<h2 id="tocS_ReservaCombo">ReservaCombo</h2>

<a id="schemareservacombo"></a>
<a id="schema_ReservaCombo"></a>
<a id="tocSreservacombo"></a>
<a id="tocsreservacombo"></a>

```json
{
  "fechaCreado": "26-04-2024 12:37:36",
  "creadoPor": "string",
  "fechaModificado": "26-04-2024 12:37:36",
  "modificadoPor": "string",
  "id": "df668ac0-9ea6-4772-b396-ed7e4b6e11fb",
  "combo": {
    "fechaCreado": "26-04-2024 12:37:36",
    "creadoPor": "string",
    "fechaModificado": "26-04-2024 12:37:36",
    "modificadoPor": "string",
    "id": "6c872a0f-4e21-460a-ae3d-2f3994f73dc6",
    "codigo": "string",
    "nombre": "Producto A",
    "descripcion": "Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua",
    "valorVariable": true,
    "valor": 30000,
    "imagenId": "644176ac-41f6-48ac-a4ef-3db5eb09fbf9",
    "tipo": "BOLETA",
    "productosCombo": [
      {
        "fechaCreado": "26-04-2024 12:37:36",
        "creadoPor": "string",
        "fechaModificado": "26-04-2024 12:37:36",
        "modificadoPor": "string",
        "producto": {
          "fechaCreado": "[",
          "creadoPor": "string",
          "fechaModificado": "[",
          "modificadoPor": "string",
          "id": "[",
          "codigo": "string",
          "nombre": "[",
          "descripcion": "[",
          "valorVariable": true,
          "valor": "[",
          "imagenId": "[",
          "tipo": "[",
          "productosCombo": [
            null
          ],
          "ventaFechaInicio": "[",
          "ventaFechaFin": "[",
          "consumoFechaInicio": "[",
          "consumoFechaFin": "[",
          "excepcionesDiasSemana": [
            null
          ],
          "activacionDesactivacionAutomatica": true
        },
        "cantidad": 0
      }
    ],
    "ventaFechaInicio": "26-04-2024",
    "ventaFechaFin": "26-04-2024",
    "consumoFechaInicio": "26-04-2024",
    "consumoFechaFin": "26-04-2024",
    "excepcionesDiasSemana": [
      {
        "id": 0,
        "tipo": "VENTA",
        "lunes": true,
        "martes": true,
        "miercoles": true,
        "jueves": true,
        "viernes": true,
        "sabado": true,
        "domingo": true
      }
    ],
    "activacionDesactivacionAutomatica": true
  },
  "reservaProducto": [
    {
      "fechaCreado": "26-04-2024 12:37:36",
      "creadoPor": "string",
      "fechaModificado": "26-04-2024 12:37:36",
      "modificadoPor": "string",
      "id": 0,
      "tipoProducto": "BOLETA",
      "reservaProductoId": "839d0ba2-4b42-487d-b280-4c3ba14bac66"
    }
  ],
  "estadoPago": "APROBADO"
}

```

combos de productos asociados con esta reserva

### Attribute

|Name|Type|Required|Restrictions|Title|Description|
|---|---|---|---|---|---|
|fechaCreado|string|false|none||none|
|creadoPor|string|false|none||none|
|fechaModificado|string|false|none||none|
|modificadoPor|string|false|none||none|
|id|string(uuid)|false|none||id de la reserva de combo|
|combo|[Producto](#schemaproducto)|false|none||detalle del producto|
|reservaProducto|[[ReservaComboProducto](#schemareservacomboproducto)]|false|none||none|
|estadoPago|string|false|none||none|

#### Enum

|Name|Value|
|---|---|
|estadoPago|APROBADO|
|estadoPago|PENDIENTE|
|estadoPago|ANULADO|

<h2 id="tocS_ReservaComboProducto">ReservaComboProducto</h2>

<a id="schemareservacomboproducto"></a>
<a id="schema_ReservaComboProducto"></a>
<a id="tocSreservacomboproducto"></a>
<a id="tocsreservacomboproducto"></a>

```json
{
  "fechaCreado": "26-04-2024 12:37:36",
  "creadoPor": "string",
  "fechaModificado": "26-04-2024 12:37:36",
  "modificadoPor": "string",
  "id": 0,
  "tipoProducto": "BOLETA",
  "reservaProductoId": "839d0ba2-4b42-487d-b280-4c3ba14bac66"
}

```

### Attribute

|Name|Type|Required|Restrictions|Title|Description|
|---|---|---|---|---|---|
|fechaCreado|string|false|none||none|
|creadoPor|string|false|none||none|
|fechaModificado|string|false|none||none|
|modificadoPor|string|false|none||none|
|id|integer(int64)|false|none||none|
|tipoProducto|string|false|none||tipo de producto|
|reservaProductoId|string(uuid)|false|none||none|

#### Enum

|Name|Value|
|---|---|
|tipoProducto|BOLETA|
|tipoProducto|PARQUEADERO|
|tipoProducto|CASILLA|
|tipoProducto|SERVICIO_ADICIONAL|
|tipoProducto|COMBO|

<h2 id="tocS_Producto">Producto</h2>

<a id="schemaproducto"></a>
<a id="schema_Producto"></a>
<a id="tocSproducto"></a>
<a id="tocsproducto"></a>

```json
{
  "fechaCreado": "26-04-2024 12:37:36",
  "creadoPor": "string",
  "fechaModificado": "26-04-2024 12:37:36",
  "modificadoPor": "string",
  "id": "6c872a0f-4e21-460a-ae3d-2f3994f73dc6",
  "codigo": "string",
  "nombre": "Producto A",
  "descripcion": "Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua",
  "valorVariable": true,
  "valor": 30000,
  "imagenId": "644176ac-41f6-48ac-a4ef-3db5eb09fbf9",
  "tipo": "BOLETA",
  "productosCombo": [
    {
      "fechaCreado": "26-04-2024 12:37:36",
      "creadoPor": "string",
      "fechaModificado": "26-04-2024 12:37:36",
      "modificadoPor": "string",
      "producto": {
        "fechaCreado": "26-04-2024 12:37:36",
        "creadoPor": "string",
        "fechaModificado": "26-04-2024 12:37:36",
        "modificadoPor": "string",
        "id": "6c872a0f-4e21-460a-ae3d-2f3994f73dc6",
        "codigo": "string",
        "nombre": "Producto A",
        "descripcion": "Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua",
        "valorVariable": true,
        "valor": 30000,
        "imagenId": "644176ac-41f6-48ac-a4ef-3db5eb09fbf9",
        "tipo": "BOLETA",
        "productosCombo": [
          {
            "fechaCreado": null,
            "creadoPor": null,
            "fechaModificado": null,
            "modificadoPor": null,
            "producto": null,
            "cantidad": null
          }
        ],
        "ventaFechaInicio": "26-04-2024",
        "ventaFechaFin": "26-04-2024",
        "consumoFechaInicio": "26-04-2024",
        "consumoFechaFin": "26-04-2024",
        "excepcionesDiasSemana": [
          {
            "id": null,
            "tipo": null,
            "lunes": null,
            "martes": null,
            "miercoles": null,
            "jueves": null,
            "viernes": null,
            "sabado": null,
            "domingo": null
          }
        ],
        "activacionDesactivacionAutomatica": true
      },
      "cantidad": 0
    }
  ],
  "ventaFechaInicio": "26-04-2024",
  "ventaFechaFin": "26-04-2024",
  "consumoFechaInicio": "26-04-2024",
  "consumoFechaFin": "26-04-2024",
  "excepcionesDiasSemana": [
    {
      "id": 0,
      "tipo": "VENTA",
      "lunes": true,
      "martes": true,
      "miercoles": true,
      "jueves": true,
      "viernes": true,
      "sabado": true,
      "domingo": true
    }
  ],
  "activacionDesactivacionAutomatica": true
}

```

detalle del producto

### Attribute

|Name|Type|Required|Restrictions|Title|Description|
|---|---|---|---|---|---|
|fechaCreado|string|false|none||none|
|creadoPor|string|false|none||none|
|fechaModificado|string|false|none||none|
|modificadoPor|string|false|none||none|
|id|string(uuid)|false|none||id del producto|
|codigo|string|false|none||none|
|nombre|string|false|none||nombre del producto|
|descripcion|string|false|none||descripcion del producto|
|valorVariable|boolean|false|none||none|
|valor|number(double)|false|none||valor del producto|
|imagenId|string(uuid)|false|none||id de la imagen del producto del producto|
|tipo|string|false|none||tipo de producto|
|productosCombo|[[ProductoCombo](#schemaproductocombo)]|false|none||none|
|ventaFechaInicio|string|false|none||none|
|ventaFechaFin|string|false|none||none|
|consumoFechaInicio|string|false|none||none|
|consumoFechaFin|string|false|none||none|
|excepcionesDiasSemana|[[ProductoExcepcionesDiasSemana](#schemaproductoexcepcionesdiassemana)]|false|none||none|
|activacionDesactivacionAutomatica|boolean|false|none||none|

#### Enum

|Name|Value|
|---|---|
|tipo|BOLETA|
|tipo|PARQUEADERO|
|tipo|CASILLA|
|tipo|SERVICIO_ADICIONAL|
|tipo|COMBO|

<h2 id="tocS_ProductoExcepcionesDiasSemana">ProductoExcepcionesDiasSemana</h2>

<a id="schemaproductoexcepcionesdiassemana"></a>
<a id="schema_ProductoExcepcionesDiasSemana"></a>
<a id="tocSproductoexcepcionesdiassemana"></a>
<a id="tocsproductoexcepcionesdiassemana"></a>

```json
{
  "id": 0,
  "tipo": "VENTA",
  "lunes": true,
  "martes": true,
  "miercoles": true,
  "jueves": true,
  "viernes": true,
  "sabado": true,
  "domingo": true
}

```

### Attribute

|Name|Type|Required|Restrictions|Title|Description|
|---|---|---|---|---|---|
|id|integer(int64)|false|none||none|
|tipo|string|false|none||none|
|lunes|boolean|false|none||none|
|martes|boolean|false|none||none|
|miercoles|boolean|false|none||none|
|jueves|boolean|false|none||none|
|viernes|boolean|false|none||none|
|sabado|boolean|false|none||none|
|domingo|boolean|false|none||none|

#### Enum

|Name|Value|
|---|---|
|tipo|VENTA|
|tipo|CONSUMO|

<h2 id="tocS_ProductoCombo">ProductoCombo</h2>

<a id="schemaproductocombo"></a>
<a id="schema_ProductoCombo"></a>
<a id="tocSproductocombo"></a>
<a id="tocsproductocombo"></a>

```json
{
  "fechaCreado": "26-04-2024 12:37:36",
  "creadoPor": "string",
  "fechaModificado": "26-04-2024 12:37:36",
  "modificadoPor": "string",
  "producto": {
    "fechaCreado": "26-04-2024 12:37:36",
    "creadoPor": "string",
    "fechaModificado": "26-04-2024 12:37:36",
    "modificadoPor": "string",
    "id": "6c872a0f-4e21-460a-ae3d-2f3994f73dc6",
    "codigo": "string",
    "nombre": "Producto A",
    "descripcion": "Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua",
    "valorVariable": true,
    "valor": 30000,
    "imagenId": "644176ac-41f6-48ac-a4ef-3db5eb09fbf9",
    "tipo": "BOLETA",
    "productosCombo": [
      {
        "fechaCreado": "26-04-2024 12:37:36",
        "creadoPor": "string",
        "fechaModificado": "26-04-2024 12:37:36",
        "modificadoPor": "string",
        "producto": {
          "fechaCreado": "[",
          "creadoPor": "string",
          "fechaModificado": "[",
          "modificadoPor": "string",
          "id": "[",
          "codigo": "string",
          "nombre": "[",
          "descripcion": "[",
          "valorVariable": true,
          "valor": "[",
          "imagenId": "[",
          "tipo": "[",
          "productosCombo": [
            null
          ],
          "ventaFechaInicio": "[",
          "ventaFechaFin": "[",
          "consumoFechaInicio": "[",
          "consumoFechaFin": "[",
          "excepcionesDiasSemana": [
            null
          ],
          "activacionDesactivacionAutomatica": true
        },
        "cantidad": 0
      }
    ],
    "ventaFechaInicio": "26-04-2024",
    "ventaFechaFin": "26-04-2024",
    "consumoFechaInicio": "26-04-2024",
    "consumoFechaFin": "26-04-2024",
    "excepcionesDiasSemana": [
      {
        "id": 0,
        "tipo": "VENTA",
        "lunes": true,
        "martes": true,
        "miercoles": true,
        "jueves": true,
        "viernes": true,
        "sabado": true,
        "domingo": true
      }
    ],
    "activacionDesactivacionAutomatica": true
  },
  "cantidad": 0
}

```

### Attribute

|Name|Type|Required|Restrictions|Title|Description|
|---|---|---|---|---|---|
|fechaCreado|string|false|none||none|
|creadoPor|string|false|none||none|
|fechaModificado|string|false|none||none|
|modificadoPor|string|false|none||none|
|producto|[Producto](#schemaproducto)|false|none||detalle del producto|
|cantidad|integer(int32)|false|none||none|

<h2 id="tocS_ReservaVehiculo">ReservaVehiculo</h2>

<a id="schemareservavehiculo"></a>
<a id="schema_ReservaVehiculo"></a>
<a id="tocSreservavehiculo"></a>
<a id="tocsreservavehiculo"></a>

```json
{
  "fechaCreado": "26-04-2024 12:37:36",
  "creadoPor": "string",
  "fechaModificado": "26-04-2024 12:37:36",
  "modificadoPor": "string",
  "id": "df668ac0-9ea6-4772-b396-ed7e4b6e11fb",
  "vehiculo": {
    "fechaCreado": "26-04-2024 12:37:36",
    "creadoPor": "string",
    "fechaModificado": "26-04-2024 12:37:36",
    "modificadoPor": "string",
    "id": "a90fbb8e-6318-4d52-812b-2b98018460c5",
    "placa": "AAA111",
    "tipo": {
      "fechaCreado": "26-04-2024 12:37:36",
      "creadoPor": "string",
      "fechaModificado": "26-04-2024 12:37:36",
      "modificadoPor": "string",
      "id": 1,
      "nombre": "AUTOMOVIL"
    },
    "hikcentralVehicleId": "1"
  },
  "zonaParqueadero": {
    "fechaCreado": "26-04-2024 12:37:36",
    "creadoPor": "string",
    "fechaModificado": "26-04-2024 12:37:36",
    "modificadoPor": "string",
    "id": 1,
    "nombre": "Zona de paqueadero A",
    "aforoMax": 40,
    "reservaMax": 30,
    "tiempoMaxSalidaSinCobro": 15,
    "tipoServicio": {
      "fechaCreado": "26-04-2024 12:37:36",
      "creadoPor": "string",
      "fechaModificado": "26-04-2024 12:37:36",
      "modificadoPor": "string",
      "id": 1,
      "producto": {
        "fechaCreado": "26-04-2024 12:37:36",
        "creadoPor": "string",
        "fechaModificado": "26-04-2024 12:37:36",
        "modificadoPor": "string",
        "id": "6c872a0f-4e21-460a-ae3d-2f3994f73dc6",
        "codigo": "string",
        "nombre": "Producto A",
        "descripcion": "Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua",
        "valorVariable": true,
        "valor": 30000,
        "imagenId": "644176ac-41f6-48ac-a4ef-3db5eb09fbf9",
        "tipo": "BOLETA",
        "productosCombo": [
          {}
        ],
        "ventaFechaInicio": "26-04-2024",
        "ventaFechaFin": "26-04-2024",
        "consumoFechaInicio": "26-04-2024",
        "consumoFechaFin": "26-04-2024",
        "excepcionesDiasSemana": [
          {}
        ],
        "activacionDesactivacionAutomatica": true
      },
      "tiposVehiculo": [
        {
          "fechaCreado": "[",
          "creadoPor": "string",
          "fechaModificado": "[",
          "modificadoPor": "string",
          "id": "[",
          "nombre": "["
        }
      ],
      "estado": "ACTIVO"
    },
    "camarasPlaca": [
      {
        "fechaCreado": "26-04-2024 12:37:36",
        "creadoPor": "string",
        "fechaModificado": "26-04-2024 12:37:36",
        "modificadoPor": "string",
        "id": 1,
        "nombre": "Camara de placas 1",
        "tipo": "ENTRADA",
        "zonaParqueadero": {
          "fechaCreado": "[",
          "creadoPor": "string",
          "fechaModificado": "[",
          "modificadoPor": "string",
          "id": "[",
          "nombre": "[",
          "aforoMax": "[",
          "reservaMax": "[",
          "tiempoMaxSalidaSinCobro": "[",
          "tipoServicio": {},
          "camarasPlaca": [
            null
          ],
          "parkingLotIndexCode": "[",
          "listaNegraEntradaIndexCode": "[",
          "listaBlancaSalidaIndexCode": "[",
          "estado": "["
        },
        "cameraIndexCode": "1",
        "estado": "ACTIVO"
      }
    ],
    "parkingLotIndexCode": "1",
    "listaNegraEntradaIndexCode": "1",
    "listaBlancaSalidaIndexCode": "1",
    "estado": "ACTIVO"
  },
  "visitanteId": "df668ac0-9ea6-4772-b396-ed7e4b6e11fb",
  "estadoPago": "APROBADO"
}

```

vehiculos asociados con esta reserva

### Attribute

|Name|Type|Required|Restrictions|Title|Description|
|---|---|---|---|---|---|
|fechaCreado|string|false|none||none|
|creadoPor|string|false|none||none|
|fechaModificado|string|false|none||none|
|modificadoPor|string|false|none||none|
|id|string(uuid)|false|none||id de la reserva de vehiculo|
|vehiculo|[Vehiculo](#schemavehiculo)|false|none||none|
|zonaParqueadero|[ZonaParqueadero](#schemazonaparqueadero)|false|none||none|
|visitanteId|string(uuid)|false|none||id del visitante asociado a la reserva|
|estadoPago|string|false|none||estado del pago de la reserva|

#### Enum

|Name|Value|
|---|---|
|estadoPago|APROBADO|
|estadoPago|PENDIENTE|
|estadoPago|ANULADO|

<h2 id="tocS_ZonaParqueadero">ZonaParqueadero</h2>

<a id="schemazonaparqueadero"></a>
<a id="schema_ZonaParqueadero"></a>
<a id="tocSzonaparqueadero"></a>
<a id="tocszonaparqueadero"></a>

```json
{
  "fechaCreado": "26-04-2024 12:37:36",
  "creadoPor": "string",
  "fechaModificado": "26-04-2024 12:37:36",
  "modificadoPor": "string",
  "id": 1,
  "nombre": "Zona de paqueadero A",
  "aforoMax": 40,
  "reservaMax": 30,
  "tiempoMaxSalidaSinCobro": 15,
  "tipoServicio": {
    "fechaCreado": "26-04-2024 12:37:36",
    "creadoPor": "string",
    "fechaModificado": "26-04-2024 12:37:36",
    "modificadoPor": "string",
    "id": 1,
    "producto": {
      "fechaCreado": "26-04-2024 12:37:36",
      "creadoPor": "string",
      "fechaModificado": "26-04-2024 12:37:36",
      "modificadoPor": "string",
      "id": "6c872a0f-4e21-460a-ae3d-2f3994f73dc6",
      "codigo": "string",
      "nombre": "Producto A",
      "descripcion": "Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua",
      "valorVariable": true,
      "valor": 30000,
      "imagenId": "644176ac-41f6-48ac-a4ef-3db5eb09fbf9",
      "tipo": "BOLETA",
      "productosCombo": [
        {
          "fechaCreado": "[",
          "creadoPor": "string",
          "fechaModificado": "[",
          "modificadoPor": "string",
          "producto": {},
          "cantidad": 0
        }
      ],
      "ventaFechaInicio": "26-04-2024",
      "ventaFechaFin": "26-04-2024",
      "consumoFechaInicio": "26-04-2024",
      "consumoFechaFin": "26-04-2024",
      "excepcionesDiasSemana": [
        {
          "id": 0,
          "tipo": "[",
          "lunes": true,
          "martes": true,
          "miercoles": true,
          "jueves": true,
          "viernes": true,
          "sabado": true,
          "domingo": true
        }
      ],
      "activacionDesactivacionAutomatica": true
    },
    "tiposVehiculo": [
      {
        "fechaCreado": "26-04-2024 12:37:36",
        "creadoPor": "string",
        "fechaModificado": "26-04-2024 12:37:36",
        "modificadoPor": "string",
        "id": 1,
        "nombre": "AUTOMOVIL"
      }
    ],
    "estado": "ACTIVO"
  },
  "camarasPlaca": [
    {
      "fechaCreado": "26-04-2024 12:37:36",
      "creadoPor": "string",
      "fechaModificado": "26-04-2024 12:37:36",
      "modificadoPor": "string",
      "id": 1,
      "nombre": "Camara de placas 1",
      "tipo": "ENTRADA",
      "zonaParqueadero": {
        "fechaCreado": "26-04-2024 12:37:36",
        "creadoPor": "string",
        "fechaModificado": "26-04-2024 12:37:36",
        "modificadoPor": "string",
        "id": 1,
        "nombre": "Zona de paqueadero A",
        "aforoMax": 40,
        "reservaMax": 30,
        "tiempoMaxSalidaSinCobro": 15,
        "tipoServicio": {
          "fechaCreado": "[",
          "creadoPor": "string",
          "fechaModificado": "[",
          "modificadoPor": "string",
          "id": "[",
          "producto": {},
          "tiposVehiculo": [
            null
          ],
          "estado": "["
        },
        "camarasPlaca": [
          {
            "fechaCreado": null,
            "creadoPor": null,
            "fechaModificado": null,
            "modificadoPor": null,
            "id": null,
            "nombre": null,
            "tipo": null,
            "zonaParqueadero": null,
            "cameraIndexCode": null,
            "estado": null
          }
        ],
        "parkingLotIndexCode": "1",
        "listaNegraEntradaIndexCode": "1",
        "listaBlancaSalidaIndexCode": "1",
        "estado": "ACTIVO"
      },
      "cameraIndexCode": "1",
      "estado": "ACTIVO"
    }
  ],
  "parkingLotIndexCode": "1",
  "listaNegraEntradaIndexCode": "1",
  "listaBlancaSalidaIndexCode": "1",
  "estado": "ACTIVO"
}

```

### Attribute

|Name|Type|Required|Restrictions|Title|Description|
|---|---|---|---|---|---|
|fechaCreado|string|false|none||none|
|creadoPor|string|false|none||none|
|fechaModificado|string|false|none||none|
|modificadoPor|string|false|none||none|
|id|integer(int64)|false|none||id de la zona de parqueadero|
|nombre|string|false|none||nombre de la zona de parqueadero|
|aforoMax|integer(int32)|false|none||cantidad maxima de vehiculos que permite esta zona de parqueaderos|
|reservaMax|integer(int32)|false|none||cantidad maxima reservable de espacios en la zona de parqueadero por dia|
|tiempoMaxSalidaSinCobro|integer(int32)|false|none||tiempo maximo de estadia en el parqueadero sin cobro en minutos|
|tipoServicio|[TipoServicioParqueadero](#schematiposervicioparqueadero)|false|none||none|
|camarasPlaca|[[CamaraPlacasHikvision](#schemacamaraplacashikvision)]|false|none||none|
|parkingLotIndexCode|string|false|none||id del parqueadero de hikcentral|
|listaNegraEntradaIndexCode|string|false|none||id del grupo de vehiculos de la lista de negra de entrada|
|listaBlancaSalidaIndexCode|string|false|none||id del grupo de vehiculos de la lista de blanca de salida|
|estado|string|false|none||estado de la zona de parqueadero|

#### Enum

|Name|Value|
|---|---|
|estado|ACTIVO|
|estado|INACTIVO|

<h2 id="tocS_CamaraPlacasHikvision">CamaraPlacasHikvision</h2>

<a id="schemacamaraplacashikvision"></a>
<a id="schema_CamaraPlacasHikvision"></a>
<a id="tocScamaraplacashikvision"></a>
<a id="tocscamaraplacashikvision"></a>

```json
{
  "fechaCreado": "26-04-2024 12:37:36",
  "creadoPor": "string",
  "fechaModificado": "26-04-2024 12:37:36",
  "modificadoPor": "string",
  "id": 1,
  "nombre": "Camara de placas 1",
  "tipo": "ENTRADA",
  "zonaParqueadero": {
    "fechaCreado": "26-04-2024 12:37:36",
    "creadoPor": "string",
    "fechaModificado": "26-04-2024 12:37:36",
    "modificadoPor": "string",
    "id": 1,
    "nombre": "Zona de paqueadero A",
    "aforoMax": 40,
    "reservaMax": 30,
    "tiempoMaxSalidaSinCobro": 15,
    "tipoServicio": {
      "fechaCreado": "26-04-2024 12:37:36",
      "creadoPor": "string",
      "fechaModificado": "26-04-2024 12:37:36",
      "modificadoPor": "string",
      "id": 1,
      "producto": {
        "fechaCreado": "26-04-2024 12:37:36",
        "creadoPor": "string",
        "fechaModificado": "26-04-2024 12:37:36",
        "modificadoPor": "string",
        "id": "6c872a0f-4e21-460a-ae3d-2f3994f73dc6",
        "codigo": "string",
        "nombre": "Producto A",
        "descripcion": "Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua",
        "valorVariable": true,
        "valor": 30000,
        "imagenId": "644176ac-41f6-48ac-a4ef-3db5eb09fbf9",
        "tipo": "BOLETA",
        "productosCombo": [
          {}
        ],
        "ventaFechaInicio": "26-04-2024",
        "ventaFechaFin": "26-04-2024",
        "consumoFechaInicio": "26-04-2024",
        "consumoFechaFin": "26-04-2024",
        "excepcionesDiasSemana": [
          {}
        ],
        "activacionDesactivacionAutomatica": true
      },
      "tiposVehiculo": [
        {
          "fechaCreado": "[",
          "creadoPor": "string",
          "fechaModificado": "[",
          "modificadoPor": "string",
          "id": "[",
          "nombre": "["
        }
      ],
      "estado": "ACTIVO"
    },
    "camarasPlaca": [
      {
        "fechaCreado": "26-04-2024 12:37:36",
        "creadoPor": "string",
        "fechaModificado": "26-04-2024 12:37:36",
        "modificadoPor": "string",
        "id": 1,
        "nombre": "Camara de placas 1",
        "tipo": "ENTRADA",
        "zonaParqueadero": {
          "fechaCreado": "[",
          "creadoPor": "string",
          "fechaModificado": "[",
          "modificadoPor": "string",
          "id": "[",
          "nombre": "[",
          "aforoMax": "[",
          "reservaMax": "[",
          "tiempoMaxSalidaSinCobro": "[",
          "tipoServicio": {},
          "camarasPlaca": [
            null
          ],
          "parkingLotIndexCode": "[",
          "listaNegraEntradaIndexCode": "[",
          "listaBlancaSalidaIndexCode": "[",
          "estado": "["
        },
        "cameraIndexCode": "1",
        "estado": "ACTIVO"
      }
    ],
    "parkingLotIndexCode": "1",
    "listaNegraEntradaIndexCode": "1",
    "listaBlancaSalidaIndexCode": "1",
    "estado": "ACTIVO"
  },
  "cameraIndexCode": "1",
  "estado": "ACTIVO"
}

```

### Attribute

|Name|Type|Required|Restrictions|Title|Description|
|---|---|---|---|---|---|
|fechaCreado|string|false|none||none|
|creadoPor|string|false|none||none|
|fechaModificado|string|false|none||none|
|modificadoPor|string|false|none||none|
|id|integer(int64)|false|none||id de la camara de placas|
|nombre|string|false|none||nombre de la camara de placas|
|tipo|string|false|none||tipo de uso de la camara de placas|
|zonaParqueadero|[ZonaParqueadero](#schemazonaparqueadero)|false|none||none|
|cameraIndexCode|string|false|none||id la camara de placas de hikcentral|
|estado|string|false|none||estado la camara de placas de hikcentral|

#### Enum

|Name|Value|
|---|---|
|tipo|ENTRADA|
|tipo|SALIDA|
|estado|ACTIVO|
|estado|INACTIVO|

<h2 id="tocS_TipoServicioParqueadero">TipoServicioParqueadero</h2>

<a id="schematiposervicioparqueadero"></a>
<a id="schema_TipoServicioParqueadero"></a>
<a id="tocStiposervicioparqueadero"></a>
<a id="tocstiposervicioparqueadero"></a>

```json
{
  "fechaCreado": "26-04-2024 12:37:36",
  "creadoPor": "string",
  "fechaModificado": "26-04-2024 12:37:36",
  "modificadoPor": "string",
  "id": 1,
  "producto": {
    "fechaCreado": "26-04-2024 12:37:36",
    "creadoPor": "string",
    "fechaModificado": "26-04-2024 12:37:36",
    "modificadoPor": "string",
    "id": "6c872a0f-4e21-460a-ae3d-2f3994f73dc6",
    "codigo": "string",
    "nombre": "Producto A",
    "descripcion": "Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua",
    "valorVariable": true,
    "valor": 30000,
    "imagenId": "644176ac-41f6-48ac-a4ef-3db5eb09fbf9",
    "tipo": "BOLETA",
    "productosCombo": [
      {
        "fechaCreado": "26-04-2024 12:37:36",
        "creadoPor": "string",
        "fechaModificado": "26-04-2024 12:37:36",
        "modificadoPor": "string",
        "producto": {
          "fechaCreado": "[",
          "creadoPor": "string",
          "fechaModificado": "[",
          "modificadoPor": "string",
          "id": "[",
          "codigo": "string",
          "nombre": "[",
          "descripcion": "[",
          "valorVariable": true,
          "valor": "[",
          "imagenId": "[",
          "tipo": "[",
          "productosCombo": [
            null
          ],
          "ventaFechaInicio": "[",
          "ventaFechaFin": "[",
          "consumoFechaInicio": "[",
          "consumoFechaFin": "[",
          "excepcionesDiasSemana": [
            null
          ],
          "activacionDesactivacionAutomatica": true
        },
        "cantidad": 0
      }
    ],
    "ventaFechaInicio": "26-04-2024",
    "ventaFechaFin": "26-04-2024",
    "consumoFechaInicio": "26-04-2024",
    "consumoFechaFin": "26-04-2024",
    "excepcionesDiasSemana": [
      {
        "id": 0,
        "tipo": "VENTA",
        "lunes": true,
        "martes": true,
        "miercoles": true,
        "jueves": true,
        "viernes": true,
        "sabado": true,
        "domingo": true
      }
    ],
    "activacionDesactivacionAutomatica": true
  },
  "tiposVehiculo": [
    {
      "fechaCreado": "26-04-2024 12:37:36",
      "creadoPor": "string",
      "fechaModificado": "26-04-2024 12:37:36",
      "modificadoPor": "string",
      "id": 1,
      "nombre": "AUTOMOVIL"
    }
  ],
  "estado": "ACTIVO"
}

```

### Attribute

|Name|Type|Required|Restrictions|Title|Description|
|---|---|---|---|---|---|
|fechaCreado|string|false|none||none|
|creadoPor|string|false|none||none|
|fechaModificado|string|false|none||none|
|modificadoPor|string|false|none||none|
|id|integer(int64)|false|none||id del tipo de servicio de parqueadero|
|producto|[Producto](#schemaproducto)|false|none||detalle del producto|
|tiposVehiculo|[[TipoVehiculo](#schematipovehiculo)]|false|none||[tipo de vehiculo]|
|estado|string|false|none||estado del tipo de servicio de parqueadero|

#### Enum

|Name|Value|
|---|---|
|estado|ACTIVO|
|estado|INACTIVO|

<h2 id="tocS_TipoVehiculo">TipoVehiculo</h2>

<a id="schematipovehiculo"></a>
<a id="schema_TipoVehiculo"></a>
<a id="tocStipovehiculo"></a>
<a id="tocstipovehiculo"></a>

```json
{
  "fechaCreado": "26-04-2024 12:37:36",
  "creadoPor": "string",
  "fechaModificado": "26-04-2024 12:37:36",
  "modificadoPor": "string",
  "id": 1,
  "nombre": "AUTOMOVIL"
}

```

tipo de vehiculo

### Attribute

|Name|Type|Required|Restrictions|Title|Description|
|---|---|---|---|---|---|
|fechaCreado|string|false|none||none|
|creadoPor|string|false|none||none|
|fechaModificado|string|false|none||none|
|modificadoPor|string|false|none||none|
|id|integer(int64)|false|none||id del tipo de vehiculo|
|nombre|string|false|none||nombre del tipo de vehiculo|

<h2 id="tocS_Vehiculo">Vehiculo</h2>

<a id="schemavehiculo"></a>
<a id="schema_Vehiculo"></a>
<a id="tocSvehiculo"></a>
<a id="tocsvehiculo"></a>

```json
{
  "fechaCreado": "26-04-2024 12:37:36",
  "creadoPor": "string",
  "fechaModificado": "26-04-2024 12:37:36",
  "modificadoPor": "string",
  "id": "a90fbb8e-6318-4d52-812b-2b98018460c5",
  "placa": "AAA111",
  "tipo": {
    "fechaCreado": "26-04-2024 12:37:36",
    "creadoPor": "string",
    "fechaModificado": "26-04-2024 12:37:36",
    "modificadoPor": "string",
    "id": 1,
    "nombre": "AUTOMOVIL"
  },
  "hikcentralVehicleId": "1"
}

```

### Attribute

|Name|Type|Required|Restrictions|Title|Description|
|---|---|---|---|---|---|
|fechaCreado|string|false|none||none|
|creadoPor|string|false|none||none|
|fechaModificado|string|false|none||none|
|modificadoPor|string|false|none||none|
|id|string(uuid)|false|none||id del vehiculo|
|placa|string|false|none||placa del vehiculo|
|tipo|[TipoVehiculo](#schematipovehiculo)|false|none||tipo de vehiculo|
|hikcentralVehicleId|string|false|none||id del vehiculo en hikcentral|

<h2 id="tocS_ReservaCasilla">ReservaCasilla</h2>

<a id="schemareservacasilla"></a>
<a id="schema_ReservaCasilla"></a>
<a id="tocSreservacasilla"></a>
<a id="tocsreservacasilla"></a>

```json
{
  "fechaCreado": "26-04-2024 12:37:36",
  "creadoPor": "string",
  "fechaModificado": "26-04-2024 12:37:36",
  "modificadoPor": "string",
  "id": "e3617a05-6e65-433f-b0db-c2a8747f3314",
  "casilla": {
    "fechaCreado": "26-04-2024 12:37:36",
    "creadoPor": "string",
    "fechaModificado": "26-04-2024 12:37:36",
    "modificadoPor": "string",
    "id": 1,
    "hid": "1527-1",
    "nombre": "226",
    "casillero": {
      "fechaCreado": "26-04-2024 12:37:36",
      "creadoPor": "string",
      "fechaModificado": "26-04-2024 12:37:36",
      "modificadoPor": "string",
      "id": 1,
      "hid": "wkt1310",
      "nombre": "Casillero 1",
      "hikcentralPrivilegeGroupId": "1",
      "ubicacion": {
        "fechaCreado": "26-04-2024 12:37:36",
        "creadoPor": "string",
        "fechaModificado": "26-04-2024 12:37:36",
        "modificadoPor": "string",
        "id": 1,
        "nombre": "Ubicacion A"
      },
      "prioridad": 1
    },
    "tipo": {
      "fechaCreado": "26-04-2024 12:37:36",
      "creadoPor": "string",
      "fechaModificado": "26-04-2024 12:37:36",
      "modificadoPor": "string",
      "id": 1,
      "producto": {
        "fechaCreado": "26-04-2024 12:37:36",
        "creadoPor": "string",
        "fechaModificado": "26-04-2024 12:37:36",
        "modificadoPor": "string",
        "id": "6c872a0f-4e21-460a-ae3d-2f3994f73dc6",
        "codigo": "string",
        "nombre": "Producto A",
        "descripcion": "Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua",
        "valorVariable": true,
        "valor": 30000,
        "imagenId": "644176ac-41f6-48ac-a4ef-3db5eb09fbf9",
        "tipo": "BOLETA",
        "productosCombo": [
          {}
        ],
        "ventaFechaInicio": "26-04-2024",
        "ventaFechaFin": "26-04-2024",
        "consumoFechaInicio": "26-04-2024",
        "consumoFechaFin": "26-04-2024",
        "excepcionesDiasSemana": [
          {}
        ],
        "activacionDesactivacionAutomatica": true
      },
      "estado": "ACTIVO"
    },
    "clave": "F457U"
  },
  "visitanteId": "71b09bc0-f6f6-4f86-b937-6c6689187632",
  "codigo": "6A5SD",
  "fechaPrimeraApertura": "26-04-2024 12:37:36",
  "estadoPago": "APROBADO"
}

```

reserva de casilla asociada al visitante

### Attribute

|Name|Type|Required|Restrictions|Title|Description|
|---|---|---|---|---|---|
|fechaCreado|string|false|none||none|
|creadoPor|string|false|none||none|
|fechaModificado|string|false|none||none|
|modificadoPor|string|false|none||none|
|id|string(uuid)|false|none||id de la reserva de casilla|
|casilla|[Casilla](#schemacasilla)|false|none||casilla de la reserva|
|visitanteId|string(uuid)|false|none||id del visitante que tiene asginada esta reserva de casilla|
|codigo|string|false|none||codigo para apertura sin visitante|
|fechaPrimeraApertura|string|false|none||fecha de la primera apertura de la casilla|
|estadoPago|string|false|none||estado del pago de la reserva de casilla|

#### Enum

|Name|Value|
|---|---|
|estadoPago|APROBADO|
|estadoPago|PENDIENTE|
|estadoPago|ANULADO|

<h2 id="tocS_Casilla">Casilla</h2>

<a id="schemacasilla"></a>
<a id="schema_Casilla"></a>
<a id="tocScasilla"></a>
<a id="tocscasilla"></a>

```json
{
  "fechaCreado": "26-04-2024 12:37:36",
  "creadoPor": "string",
  "fechaModificado": "26-04-2024 12:37:36",
  "modificadoPor": "string",
  "id": 1,
  "hid": "1527-1",
  "nombre": "226",
  "casillero": {
    "fechaCreado": "26-04-2024 12:37:36",
    "creadoPor": "string",
    "fechaModificado": "26-04-2024 12:37:36",
    "modificadoPor": "string",
    "id": 1,
    "hid": "wkt1310",
    "nombre": "Casillero 1",
    "hikcentralPrivilegeGroupId": "1",
    "ubicacion": {
      "fechaCreado": "26-04-2024 12:37:36",
      "creadoPor": "string",
      "fechaModificado": "26-04-2024 12:37:36",
      "modificadoPor": "string",
      "id": 1,
      "nombre": "Ubicacion A"
    },
    "prioridad": 1
  },
  "tipo": {
    "fechaCreado": "26-04-2024 12:37:36",
    "creadoPor": "string",
    "fechaModificado": "26-04-2024 12:37:36",
    "modificadoPor": "string",
    "id": 1,
    "producto": {
      "fechaCreado": "26-04-2024 12:37:36",
      "creadoPor": "string",
      "fechaModificado": "26-04-2024 12:37:36",
      "modificadoPor": "string",
      "id": "6c872a0f-4e21-460a-ae3d-2f3994f73dc6",
      "codigo": "string",
      "nombre": "Producto A",
      "descripcion": "Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua",
      "valorVariable": true,
      "valor": 30000,
      "imagenId": "644176ac-41f6-48ac-a4ef-3db5eb09fbf9",
      "tipo": "BOLETA",
      "productosCombo": [
        {
          "fechaCreado": "[",
          "creadoPor": "string",
          "fechaModificado": "[",
          "modificadoPor": "string",
          "producto": {},
          "cantidad": 0
        }
      ],
      "ventaFechaInicio": "26-04-2024",
      "ventaFechaFin": "26-04-2024",
      "consumoFechaInicio": "26-04-2024",
      "consumoFechaFin": "26-04-2024",
      "excepcionesDiasSemana": [
        {
          "id": 0,
          "tipo": "[",
          "lunes": true,
          "martes": true,
          "miercoles": true,
          "jueves": true,
          "viernes": true,
          "sabado": true,
          "domingo": true
        }
      ],
      "activacionDesactivacionAutomatica": true
    },
    "estado": "ACTIVO"
  },
  "clave": "F457U"
}

```

casilla de la reserva

### Attribute

|Name|Type|Required|Restrictions|Title|Description|
|---|---|---|---|---|---|
|fechaCreado|string|false|none||none|
|creadoPor|string|false|none||none|
|fechaModificado|string|false|none||none|
|modificadoPor|string|false|none||none|
|id|integer(int64)|false|none||id de la casilla|
|hid|string|false|none||id de hardware la casilla|
|nombre|string|false|none||nombre de la casilla|
|casillero|[Casillero](#schemacasillero)|false|none||casillero de la casilla en el cual se encuentra la casilla|
|tipo|[TipoCasilla](#schematipocasilla)|false|none||tipo de casilla|
|clave|string|false|none||clave de la casilla|

<h2 id="tocS_TipoCasilla">TipoCasilla</h2>

<a id="schematipocasilla"></a>
<a id="schema_TipoCasilla"></a>
<a id="tocStipocasilla"></a>
<a id="tocstipocasilla"></a>

```json
{
  "fechaCreado": "26-04-2024 12:37:36",
  "creadoPor": "string",
  "fechaModificado": "26-04-2024 12:37:36",
  "modificadoPor": "string",
  "id": 1,
  "producto": {
    "fechaCreado": "26-04-2024 12:37:36",
    "creadoPor": "string",
    "fechaModificado": "26-04-2024 12:37:36",
    "modificadoPor": "string",
    "id": "6c872a0f-4e21-460a-ae3d-2f3994f73dc6",
    "codigo": "string",
    "nombre": "Producto A",
    "descripcion": "Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua",
    "valorVariable": true,
    "valor": 30000,
    "imagenId": "644176ac-41f6-48ac-a4ef-3db5eb09fbf9",
    "tipo": "BOLETA",
    "productosCombo": [
      {
        "fechaCreado": "26-04-2024 12:37:36",
        "creadoPor": "string",
        "fechaModificado": "26-04-2024 12:37:36",
        "modificadoPor": "string",
        "producto": {
          "fechaCreado": "[",
          "creadoPor": "string",
          "fechaModificado": "[",
          "modificadoPor": "string",
          "id": "[",
          "codigo": "string",
          "nombre": "[",
          "descripcion": "[",
          "valorVariable": true,
          "valor": "[",
          "imagenId": "[",
          "tipo": "[",
          "productosCombo": [
            null
          ],
          "ventaFechaInicio": "[",
          "ventaFechaFin": "[",
          "consumoFechaInicio": "[",
          "consumoFechaFin": "[",
          "excepcionesDiasSemana": [
            null
          ],
          "activacionDesactivacionAutomatica": true
        },
        "cantidad": 0
      }
    ],
    "ventaFechaInicio": "26-04-2024",
    "ventaFechaFin": "26-04-2024",
    "consumoFechaInicio": "26-04-2024",
    "consumoFechaFin": "26-04-2024",
    "excepcionesDiasSemana": [
      {
        "id": 0,
        "tipo": "VENTA",
        "lunes": true,
        "martes": true,
        "miercoles": true,
        "jueves": true,
        "viernes": true,
        "sabado": true,
        "domingo": true
      }
    ],
    "activacionDesactivacionAutomatica": true
  },
  "estado": "ACTIVO"
}

```

tipo de casilla

### Attribute

|Name|Type|Required|Restrictions|Title|Description|
|---|---|---|---|---|---|
|fechaCreado|string|false|none||none|
|creadoPor|string|false|none||none|
|fechaModificado|string|false|none||none|
|modificadoPor|string|false|none||none|
|id|integer(int64)|false|none||id del tipo de casilla|
|producto|[Producto](#schemaproducto)|false|none||detalle del producto|
|estado|string|false|none||estado del tipo de casilla|

#### Enum

|Name|Value|
|---|---|
|estado|ACTIVO|
|estado|INACTIVO|

<h2 id="tocS_Casillero">Casillero</h2>

<a id="schemacasillero"></a>
<a id="schema_Casillero"></a>
<a id="tocScasillero"></a>
<a id="tocscasillero"></a>

```json
{
  "fechaCreado": "26-04-2024 12:37:36",
  "creadoPor": "string",
  "fechaModificado": "26-04-2024 12:37:36",
  "modificadoPor": "string",
  "id": 1,
  "hid": "wkt1310",
  "nombre": "Casillero 1",
  "hikcentralPrivilegeGroupId": "1",
  "ubicacion": {
    "fechaCreado": "26-04-2024 12:37:36",
    "creadoPor": "string",
    "fechaModificado": "26-04-2024 12:37:36",
    "modificadoPor": "string",
    "id": 1,
    "nombre": "Ubicacion A"
  },
  "prioridad": 1
}

```

casillero de la casilla en el cual se encuentra la casilla

### Attribute

|Name|Type|Required|Restrictions|Title|Description|
|---|---|---|---|---|---|
|fechaCreado|string|false|none||none|
|creadoPor|string|false|none||none|
|fechaModificado|string|false|none||none|
|modificadoPor|string|false|none||none|
|id|integer(int64)|false|none||id del casillero|
|hid|string|false|none||id de hardware del casillero|
|nombre|string|false|none||nombre del casillero|
|hikcentralPrivilegeGroupId|string|false|none||id del grupo de privilegios de hikcentral|
|ubicacion|[UbicacionCasillero](#schemaubicacioncasillero)|false|none||ubicacion del casillero|
|prioridad|integer(int32)|false|none||prioridad del casillero|

<h2 id="tocS_UbicacionCasillero">UbicacionCasillero</h2>

<a id="schemaubicacioncasillero"></a>
<a id="schema_UbicacionCasillero"></a>
<a id="tocSubicacioncasillero"></a>
<a id="tocsubicacioncasillero"></a>

```json
{
  "fechaCreado": "26-04-2024 12:37:36",
  "creadoPor": "string",
  "fechaModificado": "26-04-2024 12:37:36",
  "modificadoPor": "string",
  "id": 1,
  "nombre": "Ubicacion A"
}

```

ubicacion del casillero

### Attribute

|Name|Type|Required|Restrictions|Title|Description|
|---|---|---|---|---|---|
|fechaCreado|string|false|none||none|
|creadoPor|string|false|none||none|
|fechaModificado|string|false|none||none|
|modificadoPor|string|false|none||none|
|id|integer(int64)|false|none||id de la ubicacion|
|nombre|string|false|none||nombre de la ubicacion|

<h2 id="tocS_ReservaServicioAdicional">ReservaServicioAdicional</h2>

<a id="schemareservaservicioadicional"></a>
<a id="schema_ReservaServicioAdicional"></a>
<a id="tocSreservaservicioadicional"></a>
<a id="tocsreservaservicioadicional"></a>

```json
{
  "fechaCreado": "26-04-2024 12:37:36",
  "creadoPor": "string",
  "fechaModificado": "26-04-2024 12:37:36",
  "modificadoPor": "string",
  "id": "497f6eca-6276-4993-bfeb-53cbbbba6f08",
  "servicioAdicional": {
    "fechaCreado": "26-04-2024 12:37:36",
    "creadoPor": "string",
    "fechaModificado": "26-04-2024 12:37:36",
    "modificadoPor": "string",
    "id": 1,
    "producto": {
      "fechaCreado": "26-04-2024 12:37:36",
      "creadoPor": "string",
      "fechaModificado": "26-04-2024 12:37:36",
      "modificadoPor": "string",
      "id": "6c872a0f-4e21-460a-ae3d-2f3994f73dc6",
      "codigo": "string",
      "nombre": "Producto A",
      "descripcion": "Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua",
      "valorVariable": true,
      "valor": 30000,
      "imagenId": "644176ac-41f6-48ac-a4ef-3db5eb09fbf9",
      "tipo": "BOLETA",
      "productosCombo": [
        {
          "fechaCreado": "[",
          "creadoPor": "string",
          "fechaModificado": "[",
          "modificadoPor": "string",
          "producto": {},
          "cantidad": 0
        }
      ],
      "ventaFechaInicio": "26-04-2024",
      "ventaFechaFin": "26-04-2024",
      "consumoFechaInicio": "26-04-2024",
      "consumoFechaFin": "26-04-2024",
      "excepcionesDiasSemana": [
        {
          "id": 0,
          "tipo": "[",
          "lunes": true,
          "martes": true,
          "miercoles": true,
          "jueves": true,
          "viernes": true,
          "sabado": true,
          "domingo": true
        }
      ],
      "activacionDesactivacionAutomatica": true
    },
    "categoriaServicio": {
      "fechaCreado": "26-04-2024 12:37:36",
      "creadoPor": "string",
      "fechaModificado": "26-04-2024 12:37:36",
      "modificadoPor": "string",
      "id": 1,
      "nombre": "Servicios A"
    }
  },
  "visitanteId": "8c06e1d1-3f95-45bd-b423-7fe0ab137edf",
  "consumido": false,
  "estadoPago": "APROBADO"
}

```

servicios adicionales asociados con esta reserva

### Attribute

|Name|Type|Required|Restrictions|Title|Description|
|---|---|---|---|---|---|
|fechaCreado|string|false|none||none|
|creadoPor|string|false|none||none|
|fechaModificado|string|false|none||none|
|modificadoPor|string|false|none||none|
|id|string(uuid)|false|none||id de la reserva de servicio adicional|
|servicioAdicional|[ServicioAdicional](#schemaservicioadicional)|false|none||none|
|visitanteId|string(uuid)|false|none||none|
|consumido|boolean|false|none||el servicio adicional ya ha sido consumido (si/no)|
|estadoPago|string|false|none||none|

#### Enum

|Name|Value|
|---|---|
|estadoPago|APROBADO|
|estadoPago|PENDIENTE|
|estadoPago|ANULADO|

<h2 id="tocS_ServicioAdicional">ServicioAdicional</h2>

<a id="schemaservicioadicional"></a>
<a id="schema_ServicioAdicional"></a>
<a id="tocSservicioadicional"></a>
<a id="tocsservicioadicional"></a>

```json
{
  "fechaCreado": "26-04-2024 12:37:36",
  "creadoPor": "string",
  "fechaModificado": "26-04-2024 12:37:36",
  "modificadoPor": "string",
  "id": 1,
  "producto": {
    "fechaCreado": "26-04-2024 12:37:36",
    "creadoPor": "string",
    "fechaModificado": "26-04-2024 12:37:36",
    "modificadoPor": "string",
    "id": "6c872a0f-4e21-460a-ae3d-2f3994f73dc6",
    "codigo": "string",
    "nombre": "Producto A",
    "descripcion": "Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua",
    "valorVariable": true,
    "valor": 30000,
    "imagenId": "644176ac-41f6-48ac-a4ef-3db5eb09fbf9",
    "tipo": "BOLETA",
    "productosCombo": [
      {
        "fechaCreado": "26-04-2024 12:37:36",
        "creadoPor": "string",
        "fechaModificado": "26-04-2024 12:37:36",
        "modificadoPor": "string",
        "producto": {
          "fechaCreado": "[",
          "creadoPor": "string",
          "fechaModificado": "[",
          "modificadoPor": "string",
          "id": "[",
          "codigo": "string",
          "nombre": "[",
          "descripcion": "[",
          "valorVariable": true,
          "valor": "[",
          "imagenId": "[",
          "tipo": "[",
          "productosCombo": [
            null
          ],
          "ventaFechaInicio": "[",
          "ventaFechaFin": "[",
          "consumoFechaInicio": "[",
          "consumoFechaFin": "[",
          "excepcionesDiasSemana": [
            null
          ],
          "activacionDesactivacionAutomatica": true
        },
        "cantidad": 0
      }
    ],
    "ventaFechaInicio": "26-04-2024",
    "ventaFechaFin": "26-04-2024",
    "consumoFechaInicio": "26-04-2024",
    "consumoFechaFin": "26-04-2024",
    "excepcionesDiasSemana": [
      {
        "id": 0,
        "tipo": "VENTA",
        "lunes": true,
        "martes": true,
        "miercoles": true,
        "jueves": true,
        "viernes": true,
        "sabado": true,
        "domingo": true
      }
    ],
    "activacionDesactivacionAutomatica": true
  },
  "categoriaServicio": {
    "fechaCreado": "26-04-2024 12:37:36",
    "creadoPor": "string",
    "fechaModificado": "26-04-2024 12:37:36",
    "modificadoPor": "string",
    "id": 1,
    "nombre": "Servicios A"
  }
}

```

### Attribute

|Name|Type|Required|Restrictions|Title|Description|
|---|---|---|---|---|---|
|fechaCreado|string|false|none||none|
|creadoPor|string|false|none||none|
|fechaModificado|string|false|none||none|
|modificadoPor|string|false|none||none|
|id|integer(int64)|false|none||id del servicio adicional|
|producto|[Producto](#schemaproducto)|false|none||detalle del producto|
|categoriaServicio|[CategoriaServicio](#schemacategoriaservicio)|false|none||none|

<h2 id="tocS_CategoriaServicio">CategoriaServicio</h2>

<a id="schemacategoriaservicio"></a>
<a id="schema_CategoriaServicio"></a>
<a id="tocScategoriaservicio"></a>
<a id="tocscategoriaservicio"></a>

```json
{
  "fechaCreado": "26-04-2024 12:37:36",
  "creadoPor": "string",
  "fechaModificado": "26-04-2024 12:37:36",
  "modificadoPor": "string",
  "id": 1,
  "nombre": "Servicios A"
}

```

### Attribute

|Name|Type|Required|Restrictions|Title|Description|
|---|---|---|---|---|---|
|fechaCreado|string|false|none||none|
|creadoPor|string|false|none||none|
|fechaModificado|string|false|none||none|
|modificadoPor|string|false|none||none|
|id|integer(int64)|false|none||id de la categoria de servicios adicionales|
|nombre|string|false|none||nombre de la categoria de servicios adicionales|

<h2 id="tocS_Canal">Canal</h2>

<a id="schemacanal"></a>
<a id="schema_Canal"></a>
<a id="tocScanal"></a>
<a id="tocscanal"></a>

```json
{
  "fechaCreado": "26-04-2024 12:37:36",
  "creadoPor": "string",
  "fechaModificado": "26-04-2024 12:37:36",
  "modificadoPor": "string",
  "id": 1,
  "nombre": "Canal A"
}

```

canal asociado con esta reserva

### Attribute

|Name|Type|Required|Restrictions|Title|Description|
|---|---|---|---|---|---|
|fechaCreado|string|false|none||none|
|creadoPor|string|false|none||none|
|fechaModificado|string|false|none||none|
|modificadoPor|string|false|none||none|
|id|integer(int64)|false|none||id del canal|
|nombre|string|false|none||nombre del canal|

<h2 id="tocS_Cliente">Cliente</h2>

<a id="schemacliente"></a>
<a id="schema_Cliente"></a>
<a id="tocScliente"></a>
<a id="tocscliente"></a>

```json
{
  "fechaCreado": "26-04-2024 12:37:36",
  "creadoPor": "string",
  "fechaModificado": "26-04-2024 12:37:36",
  "modificadoPor": "string",
  "identificacion": {
    "tipo": "CC",
    "numero": "1111111111"
  },
  "primerNombre": "Nombre 1",
  "segundoNombre": "Nombre 2",
  "primerApellido": "Apellido 1",
  "segundoApellido": "Apellido 2",
  "nombreCompleto": "Nombre 1 Nombre 2 Apellido 1 Apellido 2",
  "email": "example@email.com",
  "telefono": "3005557777",
  "genero": "M",
  "fechaNacimiento": "26-04-2024",
  "ciudad": "11001.11.Co",
  "direccion": "Calle 1 # 1 - 1"
}

```

cliente asociado con esta reserva

### Attribute

|Name|Type|Required|Restrictions|Title|Description|
|---|---|---|---|---|---|
|fechaCreado|string|false|none||none|
|creadoPor|string|false|none||none|
|fechaModificado|string|false|none||none|
|modificadoPor|string|false|none||none|
|identificacion|[Identificacion](#schemaidentificacion)|false|none||identificacion del cliente|
|primerNombre|string|false|none||primer nombre del cliente|
|segundoNombre|string|false|none||segundo nombre del cliente|
|primerApellido|string|false|none||primer apellido del cliente|
|segundoApellido|string|false|none||segundo apellido del cliente|
|nombreCompleto|string|false|none||nombre completo del cliente|
|email|string|false|none||direccion de correo electronico del cliente|
|telefono|string|false|none||telefono del cliente|
|genero|string|false|none||genero del cliente|
|fechaNacimiento|string|false|none||fecha de nacimiento del cliente|
|ciudad|[Ciudad](#schemaciudad)|false|none||ciudad del cliente|
|direccion|string|false|none||direccion del cliente|

#### Enum

|Name|Value|
|---|---|
|genero|M|
|genero|F|
|genero|O|

<h2 id="tocS_Ciudad">Ciudad</h2>

<a id="schemaciudad"></a>
<a id="schema_Ciudad"></a>
<a id="tocSciudad"></a>
<a id="tocsciudad"></a>

```json
"11001.11.Co"

```

ciudad del cliente

### Attribute

|Name|Type|Required|Restrictions|Title|Description|
|---|---|---|---|---|---|
|id|string|false|none||none|
|codigo|string|false|none||none|
|nombre|string|false|none||none|
|estado|[Estado](#schemaestado)|false|none||none|

<h2 id="tocS_Estado">Estado</h2>

<a id="schemaestado"></a>
<a id="schema_Estado"></a>
<a id="tocSestado"></a>
<a id="tocsestado"></a>

```json
{
  "id": "string",
  "codigo": "string",
  "nombre": "string",
  "pais": {
    "id": "string",
    "codigo": "string",
    "nombre": "string"
  }
}

```

### Attribute

|Name|Type|Required|Restrictions|Title|Description|
|---|---|---|---|---|---|
|id|string|false|none||none|
|codigo|string|false|none||none|
|nombre|string|false|none||none|
|pais|[Pais](#schemapais)|false|none||none|

<h2 id="tocS_Pais">Pais</h2>

<a id="schemapais"></a>
<a id="schema_Pais"></a>
<a id="tocSpais"></a>
<a id="tocspais"></a>

```json
{
  "id": "string",
  "codigo": "string",
  "nombre": "string"
}

```

### Attribute

|Name|Type|Required|Restrictions|Title|Description|
|---|---|---|---|---|---|
|id|string|false|none||none|
|codigo|string|false|none||none|
|nombre|string|false|none||none|

<h2 id="tocS_Identificacion">Identificacion</h2>

<a id="schemaidentificacion"></a>
<a id="schema_Identificacion"></a>
<a id="tocSidentificacion"></a>
<a id="tocsidentificacion"></a>

```json
{
  "tipo": "CC",
  "numero": "1111111111"
}

```

identificacion del cliente

### Attribute

|Name|Type|Required|Restrictions|Title|Description|
|---|---|---|---|---|---|
|tipo|string|false|none||tipo de identificacion|
|numero|string|false|none||numero de identificacion|

#### Enum

|Name|Value|
|---|---|
|tipo|CC|
|tipo|NIT|
|tipo|CE|
|tipo|PAS|
|tipo|TI|
|tipo|RC|
|tipo|DNI|

<h2 id="tocS_PageTipoBoleta">PageTipoBoleta</h2>

<a id="schemapagetipoboleta"></a>
<a id="schema_PageTipoBoleta"></a>
<a id="tocSpagetipoboleta"></a>
<a id="tocspagetipoboleta"></a>

```json
{
  "totalPages": 0,
  "totalElements": 0,
  "size": 0,
  "content": [
    {
      "fechaCreado": "26-04-2024 12:37:36",
      "creadoPor": "string",
      "fechaModificado": "26-04-2024 12:37:36",
      "modificadoPor": "string",
      "id": 1,
      "producto": {
        "fechaCreado": "26-04-2024 12:37:36",
        "creadoPor": "string",
        "fechaModificado": "26-04-2024 12:37:36",
        "modificadoPor": "string",
        "id": "6c872a0f-4e21-460a-ae3d-2f3994f73dc6",
        "codigo": "string",
        "nombre": "Producto A",
        "descripcion": "Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua",
        "valorVariable": true,
        "valor": 30000,
        "imagenId": "644176ac-41f6-48ac-a4ef-3db5eb09fbf9",
        "tipo": "BOLETA",
        "productosCombo": [
          {
            "fechaCreado": null,
            "creadoPor": null,
            "fechaModificado": null,
            "modificadoPor": null,
            "producto": null,
            "cantidad": null
          }
        ],
        "ventaFechaInicio": "26-04-2024",
        "ventaFechaFin": "26-04-2024",
        "consumoFechaInicio": "26-04-2024",
        "consumoFechaFin": "26-04-2024",
        "excepcionesDiasSemana": [
          {
            "id": null,
            "tipo": null,
            "lunes": null,
            "martes": null,
            "miercoles": null,
            "jueves": null,
            "viernes": null,
            "sabado": null,
            "domingo": null
          }
        ],
        "activacionDesactivacionAutomatica": true
      },
      "categoriaEdad": {
        "fechaCreado": "26-04-2024 12:37:36",
        "creadoPor": "string",
        "fechaModificado": "26-04-2024 12:37:36",
        "modificadoPor": "string",
        "id": 1,
        "nombre": "Categoria de edad A",
        "edadInicial": 8,
        "edadFinal": 60
      },
      "categoriaEstatura": {
        "fechaCreado": "26-04-2024 12:37:36",
        "creadoPor": "string",
        "fechaModificado": "26-04-2024 12:37:36",
        "modificadoPor": "string",
        "id": 1,
        "nombre": "Categoria de estatura A",
        "estaturaCmMin": 120,
        "estaturaCmMax": 180
      },
      "hikcentralPrivilegeGroupId": "1"
    }
  ],
  "number": 0,
  "sort": {
    "empty": true,
    "sorted": true,
    "unsorted": true
  },
  "first": true,
  "pageable": {
    "offset": 0,
    "sort": {
      "empty": true,
      "sorted": true,
      "unsorted": true
    },
    "pageNumber": 0,
    "pageSize": 0,
    "unpaged": true,
    "paged": true
  },
  "numberOfElements": 0,
  "last": true,
  "empty": true
}

```

### Attribute

|Name|Type|Required|Restrictions|Title|Description|
|---|---|---|---|---|---|
|totalPages|integer(int32)|false|none||none|
|totalElements|integer(int64)|false|none||none|
|size|integer(int32)|false|none||none|
|content|[[TipoBoleta](#schematipoboleta)]|false|none||[tipo de boleta]|
|number|integer(int32)|false|none||none|
|sort|[SortObject](#schemasortobject)|false|none||none|
|first|boolean|false|none||none|
|pageable|[PageableObject](#schemapageableobject)|false|none||none|
|numberOfElements|integer(int32)|false|none||none|
|last|boolean|false|none||none|
|empty|boolean|false|none||none|

<h2 id="tocS_TipoBoleta">TipoBoleta</h2>

<a id="schematipoboleta"></a>
<a id="schema_TipoBoleta"></a>
<a id="tocStipoboleta"></a>
<a id="tocstipoboleta"></a>

```json
{
  "fechaCreado": "26-04-2024 12:37:36",
  "creadoPor": "string",
  "fechaModificado": "26-04-2024 12:37:36",
  "modificadoPor": "string",
  "id": 1,
  "producto": {
    "fechaCreado": "26-04-2024 12:37:36",
    "creadoPor": "string",
    "fechaModificado": "26-04-2024 12:37:36",
    "modificadoPor": "string",
    "id": "6c872a0f-4e21-460a-ae3d-2f3994f73dc6",
    "codigo": "string",
    "nombre": "Producto A",
    "descripcion": "Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua",
    "valorVariable": true,
    "valor": 30000,
    "imagenId": "644176ac-41f6-48ac-a4ef-3db5eb09fbf9",
    "tipo": "BOLETA",
    "productosCombo": [
      {
        "fechaCreado": "26-04-2024 12:37:36",
        "creadoPor": "string",
        "fechaModificado": "26-04-2024 12:37:36",
        "modificadoPor": "string",
        "producto": {
          "fechaCreado": "[",
          "creadoPor": "string",
          "fechaModificado": "[",
          "modificadoPor": "string",
          "id": "[",
          "codigo": "string",
          "nombre": "[",
          "descripcion": "[",
          "valorVariable": true,
          "valor": "[",
          "imagenId": "[",
          "tipo": "[",
          "productosCombo": [
            null
          ],
          "ventaFechaInicio": "[",
          "ventaFechaFin": "[",
          "consumoFechaInicio": "[",
          "consumoFechaFin": "[",
          "excepcionesDiasSemana": [
            null
          ],
          "activacionDesactivacionAutomatica": true
        },
        "cantidad": 0
      }
    ],
    "ventaFechaInicio": "26-04-2024",
    "ventaFechaFin": "26-04-2024",
    "consumoFechaInicio": "26-04-2024",
    "consumoFechaFin": "26-04-2024",
    "excepcionesDiasSemana": [
      {
        "id": 0,
        "tipo": "VENTA",
        "lunes": true,
        "martes": true,
        "miercoles": true,
        "jueves": true,
        "viernes": true,
        "sabado": true,
        "domingo": true
      }
    ],
    "activacionDesactivacionAutomatica": true
  },
  "categoriaEdad": {
    "fechaCreado": "26-04-2024 12:37:36",
    "creadoPor": "string",
    "fechaModificado": "26-04-2024 12:37:36",
    "modificadoPor": "string",
    "id": 1,
    "nombre": "Categoria de edad A",
    "edadInicial": 8,
    "edadFinal": 60
  },
  "categoriaEstatura": {
    "fechaCreado": "26-04-2024 12:37:36",
    "creadoPor": "string",
    "fechaModificado": "26-04-2024 12:37:36",
    "modificadoPor": "string",
    "id": 1,
    "nombre": "Categoria de estatura A",
    "estaturaCmMin": 120,
    "estaturaCmMax": 180
  },
  "hikcentralPrivilegeGroupId": "1"
}

```

tipo de boleta

### Attribute

|Name|Type|Required|Restrictions|Title|Description|
|---|---|---|---|---|---|
|fechaCreado|string|false|none||none|
|creadoPor|string|false|none||none|
|fechaModificado|string|false|none||none|
|modificadoPor|string|false|none||none|
|id|integer(int64)|false|none||id del tipo de boleta|
|producto|[Producto](#schemaproducto)|false|none||detalle del producto|
|categoriaEdad|[CategoriaEdad](#schemacategoriaedad)|false|none||categoria de edad|
|categoriaEstatura|[CategoriaEstatura](#schemacategoriaestatura)|false|none||categoria de estatura|
|hikcentralPrivilegeGroupId|string|false|none||id del grupo de privilegios de hikcentral|

<h2 id="tocS_CategoriaEstatura">CategoriaEstatura</h2>

<a id="schemacategoriaestatura"></a>
<a id="schema_CategoriaEstatura"></a>
<a id="tocScategoriaestatura"></a>
<a id="tocscategoriaestatura"></a>

```json
{
  "fechaCreado": "26-04-2024 12:37:36",
  "creadoPor": "string",
  "fechaModificado": "26-04-2024 12:37:36",
  "modificadoPor": "string",
  "id": 1,
  "nombre": "Categoria de estatura A",
  "estaturaCmMin": 120,
  "estaturaCmMax": 180
}

```

categoria de estatura

### Attribute

|Name|Type|Required|Restrictions|Title|Description|
|---|---|---|---|---|---|
|fechaCreado|string|false|none||none|
|creadoPor|string|false|none||none|
|fechaModificado|string|false|none||none|
|modificadoPor|string|false|none||none|
|id|integer(int64)|false|none||id de la categoria de estatura|
|nombre|string|false|none||nombre de la categoria de estatura|
|estaturaCmMin|integer(int32)|false|none||estatura minima de la categoria en centimetros|
|estaturaCmMax|integer(int32)|false|none||estatura maxima de la categoria en centimetros|

<h2 id="tocS_CategoriaEdad">CategoriaEdad</h2>

<a id="schemacategoriaedad"></a>
<a id="schema_CategoriaEdad"></a>
<a id="tocScategoriaedad"></a>
<a id="tocscategoriaedad"></a>

```json
{
  "fechaCreado": "26-04-2024 12:37:36",
  "creadoPor": "string",
  "fechaModificado": "26-04-2024 12:37:36",
  "modificadoPor": "string",
  "id": 1,
  "nombre": "Categoria de edad A",
  "edadInicial": 8,
  "edadFinal": 60
}

```

categoria de edad

### Attribute

|Name|Type|Required|Restrictions|Title|Description|
|---|---|---|---|---|---|
|fechaCreado|string|false|none||none|
|creadoPor|string|false|none||none|
|fechaModificado|string|false|none||none|
|modificadoPor|string|false|none||none|
|id|integer(int64)|false|none||id de la categoria de edad|
|nombre|string|false|none||nombre de la categoria de edad|
|edadInicial|integer(int32)|false|none||edad inicial de la categoria de edad|
|edadFinal|integer(int32)|false|none||edad final de la categoria de edad|

<h2 id="tocS_PageTipoCasilla">PageTipoCasilla</h2>

<a id="schemapagetipocasilla"></a>
<a id="schema_PageTipoCasilla"></a>
<a id="tocSpagetipocasilla"></a>
<a id="tocspagetipocasilla"></a>

```json
{
  "totalPages": 0,
  "totalElements": 0,
  "size": 0,
  "content": [
    {
      "fechaCreado": "26-04-2024 12:37:36",
      "creadoPor": "string",
      "fechaModificado": "26-04-2024 12:37:36",
      "modificadoPor": "string",
      "id": 1,
      "producto": {
        "fechaCreado": "26-04-2024 12:37:36",
        "creadoPor": "string",
        "fechaModificado": "26-04-2024 12:37:36",
        "modificadoPor": "string",
        "id": "6c872a0f-4e21-460a-ae3d-2f3994f73dc6",
        "codigo": "string",
        "nombre": "Producto A",
        "descripcion": "Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua",
        "valorVariable": true,
        "valor": 30000,
        "imagenId": "644176ac-41f6-48ac-a4ef-3db5eb09fbf9",
        "tipo": "BOLETA",
        "productosCombo": [
          {
            "fechaCreado": null,
            "creadoPor": null,
            "fechaModificado": null,
            "modificadoPor": null,
            "producto": null,
            "cantidad": null
          }
        ],
        "ventaFechaInicio": "26-04-2024",
        "ventaFechaFin": "26-04-2024",
        "consumoFechaInicio": "26-04-2024",
        "consumoFechaFin": "26-04-2024",
        "excepcionesDiasSemana": [
          {
            "id": null,
            "tipo": null,
            "lunes": null,
            "martes": null,
            "miercoles": null,
            "jueves": null,
            "viernes": null,
            "sabado": null,
            "domingo": null
          }
        ],
        "activacionDesactivacionAutomatica": true
      },
      "estado": "ACTIVO"
    }
  ],
  "number": 0,
  "sort": {
    "empty": true,
    "sorted": true,
    "unsorted": true
  },
  "first": true,
  "pageable": {
    "offset": 0,
    "sort": {
      "empty": true,
      "sorted": true,
      "unsorted": true
    },
    "pageNumber": 0,
    "pageSize": 0,
    "unpaged": true,
    "paged": true
  },
  "numberOfElements": 0,
  "last": true,
  "empty": true
}

```

### Attribute

|Name|Type|Required|Restrictions|Title|Description|
|---|---|---|---|---|---|
|totalPages|integer(int32)|false|none||none|
|totalElements|integer(int64)|false|none||none|
|size|integer(int32)|false|none||none|
|content|[[TipoCasilla](#schematipocasilla)]|false|none||[tipo de casilla]|
|number|integer(int32)|false|none||none|
|sort|[SortObject](#schemasortobject)|false|none||none|
|first|boolean|false|none||none|
|pageable|[PageableObject](#schemapageableobject)|false|none||none|
|numberOfElements|integer(int32)|false|none||none|
|last|boolean|false|none||none|
|empty|boolean|false|none||none|

<h2 id="tocS_PageTipoServicioParqueadero">PageTipoServicioParqueadero</h2>

<a id="schemapagetiposervicioparqueadero"></a>
<a id="schema_PageTipoServicioParqueadero"></a>
<a id="tocSpagetiposervicioparqueadero"></a>
<a id="tocspagetiposervicioparqueadero"></a>

```json
{
  "totalPages": 0,
  "totalElements": 0,
  "size": 0,
  "content": [
    {
      "fechaCreado": "26-04-2024 12:37:36",
      "creadoPor": "string",
      "fechaModificado": "26-04-2024 12:37:36",
      "modificadoPor": "string",
      "id": 1,
      "producto": {
        "fechaCreado": "26-04-2024 12:37:36",
        "creadoPor": "string",
        "fechaModificado": "26-04-2024 12:37:36",
        "modificadoPor": "string",
        "id": "6c872a0f-4e21-460a-ae3d-2f3994f73dc6",
        "codigo": "string",
        "nombre": "Producto A",
        "descripcion": "Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua",
        "valorVariable": true,
        "valor": 30000,
        "imagenId": "644176ac-41f6-48ac-a4ef-3db5eb09fbf9",
        "tipo": "BOLETA",
        "productosCombo": [
          {
            "fechaCreado": null,
            "creadoPor": null,
            "fechaModificado": null,
            "modificadoPor": null,
            "producto": null,
            "cantidad": null
          }
        ],
        "ventaFechaInicio": "26-04-2024",
        "ventaFechaFin": "26-04-2024",
        "consumoFechaInicio": "26-04-2024",
        "consumoFechaFin": "26-04-2024",
        "excepcionesDiasSemana": [
          {
            "id": null,
            "tipo": null,
            "lunes": null,
            "martes": null,
            "miercoles": null,
            "jueves": null,
            "viernes": null,
            "sabado": null,
            "domingo": null
          }
        ],
        "activacionDesactivacionAutomatica": true
      },
      "tiposVehiculo": [
        {
          "fechaCreado": "26-04-2024 12:37:36",
          "creadoPor": "string",
          "fechaModificado": "26-04-2024 12:37:36",
          "modificadoPor": "string",
          "id": 1,
          "nombre": "AUTOMOVIL"
        }
      ],
      "estado": "ACTIVO"
    }
  ],
  "number": 0,
  "sort": {
    "empty": true,
    "sorted": true,
    "unsorted": true
  },
  "first": true,
  "pageable": {
    "offset": 0,
    "sort": {
      "empty": true,
      "sorted": true,
      "unsorted": true
    },
    "pageNumber": 0,
    "pageSize": 0,
    "unpaged": true,
    "paged": true
  },
  "numberOfElements": 0,
  "last": true,
  "empty": true
}

```

### Attribute

|Name|Type|Required|Restrictions|Title|Description|
|---|---|---|---|---|---|
|totalPages|integer(int32)|false|none||none|
|totalElements|integer(int64)|false|none||none|
|size|integer(int32)|false|none||none|
|content|[[TipoServicioParqueadero](#schematiposervicioparqueadero)]|false|none||none|
|number|integer(int32)|false|none||none|
|sort|[SortObject](#schemasortobject)|false|none||none|
|first|boolean|false|none||none|
|pageable|[PageableObject](#schemapageableobject)|false|none||none|
|numberOfElements|integer(int32)|false|none||none|
|last|boolean|false|none||none|
|empty|boolean|false|none||none|

<h2 id="tocS_PageTipoVehiculo">PageTipoVehiculo</h2>

<a id="schemapagetipovehiculo"></a>
<a id="schema_PageTipoVehiculo"></a>
<a id="tocSpagetipovehiculo"></a>
<a id="tocspagetipovehiculo"></a>

```json
{
  "totalPages": 0,
  "totalElements": 0,
  "size": 0,
  "content": [
    {
      "fechaCreado": "26-04-2024 12:37:36",
      "creadoPor": "string",
      "fechaModificado": "26-04-2024 12:37:36",
      "modificadoPor": "string",
      "id": 1,
      "nombre": "AUTOMOVIL"
    }
  ],
  "number": 0,
  "sort": {
    "empty": true,
    "sorted": true,
    "unsorted": true
  },
  "first": true,
  "pageable": {
    "offset": 0,
    "sort": {
      "empty": true,
      "sorted": true,
      "unsorted": true
    },
    "pageNumber": 0,
    "pageSize": 0,
    "unpaged": true,
    "paged": true
  },
  "numberOfElements": 0,
  "last": true,
  "empty": true
}

```

### Attribute

|Name|Type|Required|Restrictions|Title|Description|
|---|---|---|---|---|---|
|totalPages|integer(int32)|false|none||none|
|totalElements|integer(int64)|false|none||none|
|size|integer(int32)|false|none||none|
|content|[[TipoVehiculo](#schematipovehiculo)]|false|none||[tipo de vehiculo]|
|number|integer(int32)|false|none||none|
|sort|[SortObject](#schemasortobject)|false|none||none|
|first|boolean|false|none||none|
|pageable|[PageableObject](#schemapageableobject)|false|none||none|
|numberOfElements|integer(int32)|false|none||none|
|last|boolean|false|none||none|
|empty|boolean|false|none||none|

<h2 id="tocS_PageVenta">PageVenta</h2>

<a id="schemapageventa"></a>
<a id="schema_PageVenta"></a>
<a id="tocSpageventa"></a>
<a id="tocspageventa"></a>

```json
{
  "totalPages": 0,
  "totalElements": 0,
  "size": 0,
  "content": [
    {
      "fechaCreado": "26-04-2024 12:37:36",
      "creadoPor": "string",
      "fechaModificado": "26-04-2024 12:37:36",
      "modificadoPor": "string",
      "id": 1,
      "reservaId": "e4b3b3b3-4b3b-4b3b-4b3b-4b3b4b3b4b3b",
      "cliente": {
        "fechaCreado": "26-04-2024 12:37:36",
        "creadoPor": "string",
        "fechaModificado": "26-04-2024 12:37:36",
        "modificadoPor": "string",
        "identificacion": {
          "tipo": "[",
          "numero": "["
        },
        "primerNombre": "Nombre 1",
        "segundoNombre": "Nombre 2",
        "primerApellido": "Apellido 1",
        "segundoApellido": "Apellido 2",
        "nombreCompleto": "Nombre 1 Nombre 2 Apellido 1 Apellido 2",
        "email": "example@email.com",
        "telefono": "3005557777",
        "genero": "M",
        "fechaNacimiento": "26-04-2024",
        "ciudad": "11001.11.Co",
        "direccion": "Calle 1 # 1 - 1"
      },
      "registroTaquillaId": "b3b3b3b3-4b3b-4b3b-4b3b-4b3b4b3b4b3b",
      "reciboTaquilla": {
        "fechaCreado": "26-04-2024 12:37:36",
        "creadoPor": "string",
        "fechaModificado": "26-04-2024 12:37:36",
        "modificadoPor": "string",
        "id": 0,
        "numero": 0,
        "ultimoRegistroImpresion": {
          "fechaCreado": "[",
          "creadoPor": "string",
          "fechaModificado": "[",
          "modificadoPor": "string",
          "id": 0,
          "tipoImpresion": "[",
          "impresora": {},
          "identificador": "string",
          "estado": "[",
          "mensajeError": "["
        }
      },
      "recepcionPago": "TAQUILLA",
      "detallesVentaProductos": {
        "fechaCreado": "26-04-2024 12:37:36",
        "creadoPor": "string",
        "fechaModificado": "26-04-2024 12:37:36",
        "modificadoPor": "string",
        "id": 0,
        "clienteTipoIdentificacion": "CC",
        "clienteNumeroIdentificacion": "1111222333",
        "clienteNombre": "Nombre 1 Nombre 2 Apellido 1 Apellido 2",
        "reservaId": "dd36d635-3836-499b-b9e8-a21f7b8f8d99",
        "productoId": "facf4a34-c5cd-4888-bb4d-b65af8ae4dd9",
        "productoCodigo": "string",
        "productoTipo": "BOLETA",
        "productoNombre": "string",
        "productoValor": 0,
        "descuentoValor": 0,
        "valor": 0,
        "boletaId": "1bdd62d6-cfe6-46e0-9d28-6efc9e2d97ee",
        "reservaCasillaId": "ffa80c2d-a380-4e24-8b51-81cc376fde36",
        "reservaVehiculoId": "e3e6894b-2f0a-4368-ab7e-d7263f01cea3",
        "espacioParqueaderoId": 0,
        "reservaServicioAdicionalId": "e2db60eb-fe50-40b8-8bf7-7fd2f4953292",
        "reservaComboId": "b5015fcd-c071-4677-a321-3ff1e45a389a",
        "descuento": {
          "fechaCreado": "[",
          "creadoPor": "string",
          "fechaModificado": "[",
          "modificadoPor": "string",
          "id": "[",
          "nombre": "[",
          "tiposProducto": [
            null
          ],
          "aplicarConCodigo": "[",
          "codigo": "[",
          "aplicarConVigencia": "[",
          "vigenciaInicio": "[",
          "vigenciaFin": "[",
          "tipo": "[",
          "valor": "[",
          "consumoMax": "[",
          "consumoMaxCliente": "[",
          "consumo": "[",
          "estado": "[",
          "clientesObjetivo": "[",
          "clientesCompraronEnFechas": "[",
          "ccefFechaInicio": "[",
          "ccefFechaFin": "[",
          "clientesEspecificos": "["
        },
        "estadoPago": "APROBADO",
        "reservaFecha": "26-04-2024"
      },
      "transaccionesPago": {
        "fechaCreado": "26-04-2024 12:37:36",
        "creadoPor": "string",
        "fechaModificado": "26-04-2024 12:37:36",
        "modificadoPor": "string",
        "id": 0,
        "recepcionPago": "TAQUILLA",
        "metodoPago": {
          "fechaCreado": "[",
          "creadoPor": "string",
          "fechaModificado": "[",
          "modificadoPor": "string",
          "id": "[",
          "nombre": "[",
          "cuentaDestino": "[",
          "tipo": "[",
          "requiereDatosAutorizacion": "[",
          "recepcionesPago": [
            null
          ],
          "estado": "["
        },
        "valor": 50000,
        "transaccionTaquilla": {
          "fechaCreado": "[",
          "creadoPor": "string",
          "fechaModificado": "[",
          "modificadoPor": "string",
          "id": "[",
          "reservaId": "dd36d635-3836-499b-b9e8-a21f7b8f8d99",
          "metodoPago": {},
          "valor": "[",
          "numeroAutorizacion": "[",
          "ultimosDigitos": "[",
          "registroTaquillaId": "aded13d6-1970-4003-aa21-1f29fc5692a9",
          "cambioEfectivo": {},
          "reciboTaquillaNumero": 0,
          "taquillaId": 0,
          "taquillaNombre": "string"
        },
        "transaccionPasarela": {
          "fechaCreado": "[",
          "creadoPor": "string",
          "fechaModificado": "[",
          "modificadoPor": "string",
          "id": "[",
          "reservaId": "[",
          "tipoIdentificacionCliente": "[",
          "numeroIdentificacionCliente": "[",
          "valor": "[",
          "origen": "[",
          "ip": "[",
          "metodoPago": {},
          "fechaHoraInicio": "[",
          "fechaHoraFin": "[",
          "estado": "["
        },
        "transaccionParqueadero": {
          "fechaCreado": "[",
          "creadoPor": "string",
          "fechaModificado": "[",
          "modificadoPor": "string",
          "id": "[",
          "metodoPago": {},
          "valor": "[",
          "numeroAutorizacion": "[",
          "ultimosDigitos": "[",
          "zonaParqueaderoId": 0,
          "placa": "string",
          "fechaParqueo": "[",
          "cambioEfectivo": {}
        },
        "transaccionPartner": {
          "fechaCreado": "[",
          "creadoPor": "string",
          "fechaModificado": "[",
          "modificadoPor": "string",
          "id": "[",
          "partnerId": "bf408d53-df49-40a6-8455-a34bd4360901",
          "reservaId": "[",
          "tipoIdentificacionCliente": "[",
          "numeroIdentificacionCliente": "[",
          "valor": "[",
          "barcode": "string",
          "orderId": 0
        }
      },
      "valorSinDescuento": 100000,
      "valorPagoTotal": 100000,
      "canal": {
        "fechaCreado": "26-04-2024 12:37:36",
        "creadoPor": "string",
        "fechaModificado": "26-04-2024 12:37:36",
        "modificadoPor": "string",
        "id": 1,
        "nombre": "Canal A"
      },
      "reservaFecha": "26-04-2024",
      "taquilla": {
        "fechaCreado": "26-04-2024 12:37:36",
        "creadoPor": "string",
        "fechaModificado": "26-04-2024 12:37:36",
        "modificadoPor": "string",
        "id": 1,
        "nombre": "Taquilla 1",
        "conteoRecibos": 0,
        "estado": "ACTIVO",
        "impresoras": [
          {
            "fechaCreado": null,
            "creadoPor": null,
            "fechaModificado": null,
            "modificadoPor": null,
            "id": null,
            "nombre": null,
            "direccionIp": null,
            "estado": null,
            "marca": null,
            "referencia": null,
            "serial": null,
            "tipoImpresora": null
          }
        ]
      },
      "facturaVentaNumero": 1,
      "reservaDescuento": {
        "fechaCreado": "26-04-2024 12:37:36",
        "creadoPor": "string",
        "fechaModificado": "26-04-2024 12:37:36",
        "modificadoPor": "string",
        "id": "6ae369b6-847e-446a-a096-06e589c63db7",
        "nombre": "Descuento A",
        "tiposProducto": [
          {
            "fechaCreado": null,
            "creadoPor": null,
            "fechaModificado": null,
            "modificadoPor": null,
            "tipoProducto": null,
            "cantidadMax": null
          }
        ],
        "aplicarConCodigo": true,
        "codigo": "D1AHF524A0",
        "aplicarConVigencia": true,
        "vigenciaInicio": "26-04-2024 12:37:36",
        "vigenciaFin": "26-04-2024 12:37:36",
        "tipo": "PORCENTAJE",
        "valor": 20,
        "consumoMax": 100,
        "consumoMaxCliente": 1,
        "consumo": 5,
        "estado": "ACTIVO",
        "clientesObjetivo": true,
        "clientesCompraronEnFechas": true,
        "ccefFechaInicio": "26-04-2024 12:37:36",
        "ccefFechaFin": "26-04-2024 12:37:36",
        "clientesEspecificos": false
      }
    }
  ],
  "number": 0,
  "sort": {
    "empty": true,
    "sorted": true,
    "unsorted": true
  },
  "first": true,
  "pageable": {
    "offset": 0,
    "sort": {
      "empty": true,
      "sorted": true,
      "unsorted": true
    },
    "pageNumber": 0,
    "pageSize": 0,
    "unpaged": true,
    "paged": true
  },
  "numberOfElements": 0,
  "last": true,
  "empty": true
}

```

### Attribute

|Name|Type|Required|Restrictions|Title|Description|
|---|---|---|---|---|---|
|totalPages|integer(int32)|false|none||none|
|totalElements|integer(int64)|false|none||none|
|size|integer(int32)|false|none||none|
|content|[[Venta](#schemaventa)]|false|none||none|
|number|integer(int32)|false|none||none|
|sort|[SortObject](#schemasortobject)|false|none||none|
|first|boolean|false|none||none|
|pageable|[PageableObject](#schemapageableobject)|false|none||none|
|numberOfElements|integer(int32)|false|none||none|
|last|boolean|false|none||none|
|empty|boolean|false|none||none|

<h2 id="tocS_Venta">Venta</h2>

<a id="schemaventa"></a>
<a id="schema_Venta"></a>
<a id="tocSventa"></a>
<a id="tocsventa"></a>

```json
{
  "fechaCreado": "26-04-2024 12:37:36",
  "creadoPor": "string",
  "fechaModificado": "26-04-2024 12:37:36",
  "modificadoPor": "string",
  "id": 1,
  "reservaId": "e4b3b3b3-4b3b-4b3b-4b3b-4b3b4b3b4b3b",
  "cliente": {
    "fechaCreado": "26-04-2024 12:37:36",
    "creadoPor": "string",
    "fechaModificado": "26-04-2024 12:37:36",
    "modificadoPor": "string",
    "identificacion": {
      "tipo": "CC",
      "numero": "1111111111"
    },
    "primerNombre": "Nombre 1",
    "segundoNombre": "Nombre 2",
    "primerApellido": "Apellido 1",
    "segundoApellido": "Apellido 2",
    "nombreCompleto": "Nombre 1 Nombre 2 Apellido 1 Apellido 2",
    "email": "example@email.com",
    "telefono": "3005557777",
    "genero": "M",
    "fechaNacimiento": "26-04-2024",
    "ciudad": "11001.11.Co",
    "direccion": "Calle 1 # 1 - 1"
  },
  "registroTaquillaId": "b3b3b3b3-4b3b-4b3b-4b3b-4b3b4b3b4b3b",
  "reciboTaquilla": {
    "fechaCreado": "26-04-2024 12:37:36",
    "creadoPor": "string",
    "fechaModificado": "26-04-2024 12:37:36",
    "modificadoPor": "string",
    "id": 0,
    "numero": 0,
    "ultimoRegistroImpresion": {
      "fechaCreado": "26-04-2024 12:37:36",
      "creadoPor": "string",
      "fechaModificado": "26-04-2024 12:37:36",
      "modificadoPor": "string",
      "id": 0,
      "tipoImpresion": "MANILLA",
      "impresora": {
        "fechaCreado": "26-04-2024 12:37:36",
        "creadoPor": "string",
        "fechaModificado": "26-04-2024 12:37:36",
        "modificadoPor": "string",
        "id": 0,
        "nombre": "string",
        "direccionIp": "string",
        "estado": "ACTIVO",
        "marca": "ZEBRA",
        "referencia": "string",
        "serial": "string",
        "tipoImpresora": "IMPRESORA_MANILLAS"
      },
      "identificador": "string",
      "estado": "EXITOSO",
      "mensajeError": "Error"
    }
  },
  "recepcionPago": "TAQUILLA",
  "detallesVentaProductos": {
    "fechaCreado": "26-04-2024 12:37:36",
    "creadoPor": "string",
    "fechaModificado": "26-04-2024 12:37:36",
    "modificadoPor": "string",
    "id": 0,
    "clienteTipoIdentificacion": "CC",
    "clienteNumeroIdentificacion": "1111222333",
    "clienteNombre": "Nombre 1 Nombre 2 Apellido 1 Apellido 2",
    "reservaId": "dd36d635-3836-499b-b9e8-a21f7b8f8d99",
    "productoId": "facf4a34-c5cd-4888-bb4d-b65af8ae4dd9",
    "productoCodigo": "string",
    "productoTipo": "BOLETA",
    "productoNombre": "string",
    "productoValor": 0,
    "descuentoValor": 0,
    "valor": 0,
    "boletaId": "1bdd62d6-cfe6-46e0-9d28-6efc9e2d97ee",
    "reservaCasillaId": "ffa80c2d-a380-4e24-8b51-81cc376fde36",
    "reservaVehiculoId": "e3e6894b-2f0a-4368-ab7e-d7263f01cea3",
    "espacioParqueaderoId": 0,
    "reservaServicioAdicionalId": "e2db60eb-fe50-40b8-8bf7-7fd2f4953292",
    "reservaComboId": "b5015fcd-c071-4677-a321-3ff1e45a389a",
    "descuento": {
      "fechaCreado": "26-04-2024 12:37:36",
      "creadoPor": "string",
      "fechaModificado": "26-04-2024 12:37:36",
      "modificadoPor": "string",
      "id": "6ae369b6-847e-446a-a096-06e589c63db7",
      "nombre": "Descuento A",
      "tiposProducto": [
        {
          "fechaCreado": "[",
          "creadoPor": "string",
          "fechaModificado": "[",
          "modificadoPor": "string",
          "tipoProducto": "[",
          "cantidadMax": 0
        }
      ],
      "aplicarConCodigo": true,
      "codigo": "D1AHF524A0",
      "aplicarConVigencia": true,
      "vigenciaInicio": "26-04-2024 12:37:36",
      "vigenciaFin": "26-04-2024 12:37:36",
      "tipo": "PORCENTAJE",
      "valor": 20,
      "consumoMax": 100,
      "consumoMaxCliente": 1,
      "consumo": 5,
      "estado": "ACTIVO",
      "clientesObjetivo": true,
      "clientesCompraronEnFechas": true,
      "ccefFechaInicio": "26-04-2024 12:37:36",
      "ccefFechaFin": "26-04-2024 12:37:36",
      "clientesEspecificos": false
    },
    "estadoPago": "APROBADO",
    "reservaFecha": "26-04-2024"
  },
  "transaccionesPago": {
    "fechaCreado": "26-04-2024 12:37:36",
    "creadoPor": "string",
    "fechaModificado": "26-04-2024 12:37:36",
    "modificadoPor": "string",
    "id": 0,
    "recepcionPago": "TAQUILLA",
    "metodoPago": {
      "fechaCreado": "26-04-2024 12:37:36",
      "creadoPor": "string",
      "fechaModificado": "26-04-2024 12:37:36",
      "modificadoPor": "string",
      "id": 1,
      "nombre": "Metodo de pago A",
      "cuentaDestino": "1111444499997777",
      "tipo": "ELECTRONICO",
      "requiereDatosAutorizacion": false,
      "recepcionesPago": [
        {
          "fechaCreado": "[",
          "creadoPor": "string",
          "fechaModificado": "[",
          "modificadoPor": "string",
          "id": 0,
          "recepcionPago": "[",
          "metodoPago": {}
        }
      ],
      "estado": "ACTIVO"
    },
    "valor": 50000,
    "transaccionTaquilla": {
      "fechaCreado": "26-04-2024 12:37:36",
      "creadoPor": "string",
      "fechaModificado": "26-04-2024 12:37:36",
      "modificadoPor": "string",
      "id": "b169240e-56b1-4e38-8c50-279c8a04e5aa",
      "reservaId": "dd36d635-3836-499b-b9e8-a21f7b8f8d99",
      "metodoPago": {
        "fechaCreado": "26-04-2024 12:37:36",
        "creadoPor": "string",
        "fechaModificado": "26-04-2024 12:37:36",
        "modificadoPor": "string",
        "id": 1,
        "nombre": "Metodo de pago A",
        "cuentaDestino": "1111444499997777",
        "tipo": "ELECTRONICO",
        "requiereDatosAutorizacion": false,
        "recepcionesPago": [
          {}
        ],
        "estado": "ACTIVO"
      },
      "valor": 50000,
      "numeroAutorizacion": "00032325",
      "ultimosDigitos": "4488",
      "registroTaquillaId": "aded13d6-1970-4003-aa21-1f29fc5692a9",
      "cambioEfectivo": {
        "fechaCreado": "26-04-2024 12:37:36",
        "creadoPor": "string",
        "fechaModificado": "26-04-2024 12:37:36",
        "modificadoPor": "string",
        "id": 0,
        "efectivo": 0,
        "cambio": 0
      },
      "reciboTaquillaNumero": 0,
      "taquillaId": 0,
      "taquillaNombre": "string"
    },
    "transaccionPasarela": {
      "fechaCreado": "26-04-2024 12:37:36",
      "creadoPor": "string",
      "fechaModificado": "26-04-2024 12:37:36",
      "modificadoPor": "string",
      "id": "1c8356b0e24442b2acc579cf1ae4d8145",
      "reservaId": "755864a6-0c1f-4f32-9c54-7fb38f9dd9b1",
      "tipoIdentificacionCliente": "CC",
      "numeroIdentificacionCliente": "1111111111",
      "valor": 50000,
      "origen": "Origen X",
      "ip": "192.168.1.1",
      "metodoPago": {
        "fechaCreado": "26-04-2024 12:37:36",
        "creadoPor": "string",
        "fechaModificado": "26-04-2024 12:37:36",
        "modificadoPor": "string",
        "id": 1,
        "nombre": "Metodo de pago A",
        "cuentaDestino": "1111444499997777",
        "tipo": "ELECTRONICO",
        "requiereDatosAutorizacion": false,
        "recepcionesPago": [
          {}
        ],
        "estado": "ACTIVO"
      },
      "fechaHoraInicio": "26-04-2024 12:37:36",
      "fechaHoraFin": "26-04-2024 12:37:36",
      "estado": "EN_PROCESO"
    },
    "transaccionParqueadero": {
      "fechaCreado": "26-04-2024 12:37:36",
      "creadoPor": "string",
      "fechaModificado": "26-04-2024 12:37:36",
      "modificadoPor": "string",
      "id": "b169240e-56b1-4e38-8c50-279c8a04e5aa",
      "metodoPago": {
        "fechaCreado": "26-04-2024 12:37:36",
        "creadoPor": "string",
        "fechaModificado": "26-04-2024 12:37:36",
        "modificadoPor": "string",
        "id": 1,
        "nombre": "Metodo de pago A",
        "cuentaDestino": "1111444499997777",
        "tipo": "ELECTRONICO",
        "requiereDatosAutorizacion": false,
        "recepcionesPago": [
          {}
        ],
        "estado": "ACTIVO"
      },
      "valor": 50000,
      "numeroAutorizacion": "00032325",
      "ultimosDigitos": "4488",
      "zonaParqueaderoId": 0,
      "placa": "string",
      "fechaParqueo": "26-04-2024",
      "cambioEfectivo": {
        "fechaCreado": "26-04-2024 12:37:36",
        "creadoPor": "string",
        "fechaModificado": "26-04-2024 12:37:36",
        "modificadoPor": "string",
        "id": 0,
        "efectivo": 0,
        "cambio": 0
      }
    },
    "transaccionPartner": {
      "fechaCreado": "26-04-2024 12:37:36",
      "creadoPor": "string",
      "fechaModificado": "26-04-2024 12:37:36",
      "modificadoPor": "string",
      "id": "b169240e-56b1-4e38-8c50-279c8a04e5aa",
      "partnerId": "bf408d53-df49-40a6-8455-a34bd4360901",
      "reservaId": "755864a6-0c1f-4f32-9c54-7fb38f9dd9b1",
      "tipoIdentificacionCliente": "CC",
      "numeroIdentificacionCliente": "1111111111",
      "valor": 50000,
      "barcode": "string",
      "orderId": 0
    }
  },
  "valorSinDescuento": 100000,
  "valorPagoTotal": 100000,
  "canal": {
    "fechaCreado": "26-04-2024 12:37:36",
    "creadoPor": "string",
    "fechaModificado": "26-04-2024 12:37:36",
    "modificadoPor": "string",
    "id": 1,
    "nombre": "Canal A"
  },
  "reservaFecha": "26-04-2024",
  "taquilla": {
    "fechaCreado": "26-04-2024 12:37:36",
    "creadoPor": "string",
    "fechaModificado": "26-04-2024 12:37:36",
    "modificadoPor": "string",
    "id": 1,
    "nombre": "Taquilla 1",
    "conteoRecibos": 0,
    "estado": "ACTIVO",
    "impresoras": [
      {
        "fechaCreado": "26-04-2024 12:37:36",
        "creadoPor": "string",
        "fechaModificado": "26-04-2024 12:37:36",
        "modificadoPor": "string",
        "id": 0,
        "nombre": "string",
        "direccionIp": "string",
        "estado": "ACTIVO",
        "marca": "ZEBRA",
        "referencia": "string",
        "serial": "string",
        "tipoImpresora": "IMPRESORA_MANILLAS"
      }
    ]
  },
  "facturaVentaNumero": 1,
  "reservaDescuento": {
    "fechaCreado": "26-04-2024 12:37:36",
    "creadoPor": "string",
    "fechaModificado": "26-04-2024 12:37:36",
    "modificadoPor": "string",
    "id": "6ae369b6-847e-446a-a096-06e589c63db7",
    "nombre": "Descuento A",
    "tiposProducto": [
      {
        "fechaCreado": "26-04-2024 12:37:36",
        "creadoPor": "string",
        "fechaModificado": "26-04-2024 12:37:36",
        "modificadoPor": "string",
        "tipoProducto": "BOLETA",
        "cantidadMax": 0
      }
    ],
    "aplicarConCodigo": true,
    "codigo": "D1AHF524A0",
    "aplicarConVigencia": true,
    "vigenciaInicio": "26-04-2024 12:37:36",
    "vigenciaFin": "26-04-2024 12:37:36",
    "tipo": "PORCENTAJE",
    "valor": 20,
    "consumoMax": 100,
    "consumoMaxCliente": 1,
    "consumo": 5,
    "estado": "ACTIVO",
    "clientesObjetivo": true,
    "clientesCompraronEnFechas": true,
    "ccefFechaInicio": "26-04-2024 12:37:36",
    "ccefFechaFin": "26-04-2024 12:37:36",
    "clientesEspecificos": false
  }
}

```

### Attribute

|Name|Type|Required|Restrictions|Title|Description|
|---|---|---|---|---|---|
|fechaCreado|string|false|none||none|
|creadoPor|string|false|none||none|
|fechaModificado|string|false|none||none|
|modificadoPor|string|false|none||none|
|id|integer(int64)|false|none||id de la venta|
|reservaId|string(uuid)|false|none||id de la reserva asociada a esta venta|
|cliente|[Cliente](#schemacliente)|false|none||cliente asociado con esta reserva|
|registroTaquillaId|string(uuid)|false|none||id del registro de taquilla asociado a esta venta|
|reciboTaquilla|[ReciboTaquilla](#schemarecibotaquilla)|false|none||recibo de taquilla asociado a esta venta|
|recepcionPago|string|false|none||modo de recepcion de pago de la venta|
|detallesVentaProductos|[DetalleVentaProducto](#schemadetalleventaproducto)|false|none||detalles de productos vendidos en la venta|
|transaccionesPago|[TransaccionPago](#schematransaccionpago)|false|none||detalles de transacciones de pago en la venta|
|valorSinDescuento|number(double)|false|none||valor total de la venta sin descuento|
|valorPagoTotal|number(double)|false|none||valor total pagado en la venta|
|canal|[Canal](#schemacanal)|false|none||canal asociado con esta reserva|
|reservaFecha|string|false|none||fecha la reserva asociada a esta venta|
|taquilla|[Taquilla](#schemataquilla)|false|none||none|
|facturaVentaNumero|integer(int64)|false|none||numero de la factura de venta asociada a esta venta|
|reservaDescuento|[Descuento](#schemadescuento)|false|none||descuento asociado con esta reserva|

#### Enum

|Name|Value|
|---|---|
|recepcionPago|TAQUILLA|
|recepcionPago|PASARELA|
|recepcionPago|PARTNER|
|recepcionPago|PARQUEADERO|

<h2 id="tocS_Taquilla">Taquilla</h2>

<a id="schemataquilla"></a>
<a id="schema_Taquilla"></a>
<a id="tocStaquilla"></a>
<a id="tocstaquilla"></a>

```json
{
  "fechaCreado": "26-04-2024 12:37:36",
  "creadoPor": "string",
  "fechaModificado": "26-04-2024 12:37:36",
  "modificadoPor": "string",
  "id": 1,
  "nombre": "Taquilla 1",
  "conteoRecibos": 0,
  "estado": "ACTIVO",
  "impresoras": [
    {
      "fechaCreado": "26-04-2024 12:37:36",
      "creadoPor": "string",
      "fechaModificado": "26-04-2024 12:37:36",
      "modificadoPor": "string",
      "id": 0,
      "nombre": "string",
      "direccionIp": "string",
      "estado": "ACTIVO",
      "marca": "ZEBRA",
      "referencia": "string",
      "serial": "string",
      "tipoImpresora": "IMPRESORA_MANILLAS"
    }
  ]
}

```

### Attribute

|Name|Type|Required|Restrictions|Title|Description|
|---|---|---|---|---|---|
|fechaCreado|string|false|none||none|
|creadoPor|string|false|none||none|
|fechaModificado|string|false|none||none|
|modificadoPor|string|false|none||none|
|id|integer(int64)|false|none||id de la taquilla|
|nombre|string|false|none||nombre de la taquilla|
|conteoRecibos|integer(int64)|false|none||none|
|estado|string|false|none||estado de la taquilla|
|impresoras|[[Impresora](#schemaimpresora)]|false|none||[impresoras asignadas a una taquilla]|

#### Enum

|Name|Value|
|---|---|
|estado|ACTIVO|
|estado|INACTIVO|

<h2 id="tocS_Impresora">Impresora</h2>

<a id="schemaimpresora"></a>
<a id="schema_Impresora"></a>
<a id="tocSimpresora"></a>
<a id="tocsimpresora"></a>

```json
{
  "fechaCreado": "26-04-2024 12:37:36",
  "creadoPor": "string",
  "fechaModificado": "26-04-2024 12:37:36",
  "modificadoPor": "string",
  "id": 0,
  "nombre": "string",
  "direccionIp": "string",
  "estado": "ACTIVO",
  "marca": "ZEBRA",
  "referencia": "string",
  "serial": "string",
  "tipoImpresora": "IMPRESORA_MANILLAS"
}

```

impresoras asignadas a una taquilla

### Attribute

|Name|Type|Required|Restrictions|Title|Description|
|---|---|---|---|---|---|
|fechaCreado|string|false|none||none|
|creadoPor|string|false|none||none|
|fechaModificado|string|false|none||none|
|modificadoPor|string|false|none||none|
|id|integer(int64)|false|none||none|
|nombre|string|false|none||none|
|direccionIp|string|false|none||none|
|estado|string|false|none||none|
|marca|string|false|none||none|
|referencia|string|false|none||none|
|serial|string|false|none||none|
|tipoImpresora|string|false|none||none|

#### Enum

|Name|Value|
|---|---|
|estado|ACTIVO|
|estado|INACTIVO|
|estado|MANTENIMIENTO|
|marca|ZEBRA|
|marca|CHAINWAY|
|marca|GAINSCHA|
|marca|SAT|
|tipoImpresora|IMPRESORA_MANILLAS|
|tipoImpresora|IMPRESORA_BOLETAS|

<h2 id="tocS_TransaccionPago">TransaccionPago</h2>

<a id="schematransaccionpago"></a>
<a id="schema_TransaccionPago"></a>
<a id="tocStransaccionpago"></a>
<a id="tocstransaccionpago"></a>

```json
{
  "fechaCreado": "26-04-2024 12:37:36",
  "creadoPor": "string",
  "fechaModificado": "26-04-2024 12:37:36",
  "modificadoPor": "string",
  "id": 0,
  "recepcionPago": "TAQUILLA",
  "metodoPago": {
    "fechaCreado": "26-04-2024 12:37:36",
    "creadoPor": "string",
    "fechaModificado": "26-04-2024 12:37:36",
    "modificadoPor": "string",
    "id": 1,
    "nombre": "Metodo de pago A",
    "cuentaDestino": "1111444499997777",
    "tipo": "ELECTRONICO",
    "requiereDatosAutorizacion": false,
    "recepcionesPago": [
      {
        "fechaCreado": "26-04-2024 12:37:36",
        "creadoPor": "string",
        "fechaModificado": "26-04-2024 12:37:36",
        "modificadoPor": "string",
        "id": 0,
        "recepcionPago": "TAQUILLA",
        "metodoPago": {
          "fechaCreado": "[",
          "creadoPor": "string",
          "fechaModificado": "[",
          "modificadoPor": "string",
          "id": "[",
          "nombre": "[",
          "cuentaDestino": "[",
          "tipo": "[",
          "requiereDatosAutorizacion": "[",
          "recepcionesPago": [
            null
          ],
          "estado": "["
        }
      }
    ],
    "estado": "ACTIVO"
  },
  "valor": 50000,
  "transaccionTaquilla": {
    "fechaCreado": "26-04-2024 12:37:36",
    "creadoPor": "string",
    "fechaModificado": "26-04-2024 12:37:36",
    "modificadoPor": "string",
    "id": "b169240e-56b1-4e38-8c50-279c8a04e5aa",
    "reservaId": "dd36d635-3836-499b-b9e8-a21f7b8f8d99",
    "metodoPago": {
      "fechaCreado": "26-04-2024 12:37:36",
      "creadoPor": "string",
      "fechaModificado": "26-04-2024 12:37:36",
      "modificadoPor": "string",
      "id": 1,
      "nombre": "Metodo de pago A",
      "cuentaDestino": "1111444499997777",
      "tipo": "ELECTRONICO",
      "requiereDatosAutorizacion": false,
      "recepcionesPago": [
        {
          "fechaCreado": "[",
          "creadoPor": "string",
          "fechaModificado": "[",
          "modificadoPor": "string",
          "id": 0,
          "recepcionPago": "[",
          "metodoPago": {}
        }
      ],
      "estado": "ACTIVO"
    },
    "valor": 50000,
    "numeroAutorizacion": "00032325",
    "ultimosDigitos": "4488",
    "registroTaquillaId": "aded13d6-1970-4003-aa21-1f29fc5692a9",
    "cambioEfectivo": {
      "fechaCreado": "26-04-2024 12:37:36",
      "creadoPor": "string",
      "fechaModificado": "26-04-2024 12:37:36",
      "modificadoPor": "string",
      "id": 0,
      "efectivo": 0,
      "cambio": 0
    },
    "reciboTaquillaNumero": 0,
    "taquillaId": 0,
    "taquillaNombre": "string"
  },
  "transaccionPasarela": {
    "fechaCreado": "26-04-2024 12:37:36",
    "creadoPor": "string",
    "fechaModificado": "26-04-2024 12:37:36",
    "modificadoPor": "string",
    "id": "1c8356b0e24442b2acc579cf1ae4d8145",
    "reservaId": "755864a6-0c1f-4f32-9c54-7fb38f9dd9b1",
    "tipoIdentificacionCliente": "CC",
    "numeroIdentificacionCliente": "1111111111",
    "valor": 50000,
    "origen": "Origen X",
    "ip": "192.168.1.1",
    "metodoPago": {
      "fechaCreado": "26-04-2024 12:37:36",
      "creadoPor": "string",
      "fechaModificado": "26-04-2024 12:37:36",
      "modificadoPor": "string",
      "id": 1,
      "nombre": "Metodo de pago A",
      "cuentaDestino": "1111444499997777",
      "tipo": "ELECTRONICO",
      "requiereDatosAutorizacion": false,
      "recepcionesPago": [
        {
          "fechaCreado": "[",
          "creadoPor": "string",
          "fechaModificado": "[",
          "modificadoPor": "string",
          "id": 0,
          "recepcionPago": "[",
          "metodoPago": {}
        }
      ],
      "estado": "ACTIVO"
    },
    "fechaHoraInicio": "26-04-2024 12:37:36",
    "fechaHoraFin": "26-04-2024 12:37:36",
    "estado": "EN_PROCESO"
  },
  "transaccionParqueadero": {
    "fechaCreado": "26-04-2024 12:37:36",
    "creadoPor": "string",
    "fechaModificado": "26-04-2024 12:37:36",
    "modificadoPor": "string",
    "id": "b169240e-56b1-4e38-8c50-279c8a04e5aa",
    "metodoPago": {
      "fechaCreado": "26-04-2024 12:37:36",
      "creadoPor": "string",
      "fechaModificado": "26-04-2024 12:37:36",
      "modificadoPor": "string",
      "id": 1,
      "nombre": "Metodo de pago A",
      "cuentaDestino": "1111444499997777",
      "tipo": "ELECTRONICO",
      "requiereDatosAutorizacion": false,
      "recepcionesPago": [
        {
          "fechaCreado": "[",
          "creadoPor": "string",
          "fechaModificado": "[",
          "modificadoPor": "string",
          "id": 0,
          "recepcionPago": "[",
          "metodoPago": {}
        }
      ],
      "estado": "ACTIVO"
    },
    "valor": 50000,
    "numeroAutorizacion": "00032325",
    "ultimosDigitos": "4488",
    "zonaParqueaderoId": 0,
    "placa": "string",
    "fechaParqueo": "26-04-2024",
    "cambioEfectivo": {
      "fechaCreado": "26-04-2024 12:37:36",
      "creadoPor": "string",
      "fechaModificado": "26-04-2024 12:37:36",
      "modificadoPor": "string",
      "id": 0,
      "efectivo": 0,
      "cambio": 0
    }
  },
  "transaccionPartner": {
    "fechaCreado": "26-04-2024 12:37:36",
    "creadoPor": "string",
    "fechaModificado": "26-04-2024 12:37:36",
    "modificadoPor": "string",
    "id": "b169240e-56b1-4e38-8c50-279c8a04e5aa",
    "partnerId": "bf408d53-df49-40a6-8455-a34bd4360901",
    "reservaId": "755864a6-0c1f-4f32-9c54-7fb38f9dd9b1",
    "tipoIdentificacionCliente": "CC",
    "numeroIdentificacionCliente": "1111111111",
    "valor": 50000,
    "barcode": "string",
    "orderId": 0
  }
}

```

detalles de transacciones de pago en la venta

### Attribute

|Name|Type|Required|Restrictions|Title|Description|
|---|---|---|---|---|---|
|fechaCreado|string|false|none||none|
|creadoPor|string|false|none||none|
|fechaModificado|string|false|none||none|
|modificadoPor|string|false|none||none|
|id|integer(int64)|false|none||none|
|recepcionPago|string|false|none||none|
|metodoPago|[MetodoPago](#schemametodopago)|false|none||none|
|valor|number(double)|false|none||valor del pago|
|transaccionTaquilla|[TransaccionTaquilla](#schematransacciontaquilla)|false|none||none|
|transaccionPasarela|[TransaccionPasarela](#schematransaccionpasarela)|false|none||none|
|transaccionParqueadero|[TransaccionParqueadero](#schematransaccionparqueadero)|false|none||none|
|transaccionPartner|[TransaccionPartner](#schematransaccionpartner)|false|none||none|

#### Enum

|Name|Value|
|---|---|
|recepcionPago|TAQUILLA|
|recepcionPago|PASARELA|
|recepcionPago|PARTNER|
|recepcionPago|PARQUEADERO|

<h2 id="tocS_TransaccionPartner">TransaccionPartner</h2>

<a id="schematransaccionpartner"></a>
<a id="schema_TransaccionPartner"></a>
<a id="tocStransaccionpartner"></a>
<a id="tocstransaccionpartner"></a>

```json
{
  "fechaCreado": "26-04-2024 12:37:36",
  "creadoPor": "string",
  "fechaModificado": "26-04-2024 12:37:36",
  "modificadoPor": "string",
  "id": "b169240e-56b1-4e38-8c50-279c8a04e5aa",
  "partnerId": "bf408d53-df49-40a6-8455-a34bd4360901",
  "reservaId": "755864a6-0c1f-4f32-9c54-7fb38f9dd9b1",
  "tipoIdentificacionCliente": "CC",
  "numeroIdentificacionCliente": "1111111111",
  "valor": 50000,
  "barcode": "string",
  "orderId": 0
}

```

### Attribute

|Name|Type|Required|Restrictions|Title|Description|
|---|---|---|---|---|---|
|fechaCreado|string|false|none||none|
|creadoPor|string|false|none||none|
|fechaModificado|string|false|none||none|
|modificadoPor|string|false|none||none|
|id|string(uuid)|false|none||id del pago|
|partnerId|string(uuid)|false|none||none|
|reservaId|string(uuid)|false|none||id de la reserva asociada a esta transaccion|
|tipoIdentificacionCliente|string|false|none||tipo de identificacion del cliente|
|numeroIdentificacionCliente|string|false|none||numero de identificacion del cliente|
|valor|number(double)|false|none||valor de la transaccion|
|barcode|string|false|none||none|
|orderId|integer(int64)|false|none||none|

#### Enum

|Name|Value|
|---|---|
|tipoIdentificacionCliente|CC|
|tipoIdentificacionCliente|NIT|
|tipoIdentificacionCliente|CE|
|tipoIdentificacionCliente|PAS|
|tipoIdentificacionCliente|TI|
|tipoIdentificacionCliente|RC|
|tipoIdentificacionCliente|DNI|

<h2 id="tocS_TransaccionParqueadero">TransaccionParqueadero</h2>

<a id="schematransaccionparqueadero"></a>
<a id="schema_TransaccionParqueadero"></a>
<a id="tocStransaccionparqueadero"></a>
<a id="tocstransaccionparqueadero"></a>

```json
{
  "fechaCreado": "26-04-2024 12:37:36",
  "creadoPor": "string",
  "fechaModificado": "26-04-2024 12:37:36",
  "modificadoPor": "string",
  "id": "b169240e-56b1-4e38-8c50-279c8a04e5aa",
  "metodoPago": {
    "fechaCreado": "26-04-2024 12:37:36",
    "creadoPor": "string",
    "fechaModificado": "26-04-2024 12:37:36",
    "modificadoPor": "string",
    "id": 1,
    "nombre": "Metodo de pago A",
    "cuentaDestino": "1111444499997777",
    "tipo": "ELECTRONICO",
    "requiereDatosAutorizacion": false,
    "recepcionesPago": [
      {
        "fechaCreado": "26-04-2024 12:37:36",
        "creadoPor": "string",
        "fechaModificado": "26-04-2024 12:37:36",
        "modificadoPor": "string",
        "id": 0,
        "recepcionPago": "TAQUILLA",
        "metodoPago": {
          "fechaCreado": "[",
          "creadoPor": "string",
          "fechaModificado": "[",
          "modificadoPor": "string",
          "id": "[",
          "nombre": "[",
          "cuentaDestino": "[",
          "tipo": "[",
          "requiereDatosAutorizacion": "[",
          "recepcionesPago": [
            null
          ],
          "estado": "["
        }
      }
    ],
    "estado": "ACTIVO"
  },
  "valor": 50000,
  "numeroAutorizacion": "00032325",
  "ultimosDigitos": "4488",
  "zonaParqueaderoId": 0,
  "placa": "string",
  "fechaParqueo": "26-04-2024",
  "cambioEfectivo": {
    "fechaCreado": "26-04-2024 12:37:36",
    "creadoPor": "string",
    "fechaModificado": "26-04-2024 12:37:36",
    "modificadoPor": "string",
    "id": 0,
    "efectivo": 0,
    "cambio": 0
  }
}

```

### Attribute

|Name|Type|Required|Restrictions|Title|Description|
|---|---|---|---|---|---|
|fechaCreado|string|false|none||none|
|creadoPor|string|false|none||none|
|fechaModificado|string|false|none||none|
|modificadoPor|string|false|none||none|
|id|string(uuid)|false|none||id del pago|
|metodoPago|[MetodoPago](#schemametodopago)|false|none||none|
|valor|number(double)|false|none||valor del pago|
|numeroAutorizacion|string|false|none||numero de autorizacion del pago|
|ultimosDigitos|string|false|none||ultimos digitos del metodo de pago|
|zonaParqueaderoId|integer(int64)|false|none||none|
|placa|string|false|none||none|
|fechaParqueo|string|false|none||none|
|cambioEfectivo|[CambioEfectivo](#schemacambioefectivo)|false|none||none|

<h2 id="tocS_CambioEfectivo">CambioEfectivo</h2>

<a id="schemacambioefectivo"></a>
<a id="schema_CambioEfectivo"></a>
<a id="tocScambioefectivo"></a>
<a id="tocscambioefectivo"></a>

```json
{
  "fechaCreado": "26-04-2024 12:37:36",
  "creadoPor": "string",
  "fechaModificado": "26-04-2024 12:37:36",
  "modificadoPor": "string",
  "id": 0,
  "efectivo": 0,
  "cambio": 0
}

```

### Attribute

|Name|Type|Required|Restrictions|Title|Description|
|---|---|---|---|---|---|
|fechaCreado|string|false|none||none|
|creadoPor|string|false|none||none|
|fechaModificado|string|false|none||none|
|modificadoPor|string|false|none||none|
|id|integer(int64)|false|none||none|
|efectivo|number(double)|false|none||none|
|cambio|number(double)|false|none||none|

<h2 id="tocS_TransaccionPasarela">TransaccionPasarela</h2>

<a id="schematransaccionpasarela"></a>
<a id="schema_TransaccionPasarela"></a>
<a id="tocStransaccionpasarela"></a>
<a id="tocstransaccionpasarela"></a>

```json
{
  "fechaCreado": "26-04-2024 12:37:36",
  "creadoPor": "string",
  "fechaModificado": "26-04-2024 12:37:36",
  "modificadoPor": "string",
  "id": "1c8356b0e24442b2acc579cf1ae4d8145",
  "reservaId": "755864a6-0c1f-4f32-9c54-7fb38f9dd9b1",
  "tipoIdentificacionCliente": "CC",
  "numeroIdentificacionCliente": "1111111111",
  "valor": 50000,
  "origen": "Origen X",
  "ip": "192.168.1.1",
  "metodoPago": {
    "fechaCreado": "26-04-2024 12:37:36",
    "creadoPor": "string",
    "fechaModificado": "26-04-2024 12:37:36",
    "modificadoPor": "string",
    "id": 1,
    "nombre": "Metodo de pago A",
    "cuentaDestino": "1111444499997777",
    "tipo": "ELECTRONICO",
    "requiereDatosAutorizacion": false,
    "recepcionesPago": [
      {
        "fechaCreado": "26-04-2024 12:37:36",
        "creadoPor": "string",
        "fechaModificado": "26-04-2024 12:37:36",
        "modificadoPor": "string",
        "id": 0,
        "recepcionPago": "TAQUILLA",
        "metodoPago": {
          "fechaCreado": "[",
          "creadoPor": "string",
          "fechaModificado": "[",
          "modificadoPor": "string",
          "id": "[",
          "nombre": "[",
          "cuentaDestino": "[",
          "tipo": "[",
          "requiereDatosAutorizacion": "[",
          "recepcionesPago": [
            null
          ],
          "estado": "["
        }
      }
    ],
    "estado": "ACTIVO"
  },
  "fechaHoraInicio": "26-04-2024 12:37:36",
  "fechaHoraFin": "26-04-2024 12:37:36",
  "estado": "EN_PROCESO"
}

```

### Attribute

|Name|Type|Required|Restrictions|Title|Description|
|---|---|---|---|---|---|
|fechaCreado|string|false|none||none|
|creadoPor|string|false|none||none|
|fechaModificado|string|false|none||none|
|modificadoPor|string|false|none||none|
|id|string|false|none||id de la transaccion de pago|
|reservaId|string(uuid)|false|none||id de la reserva asociada a esta transaccion|
|tipoIdentificacionCliente|string|false|none||tipo de identificacion del cliente|
|numeroIdentificacionCliente|string|false|none||numero de identificacion del cliente|
|valor|number(double)|false|none||valor de la transaccion|
|origen|string|false|none||origen de la transaccion|
|ip|string|false|none||direccion ip del cliente asociado con esta transaccion|
|metodoPago|[MetodoPago](#schemametodopago)|false|none||none|
|fechaHoraInicio|string|false|none||fecha y hora de inicio de la transaccion|
|fechaHoraFin|string|false|none||fecha y hora de finalizacion de la transaccion|
|estado|string|false|none||estado de la transaccion|

#### Enum

|Name|Value|
|---|---|
|tipoIdentificacionCliente|CC|
|tipoIdentificacionCliente|NIT|
|tipoIdentificacionCliente|CE|
|tipoIdentificacionCliente|PAS|
|tipoIdentificacionCliente|TI|
|tipoIdentificacionCliente|RC|
|tipoIdentificacionCliente|DNI|
|estado|APROBADO|
|estado|EN_PROCESO|
|estado|CANCELADO|
|estado|RECHAZADO|

<h2 id="tocS_TransaccionTaquilla">TransaccionTaquilla</h2>

<a id="schematransacciontaquilla"></a>
<a id="schema_TransaccionTaquilla"></a>
<a id="tocStransacciontaquilla"></a>
<a id="tocstransacciontaquilla"></a>

```json
{
  "fechaCreado": "26-04-2024 12:37:36",
  "creadoPor": "string",
  "fechaModificado": "26-04-2024 12:37:36",
  "modificadoPor": "string",
  "id": "b169240e-56b1-4e38-8c50-279c8a04e5aa",
  "reservaId": "dd36d635-3836-499b-b9e8-a21f7b8f8d99",
  "metodoPago": {
    "fechaCreado": "26-04-2024 12:37:36",
    "creadoPor": "string",
    "fechaModificado": "26-04-2024 12:37:36",
    "modificadoPor": "string",
    "id": 1,
    "nombre": "Metodo de pago A",
    "cuentaDestino": "1111444499997777",
    "tipo": "ELECTRONICO",
    "requiereDatosAutorizacion": false,
    "recepcionesPago": [
      {
        "fechaCreado": "26-04-2024 12:37:36",
        "creadoPor": "string",
        "fechaModificado": "26-04-2024 12:37:36",
        "modificadoPor": "string",
        "id": 0,
        "recepcionPago": "TAQUILLA",
        "metodoPago": {
          "fechaCreado": "[",
          "creadoPor": "string",
          "fechaModificado": "[",
          "modificadoPor": "string",
          "id": "[",
          "nombre": "[",
          "cuentaDestino": "[",
          "tipo": "[",
          "requiereDatosAutorizacion": "[",
          "recepcionesPago": [
            null
          ],
          "estado": "["
        }
      }
    ],
    "estado": "ACTIVO"
  },
  "valor": 50000,
  "numeroAutorizacion": "00032325",
  "ultimosDigitos": "4488",
  "registroTaquillaId": "aded13d6-1970-4003-aa21-1f29fc5692a9",
  "cambioEfectivo": {
    "fechaCreado": "26-04-2024 12:37:36",
    "creadoPor": "string",
    "fechaModificado": "26-04-2024 12:37:36",
    "modificadoPor": "string",
    "id": 0,
    "efectivo": 0,
    "cambio": 0
  },
  "reciboTaquillaNumero": 0,
  "taquillaId": 0,
  "taquillaNombre": "string"
}

```

### Attribute

|Name|Type|Required|Restrictions|Title|Description|
|---|---|---|---|---|---|
|fechaCreado|string|false|none||none|
|creadoPor|string|false|none||none|
|fechaModificado|string|false|none||none|
|modificadoPor|string|false|none||none|
|id|string(uuid)|false|none||id del pago|
|reservaId|string(uuid)|false|none||none|
|metodoPago|[MetodoPago](#schemametodopago)|false|none||none|
|valor|number(double)|false|none||valor del pago|
|numeroAutorizacion|string|false|none||numero de autorizacion del pago|
|ultimosDigitos|string|false|none||ultimos digitos del metodo de pago|
|registroTaquillaId|string(uuid)|false|none||none|
|cambioEfectivo|[CambioEfectivo](#schemacambioefectivo)|false|none||none|
|reciboTaquillaNumero|integer(int64)|false|none||none|
|taquillaId|integer(int64)|false|none||none|
|taquillaNombre|string|false|none||none|

<h2 id="tocS_MetodoPago">MetodoPago</h2>

<a id="schemametodopago"></a>
<a id="schema_MetodoPago"></a>
<a id="tocSmetodopago"></a>
<a id="tocsmetodopago"></a>

```json
{
  "fechaCreado": "26-04-2024 12:37:36",
  "creadoPor": "string",
  "fechaModificado": "26-04-2024 12:37:36",
  "modificadoPor": "string",
  "id": 1,
  "nombre": "Metodo de pago A",
  "cuentaDestino": "1111444499997777",
  "tipo": "ELECTRONICO",
  "requiereDatosAutorizacion": false,
  "recepcionesPago": [
    {
      "fechaCreado": "26-04-2024 12:37:36",
      "creadoPor": "string",
      "fechaModificado": "26-04-2024 12:37:36",
      "modificadoPor": "string",
      "id": 0,
      "recepcionPago": "TAQUILLA",
      "metodoPago": {
        "fechaCreado": "26-04-2024 12:37:36",
        "creadoPor": "string",
        "fechaModificado": "26-04-2024 12:37:36",
        "modificadoPor": "string",
        "id": 1,
        "nombre": "Metodo de pago A",
        "cuentaDestino": "1111444499997777",
        "tipo": "ELECTRONICO",
        "requiereDatosAutorizacion": false,
        "recepcionesPago": [
          {
            "fechaCreado": null,
            "creadoPor": null,
            "fechaModificado": null,
            "modificadoPor": null,
            "id": null,
            "recepcionPago": null,
            "metodoPago": null
          }
        ],
        "estado": "ACTIVO"
      }
    }
  ],
  "estado": "ACTIVO"
}

```

### Attribute

|Name|Type|Required|Restrictions|Title|Description|
|---|---|---|---|---|---|
|fechaCreado|string|false|none||none|
|creadoPor|string|false|none||none|
|fechaModificado|string|false|none||none|
|modificadoPor|string|false|none||none|
|id|integer(int64)|false|none||id del metodo de pago|
|nombre|string|false|none||nombre del metodo de pago|
|cuentaDestino|string|false|none||cuenta destino a la cual se transfieren los pago realizados|
|tipo|string|false|none||tipo de metodo de pago|
|requiereDatosAutorizacion|boolean|false|none||el metodo de pago requiere datos de autorizacion (si/no)|
|recepcionesPago|[[MetodoPagoRecepcionPago](#schemametodopagorecepcionpago)]|false|none||none|
|estado|string|false|none||estado del metodo de pago|

#### Enum

|Name|Value|
|---|---|
|tipo|EFECTIVO|
|tipo|ELECTRONICO|
|tipo|DATAFONO|
|estado|ACTIVO|
|estado|INACTIVO|

<h2 id="tocS_MetodoPagoRecepcionPago">MetodoPagoRecepcionPago</h2>

<a id="schemametodopagorecepcionpago"></a>
<a id="schema_MetodoPagoRecepcionPago"></a>
<a id="tocSmetodopagorecepcionpago"></a>
<a id="tocsmetodopagorecepcionpago"></a>

```json
{
  "fechaCreado": "26-04-2024 12:37:36",
  "creadoPor": "string",
  "fechaModificado": "26-04-2024 12:37:36",
  "modificadoPor": "string",
  "id": 0,
  "recepcionPago": "TAQUILLA",
  "metodoPago": {
    "fechaCreado": "26-04-2024 12:37:36",
    "creadoPor": "string",
    "fechaModificado": "26-04-2024 12:37:36",
    "modificadoPor": "string",
    "id": 1,
    "nombre": "Metodo de pago A",
    "cuentaDestino": "1111444499997777",
    "tipo": "ELECTRONICO",
    "requiereDatosAutorizacion": false,
    "recepcionesPago": [
      {
        "fechaCreado": "26-04-2024 12:37:36",
        "creadoPor": "string",
        "fechaModificado": "26-04-2024 12:37:36",
        "modificadoPor": "string",
        "id": 0,
        "recepcionPago": "TAQUILLA",
        "metodoPago": {
          "fechaCreado": "[",
          "creadoPor": "string",
          "fechaModificado": "[",
          "modificadoPor": "string",
          "id": "[",
          "nombre": "[",
          "cuentaDestino": "[",
          "tipo": "[",
          "requiereDatosAutorizacion": "[",
          "recepcionesPago": [
            null
          ],
          "estado": "["
        }
      }
    ],
    "estado": "ACTIVO"
  }
}

```

### Attribute

|Name|Type|Required|Restrictions|Title|Description|
|---|---|---|---|---|---|
|fechaCreado|string|false|none||none|
|creadoPor|string|false|none||none|
|fechaModificado|string|false|none||none|
|modificadoPor|string|false|none||none|
|id|integer(int64)|false|none||none|
|recepcionPago|string|false|none||none|
|metodoPago|[MetodoPago](#schemametodopago)|false|none||none|

#### Enum

|Name|Value|
|---|---|
|recepcionPago|TAQUILLA|
|recepcionPago|PASARELA|
|recepcionPago|PARTNER|
|recepcionPago|PARQUEADERO|

<h2 id="tocS_DetalleVentaProducto">DetalleVentaProducto</h2>

<a id="schemadetalleventaproducto"></a>
<a id="schema_DetalleVentaProducto"></a>
<a id="tocSdetalleventaproducto"></a>
<a id="tocsdetalleventaproducto"></a>

```json
{
  "fechaCreado": "26-04-2024 12:37:36",
  "creadoPor": "string",
  "fechaModificado": "26-04-2024 12:37:36",
  "modificadoPor": "string",
  "id": 0,
  "clienteTipoIdentificacion": "CC",
  "clienteNumeroIdentificacion": "1111222333",
  "clienteNombre": "Nombre 1 Nombre 2 Apellido 1 Apellido 2",
  "reservaId": "dd36d635-3836-499b-b9e8-a21f7b8f8d99",
  "productoId": "facf4a34-c5cd-4888-bb4d-b65af8ae4dd9",
  "productoCodigo": "string",
  "productoTipo": "BOLETA",
  "productoNombre": "string",
  "productoValor": 0,
  "descuentoValor": 0,
  "valor": 0,
  "boletaId": "1bdd62d6-cfe6-46e0-9d28-6efc9e2d97ee",
  "reservaCasillaId": "ffa80c2d-a380-4e24-8b51-81cc376fde36",
  "reservaVehiculoId": "e3e6894b-2f0a-4368-ab7e-d7263f01cea3",
  "espacioParqueaderoId": 0,
  "reservaServicioAdicionalId": "e2db60eb-fe50-40b8-8bf7-7fd2f4953292",
  "reservaComboId": "b5015fcd-c071-4677-a321-3ff1e45a389a",
  "descuento": {
    "fechaCreado": "26-04-2024 12:37:36",
    "creadoPor": "string",
    "fechaModificado": "26-04-2024 12:37:36",
    "modificadoPor": "string",
    "id": "6ae369b6-847e-446a-a096-06e589c63db7",
    "nombre": "Descuento A",
    "tiposProducto": [
      {
        "fechaCreado": "26-04-2024 12:37:36",
        "creadoPor": "string",
        "fechaModificado": "26-04-2024 12:37:36",
        "modificadoPor": "string",
        "tipoProducto": "BOLETA",
        "cantidadMax": 0
      }
    ],
    "aplicarConCodigo": true,
    "codigo": "D1AHF524A0",
    "aplicarConVigencia": true,
    "vigenciaInicio": "26-04-2024 12:37:36",
    "vigenciaFin": "26-04-2024 12:37:36",
    "tipo": "PORCENTAJE",
    "valor": 20,
    "consumoMax": 100,
    "consumoMaxCliente": 1,
    "consumo": 5,
    "estado": "ACTIVO",
    "clientesObjetivo": true,
    "clientesCompraronEnFechas": true,
    "ccefFechaInicio": "26-04-2024 12:37:36",
    "ccefFechaFin": "26-04-2024 12:37:36",
    "clientesEspecificos": false
  },
  "estadoPago": "APROBADO",
  "reservaFecha": "26-04-2024"
}

```

detalles de productos vendidos en la venta

### Attribute

|Name|Type|Required|Restrictions|Title|Description|
|---|---|---|---|---|---|
|fechaCreado|string|false|none||none|
|creadoPor|string|false|none||none|
|fechaModificado|string|false|none||none|
|modificadoPor|string|false|none||none|
|id|integer(int64)|false|none||none|
|clienteTipoIdentificacion|string|false|none||tipo de identificacion del cliente|
|clienteNumeroIdentificacion|string|false|none||numero de identificacion del cliente|
|clienteNombre|string|false|none||nombre completo del cliente|
|reservaId|string(uuid)|false|none||none|
|productoId|string(uuid)|false|none||none|
|productoCodigo|string|false|none||none|
|productoTipo|string|false|none||none|
|productoNombre|string|false|none||none|
|productoValor|number(double)|false|none||none|
|descuentoValor|number(double)|false|none||none|
|valor|number(double)|false|none||none|
|boletaId|string(uuid)|false|none||none|
|reservaCasillaId|string(uuid)|false|none||none|
|reservaVehiculoId|string(uuid)|false|none||none|
|espacioParqueaderoId|integer(int64)|false|none||none|
|reservaServicioAdicionalId|string(uuid)|false|none||none|
|reservaComboId|string(uuid)|false|none||none|
|descuento|[Descuento](#schemadescuento)|false|none||descuento asociado con esta reserva|
|estadoPago|string|false|none||none|
|reservaFecha|string|false|none||none|

#### Enum

|Name|Value|
|---|---|
|clienteTipoIdentificacion|CC|
|clienteTipoIdentificacion|NIT|
|clienteTipoIdentificacion|CE|
|clienteTipoIdentificacion|PAS|
|clienteTipoIdentificacion|TI|
|clienteTipoIdentificacion|RC|
|clienteTipoIdentificacion|DNI|
|productoTipo|BOLETA|
|productoTipo|PARQUEADERO|
|productoTipo|CASILLA|
|productoTipo|SERVICIO_ADICIONAL|
|productoTipo|COMBO|
|estadoPago|APROBADO|
|estadoPago|PENDIENTE|
|estadoPago|ANULADO|

<h2 id="tocS_ReciboTaquilla">ReciboTaquilla</h2>

<a id="schemarecibotaquilla"></a>
<a id="schema_ReciboTaquilla"></a>
<a id="tocSrecibotaquilla"></a>
<a id="tocsrecibotaquilla"></a>

```json
{
  "fechaCreado": "26-04-2024 12:37:36",
  "creadoPor": "string",
  "fechaModificado": "26-04-2024 12:37:36",
  "modificadoPor": "string",
  "id": 0,
  "numero": 0,
  "ultimoRegistroImpresion": {
    "fechaCreado": "26-04-2024 12:37:36",
    "creadoPor": "string",
    "fechaModificado": "26-04-2024 12:37:36",
    "modificadoPor": "string",
    "id": 0,
    "tipoImpresion": "MANILLA",
    "impresora": {
      "fechaCreado": "26-04-2024 12:37:36",
      "creadoPor": "string",
      "fechaModificado": "26-04-2024 12:37:36",
      "modificadoPor": "string",
      "id": 0,
      "nombre": "string",
      "direccionIp": "string",
      "estado": "ACTIVO",
      "marca": "ZEBRA",
      "referencia": "string",
      "serial": "string",
      "tipoImpresora": "IMPRESORA_MANILLAS"
    },
    "identificador": "string",
    "estado": "EXITOSO",
    "mensajeError": "Error"
  }
}

```

recibo de taquilla asociado a esta venta

### Attribute

|Name|Type|Required|Restrictions|Title|Description|
|---|---|---|---|---|---|
|fechaCreado|string|false|none||none|
|creadoPor|string|false|none||none|
|fechaModificado|string|false|none||none|
|modificadoPor|string|false|none||none|
|id|integer(int64)|false|none||none|
|numero|integer(int64)|false|none||none|
|ultimoRegistroImpresion|[RegistroImpresion](#schemaregistroimpresion)|false|none||none|

<h2 id="tocS_RegistroImpresion">RegistroImpresion</h2>

<a id="schemaregistroimpresion"></a>
<a id="schema_RegistroImpresion"></a>
<a id="tocSregistroimpresion"></a>
<a id="tocsregistroimpresion"></a>

```json
{
  "fechaCreado": "26-04-2024 12:37:36",
  "creadoPor": "string",
  "fechaModificado": "26-04-2024 12:37:36",
  "modificadoPor": "string",
  "id": 0,
  "tipoImpresion": "MANILLA",
  "impresora": {
    "fechaCreado": "26-04-2024 12:37:36",
    "creadoPor": "string",
    "fechaModificado": "26-04-2024 12:37:36",
    "modificadoPor": "string",
    "id": 0,
    "nombre": "string",
    "direccionIp": "string",
    "estado": "ACTIVO",
    "marca": "ZEBRA",
    "referencia": "string",
    "serial": "string",
    "tipoImpresora": "IMPRESORA_MANILLAS"
  },
  "identificador": "string",
  "estado": "EXITOSO",
  "mensajeError": "Error"
}

```

### Attribute

|Name|Type|Required|Restrictions|Title|Description|
|---|---|---|---|---|---|
|fechaCreado|string|false|none||none|
|creadoPor|string|false|none||none|
|fechaModificado|string|false|none||none|
|modificadoPor|string|false|none||none|
|id|integer(int64)|false|none||none|
|tipoImpresion|string|false|none||tipo de impresion|
|impresora|[Impresora](#schemaimpresora)|false|none||impresoras asignadas a una taquilla|
|identificador|string|false|none||none|
|estado|string|false|none||estado de impresion|
|mensajeError|string|false|none||mesaje de error de una impresion fallida|

#### Enum

|Name|Value|
|---|---|
|tipoImpresion|BOLETA_PERSONAL|
|tipoImpresion|BOLETA_GENERAL|
|tipoImpresion|MANILLA|
|estado|EXITOSO|
|estado|FALLIDO|

<h2 id="tocS_ImageBase64Response">ImageBase64Response</h2>

<a id="schemaimagebase64response"></a>
<a id="schema_ImageBase64Response"></a>
<a id="tocSimagebase64response"></a>
<a id="tocsimagebase64response"></a>

```json
{
  "mimeType": "string",
  "imageBase64": "/9j/4AAQSkZJRgABAgAAAQABAAD/7QCEUGhvdG9zaG9wIDMuMAA4QklNBAQAAAAAAGccAigAYkZCTUQwMTAwMGFhNjAzMDAwMDY5MD"
}

```

### Attribute

|Name|Type|Required|Restrictions|Title|Description|
|---|---|---|---|---|---|
|mimeType|string|false|none||mimetype de la imagen|
|imageBase64|string|false|none||datos binarios de la imagen en base64|

<h2 id="tocS_Partner">Partner</h2>

<a id="schemapartner"></a>
<a id="schema_Partner"></a>
<a id="tocSpartner"></a>
<a id="tocspartner"></a>

```json
{
  "fechaCreado": "26-04-2024 12:37:36",
  "creadoPor": "string",
  "fechaModificado": "26-04-2024 12:37:36",
  "modificadoPor": "string",
  "id": "e3617a05-6e65-433f-b0db-c2a8747f3314",
  "nombre": "Partner 1",
  "boletasMax": 0,
  "boletasRest": 0,
  "account": {
    "fechaCreado": "26-04-2024 12:37:36",
    "creadoPor": "string",
    "fechaModificado": "26-04-2024 12:37:36",
    "modificadoPor": "string",
    "id": "23d4c71f-dc56-4d1e-b2b0-d64110d778ca",
    "name": "admin",
    "email": "example@email.com",
    "role": {
      "fechaCreado": "26-04-2024 12:37:36",
      "creadoPor": "string",
      "fechaModificado": "26-04-2024 12:37:36",
      "modificadoPor": "string",
      "id": 1,
      "name": "ADMIN",
      "urlInicio": "/index.html",
      "menus": [
        {
          "fechaCreado": "[",
          "creadoPor": "string",
          "fechaModificado": "[",
          "modificadoPor": "string",
          "role": {},
          "menu": {}
        }
      ],
      "estado": "ADMIN"
    },
    "estado": "ACTIVO"
  },
  "canal": {
    "fechaCreado": "26-04-2024 12:37:36",
    "creadoPor": "string",
    "fechaModificado": "26-04-2024 12:37:36",
    "modificadoPor": "string",
    "id": 1,
    "nombre": "Canal A"
  },
  "tarifas": [
    {
      "id": 1,
      "nombre": "TARIFA 1",
      "tipoBoleta": {
        "fechaCreado": "26-04-2024 12:37:36",
        "creadoPor": "string",
        "fechaModificado": "26-04-2024 12:37:36",
        "modificadoPor": "string",
        "id": 1,
        "producto": {
          "fechaCreado": "[",
          "creadoPor": "string",
          "fechaModificado": "[",
          "modificadoPor": "string",
          "id": "[",
          "codigo": "string",
          "nombre": "[",
          "descripcion": "[",
          "valorVariable": true,
          "valor": "[",
          "imagenId": "[",
          "tipo": "[",
          "productosCombo": [
            null
          ],
          "ventaFechaInicio": "[",
          "ventaFechaFin": "[",
          "consumoFechaInicio": "[",
          "consumoFechaFin": "[",
          "excepcionesDiasSemana": [
            null
          ],
          "activacionDesactivacionAutomatica": true
        },
        "categoriaEdad": {
          "fechaCreado": "[",
          "creadoPor": "string",
          "fechaModificado": "[",
          "modificadoPor": "string",
          "id": "[",
          "nombre": "[",
          "edadInicial": "[",
          "edadFinal": "["
        },
        "categoriaEstatura": {
          "fechaCreado": "[",
          "creadoPor": "string",
          "fechaModificado": "[",
          "modificadoPor": "string",
          "id": "[",
          "nombre": "[",
          "estaturaCmMin": "[",
          "estaturaCmMax": "["
        },
        "hikcentralPrivilegeGroupId": "1"
      }
    }
  ],
  "estado": "INACTIVO"
}

```

### Attribute

|Name|Type|Required|Restrictions|Title|Description|
|---|---|---|---|---|---|
|fechaCreado|string|false|none||none|
|creadoPor|string|false|none||none|
|fechaModificado|string|false|none||none|
|modificadoPor|string|false|none||none|
|id|string(uuid)|false|none||id del partner|
|nombre|string|false|none||nombre del partner|
|boletasMax|integer(int64)|false|none||numero de boletas maximo que puede vender el partner|
|boletasRest|integer(int64)|false|none||numero de boletas restantes que puede vender el partner|
|account|[Account](#schemaaccount)|false|none||none|
|canal|[Canal](#schemacanal)|false|none||canal asociado con esta reserva|
|tarifas|[[PartnerTarifa](#schemapartnertarifa)]|false|none||[tarifas de boletas asociadas a este partner]|
|estado|string|false|none||none|

#### Enum

|Name|Value|
|---|---|
|estado|INACTIVO|
|estado|ACTIVO|

<h2 id="tocS_PartnerTarifa">PartnerTarifa</h2>

<a id="schemapartnertarifa"></a>
<a id="schema_PartnerTarifa"></a>
<a id="tocSpartnertarifa"></a>
<a id="tocspartnertarifa"></a>

```json
{
  "id": 1,
  "nombre": "TARIFA 1",
  "tipoBoleta": {
    "fechaCreado": "26-04-2024 12:37:36",
    "creadoPor": "string",
    "fechaModificado": "26-04-2024 12:37:36",
    "modificadoPor": "string",
    "id": 1,
    "producto": {
      "fechaCreado": "26-04-2024 12:37:36",
      "creadoPor": "string",
      "fechaModificado": "26-04-2024 12:37:36",
      "modificadoPor": "string",
      "id": "6c872a0f-4e21-460a-ae3d-2f3994f73dc6",
      "codigo": "string",
      "nombre": "Producto A",
      "descripcion": "Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua",
      "valorVariable": true,
      "valor": 30000,
      "imagenId": "644176ac-41f6-48ac-a4ef-3db5eb09fbf9",
      "tipo": "BOLETA",
      "productosCombo": [
        {
          "fechaCreado": "[",
          "creadoPor": "string",
          "fechaModificado": "[",
          "modificadoPor": "string",
          "producto": {},
          "cantidad": 0
        }
      ],
      "ventaFechaInicio": "26-04-2024",
      "ventaFechaFin": "26-04-2024",
      "consumoFechaInicio": "26-04-2024",
      "consumoFechaFin": "26-04-2024",
      "excepcionesDiasSemana": [
        {
          "id": 0,
          "tipo": "[",
          "lunes": true,
          "martes": true,
          "miercoles": true,
          "jueves": true,
          "viernes": true,
          "sabado": true,
          "domingo": true
        }
      ],
      "activacionDesactivacionAutomatica": true
    },
    "categoriaEdad": {
      "fechaCreado": "26-04-2024 12:37:36",
      "creadoPor": "string",
      "fechaModificado": "26-04-2024 12:37:36",
      "modificadoPor": "string",
      "id": 1,
      "nombre": "Categoria de edad A",
      "edadInicial": 8,
      "edadFinal": 60
    },
    "categoriaEstatura": {
      "fechaCreado": "26-04-2024 12:37:36",
      "creadoPor": "string",
      "fechaModificado": "26-04-2024 12:37:36",
      "modificadoPor": "string",
      "id": 1,
      "nombre": "Categoria de estatura A",
      "estaturaCmMin": 120,
      "estaturaCmMax": 180
    },
    "hikcentralPrivilegeGroupId": "1"
  }
}

```

tarifas de boletas asociadas a este partner

### Attribute

|Name|Type|Required|Restrictions|Title|Description|
|---|---|---|---|---|---|
|id|integer(int64)|false|none||id de la tarifa del partner|
|nombre|string|false|none||nombre de la tarifa del partner|
|tipoBoleta|[TipoBoleta](#schematipoboleta)|false|none||tipo de boleta|

<h2 id="tocS_Account">Account</h2>

<a id="schemaaccount"></a>
<a id="schema_Account"></a>
<a id="tocSaccount"></a>
<a id="tocsaccount"></a>

```json
{
  "fechaCreado": "26-04-2024 12:37:36",
  "creadoPor": "string",
  "fechaModificado": "26-04-2024 12:37:36",
  "modificadoPor": "string",
  "id": "23d4c71f-dc56-4d1e-b2b0-d64110d778ca",
  "name": "admin",
  "email": "example@email.com",
  "role": {
    "fechaCreado": "26-04-2024 12:37:36",
    "creadoPor": "string",
    "fechaModificado": "26-04-2024 12:37:36",
    "modificadoPor": "string",
    "id": 1,
    "name": "ADMIN",
    "urlInicio": "/index.html",
    "menus": [
      {
        "fechaCreado": "26-04-2024 12:37:36",
        "creadoPor": "string",
        "fechaModificado": "26-04-2024 12:37:36",
        "modificadoPor": "string",
        "role": {
          "fechaCreado": "[",
          "creadoPor": "string",
          "fechaModificado": "[",
          "modificadoPor": "string",
          "id": "[",
          "name": "[",
          "urlInicio": "[",
          "menus": [
            null
          ],
          "estado": "["
        },
        "menu": {
          "fechaCreado": "[",
          "creadoPor": "string",
          "fechaModificado": "[",
          "modificadoPor": "string",
          "id": "[",
          "nombre": "[",
          "menuInfo": {},
          "menuPadre": {},
          "menus": [
            null
          ],
          "estado": "["
        }
      }
    ],
    "estado": "ADMIN"
  },
  "estado": "ACTIVO"
}

```

### Attribute

|Name|Type|Required|Restrictions|Title|Description|
|---|---|---|---|---|---|
|fechaCreado|string|false|none||none|
|creadoPor|string|false|none||none|
|fechaModificado|string|false|none||none|
|modificadoPor|string|false|none||none|
|id|string(uuid)|false|none||id del usuario|
|name|string|false|none||nombre del usuario|
|email|string|false|none||direccion de correo electronico del usuario|
|role|[Role](#schemarole)|false|none||rol del usuario|
|estado|string|false|none||estado del usuario|

#### Enum

|Name|Value|
|---|---|
|estado|ACTIVO|
|estado|INACTIVO|

<h2 id="tocS_Role">Role</h2>

<a id="schemarole"></a>
<a id="schema_Role"></a>
<a id="tocSrole"></a>
<a id="tocsrole"></a>

```json
{
  "fechaCreado": "26-04-2024 12:37:36",
  "creadoPor": "string",
  "fechaModificado": "26-04-2024 12:37:36",
  "modificadoPor": "string",
  "id": 1,
  "name": "ADMIN",
  "urlInicio": "/index.html",
  "menus": [
    {
      "fechaCreado": "26-04-2024 12:37:36",
      "creadoPor": "string",
      "fechaModificado": "26-04-2024 12:37:36",
      "modificadoPor": "string",
      "role": {
        "fechaCreado": "26-04-2024 12:37:36",
        "creadoPor": "string",
        "fechaModificado": "26-04-2024 12:37:36",
        "modificadoPor": "string",
        "id": 1,
        "name": "ADMIN",
        "urlInicio": "/index.html",
        "menus": [
          {
            "fechaCreado": null,
            "creadoPor": null,
            "fechaModificado": null,
            "modificadoPor": null,
            "role": null,
            "menu": null
          }
        ],
        "estado": "ADMIN"
      },
      "menu": {
        "fechaCreado": "26-04-2024 12:37:36",
        "creadoPor": "string",
        "fechaModificado": "26-04-2024 12:37:36",
        "modificadoPor": "string",
        "id": 1,
        "nombre": "Menu A",
        "menuInfo": {
          "url": "[",
          "imagenId": "["
        },
        "menuPadre": {
          "fechaCreado": "[",
          "creadoPor": "string",
          "fechaModificado": "[",
          "modificadoPor": "string",
          "id": "[",
          "nombre": "[",
          "menuInfo": {},
          "menuPadre": {},
          "menus": [
            null
          ],
          "estado": "["
        },
        "menus": [
          {
            "fechaCreado": null,
            "creadoPor": null,
            "fechaModificado": null,
            "modificadoPor": null,
            "id": null,
            "nombre": null,
            "menuInfo": null,
            "menuPadre": null,
            "menus": null,
            "estado": null
          }
        ],
        "estado": "ACTIVO"
      }
    }
  ],
  "estado": "ADMIN"
}

```

rol del usuario

### Attribute

|Name|Type|Required|Restrictions|Title|Description|
|---|---|---|---|---|---|
|fechaCreado|string|false|none||none|
|creadoPor|string|false|none||none|
|fechaModificado|string|false|none||none|
|modificadoPor|string|false|none||none|
|id|integer(int64)|false|none||id del rol|
|name|string|false|none||nombre del rol|
|urlInicio|string|false|none||url del inicio del rol|
|menus|[[RoleMenu](#schemarolemenu)]|false|none||[menus asociados con este rol]|
|estado|string|false|none||estado del rol|

#### Enum

|Name|Value|
|---|---|
|estado|ACTIVO|
|estado|INACTIVO|

<h2 id="tocS_RoleMenu">RoleMenu</h2>

<a id="schemarolemenu"></a>
<a id="schema_RoleMenu"></a>
<a id="tocSrolemenu"></a>
<a id="tocsrolemenu"></a>

```json
{
  "fechaCreado": "26-04-2024 12:37:36",
  "creadoPor": "string",
  "fechaModificado": "26-04-2024 12:37:36",
  "modificadoPor": "string",
  "role": {
    "fechaCreado": "26-04-2024 12:37:36",
    "creadoPor": "string",
    "fechaModificado": "26-04-2024 12:37:36",
    "modificadoPor": "string",
    "id": 1,
    "name": "ADMIN",
    "urlInicio": "/index.html",
    "menus": [
      {
        "fechaCreado": "26-04-2024 12:37:36",
        "creadoPor": "string",
        "fechaModificado": "26-04-2024 12:37:36",
        "modificadoPor": "string",
        "role": {
          "fechaCreado": "[",
          "creadoPor": "string",
          "fechaModificado": "[",
          "modificadoPor": "string",
          "id": "[",
          "name": "[",
          "urlInicio": "[",
          "menus": [
            null
          ],
          "estado": "["
        },
        "menu": {
          "fechaCreado": "[",
          "creadoPor": "string",
          "fechaModificado": "[",
          "modificadoPor": "string",
          "id": "[",
          "nombre": "[",
          "menuInfo": {},
          "menuPadre": {},
          "menus": [
            null
          ],
          "estado": "["
        }
      }
    ],
    "estado": "ADMIN"
  },
  "menu": {
    "fechaCreado": "26-04-2024 12:37:36",
    "creadoPor": "string",
    "fechaModificado": "26-04-2024 12:37:36",
    "modificadoPor": "string",
    "id": 1,
    "nombre": "Menu A",
    "menuInfo": {
      "url": "/menuA/index.html",
      "imagenId": "151c0a1d-fccd-4ead-ae4b-f05a26d3779b"
    },
    "menuPadre": {
      "fechaCreado": "26-04-2024 12:37:36",
      "creadoPor": "string",
      "fechaModificado": "26-04-2024 12:37:36",
      "modificadoPor": "string",
      "id": 1,
      "nombre": "Menu A",
      "menuInfo": {
        "url": "/menuA/index.html",
        "imagenId": "151c0a1d-fccd-4ead-ae4b-f05a26d3779b"
      },
      "menuPadre": {
        "fechaCreado": "26-04-2024 12:37:36",
        "creadoPor": "string",
        "fechaModificado": "26-04-2024 12:37:36",
        "modificadoPor": "string",
        "id": 1,
        "nombre": "Menu A",
        "menuInfo": {
          "url": null,
          "imagenId": null
        },
        "menuPadre": {
          "fechaCreado": null,
          "creadoPor": null,
          "fechaModificado": null,
          "modificadoPor": null,
          "id": null,
          "nombre": null,
          "menuInfo": null,
          "menuPadre": null,
          "menus": null,
          "estado": null
        },
        "menus": [
          {}
        ],
        "estado": "ACTIVO"
      },
      "menus": [
        {
          "fechaCreado": "[",
          "creadoPor": "string",
          "fechaModificado": "[",
          "modificadoPor": "string",
          "id": "[",
          "nombre": "[",
          "menuInfo": {},
          "menuPadre": {},
          "menus": [
            null
          ],
          "estado": "["
        }
      ],
      "estado": "ACTIVO"
    },
    "menus": [
      {
        "fechaCreado": "26-04-2024 12:37:36",
        "creadoPor": "string",
        "fechaModificado": "26-04-2024 12:37:36",
        "modificadoPor": "string",
        "id": 1,
        "nombre": "Menu A",
        "menuInfo": {
          "url": "[",
          "imagenId": "["
        },
        "menuPadre": {
          "fechaCreado": "[",
          "creadoPor": "string",
          "fechaModificado": "[",
          "modificadoPor": "string",
          "id": "[",
          "nombre": "[",
          "menuInfo": {},
          "menuPadre": {},
          "menus": [
            null
          ],
          "estado": "["
        },
        "menus": [
          {
            "fechaCreado": null,
            "creadoPor": null,
            "fechaModificado": null,
            "modificadoPor": null,
            "id": null,
            "nombre": null,
            "menuInfo": null,
            "menuPadre": null,
            "menus": null,
            "estado": null
          }
        ],
        "estado": "ACTIVO"
      }
    ],
    "estado": "ACTIVO"
  }
}

```

menus asociados con este rol

### Attribute

|Name|Type|Required|Restrictions|Title|Description|
|---|---|---|---|---|---|
|fechaCreado|string|false|none||none|
|creadoPor|string|false|none||none|
|fechaModificado|string|false|none||none|
|modificadoPor|string|false|none||none|
|role|[Role](#schemarole)|false|none||rol del usuario|
|menu|[Menu](#schemamenu)|false|none||none|

<h2 id="tocS_Menu">Menu</h2>

<a id="schemamenu"></a>
<a id="schema_Menu"></a>
<a id="tocSmenu"></a>
<a id="tocsmenu"></a>

```json
{
  "fechaCreado": "26-04-2024 12:37:36",
  "creadoPor": "string",
  "fechaModificado": "26-04-2024 12:37:36",
  "modificadoPor": "string",
  "id": 1,
  "nombre": "Menu A",
  "menuInfo": {
    "url": "/menuA/index.html",
    "imagenId": "151c0a1d-fccd-4ead-ae4b-f05a26d3779b"
  },
  "menuPadre": {
    "fechaCreado": "26-04-2024 12:37:36",
    "creadoPor": "string",
    "fechaModificado": "26-04-2024 12:37:36",
    "modificadoPor": "string",
    "id": 1,
    "nombre": "Menu A",
    "menuInfo": {
      "url": "/menuA/index.html",
      "imagenId": "151c0a1d-fccd-4ead-ae4b-f05a26d3779b"
    },
    "menuPadre": {
      "fechaCreado": "26-04-2024 12:37:36",
      "creadoPor": "string",
      "fechaModificado": "26-04-2024 12:37:36",
      "modificadoPor": "string",
      "id": 1,
      "nombre": "Menu A",
      "menuInfo": {
        "url": "/menuA/index.html",
        "imagenId": "151c0a1d-fccd-4ead-ae4b-f05a26d3779b"
      },
      "menuPadre": {
        "fechaCreado": "26-04-2024 12:37:36",
        "creadoPor": "string",
        "fechaModificado": "26-04-2024 12:37:36",
        "modificadoPor": "string",
        "id": 1,
        "nombre": "Menu A",
        "menuInfo": {
          "url": null,
          "imagenId": null
        },
        "menuPadre": {
          "fechaCreado": null,
          "creadoPor": null,
          "fechaModificado": null,
          "modificadoPor": null,
          "id": null,
          "nombre": null,
          "menuInfo": null,
          "menuPadre": null,
          "menus": null,
          "estado": null
        },
        "menus": [
          {}
        ],
        "estado": "ACTIVO"
      },
      "menus": [
        {
          "fechaCreado": "[",
          "creadoPor": "string",
          "fechaModificado": "[",
          "modificadoPor": "string",
          "id": "[",
          "nombre": "[",
          "menuInfo": {},
          "menuPadre": {},
          "menus": [
            null
          ],
          "estado": "["
        }
      ],
      "estado": "ACTIVO"
    },
    "menus": [
      {
        "fechaCreado": "26-04-2024 12:37:36",
        "creadoPor": "string",
        "fechaModificado": "26-04-2024 12:37:36",
        "modificadoPor": "string",
        "id": 1,
        "nombre": "Menu A",
        "menuInfo": {
          "url": "[",
          "imagenId": "["
        },
        "menuPadre": {
          "fechaCreado": "[",
          "creadoPor": "string",
          "fechaModificado": "[",
          "modificadoPor": "string",
          "id": "[",
          "nombre": "[",
          "menuInfo": {},
          "menuPadre": {},
          "menus": [
            null
          ],
          "estado": "["
        },
        "menus": [
          {
            "fechaCreado": null,
            "creadoPor": null,
            "fechaModificado": null,
            "modificadoPor": null,
            "id": null,
            "nombre": null,
            "menuInfo": null,
            "menuPadre": null,
            "menus": null,
            "estado": null
          }
        ],
        "estado": "ACTIVO"
      }
    ],
    "estado": "ACTIVO"
  },
  "menus": [
    {
      "fechaCreado": "26-04-2024 12:37:36",
      "creadoPor": "string",
      "fechaModificado": "26-04-2024 12:37:36",
      "modificadoPor": "string",
      "id": 1,
      "nombre": "Menu A",
      "menuInfo": {
        "url": "/menuA/index.html",
        "imagenId": "151c0a1d-fccd-4ead-ae4b-f05a26d3779b"
      },
      "menuPadre": {
        "fechaCreado": "26-04-2024 12:37:36",
        "creadoPor": "string",
        "fechaModificado": "26-04-2024 12:37:36",
        "modificadoPor": "string",
        "id": 1,
        "nombre": "Menu A",
        "menuInfo": {
          "url": "[",
          "imagenId": "["
        },
        "menuPadre": {
          "fechaCreado": "[",
          "creadoPor": "string",
          "fechaModificado": "[",
          "modificadoPor": "string",
          "id": "[",
          "nombre": "[",
          "menuInfo": {},
          "menuPadre": {},
          "menus": [
            null
          ],
          "estado": "["
        },
        "menus": [
          {
            "fechaCreado": null,
            "creadoPor": null,
            "fechaModificado": null,
            "modificadoPor": null,
            "id": null,
            "nombre": null,
            "menuInfo": null,
            "menuPadre": null,
            "menus": null,
            "estado": null
          }
        ],
        "estado": "ACTIVO"
      },
      "menus": [
        {
          "fechaCreado": "26-04-2024 12:37:36",
          "creadoPor": "string",
          "fechaModificado": "26-04-2024 12:37:36",
          "modificadoPor": "string",
          "id": 1,
          "nombre": "Menu A",
          "menuInfo": {
            "url": null,
            "imagenId": null
          },
          "menuPadre": {
            "fechaCreado": null,
            "creadoPor": null,
            "fechaModificado": null,
            "modificadoPor": null,
            "id": null,
            "nombre": null,
            "menuInfo": null,
            "menuPadre": null,
            "menus": null,
            "estado": null
          },
          "menus": [
            {}
          ],
          "estado": "ACTIVO"
        }
      ],
      "estado": "ACTIVO"
    }
  ],
  "estado": "ACTIVO"
}

```

### Attribute

|Name|Type|Required|Restrictions|Title|Description|
|---|---|---|---|---|---|
|fechaCreado|string|false|none||none|
|creadoPor|string|false|none||none|
|fechaModificado|string|false|none||none|
|modificadoPor|string|false|none||none|
|id|integer(int64)|false|none||id del menu|
|nombre|string|false|none||nombre del menu|
|menuInfo|[MenuInfo](#schemamenuinfo)|false|none||none|
|menuPadre|[Menu](#schemamenu)|false|none||none|
|menus|[[Menu](#schemamenu)]|false|none||none|
|estado|string|false|none||estado del menu|

#### Enum

|Name|Value|
|---|---|
|estado|ACTIVO|
|estado|INACTIVO|

<h2 id="tocS_MenuInfo">MenuInfo</h2>

<a id="schemamenuinfo"></a>
<a id="schema_MenuInfo"></a>
<a id="tocSmenuinfo"></a>
<a id="tocsmenuinfo"></a>

```json
{
  "url": "/menuA/index.html",
  "imagenId": "151c0a1d-fccd-4ead-ae4b-f05a26d3779b"
}

```

### Attribute

|Name|Type|Required|Restrictions|Title|Description|
|---|---|---|---|---|---|
|url|string|false|none||url del menu|
|imagenId|string(uuid)|false|none||id de la imagen del menu|

<h2 id="tocS_PostReservaBoletaPartner">PostReservaBoletaPartner</h2>

<a id="schemapostreservaboletapartner"></a>
<a id="schema_PostReservaBoletaPartner"></a>
<a id="tocSpostreservaboletapartner"></a>
<a id="tocspostreservaboletapartner"></a>

```json
{
  "fecha": "26-04-2024",
  "tipoIdentificacion": "CC",
  "numeroIdentificacion": "1111222333",
  "nombre": "Juan",
  "apellido": "Perez",
  "email": "example@email.com",
  "telefono": "3005557777",
  "tarifa": "Adulto",
  "barcode": "1234567890123456789012",
  "orderId": 1
}

```

### Attribute

|Name|Type|Required|Restrictions|Title|Description|
|---|---|---|---|---|---|
|fecha|string|false|none||fecha de la reserva|
|tipoIdentificacion|string|true|none||tipo de identificacion del cliente|
|numeroIdentificacion|string|true|none||numero de identificacion del cliente|
|nombre|string|true|none||nombre del cliente|
|apellido|string|true|none||apellido del cliente|
|email|string|true|none||direccion de correo electronico del cliente|
|telefono|string|true|none||telefono del cliente|
|tarifa|string|true|none||tipo de boleta vendido (Adulto o Niño)|
|barcode|string|false|none||codigo de barras de la boleta|
|orderId|integer(int64)|false|none||id de la orden|

#### Enum

|Name|Value|
|---|---|
|tipoIdentificacion|CC|
|tipoIdentificacion|NIT|
|tipoIdentificacion|CE|
|tipoIdentificacion|PAS|
|tipoIdentificacion|TI|
|tipoIdentificacion|RC|
|tipoIdentificacion|DNI|

<h2 id="tocS_IdMessageResponse">IdMessageResponse</h2>

<a id="schemaidmessageresponse"></a>
<a id="schema_IdMessageResponse"></a>
<a id="tocSidmessageresponse"></a>
<a id="tocsidmessageresponse"></a>

```json
{
  "message": "respuesta",
  "id": "1"
}

```

### Attribute

|Name|Type|Required|Restrictions|Title|Description|
|---|---|---|---|---|---|
|message|string|false|none||mesaje de respuesta|
|id|string|false|none||id del objeto|

<h2 id="tocS_PostReservaPartner">PostReservaPartner</h2>

<a id="schemapostreservapartner"></a>
<a id="schema_PostReservaPartner"></a>
<a id="tocSpostreservapartner"></a>
<a id="tocspostreservapartner"></a>

```json
{
  "fecha": "26-04-2024",
  "tipoIdentificacion": "CC",
  "numeroIdentificacion": "1111222333",
  "nombre": "Juan",
  "apellido": "Perez",
  "email": "example@email.com",
  "telefono": "3005557777",
  "enviarCorreos": false,
  "boletas": [
    {
      "idTipoBoleta": 1,
      "visitante": {
        "tipoIdentificacion": "CC",
        "numeroIdentificacion": "1111222333",
        "nombre": "nombre 1",
        "apellido": "apellido 1",
        "email": "example@email.com",
        "telefono": "3005557777",
        "paisProcedencia": "Colombia",
        "ciudadProcedencia": "Bogota",
        "fechaNacimiento": "26-04-2024",
        "estaturaMayor145": true,
        "genero": "M"
      },
      "idTipoCasilla": 1
    }
  ],
  "vehiculos": [
    {
      "idTipoServicio": 1,
      "idTipoVehiculo": 1,
      "placa": "AAA111"
    }
  ]
}

```

### Attribute

|Name|Type|Required|Restrictions|Title|Description|
|---|---|---|---|---|---|
|fecha|string|true|none||fecha de la reserva|
|tipoIdentificacion|string|true|none||tipo de identificacion del cliente|
|numeroIdentificacion|string|true|none||numero de identificacion del cliente|
|nombre|string|true|none||nombre del cliente|
|apellido|string|true|none||apellido del cliente|
|email|string|true|none||direccion de correo electronico del cliente|
|telefono|string|true|none||telefono del cliente|
|enviarCorreos|boolean|false|none||indica si se deben enviar correos de confirmacion (Correo de compra de reserva, correo boleta codigo QR)|
|boletas|[[PRBPBoleta](#schemaprbpboleta)]|true|none||[boletas a reservar]|
|vehiculos|[[PRBPVehiculo](#schemaprbpvehiculo)]|false|none||[espacio del parqueadero a reservar]|

#### Enum

|Name|Value|
|---|---|
|tipoIdentificacion|CC|
|tipoIdentificacion|NIT|
|tipoIdentificacion|CE|
|tipoIdentificacion|PAS|
|tipoIdentificacion|TI|
|tipoIdentificacion|RC|
|tipoIdentificacion|DNI|

<h2 id="tocS_PRBPVehiculo">PRBPVehiculo</h2>

<a id="schemaprbpvehiculo"></a>
<a id="schema_PRBPVehiculo"></a>
<a id="tocSprbpvehiculo"></a>
<a id="tocsprbpvehiculo"></a>

```json
{
  "idTipoServicio": 1,
  "idTipoVehiculo": 1,
  "placa": "AAA111"
}

```

espacio del parqueadero a reservar

### Attribute

|Name|Type|Required|Restrictions|Title|Description|
|---|---|---|---|---|---|
|idTipoServicio|integer(int64)|true|none||id del tipo de servicio de parqueadero|
|idTipoVehiculo|integer(int64)|true|none||id del tipo de vehiculo del vehiculo que se asignara a la reserva de vehiculo|
|placa|string|true|none||placa del vehiculo que se asignara a la reserva de vehiculo|

<h2 id="tocS_PRBPBoleta">PRBPBoleta</h2>

<a id="schemaprbpboleta"></a>
<a id="schema_PRBPBoleta"></a>
<a id="tocSprbpboleta"></a>
<a id="tocsprbpboleta"></a>

```json
{
  "idTipoBoleta": 1,
  "visitante": {
    "tipoIdentificacion": "CC",
    "numeroIdentificacion": "1111222333",
    "nombre": "nombre 1",
    "apellido": "apellido 1",
    "email": "example@email.com",
    "telefono": "3005557777",
    "paisProcedencia": "Colombia",
    "ciudadProcedencia": "Bogota",
    "fechaNacimiento": "26-04-2024",
    "estaturaMayor145": true,
    "genero": "M"
  },
  "idTipoCasilla": 1
}

```

boletas a reservar

### Attribute

|Name|Type|Required|Restrictions|Title|Description|
|---|---|---|---|---|---|
|idTipoBoleta|integer(int64)|true|none||id del tipo de boleta|
|visitante|[PostVisitante](#schemapostvisitante)|true|none||datos del visitante|
|idTipoCasilla|integer(int64)|false|none||id de la casilla (null si no aplica)|

<h2 id="tocS_PostVisitante">PostVisitante</h2>

<a id="schemapostvisitante"></a>
<a id="schema_PostVisitante"></a>
<a id="tocSpostvisitante"></a>
<a id="tocspostvisitante"></a>

```json
{
  "tipoIdentificacion": "CC",
  "numeroIdentificacion": "1111222333",
  "nombre": "nombre 1",
  "apellido": "apellido 1",
  "email": "example@email.com",
  "telefono": "3005557777",
  "paisProcedencia": "Colombia",
  "ciudadProcedencia": "Bogota",
  "fechaNacimiento": "26-04-2024",
  "estaturaMayor145": true,
  "genero": "M"
}

```

datos del visitante

### Attribute

|Name|Type|Required|Restrictions|Title|Description|
|---|---|---|---|---|---|
|tipoIdentificacion|string|true|none||tipo de identificacion del visitante|
|numeroIdentificacion|string|true|none||numero de identificacion del visitante|
|nombre|string|true|none||nombre del visitante|
|apellido|string|true|none||apellido del visitante|
|email|string|false|none||direccion de correo electronico del visitante|
|telefono|string|false|none||telefono del visitante|
|paisProcedencia|string|false|none||pais de procedencia del visitante|
|ciudadProcedencia|string|false|none||ciudad de procedencia del visitante|
|fechaNacimiento|string|false|none||fecha de nacimiento del visitante|
|estaturaMayor145|boolean|false|none||estatura del visitante en centimetros es mayor a 145cm si/no|
|genero|string|true|none||genero del visitante|

#### Enum

|Name|Value|
|---|---|
|tipoIdentificacion|CC|
|tipoIdentificacion|NIT|
|tipoIdentificacion|CE|
|tipoIdentificacion|PAS|
|tipoIdentificacion|TI|
|tipoIdentificacion|RC|
|tipoIdentificacion|DNI|
|genero|M|
|genero|F|
|genero|O|

