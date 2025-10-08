---
title: Aspose.Cells Cloud Web API - Token de acceso posterior
second_title: Documen
ArticleTitle: Get Access Token with Client ID and Secre
linktitle: Token de acceso posterior
type: docs
url: /es/post-access-token/
keywords: Access Token, Aspose Cloud, API Authentication, OAuth, REST API, Excel, Office Cloud, Token Managemen
description: Recupere un token de acceso utilizando el token de obtención de nube Cells API, que actúa como un servicio proxy que reenvía las solicitudes de los usuarios al servidor de autenticación de nube Aspose y devuelve el token de acceso resultante al cliente de forma segura.
weight: 100
kwords: Excel, Office Nube, REST API, Autenticación, Gestión de tokens, Integración de middleware, Seguridad API, Aspose Nube
---
Recupere un token de acceso utilizando el token de obtención de nube Cells API con ID de cliente y secreto.

## **Token de acceso postal API**

```
POST http://api.aspose.cloud/v4.0/cells/connect/token
```

### **Parámetros de la solicitud:**

| Nombre del parámetro| Tipo| Ruta/Cadena de consulta/HTTPBody| Descripción|
|:- |:- |:- |:- |
| ID de cliente| cadena| consulta| ID de cliente|
| Secreto del cliente| cadena| consulta| Secreto del cliente|

### **Respuesta**

```json
 [
        {
          "Name": "String",
          "DataType": {
            "Identifier": "String",
            "Name": "string"
          }
        }
  ]
```

## Cómo usar la clave pública API con SDK

### Especificación OpenAPI

 El[Especificación OpenAPI](https://reference.aspose.cloud/cells/#/CellsAuthorityController/PostAccessToken) define una interfaz de programación de acceso público que le permite realizar interacciones REST directamente desde un navegador web.

### Utilice los SDK de la nube Aspose.Cells

Usar el SDK es la mejor manera de acelerar el desarrollo. El SDK gestiona los detalles subyacentes, lo que permite implementar fácilmente el token de acceso para celdas con un mínimo de código.
 Por favor, consulte el[Repositorio de GitHub](https://github.com/aspose-cells-cloud) Para obtener una lista completa de los SDK de la nube Aspose.Cells. Un SDK se encarga de los detalles básicos y le permite centrarse en las tareas de su proyecto. Consulte[Repositorio de GitHub](https://github.com/aspose-cells-cloud) para obtener una lista completa de Aspose.Cells SDK en la nube.

Los siguientes ejemplos de código demuestran cómo realizar llamadas a los servicios web Aspose.Cells utilizando varios SDK:
