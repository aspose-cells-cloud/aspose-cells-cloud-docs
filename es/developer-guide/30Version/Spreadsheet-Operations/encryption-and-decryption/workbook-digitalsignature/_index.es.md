---
title: "Agregar una firma digital a un libro de Excel"
ArticleTitle: "Agregar una firma digital a un libro de Excel – Aspose.Cells Cloud API"
second_title: "Documento"
linktype: "firma digital"
type: docs
url: /excel-digital-signature/
aliases:
  - /protect/digital-signature/
  - /workbook/digital-signature/
keywords: "Aspose.Cells Cloud, firma digital, libro de Excel, API REST, .pfx, JWT, API de firma"
description: "Aprenda cómo agregar una firma digital a un libro de Excel mediante la API REST de Aspose.Cells Cloud (v4.0). Incluye el endpoint, parámetros, autenticación, esquema de respuesta, manejo de errores y ejemplos de SDK para múltiples lenguajes."
weight: 35
---

**Requisitos previos:**  
Antes de llamar a este endpoint, asegúrese de tener:

- Un token de acceso JWT válido obtenido mediante la autenticación de Aspose Cloud.  
- El libro de trabajo objetivo cargado en su almacenamiento de Aspose Cloud.  
- Un archivo de firma digital en formato `.pfx` o `.p12` y su contraseña.

Esta API REST agrega una **firma digital** a un libro de Excel.

## API PostDigitalSignature

```http
POST https://api.aspose.cloud/v4.0/cells/{name}/digitalsignature
```

### **Seguridad y autenticación**

Las API de Aspose.Cells Cloud son seguras y requieren <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">autenticación basada en token JWT</a>.

### Parámetros de solicitud

| Nombre del parámetro       | Tipo   | Ubicación             | Descripción                                             |
| -------------------------- | ------ | --------------------- | ------------------------------------------------------- |
| **name**                   | string | `<code>path</code>`   | Nombre del libro de trabajo.                            |
| **digitalsignaturefile**   | string | `<code>query</code>`  | Ruta al archivo de firma digital (`.pfx` o `.p12`).     |
| **password**               | string | `<code>query</code>`  | Contraseña del libro de trabajo, si está protegido.     |
| **folder**                 | string | `<code>query</code>`  | Carpeta donde se almacena el libro de trabajo.          |
| **storageName**            | string | `<code>query</code>`  | Nombre del servicio de almacenamiento a utilizar.       |

*Nota: Si el nombre del archivo contiene caracteres especiales, realice su codificación URL antes de incluirlo en la cadena de consulta.*

### Manejo de errores

| Estado HTTP | Significado                                               |
| ----------- | --------------------------------------------------------- |
| 200         | Firma aplicada correctamente.                             |
| 400         | Solicitud incorrecta: parámetros faltantes o no válidos. |
| 401         | No autorizado: token OAuth no válido o expirado.          |
| 403         | Prohibido: permisos insuficientes o acceso denegado.      |
| 500         | Error interno del servidor: fallo inesperado.             |

### Respuestas de error por estado HTTPS

| Estado HTTP | Código              | Descripción                                                |
| ----------- | ------------------- | ---------------------------------------------------------- |
| 400         | BadRequest          | Parámetros faltantes o no válidos.                         |
| 401         | Unauthorized        | Token de acceso no válido o faltante.                      |
| 404         | NotFound            | Libro de trabajo especificado no encontrado en la carpeta/almacenamiento indicado. |
| 500         | InternalServerError | Error inesperado del servidor.                             |

## Cómo utilizar la API PostDigitalSignature con SDK

### Especificación de la API PostDigitalSignature

La [Especificación OpenAPI](https://apireference.aspose.cloud/cells/#/Protection/PostDigitalSignature) define una interfaz de programación públicamente accesible y permite realizar interacciones REST directamente desde un navegador web.

Puede utilizar la herramienta de línea de comandos cURL para llamar a los servicios web de Aspose.Cells. El ejemplo siguiente muestra una solicitud a la API:

{{< tabs tabTotal="2" tabID="11" tabName11="Solicitud" tabName12="Respuesta" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v4.0/cells/{name}/digitalsignature?digitalsignaturefile=signature.pfx&password=SuContraseña" \
  -X POST \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <token jwt>"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

**Esquema de respuesta**  
La API devuelve un objeto JSON con los siguientes campos:

| Campo         | Tipo   | Descripción                                              |
| ------------- | ------ | -------------------------------------------------------- |
| `Code`        | int    | Código de estado similar a HTTP que indica el resultado. |
| `Status`      | string | Texto breve que describe el resultado (por ejemplo, `OK`). |
| `SignatureId` | string | Identificador de la firma digital aplicada (opcional).   |
| `Message`     | string | Información adicional o detalles de error (opcional).    |

### Utilizar los SDK de Aspose.Cells Cloud

El uso de un SDK simplifica la integración y reduce el código repetitivo. Consulte el [repositorio de GitHub](https://github.com/aspose-cells-cloud) para obtener una lista completa de los SDK de Aspose.Cells Cloud.

Los siguientes ejemplos de código muestran cómo invocar los servicios web de Aspose.Cells mediante diversos SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostDigitalSignature.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostDigitalSignature.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostDigitalSignature.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostDigitalSignature.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82a2de2e4189bc27ae92abf73c36b4df0" "Example_PostDigitalSignature.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostDigitalSignature.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostDigitalSignature.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostDigitalSignature.go" >}}

{{< /tab >}}

{{< /tabs >}}