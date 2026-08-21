---
title: "Mover una hoja de cálculo de Excel – API de Aspose.Cells Cloud (v3.0)"
second_title: "Documento"
linktitle: "Mover"
type: docs
url: /es/worksheets/move/
aliases: [  /es/move-excel-worksheets/ ]
keywords: "Aspose.Cells Cloud, Mover hoja de cálculo, Excel, API REST, SDK, C#, Java, Python, Node.js, PHP, Ruby, Go, Android, Swift, Perl, v3.0"
description: "Aprenda cómo mover una hoja de cálculo de Excel a una nueva posición utilizando la API de Aspose.Cells Cloud (v3.0). Incluye el punto de conexión, parámetros requeridos, ejemplo de cURL y código del SDK en C#, Java, Python y más."
weight: 20
ArticleTitle: "Cómo mover una hoja de cálculo de Excel con la API de Aspose.Cells Cloud v3.0"
---

Esta API REST mueve una hoja de cálculo dentro de un libro de Excel.

## API REST

```bash
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/position
```

### Parámetros de la solicitud

| Nombre del parámetro | Tipo   | Ubicación | Descripción                                                                                                           |
|----------------------|--------|-----------|-----------------------------------------------------------------------------------------------------------------------|
| name                 | string | path      | Nombre del archivo de Excel.                                                                                          |
| sheetName            | string | path      | Nombre de la hoja de cálculo que se va a mover.                                                                       |
| moving               | object | body      | Objeto JSON que especifica la hoja de cálculo de destino (`DestinationWorksheet`) y la posición relativa (`Position`). |
| folder               | string | query     | Ruta de la carpeta donde se almacena el libro.                                                                        |
| storageName          | string | query     | Nombre del servicio de almacenamiento.                                                                                |

La [Especificación OpenAPI](https://apireference.aspose.cloud/cells/#/Worksheets/PostMoveWorksheet) define una interfaz de programación accesible públicamente y le permite realizar interacciones REST directamente desde un navegador web.

Puede utilizar la herramienta de línea de comandos cURL para llamar a los servicios web de Aspose.Cells. El ejemplo siguiente muestra cómo mover una hoja de cálculo con una única solicitud.

{{< tabs tabTotal="2" tabID="1" tabName1="Solicitud" tabName2="Respuesta" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Sample_Test_Book.xls/worksheets/Sheet1/position" \
  -X POST \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>" \
  -d '{"DestinationWorksheet":"Sheet5","Position":"after"}'
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

**Códigos de estado HTTP**

| Código | Significado                 | Descripción                                                                 |
|--------|-----------------------------|-----------------------------------------------------------------------------|
| 200    | OK                          | Filtro aplicado correctamente; la respuesta contiene los detalles de la operación. |
| 400    | Solicitud incorrecta        | Parámetros faltantes o no válidos (por ejemplo, tipo de archivo no admitido). |
| 401    | No autorizado               | Token JWT inválido o faltante.                                              |
| 413    | Carga útil demasiado grande | El archivo cargado supera el límite de tamaño.                             |
| 500    | Error interno del servidor  | Error inesperado del servidor.                                              |

**Carga útil de ejemplo de error**

```json
{
  "Code": 400,
  "Status": "Bad Request",
  "Message": "Falta el parámetro obligatorio 'moving'."
}
```

{{< /tab >}}

{{< /tabs >}}

## Familia de SDK en la nube

Utilizar un SDK es la mejor forma de acelerar el desarrollo. Un SDK gestiona los detalles de bajo nivel para que usted pueda centrarse en las tareas de su proyecto. Consulte el [repositorio de GitHub](https://github.com/aspose-cells-cloud) para obtener una lista completa de los SDK de Aspose.Cells Cloud.

Los siguientes ejemplos de código demuestran cómo llamar a los servicios web de Aspose.Cells utilizando diversos SDK:

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-.NET-CellsWorksheetsPostMoveWorksheet.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-worksheet-UnhideWorksheet-unhide-worksheets.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Worksheet-PostMoveWorksheet-.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Worksheet-move_worksheet-.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "MoveExcelWorksheets.py" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-Worksheet-MoveWorksheet-1.js" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "9d725d4678edaac53f95c5208e17783c" "Examples-Android-worksheet-MoveWorksheet-move-excel-worksheets.java" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-Worksheet-MoveWorksheet-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< gist "aspose-cells-cloud-gists" "1f9b294ef1cfb23e3775c193f15ff660" >}}

{{< /tab >}}

{{< /tabs >}}