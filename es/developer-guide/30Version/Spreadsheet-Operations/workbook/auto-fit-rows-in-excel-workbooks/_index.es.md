---
title: "Ajustar filas automáticamente en un libro de Excel"
second_title: "Documento"
linktitle: "Filas"
type: docs
url: /es/autofit-rows-on-an-excel-file/
aliases: [  /es/auto-fit-rows-in-excel-workbooks/ , /es/workbook/autofit/rows/ ]
keywords: "ajustar filas automáticamente, libro de Excel, Aspose.Cells Cloud, API REST, opciones de ajuste automático"
description: "Aprenda a ajustar automáticamente la altura de las filas en un libro de Excel utilizando la API REST de Aspose.Cells Cloud. Incluye el punto final, parámetros, ejemplo de cURL y fragmentos de SDK para C#, Java, Python y más."
weight: 90
ArticleTitle: "Ajustar filas automáticamente en un libro de Excel – Aspose.Cells Cloud API"
---

**Requisitos previos**  
Antes de llamar a la API, obtenga un token Bearer JWT válido del servicio de autenticación de Aspose y asegúrese de que el libro de trabajo objetivo esté almacenado en una ubicación compatible (almacenamiento predeterminado o uno personalizado que haya configurado).

Esta API REST le permite **ajustar automáticamente las filas** en un libro de Excel, ajustando automáticamente la altura de las filas después de insertar o modificar datos.

## API REST

```bash
POST https://api.aspose.cloud/v3.0/cells/{name}/autofitrows
```

Los parámetros de la solicitud incluyen:

| Nombre del parámetro | Tipo              | Ubicación | Descripción                                                                     |
| ------------------- | ----------------- | -------- | ------------------------------------------------------------------------------- |
| name                | string            | path     | Nombre del archivo del libro de trabajo.                                       |
| autoFitterOptions   | AutoFitterOptions | body     | Opciones que controlan el comportamiento del ajuste automático.               |
| startRow            | integer           | query    | Índice de la primera fila que se ajustará automáticamente.                     |
| endRow              | integer           | query    | Índice de la última fila que se ajustará automáticamente.                      |
| firstColumn         | integer           | query    | Índice de la primera columna considerada para el ajuste automático.            |
| lastColumn          | integer           | query    | Índice de la última columna considerada para el ajuste automático.             |
| onlyAuto            | boolean           | query    | Si es **true**, solo se procesan las filas con la bandera de ajuste automático (predeterminado: **false**). |
| folder              | string            | query    | Ruta de la carpeta donde se almacena el libro de trabajo.                      |
| storageName         | string            | query    | Nombre del servicio de almacenamiento.                                         |

**AutoFitterOptions** es un objeto que especifica cómo se comporta la operación de ajuste automático (por ejemplo, `AutoFitMergedCells`, `IgnoreHidden`).

**Códigos de estado HTTP**

| Código | Significado                 | Descripción                                      |
|--------|-----------------------------|--------------------------------------------------|
| 200    | Correcto                    | Filtro aplicado correctamente; la respuesta contiene detalles de la operación. |
| 400    | Solicitud incorrecta        | Parámetros faltantes o no válidos (por ejemplo, tipo de archivo no admitido). |
| 401    | No autorizado               | Token JWT inválido o ausente. |
| 413    | Payload demasiado grande     | El archivo cargado supera el límite de tamaño. |
| 500    | Error interno del servidor  | Error inesperado en el servidor. |

La [Especificación OpenAPI](https://apireference.aspose.cloud/cells/#/Workbook/PostAutofitWorkbookRows) define una interfaz de programación accesible públicamente y le permite realizar interacciones REST directamente desde un navegador web.

Puede utilizar la herramienta de línea de comandos cURL para llamar a los servicios web de Aspose.Cells. Reemplace `<jwt token>` por un token Bearer JWT válido obtenido del servicio de autenticación de Aspose.

{{< tabs tabTotal="2" tabID="1" tabName1="Solicitud" tabName2="Respuesta" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/myWorkbook.xlsx/autofitrows" \
  -X POST \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>" \
  -d '{"AutoFitMergedCells":true, "IgnoreHidden":true}'
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

*Ejemplo de respuesta de error (por ejemplo, libro de trabajo ausente):*

```json
{
  "Code": 404,
  "Status": "Not Found",
  "Message": "El libro de trabajo especificado 'myWorkbook.xlsx' no existe."
}
```

{{< /tab >}}

{{< /tabs >}}

**Notas**  
- Cuando `AutoFitMergedCells` se establece en **true**, las celdas fusionadas se consideran como una única entidad durante la operación de ajuste automático.  
- Establecer `IgnoreHidden` en **true** omite las filas y columnas ocultas, preservando sus dimensiones actuales.

## Familia de SDK en la nube

Utilizar un SDK es la forma más rápida de desarrollar. Un SDK abstracta los detalles de bajo nivel para que pueda concentrarse en su proyecto. Consulte el [repositorio de GitHub](https://github.com/aspose-cells-cloud) para ver una lista completa de los SDK de Aspose.Cells Cloud.

Los siguientes ejemplos de código muestran cómo llamar a los servicios web de Aspose.Cells utilizando diversos SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostAutofitWorkbookRows.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostAutofitWorkbookRows.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostAutofitWorkbookRows.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostAutofitWorkbookRows.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostAutofitWorkbookRows.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostAutofitWorkbookRows.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostAutofitWorkbookRows.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostAutofitWorkbookRows.go" >}}

{{< /tab >}}

{{< /tabs >}}