---
title: "Aspose.Cells Cloud API: Fusionar rango de celdas"
second_title: "Documento"
linktitle: "Fusionar"
type: docs
url: /ranges/merge/
aliases: [/combines-a-range-of-cells-into-a-single-cell/]
keywords: "Aspose.Cells, fusionar celdas, API de Excel, REST, SDK en la nube"
description: "Fusiona un rango de celdas en una sola celda utilizando la API REST de Aspose.Cells Cloud. Aprenda sobre el formato de la solicitud, los parámetros y ejemplos de SDK para C#, Java, Python y más."
weight: 20
---

Esta API REST fusiona un rango de celdas en una sola celda en una hoja de cálculo de Excel.

**Descripción general**: La fusión de un rango combina las celdas seleccionadas en una sola celda, preservando el valor de la celda superior izquierda y descartando el resto. Utilice esta operación cuando necesite crear un encabezado que abarque varias columnas o filas, o cuando desee simplificar la disposición de una hoja de cálculo.

## API REST

```bash
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/ranges/merge
```

### **Parámetros de solicitud**

| Nombre del parámetro | Tipo   | Ubicación | Descripción                                           |
|----------------------|--------|-----------|-------------------------------------------------------|
| **name**             | string | path      | Nombre del libro de trabajo.                         |
| **sheetName**        | string | path      | Nombre de la hoja de cálculo.                        |
| **range**            | object | body      | Objeto de rango que especifica las celdas a fusionar. |
| **folder**           | string | query     | Carpeta donde se almacena el libro de trabajo.       |
| **storageName**      | string | query     | Nombre del almacenamiento.                           |

#### Esquema del cuerpo de solicitud

El objeto **Range** debe contener los siguientes campos (todos los demás son opcionales):

| Propiedad       | Tipo    | Obligatorio | Descripción                                              |
|-----------------|---------|-------------|----------------------------------------------------------|
| **FirstRow**    | integer | Sí          | Índice de fila (base cero) de la primera fila del rango. |
| **FirstColumn** | integer | Sí          | Índice de columna (base cero) de la primera columna del rango. |
| **RowCount**    | integer | Sí          | Número de filas que se incluirán en el rango.            |
| **ColumnCount** | integer | Sí          | Número de columnas que se incluirán en el rango.         |
| **Name**        | string  | No          | Nombre opcional para el rango.                           |
| **RefersTo**    | string  | No          | Fórmula a la que hace referencia el rango.               |
| **Worksheet**   | string  | No          | Nombre de la hoja de cálculo (si difiere del parámetro de ruta). |
| **RowHeight**   | number  | No          | Altura de las filas en el rango (en píxeles).            |
| **ColumnWidth** | number  | No          | Ancho de las columnas en el rango (en píxeles).          |

Puede utilizar la herramienta de línea de comandos cURL para acceder fácilmente a los servicios web de Aspose.Cells. El siguiente ejemplo muestra cómo realizar una llamada a la API en la nube mediante cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Solicitud" tabName2="Respuesta" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/ranges/merge" \
  -X POST \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>" \
  -d '{
        "FirstRow": 9,
        "FirstColumn": 0,
        "RowCount": 1,
        "ColumnCount": 7
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

{{< /tab >}}

{{< /tabs >}}

#### Detalles de la respuesta

| Estado HTTP                   | Descripción                                                | JSON de ejemplo                                            |
|-------------------------------|------------------------------------------------------------|------------------------------------------------------------|
| **200 OK**                    | El rango se fusionó correctamente.                         | `{ "Code": 200, "Status": "OK" }`                          |
| **400 Bad Request**           | Parámetros de rango no válidos (por ejemplo, índices fuera de rango). | `{ "Code": 400, "Message": "Invalid range." }`             |
| **401 Unauthorized**          | Token JWT ausente o no válido.                             | `{ "Code": 401, "Message": "Authentication failed." }`     |
| **404 Not Found**             | Libro de trabajo o hoja de cálculo no encontrados.         | `{ "Code": 404, "Message": "Resource not found." }`        |
| **500 Internal Server Error** | Error interno inesperado del servidor.                     | `{ "Code": 500, "Message": "Internal server error." }`     |

## Familia de SDK en la nube

Utilizar un SDK es la mejor forma de acelerar el desarrollo. Un SDK gestiona los detalles de bajo nivel para que usted pueda centrarse en las tareas de su proyecto. Consulte el [repositorio de GitHub](https://github.com/aspose-cells-cloud) para obtener una lista completa de los SDK de Aspose.Cells Cloud.

Los siguientes ejemplos de código muestran cómo invocar los servicios web de Aspose.Cells mediante diversos SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostWorksheetCellsRangeMerge.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostWorksheetCellsRangeMerge.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostWorksheetCellsRangeMerge.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostWorksheetCellsRangeMerge.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostWorksheetCellsRangeMerge.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostWorksheetCellsRangeMerge.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostWorksheetCellsRangeMerge.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostWorksheetCellsRangeMerge.go" >}}

{{< /tab >}}

{{< /tabs >}}