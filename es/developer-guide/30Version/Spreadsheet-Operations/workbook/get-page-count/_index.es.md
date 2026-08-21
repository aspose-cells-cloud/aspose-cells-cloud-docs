---
title: "Obtener el número de páginas de un archivo de Excel"
second_title: "Document"
linktitle: "Páginas"
type: docs
url: /es/get-page-count-from-an-excel-file/
aliases: [/es/workbook/page-count/, /es/workbook/get/page-count/]
keywords: "Aspose.Cells, API en la nube, número de páginas de Excel, paginación de libros de trabajo"
description: "Recuperar el número total de páginas imprimibles en un libro de trabajo de Excel mediante la API REST de Aspose.Cells Cloud (v3.0). Incluye formato de solicitud, parámetros obligatorios, ejemplo con cURL, esquema de respuesta, manejo de errores y fragmentos de SDK para múltiples lenguajes."
weight: 10
version: "v3.0"
ArticleTitle: "Obtener el número de páginas de un archivo de Excel usando la API de Aspose.Cells Cloud"
---

Esta API REST devuelve el **número de páginas** de un libro de trabajo.

## Seguridad y autenticación
Las API de Aspose.Cells Cloud son seguras y requieren [autenticación basada en token JWT](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/).

## API REST

```bash
GET https://api.aspose.cloud/v3.0/cells/{name}/pagecount
```

### Parámetros de la solicitud

| Nombre del parámetro | Tipo   | Ubicación | Obligatorio | Descripción                                      |
| -------------------- | ------ | --------- | ----------- | ------------------------------------------------ |
| name                 | string | path      | Sí          | El nombre del documento de Excel.               |
| folder               | string | query     | No          | La carpeta que contiene el documento.           |
| storageName          | string | query     | No          | El nombre del almacenamiento que se va a usar.  |

La [Especificación OpenAPI](https://apireference.aspose.cloud/cells/#/Workbook/GetPageCount) define una interfaz de programación públicamente accesible y permite realizar interacciones REST directamente desde un navegador web.

Puede utilizar la herramienta de línea de comandos cURL para acceder fácilmente a la API REST de Aspose.Cells. El siguiente ejemplo muestra cómo invocar el punto de conexión mediante cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Solicitud" tabName2="Respuesta" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/YourFile.xlsx/pagecount" \
  -X GET \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

*Reemplace `YourFile.xlsx` con el nombre real del libro de trabajo que desea consultar.*

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
13
```

{{< /tab >}}

{{< /tabs >}}

### Esquema de respuesta

| Estado HTTP | Tipo de datos | Descripción                                             |
| ----------- | ------------- | ------------------------------------------------------- |
| 200         | integer       | El número total de páginas imprimibles del libro (por ejemplo, `13`). |
| 4xx‑5xx     | JSON          | Objeto de error (ver sección _Manejo de errores_).    |

## Familia de SDK en la nube

Utilizar un SDK es la mejor forma de acelerar el desarrollo. Un SDK se encarga de los detalles de bajo nivel y le permite centrarse en las tareas de su proyecto. Consulte el [repositorio de GitHub](https://github.com/aspose-cells-cloud) para ver una lista completa de los SDK de Aspose.Cells Cloud.

Los siguientes ejemplos de código muestran cómo realizar llamadas a los servicios web de Aspose.Cells mediante diversos SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetPageCount.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetPageCount.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetPageCount.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetPageCount.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82deb2e4189bc27ae92abf73c36b4df0" "Example_GetPageCount.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetPageCount.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetPageCount.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetPageCount.go" >}}

{{< /tab >}}

{{< /tabs >}}

## Manejo de errores

| Estado HTTP | Descripción                              | Cuerpo JSON de ejemplo                                                                      |
| ----------- | ---------------------------------------- | ------------------------------------------------------------------------------------------- |
| 401         | Token JWT inválido o ausente.            | `{ "Code": "InvalidAuthenticationToken", "Message": "El token de acceso está ausente o es inválido." }` |
| 404         | No se pudo encontrar el libro especificado. | `{ "Code": "FileNotFound", "Message": "El archivo solicitado no existe." }`               |
| 400         | Solicitud incorrecta: parámetros obligatorios ausentes. | `{ "Code": "BadRequest", "Message": "Falta el parámetro obligatorio 'name'." }`           |
| 500         | Error interno del servidor.              | `{ "Code": "InternalError", "Message": "Ocurrió un error inesperado." }`                   |
---