# PCA API Integracion Partners

* [Autenticacion](https://infomedia-service.github.io/docs/pca/partner.html#tag/Autenticacion "Autenticacion")
* [Integracion Partner](https://infomedia-service.github.io/docs/pca/partner.html#tag/Partner "Integracion Partner")



------------

* [¿Como usar el filtro de busqueda?](https://infomedia-service.github.io/docs/filter/v2/syntax.html "¿Como usar el filtro de busqueda?")

------------


#### Crear reserva de boletas y obtener codigos QR

```mermaid
graph
A[Autenticacion:\nObtener token jwt\n/api/auth/token]
-->B[Consultar tipo boleta, tipo casilla,\n tipo servicio, etc. Segun se necesite.]
-->C[Crear nueva reserva:\nobtener id reserva\n/api/partner/reserva]
-->D[Consultar reserva:\nobtener ids de boletas\n/api/partner/buscarReserva\nUsando el filtro\nid:'id_obtenido_en_el_paso_anterior']
-->E[Generar codigos QR para cada boleta\n/api/partner/generarQRBoleta]
```
