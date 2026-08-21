---
title: "Ordenar datos de un rango en una hoja de cálculo de Excel"
second_title: "Documento"
linktitle: "Ordenar"
type: docs
url: /es/worksheets/sort-data/
aliases: [  /es/sort-worksheet-data/ ]
keywords: "Aspose.Cells Cloud, API de ordenación de Excel, ordenación de rango en hoja de cálculo, API REST, dataSorter"
description: "Ordenar un rango específico en una hoja de cálculo de Excel mediante la API REST de Aspose.Cells Cloud. Incluye el endpoint, los parámetros necesarios, los pasos de autenticación, el manejo de errores y ejemplos de SDK."
weight: 20
---

La API REST ordena los datos dentro de un rango especificado en una hoja de cálculo de Excel.

## API REST

```shell
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/sort
```

### Parámetros de la solicitud

| Nombre del parámetro | Tipo   | Ubicación | Obligatorio | Descripción                                                                 |
| --------------------- | ------ | --------- | ----------- | --------------------------------------------------------------------------- |
| name                  | string | path      | Sí          | Nombre del libro de trabajo.                                                |
| sheetName             | string | path      | Sí          | Nombre de la hoja de cálculo.                                               |
| cellArea              | string | query     | Sí          | Rango de celdas que se va a ordenar (por ejemplo, `A5:A10`).                |
| dataSorter            | object | body      | Sí          | Objeto JSON que define la configuración de ordenación (véase el esquema a continuación). |
| folder                | string | query     | No          | Carpeta que contiene el libro de trabajo.                                   |
| storageName           | string | query     | No          | Nombre del almacenamiento donde se encuentra el libro de trabajo.           |

**Esquema del objeto `dataSorter`** – El cuerpo debe contener un objeto JSON con las siguientes propiedades:

- `CaseSensitive` _(booleano, obligatorio)_ – Determina si la ordenación distingue entre mayúsculas y minúsculas.
- `HasHeaders` _(booleano, obligatorio)_ – Indica si el rango incluye una fila de encabezados.
- `KeyList` _(matriz, obligatoria)_ – Colección de claves de ordenación. Cada objeto clave incluye:
  - `Key` _(entero)_ – Índice de columna en base cero.
  - `SortOrder` _(cadena)_ – `"ascending"` (ascendente) o `"descending"` (descendente).
- `SortLeftToRight` _(booleano, obligatorio)_ – Si es `true`, la ordenación se realiza de izquierda a derecha; de lo contrario, de arriba a abajo.
- Opcionalmente, también pueden proporcionarse `CaseOrder`, `SortLeftToRight`, etc., según la especificación OpenAPI.

La [Especificación OpenAPI](https://apireference.aspose.cloud/cells/#/Worksheets/PostWorksheetRangeSort) define una interfaz de programación accesible públicamente y permite realizar interacciones REST directamente desde un navegador web.

Puede utilizar la herramienta de línea de comandos cURL para acceder fácilmente a los servicios web de Aspose.Cells. El siguiente ejemplo muestra cómo realizar una llamada a la API en la nube mediante cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Solicitud" tabName2="Respuesta" >}}

{{< tab tabNum="1" >}}

```shell
curl -v "https://api.aspose.cloud/v3.0/cells/Sample_Test_Book.xls/worksheets/Sheet1/sort?cellArea=A5:A10" \
  -X POST \
  -d '{"CaseSensitive":false,"HasHeaders":false,"KeyList":[{"Key":0,"SortOrder":"descending"}],"SortLeftToRight":false}' \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
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

**Manejo de errores** – La API puede devolver códigos de error HTTP estándar. Las respuestas típicas incluyen:

| Estado HTTP | Código | Mensaje                                                       |
| ----------- | ------ | ------------------------------------------------------------- |
| 400         | 400    | Solicitud incorrecta: faltan o son inválidos los parámetros. |
| 401         | 401    | No autorizado: token JWT inválido o ausente.                  |
| 404         | 404    | No encontrado: el libro de trabajo o la hoja de cálculo no existen. |
| 500         | 500    | Error interno del servidor.                                   |

El cuerpo de respuesta sigue el patrón `{ "Code": <status>, "Message": "<description>", "Status": "Error" }` en los casos de error.

## Familia de SDK en la nube

Utilizar un SDK es la forma más rápida de desarrollar. Un SDK gestiona los detalles de bajo nivel, permitiéndole centrarse en las tareas de su proyecto. Consulte el [repositorio de GitHub](https://github.com/aspose-cells-cloud) para obtener una lista completa de los SDK de Aspose.Cells Cloud.

Los siguientes ejemplos de código muestran cómo invocar los servicios web de Aspose.Cells mediante diversos SDK:

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-.NET-CellsWorksheetsPostWorksheetRangeSort.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-worksheet-SortWorksheetData-sort-worksheet-data.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Worksheet-PostWorksheetRangeSort-.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Worksheet-sort_worksheet_range-.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "SortWorkSheetData.py" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-Worksheet-SortWorksheetData-1.js" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "9d725d4678edaac53f95c5208e17783c" "Examples-Android-worksheet-SortWorksheetData-sort-worksheet-data.java" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-Worksheet-SortWorksheetData-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< gist "aspose-cells-cloud-gists" "48dd9dae5e2188a64e2284bb12b9201b" >}}

{{< /tab >}}

{{< /tabs >}}