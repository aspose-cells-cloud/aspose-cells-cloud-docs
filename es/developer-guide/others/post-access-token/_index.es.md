---
title: "Aspose.Cells Cloud Web API - Post Access Token"
second_title: "Document"
ArticleTitle: "Obtener token de acceso con ID de cliente y secreto"
linktitle: "Post Access Token"
type: docs
url: /post-access-token/
keywords: "Aspose.Cells, Cloud, Token de acceso, OAuth2, API, Autenticación, REST, Excel, Office Cloud"
description: "Obtenga un token de acceso OAuth2 para Aspose.Cells Cloud llamando al endpoint POST /cells/connect/token con su ID de cliente y secreto."
weight: 100
---

Recupere un token de acceso utilizando la API de Cells Cloud Get Token con un ID de cliente y un secreto.

## API Post Access Token

Antes de llamar al endpoint, asegúrese de tener:

* Una cuenta registrada en Aspose Cloud.  
* Un **ID de cliente** y un **Secreto de cliente** generados en el portal de Aspose Cloud.  

### Web API

```
POST https://api.aspose.cloud/v4.0/cells/connect/token
```

### **Seguridad y autenticación**

Las APIs de Aspose.Cells Cloud son seguras y requieren <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">autenticación basada en token JWT</a>.

### Parámetros de solicitud

| Nombre del parámetro | Tipo   | Ubicación                     | Descripción                                               |
| --------------------- | ------ | ----------------------------- | --------------------------------------------------------- |
| grant_type            | string | cuerpo (codificado como form‑url‑encoded) | Valor fijo `client_credentials` requerido para OAuth. |
| client_id             | string | cuerpo (codificado como form‑url‑encoded) | El identificador de cliente que se le ha emitido.     |
| client_secret         | string | cuerpo (codificado como form‑url‑encoded) | El secreto asociado al ID de cliente.                  |

**Ejemplo de solicitud (cURL)**  

```bash
curl -X POST "https://api.aspose.cloud/v4.0/cells/connect/token" \
     -H "Content-Type: application/x-www-form-urlencoded" \
     -d "grant_type=client_credentials&client_id=SU_ID_DE_CLIENTE&client_secret=SU_SECRETO_DE_CLIENTE"
```

### Respuesta

```json
{
  "access_token": "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9...",
  "token_type": "Bearer",
  "expires_in": 3600
}
```

**Códigos de estado HTTP**

| Código | Significado                 | Descripción                                           |
|--------|-----------------------------|-------------------------------------------------------|
| 200    | Correcto                    | Filtro aplicado correctamente; la respuesta contiene los detalles de la operación. |
| 400    | Solicitud incorrecta        | Parámetros faltantes o no válidos (por ejemplo, tipo de archivo no admitido). |
| 401    | No autorizado               | Token JWT no válido o faltante. |
| 413    | Payload demasiado grande     | El archivo subido excede el límite de tamaño. |
| 500    | Error interno del servidor  | Error inesperado en el servidor. |

**Ejemplo de manejo de errores**

```json
{
  "error": "invalid_client",
  "error_description": "Falló la autenticación del cliente."
}
```

## Cómo usar la API Get public key con SDK

### Especificación OpenAPI

La [Especificación OpenAPI](https://reference.aspose.cloud/cells/#/CellsAuthorityController/PostAccessToken) define una interfaz de programación accesible públicamente, lo que le permite realizar interacciones REST directamente desde un navegador web.

### Uso de los SDK de Aspose.Cells Cloud

Utilizar los SDK es la forma más rápida de comenzar. Los SDK ocultan los detalles HTTP subyacentes, permitiéndole obtener un token de acceso para Cells con un código mínimo.

Consulte el [repositorio de GitHub](https://github.com/aspose-cells-cloud) para obtener una lista completa de los SDK de Aspose.Cells Cloud. Un SDK se encarga de los detalles de bajo nivel para que usted pueda centrarse en las tareas de su proyecto.

Los siguientes ejemplos de código demuestran cómo llamar a los servicios web de Aspose.Cells utilizando diversos SDK:  
---