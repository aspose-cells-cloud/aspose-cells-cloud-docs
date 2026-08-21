---
title: "Ajustar automáticamente columnas en un archivo de Excel"
second_title: "Documento"
linktitle: "Columnas"
type: docs
url: /autofit-columns-on-an-excel-file/
aliases:
  [
    /auto-fit-columns-in-excel-workbooks,
    /autofit-columns-in-excel-workbooks/,
    /columns/autofit/,
    /workbook/autofit/columns/,
  ]
keywords: "Ajustar automáticamente columnas, Excel, Aspose.Cells Cloud, API REST, SDK, cURL, API"
description: "Aprenda a utilizar la API REST de Aspose.Cells Cloud para ajustar automáticamente columnas en un libro de Excel. Incluye detalles de la solicitud, un ejemplo con cURL y ejemplos de código con SDK para múltiples lenguajes."
weight: 90
---

Esta API REST admite el ajuste automático de columnas en un libro de Excel.

## API PostAutofitWorkbookColumns

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/autofitcolumns
```

Los parámetros de la solicitud son:

| Nombre del parámetro    | Tipo    | Ubicación | Descripción                                         |
| ----------------------- | ------- | --------- | --------------------------------------------------- |
| **name**                | string  | path      | El nombre del archivo del libro.                    |
| **autoFitterOptions**   | object  | body      | Opciones que controlan el comportamiento de ajuste. |
| **startColumn**         | integer | query     | Índice de base cero de la primera columna a ajustar. |
| **endColumn**           | integer | query     | Índice de base cero de la última columna a ajustar.  |
| **folder**              | string  | query     | La carpeta que contiene el libro.                   |
| **storageName**         | string  | query     | El nombre del servicio de almacenamiento.           |

La [Especificación de OpenAPI](https://apireference.aspose.cloud/cells/#/Workbook/PostAutofitWorkbookColumns){:rel="noopener noreferrer"} define una interfaz de programación públicamente accesible y le permite realizar interacciones REST directamente desde un navegador web.

Puede utilizar la herramienta de línea de comandos cURL para acceder fácilmente a los servicios web de Aspose.Cells. El siguiente ejemplo muestra cómo invocar la API en la nube con cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Solicitud" tabName2="Respuesta" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/myWorkbook.xlsx/autofitcolumns" \
-X POST \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>" \
-d '{"AutoFitMergedCells":true, "IgnoreHidden":true}'
```

> **Nota:** Siempre utilice el punto final HTTPS en producción y mantenga su token JWT confidencial.

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

### Requisitos previos
Antes de invocar esta operación, asegúrese de tener una clave válida de la API de Aspose Cloud, un token JWT generado y que el libro de destino ya exista en la ubicación de almacenamiento especificada.

**Códigos de estado HTTP**

| Código | Significado                 | Descripción                                                |
|--------|-----------------------------|------------------------------------------------------------|
| 200    | Correcto                    | Filtro aplicado correctamente; la respuesta contiene detalles de la operación. |
| 400    | Solicitud incorrecta        | Parámetros ausentes o no válidos (p. ej., tipo de archivo no admitido). |
| 401    | No autorizado               | Token JWT no válido o ausente.                             |
| 413    | Payload demasiado grande   | El archivo cargado excede el límite de tamaño.            |
| 500    | Error interno del servidor  | Error inesperado del servidor.                             |

La API puede devolver los siguientes códigos de estado HTTP:

| Código | Descripción                                |
|--------|--------------------------------------------|
| 200    | Correcto – columnas ajustadas automáticamente |
| 400    | Solicitud incorrecta – parámetros ausentes o no válidos |
| 401    | No autorizado – JWT no válido o expirado   |
| 500    | Error del servidor – fallo en el procesamiento interno |

## Familia de SDK en la nube

Utilizar un SDK es la forma más eficiente de acelerar el desarrollo. Un SDK gestiona los detalles de bajo nivel para que usted pueda centrarse en la lógica de su proyecto. Consulte el [repositorio de GitHub](https://github.com/aspose-cells-cloud){:rel="noopener noreferrer"} para ver una lista completa de los SDK de Aspose.Cells Cloud.

Los siguientes ejemplos de código muestran cómo invocar los servicios web de Aspose.Cells utilizando diversos SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostAutofitWorkbookColumns.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostAutofitWorkbookColumns.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostAutofitWorkbookColumns.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostAutofitWorkbookColumns.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostAutofitWorkbookColumns.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostAutofitWorkbookColumns.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostAutofitWorkbookColumns.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostAutofitWorkbookColumns.go" >}}

{{< /tab >}}

{{< /tabs >}}