---
title: "Cambiar el ancho de columnas dentro de un rango"
ArticleTitle: "Cambiar el ancho de columnas dentro de un rango – Aspose.Cells Cloud API"
second_title: "Document"
linktitle: "Ancho de columna"
type: docs
url: /ranges/update/column-width/
aliases: [/change-widths-of-columns-inside-the-range/]
keywords: "Aspose.Cells, ancho de columna, REST API, Excel, SDK, rango, nube"
description: "Aprenda cómo cambiar el ancho de columnas dentro de un rango utilizando la API REST de Aspose.Cells Cloud o los SDK (C#, Java, Python, etc.). Incluye cURL, detalles de solicitud/respuesta y pasos de autenticación."
weight: 74
---

Esta API REST establece el ancho de columna de un rango.

## Seguridad y autenticación
Las API de Aspose.Cells Cloud son seguras y requieren [autenticación basada en token JWT](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/).

## API REST

```bash
POST http://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/ranges/columnWidth
```

**Prerrequisitos** – Antes de llamar al punto de conexión, debe:

1. Crear una cuenta de Aspose Cloud y obtener un *client ID* y un *client secret*.  
2. Solicitar un token JWT llamando al punto de conexión OAuth (`/connect/token`). El token se devuelve en el campo `access_token`.  
3. Subir el libro de trabajo objetivo a su almacenamiento en la nube de Aspose Cloud (o asegurarse de que ya exista en la carpeta especificada).  

Los parámetros de la solicitud son:

| Nombre del parámetro | Tipo   | Ubicación | Descripción |
|----------------------|--------|-----------|-------------|
| name                 | string | path      | Nombre del archivo del libro de trabajo |
| sheetName            | string | path      | Nombre de la hoja de cálculo |
| value                | number | query     | Valor deseado para el ancho de columna |
| range                | object | body      | Objeto de rango que define las celdas objetivo |
| folder               | string | query     | Ruta de la carpeta donde se almacena el libro de trabajo |
| storageName          | string | query     | Nombre del servicio de almacenamiento |

La [Especificación OpenAPI](https://apireference.aspose.cloud/cells/#/Ranges/PostWorksheetCellsRangeColumnWidth) define una interfaz de programación públicamente accesible y le permite llevar a cabo interacciones REST directamente desde un navegador web.

Puede utilizar la herramienta de línea de comandos cURL para acceder fácilmente a los servicios web de Aspose.Cells. El siguiente ejemplo muestra cómo realizar llamadas a la API en la nube mediante cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Solicitud" tabName2="Respuesta" >}}

{{< tab tabNum="1" >}}

<h3 id="request">Solicitud</h3>

```bash
# Llamada al punto de conexión de ancho de columna para el libro de trabajo *test.xlsx*,
# hoja de cálculo *Sheet1*, estableciendo el ancho de las columnas seleccionadas en 20 puntos.
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/ranges/columnWidth?value=20" \
  -X POST \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>" \
  -d '{
        "ColumnCount": 7,
        "ColumnWidth": 19,
        "FirstColumn": 0,
        "FirstRow": 9,
        "Name": "string",
        "RefersTo": "string",
        "RowCount": 1,
        "RowHeight": 15,
        "Worksheet": "Sheet1"
      }'
```

{{< /tab >}}

{{< tab tabNum="2" >}}

<h3 id="response">Respuesta</h3>

```json
{
  "Code": 200,
  "Status": "OK"
}
```

*Posibles respuestas de error*  

| Código HTTP | Descripción                                  |
|-------------|----------------------------------------------|
| 400         | Solicitud incorrecta – JSON o parámetros inválidos |
| 401         | No autorizado – token ausente o inválido     |
| 404         | No encontrado – libro de trabajo o hoja de cálculo ausentes |

{{< /tab >}}

{{< /tabs >}}

## Familia de SDK en la nube

Utilizar un SDK es la mejor forma de acelerar el desarrollo. Un SDK gestiona los detalles de bajo nivel, permitiéndole centrarse en las tareas de su proyecto. Consulte el [repositorio de GitHub](https://github.com/aspose-cells-cloud) para obtener una lista completa de los SDK de Aspose.Cells Cloud.

Los siguientes ejemplos de código muestran cómo llamar a los servicios web de Aspose.Cells mediante diversos SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostWorksheetCellsRangeColumnWidth.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostWorksheetCellsRangeColumnWidth.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostWorksheetCellsRangeColumnWidth.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostWorksheetCellsRangeColumnWidth.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostWorksheetCellsRangeColumnWidth.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostWorksheetCellsRangeColumnWidth.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostWorksheetCellsRangeColumnWidth.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostWorksheetCellsRangeColumnWidth.go" >}}

{{< /tab >}}

{{< /tabs >}}

## Preguntas frecuentes

**P:** *¿Qué punto de conexión debo llamar para establecer el ancho de columna de un rango en un libro de Excel?*  
**R:** `POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/ranges/columnWidth`, donde `{name}` es el nombre del archivo del libro de trabajo y `{sheetName}` es la hoja de cálculo objetivo.

**P:** *¿Cómo autentico la solicitud al utilizar la API de ancho de columna?*  
**R:** Incluya el encabezado `Authorization: Bearer <jwt token>`. Obtenga el token JWT mediante el flujo OAuth de Aspose Cloud (`/connect/token`) utilizando su client ID y client secret.

**P:** *¿Qué cuerpo JSON debo enviar para cambiar el ancho de las columnas A a C a 25 puntos?*  
**R:**  

```json
{
  "FirstColumn": 0,
  "ColumnCount": 3,
  "FirstRow": 0,
  "RowCount": 1
}
```

Añada el parámetro de consulta `value=25` a la URL de la solicitud.