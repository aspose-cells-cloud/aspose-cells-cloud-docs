---
title: "Ajustar automáticamente una fila en una hoja de cálculo de Excel"
second_title: "Document"
linktype: "Row"
type: docs
url: /es/worksheets/autofit/row/
aliases: [  /es/autofit-single-row-of-worksheet/ ]
description: "Aprenda cómo utilizar la API REST de Aspose.Cells Cloud para ajustar automáticamente una fila en una hoja de cálculo de Excel. Incluye el punto final, los parámetros, la autenticación, el manejo de errores, la solicitud cURL y ejemplos de SDK."
keywords: "ajustar automáticamente fila, Aspose.Cells Cloud, API de Excel, REST, hoja de cálculo, SDK, hoja de cálculo, API en la nube"
weight: 30
ArticleTitle: "Ajustar automáticamente una fila en una hoja de cálculo de Excel usando la API de Aspose.Cells Cloud"
---

Esta API REST **ajusta automáticamente una fila** en una hoja de cálculo de Excel.

## Seguridad y autenticación
Las API de Aspose.Cells Cloud son seguras y requieren [autenticación basada en token JWT](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/).

## API REST

```bash
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/autofitrow
```

### **Parámetros de la solicitud**

| Nombre del parámetro | Tipo    | Ubicación | Descripción                                                                                                                                                                                                  |
| --------------------- | ------- | --------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| name                  | string  | path      | El nombre del archivo de Excel.                                                                                                                                                                              |
| sheetName             | string  | path      | El nombre de la hoja de cálculo.                                                                                                                                                                             |
| rowIndex              | integer | query     | Índice de fila basado en cero que se ajustará automáticamente.                                                                                                                                               |
| firstColumn           | integer | query     | Índice de la primera columna incluida en la operación.                                                                                                                                                       |
| lastColumn            | integer | query     | Índice de la última columna incluida en la operación.                                                                                                                                                        |
| autoFitterOptions     | object  | body      | Objeto que controla el comportamiento del ajuste automático (por ejemplo, si se deben considerar celdas fusionadas, texto ajustado, etc.). Consulte [AutoFitterOptions](/cells/auto-fitter-options){:rel="noopener" title="Controla el comportamiento del ajuste automático"}. |
| folder                | string  | query     | Carpeta donde se almacena el archivo.                                                                                                                                                                        |
| storageName           | string  | query     | Nombre del almacenamiento.                                                                                                                                                                                   |

**Ejemplo de cuerpo JSON para `autoFitterOptions`**

```json
{
  "IsMergedCells": true,
  "IsWrapped": false,
  "AutoFitMergedCells": true,
  "AutoFitWrappedCells": false
}
```

### Definiciones de entidades

| Entidad               | Descripción                                                                                  |
| --------------------- | -------------------------------------------------------------------------------------------- |
| `rowIndex`            | Índice basado en cero de la fila de destino.                                                 |
| `firstColumn`         | Columna inicial para la operación de ajuste automático.                                      |
| `lastColumn`          | Columna final para la operación de ajuste automático.                                        |
| `autoFitterOptions`   | Configuraciones opcionales que influyen en cómo se ajusta automáticamente la fila (celdas fusionadas, texto ajustado, etc.). |

La [Especificación OpenAPI](/cells/#/Worksheets/PostAutofitWorksheetRow) define una interfaz de programación pública accesible y permite realizar interacciones REST directamente desde un navegador web.

Puede utilizar la herramienta de línea de comandos cURL para acceder fácilmente a los servicios web de Aspose.Cells. El ejemplo siguiente muestra cómo llamar a la API mediante cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Solicitud" tabName2="Respuesta" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/sampleAutoFit.xlsx/worksheets/Sheet1/autofitrow?rowIndex=2&firstColumn=1&lastColumn=10" \
  -X POST \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

| Campo  | Descripción                               |
| ------ | ----------------------------------------- |
| Code   | `200` – solicitud exitosa.                |
| Status | `"OK"` – la fila se ajustó automáticamente. |

{{< /tab >}}

{{< /tabs >}}

## Manejo de errores

La API devuelve códigos de estado HTTP estándar. Las respuestas de error comunes para este punto final son:

| Código HTTP | Ejemplo de carga útil                                    | Significado                                                                              |
| ----------- | -------------------------------------------------------- | ---------------------------------------------------------------------------------------- |
| 400         | `{ "Code": 400, "Message": "Row index out of range." }`  | El `rowIndex` proporcionado no existe en la hoja de cálculo.                             |
| 401         | `{ "Code": 401, "Message": "Invalid or expired token." }` | Falló la autenticación: verifique el token JWT y asegúrese de que la solicitud sea por HTTPS. |
| 404         | `{ "Code": 404, "Message": "File not found." }`          | No se puede encontrar el archivo de Excel o la hoja de cálculo especificados.            |
| 500         | `{ "Code": 500, "Message": "Internal server error." }`   | Se produjo un problema inesperado del lado del servidor.                                 |

## Familia de SDK en la nube

Utilizar un SDK es la forma más rápida de desarrollar. Un SDK abstracta los detalles de bajo nivel, permitiéndole centrarse en la lógica de su negocio. Consulte el [repositorio de GitHub](https://github.com/aspose-cells-cloud){:rel="noopener noreferrer"} para obtener una lista completa de los SDK de Aspose.Cells Cloud.

Los siguientes ejemplos de código muestran cómo llamar a los servicios web de Aspose.Cells mediante diversos SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostAutofitWorksheetRow.cs" >}}
{{< /tab >}}

{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostAutofitWorksheetRow.java" >}}
{{< /tab >}}

{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostAutofitWorksheetRow.php" >}}
{{< /tab >}}

{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostAutofitWorksheetRow.rb" >}}
{{< /tab >}}

{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2c4189bc27ae92abf73c36b4df0" "Example_PostAutofitWorksheetRow.ts" >}}
{{< /tab >}}

{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostAutofitWorksheetRow.py" >}}
{{< /tab >}}

{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostAutofitWorksheetRow.pl" >}}
{{< /tab >}}

{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostAutofitWorksheetRow.go" >}}
{{< /tab >}}

{{< /tabs >}}

**Consulte también:** [Ajustar columna automáticamente](/worksheets/autofit/column/), [Ajustar filas automáticamente](/worksheets/autofit/rows/), [AutoFitterOptions](/cells/auto-fitter-options).