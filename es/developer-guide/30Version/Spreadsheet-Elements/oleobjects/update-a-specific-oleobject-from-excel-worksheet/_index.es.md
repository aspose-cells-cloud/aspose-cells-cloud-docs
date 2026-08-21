---
title: "Actualizar un objeto OLE en una hoja de cálculo de Excel"
second_title: "Document"
linktitle: "Update"
type: docs
url: /es/oleobjects/update/
aliases: [  /es/update-a-specific-oleobject-from-excel-worksheet/ ]
keywords: "actualizar objeto OLE, Excel, Aspose.Cells Cloud, API REST, SDK"
description: "Aprenda cómo actualizar un objeto OLE (imagen, gráfico, etc.) en una hoja de cálculo de Excel mediante la API REST de Aspose.Cells Cloud. Incluye ejemplos en cURL y SDK, pasos de autenticación y manejo de errores."
weight: 30
author: "Equipo de documentación de Aspose Cloud"
lastmod: "2024-03-01"
ArticleTitle: "Actualizar un objeto OLE en una hoja de cálculo de Excel – Guía de la API de Aspose.Cells Cloud"
---

Esta API REST actualiza un **objeto OLE** en una hoja de cálculo de Excel.

### **Seguridad y autenticación**

Las API de Aspose.Cells Cloud son seguras y requieren <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">autenticación basada en token JWT</a>.

## API PostUpdateWorksheetOleObject

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/oleobjects/{oleObjectIndex}
```

Los parámetros de la solicitud son:

| Nombre del parámetro | Tipo    | Ubicación del parámetro | Descripción                                             |
| --------------------- | ------- | ----------------------- | ------------------------------------------------------- |
| name                  | string  | path                    | Nombre del libro de trabajo.                           |
| sheetName             | string  | path                    | Nombre de la hoja de cálculo.                          |
| oleObjectIndex        | integer | path                    | Índice del objeto OLE dentro de la hoja de cálculo.    |
| ole                   | object  | body                    | Representación JSON del objeto OLE que se va a actualizar. |
| folder                | string  | query                   | Carpeta que contiene el libro de trabajo.              |
| storageName           | string  | query                   | Nombre del servicio de almacenamiento.                 |

### Campos del cuerpo de la solicitud

| Campo                 | Tipo    | Obligatorio | Descripción                                                   |
| --------------------- | ------- | ----------- | ------------------------------------------------------------- |
| ImageSourceFullName   | string  | opcional    | Ruta al archivo de imagen utilizado para el objeto OLE.       |
| IsAutoSize            | boolean | opcional    | Indica si el objeto OLE debe redimensionarse automáticamente. |
| SourceFullName        | string  | obligatorio | Archivo fuente (por ejemplo, una imagen o gráfico) del objeto OLE. |
| UpperLeftRow          | integer | obligatorio | Índice de fila (base cero) de la esquina superior izquierda.  |
| UpperLeftColumn       | integer | obligatorio | Índice de columna (base cero) de la esquina superior izquierda. |
| Left                  | integer | opcional    | Desplazamiento horizontal, en puntos, desde la esquina superior izquierda. |
| Top                   | integer | opcional    | Desplazamiento vertical, en puntos, desde la esquina superior izquierda. |
| Width                 | integer | obligatorio | Ancho del objeto OLE, en puntos.                              |
| Height                | integer | obligatorio | Alto del objeto OLE, en puntos.                               |

La [Especificación de OpenAPI](https://apireference.aspose.cloud/cells/#/OleObjects/PostUpdateWorksheetOleObject) define una interfaz de programación públicamente accesible y permite realizar interacciones REST directamente desde un navegador web.

Puede utilizar la herramienta de línea de comandos **cURL** para acceder fácilmente a los servicios web de Aspose.Cells. El siguiente ejemplo muestra cómo llamar a la API en la nube mediante cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Solicitud" tabName2="Respuesta" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/" \
  -X POST \
  -d '{"ImageSourceFullName":"aspose-logo.png","IsAutoSize":true,"SourceFullName":"Sample_Book2.xls","UpperLeftRow":15,"Top":10,"UpperLeftColumn":5,"Left":10,"Width":400,"Height":400}' \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Code": 200,
  "Status": "OK",
  "OLEObject": {
    "Index": 0,
    "ImageSourceFullName": "aspose-logo.png",
    "IsAutoSize": true,
    "SourceFullName": "Sample_Book2.xls",
    "UpperLeftRow": 15,
    "UpperLeftColumn": 5,
    "Left": 10,
    "Top": 10,
    "Width": 400,
    "Height": 400
  }
}
```

{{< /tab >}}

{{< /tabs >}}

## Respuestas de error

| Estado HTTP | Código | Mensaje                                                            |
| ----------- | ------ | ------------------------------------------------------------------ |
| 400         | 4000   | Solicitud incorrecta: parámetros faltantes o no válidos.          |
| 401         | 4010   | No autorizado: token JWT no válido o faltante.                    |
| 404         | 4040   | No encontrado: el libro de trabajo, la hoja de cálculo o el objeto OLE no existen. |
| 500         | 5000   | Error interno del servidor: fallo inesperado del lado del servidor. |

La API también devuelve un campo personalizado **Code** en el cuerpo de la respuesta que se corresponde con el estado HTTP (por ejemplo, 200 → 2000, 400 → 4000, etc.).

## ¿Cuándo utilizar esta API?

Utilice este endpoint cuando necesite modificar un objeto OLE existente —como una imagen, gráfico o documento incrustado— sin volver a cargar toda la hoja de cálculo. Los escenarios típicos incluyen actualizar la fuente de la imagen, cambiar el tamaño del objeto o modificar su posición tras haber generado el libro de trabajo. Para operaciones relacionadas, consulte [Agregar un objeto OLE](/oleobjects/add/) y [Eliminar un objeto OLE](/oleobjects/delete/).

## Familia de SDK en la nube

Utilizar un SDK es la forma más rápida de desarrollar. Un SDK abstracte los detalles de bajo nivel para que usted pueda centrarse en su proyecto. Consulte el [repositorio de GitHub](https://github.com/aspose-cells-cloud) para ver una lista completa de los SDK de Aspose.Cells Cloud.

A continuación se muestra un ejemplo breve en C# que actualiza un objeto OLE utilizando el SDK de Aspose.Cells Cloud:

```csharp
using Aspose.Cells.Cloud.SDK.Api;
using Aspose.Cells.Cloud.SDK.Model;

var config = new Configuration
{
    AppSid = "<your-app-sid>",
    AppKey = "<your-app-key>"
};
var oleApi = new OleObjectsApi(config);
var request = new OleObjectUpdateRequest
{
    ImageSourceFullName = "aspose-logo.png",
    IsAutoSize = true,
    SourceFullName = "Sample_Book2.xls",
    UpperLeftRow = 15,
    UpperLeftColumn = 5,
    Left = 10,
    Top = 10,
    Width = 400,
    Height = 400
};

var response = oleApi.UpdateWorksheetOleObject("SampleBook.xlsx", "Sheet1", 0, request, folder: "myFolder");
Console.WriteLine($"Status: {response.Status}");
```

Los siguientes ejemplos de código muestran cómo llamar a los servicios web de Aspose.Cells mediante diversos SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostUpdateWorksheetOleObject.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostUpdateWorksheetOleObject.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostUpdateWorksheetOleObject.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostUpdateWorksheetOleObject.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostUpdateWorksheetOleObject.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostUpdateWorksheetOleObject.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostUpdateWorksheetOleObject.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostUpdateWorksheetOleObject.go" >}}

{{< /tab >}}

{{< /tabs >}}