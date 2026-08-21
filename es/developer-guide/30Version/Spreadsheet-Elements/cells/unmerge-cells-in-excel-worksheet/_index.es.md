---
title: "Desagrupar celdas en una hoja de cálculo de Excel"
type: docs
url: /es/unmerge-cells-in-excel-worksheet/
weight: 120
keywords: "Aspose.Cells, Excel, desagrupar celdas, API REST, SDK en la nube"
description: "Aprenda a utilizar la API REST de Aspose.Cells Cloud para desagrupar celdas en una hoja de cálculo de Excel, con ejemplos de solicitud, formato de respuesta y ejemplos de código del SDK para múltiples lenguajes de programación."
ArticleTitle: "Desagrupar celdas en una hoja de cálculo de Excel"
---

Esta API REST desagrupa celdas en un archivo de Excel.

## API REST

```bash
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/unmerge
```

## Seguridad y autenticación

Las API de Aspose.Cells Cloud son seguras y requieren [autenticación basada en tokens JWT](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/).


**Parámetros de solicitud**

| Nombre del parámetro | Tipo    | Ubicación | Descripción                                             |
|----------------------|---------|-----------|---------------------------------------------------------|
| name                 | string  | path      | Nombre del archivo del libro de trabajo.                |
| sheetName            | string  | path      | Nombre de la hoja de cálculo.                           |
| startRow             | integer | query     | Índice de base cero de la primera fila que se desagrupará. |
| startColumn          | integer | query     | Índice de base cero de la primera columna que se desagrupará. |
| totalRows            | integer | query     | Número de filas que se incluirán en la operación de desagrupación. |
| totalColumns         | integer | query     | Número de columnas que se incluirán en la operación de desagrupación. |
| folder               | string  | query     | Ruta de la carpeta donde se almacena el libro de trabajo. |
| storageName          | string  | query     | Nombre del servicio de almacenamiento.                  |

## **Respuesta**

Devuelve `CellCloudResponse`.

- **Resumen de campos de respuesta**

| Campo           | Tipo    | Descripción                                           |
| --------------- | ------- | ----------------------------------------------------- |
| `Status`        | string  |                                                       |
| `Code`          | integer | 200, 400, 401, 500, ...                               |


```json
{
  "Status":"OK",
  "Code":200
}
```

**Códigos de estado HTTP**

| Código | Significado                 | Descripción                                      |
|--------|-----------------------------|--------------------------------------------------|
| 200    | Correcto                    | Filtro aplicado correctamente; la respuesta contiene los detalles de la operación. |
| 400    | Solicitud incorrecta        | Parámetros faltantes o no válidos (por ejemplo, tipo de archivo no admitido). |
| 401    | No autorizado               | Token JWT no válido o faltante. |
| 413    | Carga útil demasiado grande | El archivo subido supera el límite de tamaño. |
| 500    | Error interno del servidor  | Error inesperado del servidor. |

## Cómo utilizar la API PostWorksheetUnmerge con SDK

### Especificación de la API PostWorksheetUnmerge

La [Especificación OpenAPI](https://apireference.aspose.cloud/cells/#/Cells/PostWorksheetUnmerge) define una interfaz de programación accesible públicamente y le permite realizar interacciones REST directamente desde un navegador web.

Puede utilizar la herramienta de línea de comandos `cURL` para acceder fácilmente a los servicios web de Aspose.Cells. El siguiente ejemplo muestra cómo realizar llamadas a la API en la nube con `cURL`.

{{< tabs tabTotal="2" tabID="11" tabName11="Solicitud" tabName12="Respuesta" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/cells/unmerge?startRow=10&startColumn=10&totalRows=10&totalColumns=10" \
-X POST \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"
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

### Uso de los SDK de Aspose.Cells Cloud

Utilizar un SDK es la mejor forma de acelerar el desarrollo. Un SDK maneja los detalles de bajo nivel y le permite centrarse en las tareas de su proyecto. Consulte el [repositorio de GitHub](https://github.com/aspose-cells-cloud) para obtener una lista completa de los SDK de Aspose.Cells Cloud.

Los siguientes ejemplos de código muestran cómo realizar llamadas a los servicios web de Aspose.Cells utilizando diversos SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostWorksheetUnmerge.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostWorksheetUnmerge.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostWorksheetUnmerge.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostWorksheetUnmerge.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostWorksheetUnmerge.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostWorksheetUnmerge.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostWorksheetUnmerge.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostWorksheetUnmerge.go" >}}

{{< /tab >}}

{{< /tabs >}}