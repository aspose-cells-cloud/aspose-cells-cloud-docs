---
title: "Copiar un rango en una hoja de cálculo con opciones de pegado"
second_title: "Document"
linktype: "Copiar"
type: docs
url: /es/ranges/copy/
aliases: [  /es/copy-range-in-a-worksheet-with-paste-options/ ]
keywords: "Aspose.Cells Cloud, API REST, Excel, copiar rango, hoja de cálculo, opciones de pegado"
description: "Use la API REST de Aspose.Cells Cloud para copiar un rango dentro de una hoja de cálculo de Excel con soporte completo para opciones de pegado. Incluye ejemplos de SDK para múltiples lenguajes de programación."
weight: 20
ArticleTitle: "Copiar un rango en una hoja de cálculo con opciones de pegado – API de Aspose.Cells Cloud"
---

Esta API REST copia un rango en una hoja de cálculo de un libro de Excel. Para operaciones relacionadas, consulte la documentación sobre **Obtener rango** y **Actualizar rango**.

**Requisitos previos:** Para usar este endpoint, debe tener un token válido de OAuth 2.0 / JWT y asegurarse de que su versión de API coincida con la URL de la solicitud.

## API REST

```bash
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/ranges
```

### **Parámetros de la solicitud**

| Nombre del parámetro | Tipo   | Ubicación | Descripción                                                                          |
| --------------------- | ------ | --------- | ------------------------------------------------------------------------------------ |
| name                  | string | path      | El nombre del libro de cálculo.                                                      |
| sheetName             | string | path      | El nombre de la hoja de cálculo.                                                     |
| rangeOperate          | string | body      | La operación a realizar: `copydata`, `copystyle`, `copyto` o `copyvalue`.           |
| folder                | string | query     | La carpeta que contiene el libro de cálculo.                                         |
| storageName           | string | query     | El nombre del servicio de almacenamiento.                                            |

**Notas:** El campo `rangeOperate` determina qué se copia. Use `copydata` para copiar únicamente los valores de las celdas, `copystyle` para el formato, `copyto` para ambos (datos y formato), y `copyvalue` para copiar valores sin fórmulas. La API admite rangos de hasta 1 millón de celdas; rangos más grandes podrían provocar un tiempo de espera.

La [Especificación OpenAPI](https://apireference.aspose.cloud/cells/#/Ranges/PostWorksheetCellsRangesCopy) define una interfaz de programación pública accesible y le permite realizar interacciones REST directamente desde un navegador web.

Puede utilizar la herramienta de línea de comandos cURL para acceder fácilmente a los servicios web de Aspose.Cells. El siguiente ejemplo muestra cómo realizar llamadas a la API en la nube mediante cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Solicitud" tabName2="Respuesta" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/ranges" \
  -X POST \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>" \
  -d '{
        "Operate": "string",
        "Source": {
          "ColumnCount": 0,
          "ColumnWidth": 0,
          "FirstColumn": 0,
          "FirstRow": 0,
          "Name": "string",
          "RefersTo": "string",
          "RowCount": 0,
          "RowHeight": 0,
          "Worksheet": "string"
        },
        "Target": {
          "ColumnCount": 0,
          "ColumnWidth": 0,
          "FirstColumn": 0,
          "FirstRow": 0,
          "Name": "string",
          "RefersTo": "string",
          "RowCount": 0,
          "RowHeight": 0,
          "Worksheet": "string"
        },
        "PasteOptions": {
          "OnlyVisibleCells": true,
          "PasteType": "string",
          "SkipBlanks": true,
          "Transpose": true
        }
      }'
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

La respuesta correcta devuelve un código de estado `200 OK`. En caso de error, la API puede devolver cargas útiles como:

```json
{
  "Code": 400,
  "Message": "Bad Request – parámetros no válidos."
}
```

o

```json
{
  "Code": 401,
  "Message": "Unauthorized – token de autenticación faltante o no válido."
}
```

Estos objetos de error incluyen un código de estado HTTP y un mensaje descriptivo para ayudar a diagnosticar problemas.

{{< /tab >}}

{{< /tabs >}}

Puede descargar un libro de cálculo de ejemplo para probar la operación de copia [aquí](https://example.com/sample.xlsx).

## Familia de SDK en la nube

Utilizar un SDK es la mejor manera de acelerar el desarrollo. Un SDK gestiona los detalles de bajo nivel para que usted pueda centrarse en las tareas de su proyecto. Consulte el [repositorio de GitHub](https://github.com/aspose-cells-cloud) para ver una lista completa de los SDK de Aspose.Cells Cloud.

Los siguientes ejemplos de código muestran cómo invocar los servicios web de Aspose.Cells mediante diversos SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostWorksheetCellsRangesCopy.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostWorksheetCellsRangesCopy.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostWorksheetCellsRangesCopy.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostWorksheetCellsRangesCopy.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostWorksheetCellsRangesCopy.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostWorksheetCellsRangesCopy.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostWorksheetCellsRangesCopy.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostWorksheetCellsRangesCopy.go" >}}

{{< /tab >}}

{{< /tabs >}}