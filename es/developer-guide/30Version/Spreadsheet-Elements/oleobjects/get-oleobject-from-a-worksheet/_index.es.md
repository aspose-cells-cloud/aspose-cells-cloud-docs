---
title: "Obtener objeto OLE de una hoja de cálculo de Excel – Aspose.Cells Cloud API"
second_title: "Documento"
linktitle: "Obtener"
type: docs
url: /oleobjects/get/
aliases: [/get-oleobject-from-a-worksheet/]
keywords: "aspose, cells, objeto ole, excel, hoja de cálculo, obtener objeto ole, api rest"
description: "Recuperar un objeto OLE (imagen, gráfico o archivo incrustado) de una hoja de cálculo utilizando la API REST de Aspose.Cells Cloud. Incluye el punto de conexión HTTPS, los parámetros requeridos, un ejemplo de cURL y código de SDK en múltiples lenguajes."
ArticleTitle: "Obtener objeto OLE de una hoja de cálculo de Excel – Aspose.Cells Cloud API"
weight: 10
---

Esta API REST recupera un **objeto OLE** de una hoja de cálculo de Excel.

## Seguridad y autenticación
Las API de Aspose.Cells Cloud son seguras y requieren [autenticación basada en token JWT](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/).

## API REST

```bash
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/oleobjects/{objectNumber}?format={format}
```

### Parámetros de solicitud

| Nombre del parámetro | Tipo    | Ubicación | Descripción                                                 |
| --------------------- | ------- | --------- | ----------------------------------------------------------- |
| name                  | string  | path      | Nombre del documento.                                       |
| sheetName             | string  | path      | Nombre de la hoja de cálculo.                               |
| objectNumber          | integer | path      | Número del objeto dentro de la hoja de cálculo.             |
| format                | string  | query     | Formato de exportación deseado para el objeto (p. ej., `png`, `jpeg`). |
| folder                | string  | query     | Carpeta que contiene el documento.                          |
| storageName           | string  | query     | Nombre del almacenamiento a utilizar.                       |

### Opciones de almacenamiento

- **folder** – especifica la subcarpeta en el almacenamiento predeterminado donde se encuentra el libro.
- **storageName** – anula el nombre predeterminado del almacenamiento si el libro se encuentra en otra ubicación.

La [Especificación OpenAPI](https://apireference.aspose.cloud/cells/#/OleObjects/GetWorksheetOleObject) define una interfaz de programación públicamente accesible y permite realizar interacciones REST directamente desde un navegador web.

Puede utilizar la herramienta de línea de comandos **cURL** para llamar al servicio web de Aspose.Cells. El ejemplo siguiente muestra cómo solicitar un objeto OLE como imagen PNG.

{{< tabs tabTotal="2" tabID="1" tabName1="Solicitud" tabName2="Respuesta" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Embedded_OleObject_Sample_Book1.xlsx/worksheets/Sheet1/oleobjects/0?format=png" \
  -X GET \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

### Respuesta con imagen binaria

Cuando `format` se establece en un tipo de imagen (p. ej., `png`), la API devuelve los datos binarios de la imagen con el encabezado:

```
Content-Type: image/png
```

_(El archivo de imagen se transmite directamente al cliente.)_

### Respuesta con metadatos en JSON

Si se omite `format` o se establece en `json`, la API devuelve una carga útil en JSON que describe el objeto OLE:

```json
{
  "Code": 200,
  "Status": "OK",
  "OLEObject": {
    "Name": "Object1",
    "Width": 200,
    "Height": 150,
    "Left": 10,
    "Top": 20,
    "IsLocked": false,
    "FileFormat": "png"
  }
}
```

{{< /tab >}}

{{< /tabs >}}

## Respuestas de error

| Estado HTTP | Código de error | Descripción                                   |
| ----------- | --------------- | --------------------------------------------- |
| 400         | BadRequest      | Parámetros ausentes o no válidos.             |
| 401         | Unauthorized    | Token JWT no válido o ausente.                |
| 404         | NotFound        | Libro, hoja de cálculo u objeto OLE no encontrado. |
| 500         | ServerError     | Error inesperado del servidor.                |

**Ejemplo de respuesta 404**

```json
{
  "Code": 404,
  "Status": "NotFound",
  "Message": "No se encontró el objeto OLE solicitado con número 0 en la hoja 'Sheet1'."
}
```

## Familia de SDK en la nube

Utilizar un SDK es la forma más rápida de integrar la API. Los SDK gestionan los detalles de bajo nivel para que usted pueda centrarse en su lógica de negocio. Consulte el [repositorio de GitHub](https://github.com/aspose-cells-cloud) para obtener una lista completa de los SDK de Aspose.Cells Cloud.

Los siguientes ejemplos de código muestran cómo llamar a los servicios web de Aspose.Cells con distintos SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetWorksheetOleObject.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetWorksheetOleObject.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetWorksheetOleObject.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetWorksheetOleObject.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_GetWorksheetOleObject.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetWorksheetOleObject.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetWorksheetOleObject.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetWorksheetOleObject.go" >}}

{{< /tab >}}

{{< /tabs >}}