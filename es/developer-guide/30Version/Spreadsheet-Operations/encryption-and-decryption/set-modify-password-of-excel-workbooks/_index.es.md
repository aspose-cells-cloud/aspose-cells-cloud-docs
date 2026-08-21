---
title: "Modificar la protección por contraseña de un libro de Excel"
second_title: "Documento"
linktitle: "Modificar la contraseña de un archivo de Excel"
type: docs
url: /es/workbook/password/modify/
aliases:
  - /set-modify-password-of-excel-workbooks/
  - /workbook/modify-password/
keywords: "contraseña de Excel, Aspose.Cells Cloud, protección contra escritura, API REST, modificar contraseña de libro"
description: "Cambiar la contraseña de protección contra escritura de un libro de Excel utilizando la API REST de Aspose.Cells Cloud (v3.0). Incluye ejemplos en cURL y SDK."
weight: 100
ArticleTitle: "Modificar la protección por contraseña de un libro de Excel – Aspose.Cells Cloud"
---

Esta **API REST cambia la contraseña de protección contra escritura** de un libro de Excel existente.

Actualizar la contraseña de protección contra escritura programáticamente le permite rotar o reemplazar contraseñas sin descargar el archivo. Es especialmente útil al gestionar libros protegidos almacenados en el almacenamiento de Aspose.Cells Cloud.

## API REST

```bash
PUT https://api.aspose.cloud/v3.0/cells/{name}/writeProtection
```

### Seguridad y autenticación

Las API de Aspose.Cells Cloud son seguras y requieren [autenticación basada en token JWT](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/).

### Parámetros de la solicitud

| Nombre del parámetro | Tipo   | Ubicación | Descripción                                           |
|----------------------|--------|-----------|-------------------------------------------------------|
| **name**             | string | path      | Nombre del libro de Excel (obligatorio).             |
| **password**         | string | body (JSON) | Nueva contraseña de protección contra escritura (obligatoria). |
| **folder**           | string | query     | Carpeta opcional donde se encuentra el libro.        |
| **storageName**      | string | query     | Nombre opcional del servicio de almacenamiento.      |

### Respuesta

```json
{
  "Status":"OK",
  "Code":200
}
```

**Códigos de estado HTTP**

| Código | Significado                 | Descripción                                           |
|--------|-----------------------------|-------------------------------------------------------|
| 200    | Correcto                    | Filtro aplicado correctamente; la respuesta contiene detalles de la operación. |
| 400    | Solicitud incorrecta        | Parámetros ausentes o no válidos (por ejemplo, tipo de archivo no admitido). |
| 401    | No autorizado               | Token JWT no válido o ausente. |
| 413    | Payload demasiado grande     | El archivo cargado excede el límite de tamaño. |
| 500    | Error interno del servidor  | Error inesperado en el servidor. |

## Cómo usar la API PutDocumentProtectFromChanges con SDK

### Especificación de la API PutDocumentProtectFromChanges

La [Especificación OpenAPI](https://apireference.aspose.cloud/cells/#/Workbook/PutDocumentProtectFromChanges) define la interfaz de programación accesible públicamente que permite realizar interacciones REST directamente desde un navegador web.

Puede utilizar la herramienta de línea de comandos **cURL** para acceder fácilmente a los servicios web de Aspose.Cells. El comando cURL a continuación muestra cómo invocar la API en la nube.

{{< tabs tabTotal="2" tabID="1" tabName1="Solicitud" tabName2="Respuesta" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Sample_Test_Book.xls/writeProtection?folder=Samples&storageName=Default" \
  -X PUT \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>" \
  -d '{ "Password": "aspose" }'
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

### Utilizar los SDK de Aspose.Cells Cloud

Utilizar un SDK es la forma más rápida de desarrollar. Un SDK maneja los detalles de bajo nivel, permitiéndole centrarse en su lógica de negocio. Consulte el [repositorio de GitHub](https://github.com/aspose-cells-cloud) para obtener una lista completa de los SDK de Aspose.Cells Cloud.

Los siguientes ejemplos de código muestran cómo invocar los servicios web de Aspose.Cells mediante diversos SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePutDocumentProtectFromChanges.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PutDocumentProtectFromChanges.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PutDocumentProtectFromChanges.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PutDocumentProtectFromChanges.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PutDocumentProtectFromChanges.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PutDocumentProtectFromChanges.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PutDocumentProtectFromChanges.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PutDocumentProtectFromChanges.go" >}}

{{< /tab >}}

{{< /tabs >}}