---
title: "Ajustar automáticamente varias filas en una hoja de cálculo de Excel"
second_title: "Documento"
linktitle: "Filas"
type: docs
url: /es/worksheets/autofit/rows/
aliases: [  /es/autofit-multiple-rows-of-worksheet/ ]
keywords: "ajustar automáticamente filas, Excel, Aspose.Cells Cloud, API REST, hoja de cálculo, hoja de cálculo"
description: "Aprenda cómo utilizar la API REST de Aspose.Cells Cloud para ajustar automáticamente varias filas en una hoja de cálculo de Excel. Incluye sintaxis de solicitud, parámetros, ejemplo de cURL, fragmentos de SDK y manejo de errores."
weight: 40
ArticleTitle: "Ajustar automáticamente varias filas en una hoja de cálculo de Excel – Documentación de la API de Aspose.Cells Cloud"
---

Esta API REST ajusta automáticamente la altura de las filas en una hoja de cálculo de Excel.

## Seguridad y autenticación
Las API de Aspose.Cells Cloud son seguras y requieren [autenticación basada en token JWT](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/).

## API REST

```bash
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/autofitrows
```

### **Parámetros de la solicitud**

| Nombre del parámetro    | Tipo    | Ubicación | Descripción                                                                                                                           | Obligatorio |
| ----------------------- | ------- | --------- | ------------------------------------------------------------------------------------------------------------------------------------- | ----------- |
| **name**                | string  | path      | El nombre del archivo de Excel.                                                                                                       | ✔           |
| **sheetName**           | string  | path      | El nombre de la hoja de cálculo.                                                                                                      | ✔           |
| **autoFitterOptions**   | object  | body      | Opciones que controlan cómo se ajustan automáticamente las filas (por ejemplo, ignorar filas ocultas). Consulte la descripción breve de los campos a continuación. | ✖           |
| **startRow**            | integer | query     | La primera fila que se ajustará automáticamente (índice basado en 1).                                                                | ✔           |
| **endRow**              | integer | query     | La última fila que se ajustará automáticamente (incluida).                                                                            | ✔           |
| **onlyAuto**            | boolean | query     | Si es `true`, la API ajusta únicamente las filas cuya altura se calcula automáticamente por Excel. Si es `false`, se realiza un ajuste completo. | ✖           |
| **folder**              | string  | query     | La carpeta que contiene el documento.                                                                                                 | ✖           |
| **storageName**         | string  | query     | El nombre del servicio de almacenamiento.                                                                                            | ✖           |

Campos de **autoFitterOptions** (todos opcionales):

- `AutoFitMergedCells` _(boolean)_ – Si es `true`, se tienen en cuenta las celdas fusionadas al calcular la altura de la fila.
- `IgnoreHidden` _(boolean)_ – Si es `true`, se ignoran las filas ocultas durante el proceso de ajuste automático.
- `OnlyAuto` _(boolean)_ – Replica el parámetro de consulta `onlyAuto`; cuando se establece, sobrescribe el valor de la consulta.

La [Especificación OpenAPI](https://apireference.aspose.cloud/cells/#/Worksheets/PostAutofitWorksheetRows) define una interfaz de programación públicamente accesible y permite realizar interacciones REST directamente desde un navegador web.

Puede utilizar la herramienta de línea de comandos cURL para acceder fácilmente a los servicios web de Aspose.Cells. El siguiente ejemplo muestra cómo llamar a la API en la nube mediante cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Solicitud" tabName2="Respuesta" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/sampleAutoFit.xlsx/worksheets/Sheet1/autofitrows?startRow=1&endRow=7" \
  -X POST \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>" \
  -d '{"AutoFitMergedCells": true, "IgnoreHidden": true, "OnlyAuto": false}'
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

Las respuestas de error típicas incluyen:

- **400 Bad Request** – Valores de parámetros no válidos o cuerpo JSON con formato incorrecto.
- **401 Unauthorized** – Token JWT ausente o no válido.
- **404 Not Found** – El archivo o la hoja de cálculo especificados no existen.
- **500 Internal Server Error** – Se produjo un error inesperado en el servidor.

**Códigos de estado HTTP**

| Código | Significado                 | Descripción                                     |
|--------|-----------------------------|-------------------------------------------------|
| 200    | OK                          | Filtro aplicado correctamente; la respuesta contiene detalles de la operación. |
| 400    | Bad Request                 | Parámetros ausentes o no válidos (por ejemplo, tipo de archivo no admitido). |
| 401    | Unauthorized                | Token JWT no válido o ausente. |
| 413    | Payload Too Large           | El archivo cargado supera el límite de tamaño. |
| 500    | Internal Server Error       | Error inesperado en el servidor. |

{{< /tab >}}

{{< /tabs >}}

## Familia de SDK en la nube

Utilizar un SDK es la forma más rápida de desarrollar. Un SDK maneja los detalles de bajo nivel, permitiéndole centrarse en su proyecto. Consulte el [repositorio de GitHub](https://github.com/aspose-cells-cloud) para obtener una lista completa de los SDK de Aspose.Cells Cloud.

Los siguientes ejemplos de código muestran cómo llamar a los servicios web de Aspose.Cells mediante diversos SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostAutofitWorksheetRows.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostAutofitWorksheetRows.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostAutofitWorksheetRows.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostAutofitWorksheetRows.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostAutofitWorksheetRows.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostAutofitWorksheetRows.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostAutofitWorksheetRows.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostAutofitWorksheetRows.go" >}}

{{< /tab >}}

{{< /tabs >}}