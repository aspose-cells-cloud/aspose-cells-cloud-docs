---
title: "Ocultar filas en una hoja de cálculo de Excel"
second_title: "Document"
linktype: "Ocultar"
type: docs
url: /rows/hide/
aliases: [/hide-rows-in-excel-worksheet/]
keywords: "ocultar filas, Aspose.Cells Cloud, API de Excel, REST, SDK"
description: "Aprenda a ocultar una o varias filas en una hoja de cálculo de Excel mediante la API REST de Aspose.Cells Cloud. Incluye ejemplo con cURL, fragmentos de código de SDK, parámetros, autenticación, detalles de respuesta y manejo de errores."
weight: 40
ArticleTitle: "Ocultar filas en una hoja de cálculo de Excel mediante la API de Aspose.Cells Cloud"
---

Esta API REST oculta filas en una hoja de cálculo de Excel.

**Requisitos previos:** Un token JWT Bearer válido obtenido del endpoint OAuth de Aspose Cloud, el libro almacenado en el almacenamiento de Aspose Cloud y el nombre de la hoja de cálculo que contiene las filas que se van a ocultar. La API funciona con archivos de Excel en formatos XLS, XLSX y otros compatibles.

## API PostHideWorksheetRows

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/rows/hide
```

### **Seguridad y autenticación**

Las API de Aspose.Cells Cloud son seguras y requieren <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">autenticación basada en token JWT</a>.

### Parámetros de solicitud

| Parámetro       | Tipo    | Ubicación | Descripción                                                                 |
|-----------------|---------|-----------|-----------------------------------------------------------------------------|
| **name**        | string  | path      | Nombre del archivo del libro.                                               |
| **sheetName**   | string  | path      | Nombre de la hoja de cálculo que contiene las filas que se van a ocultar.   |
| **startrow**    | integer | query     | Índice de base cero de la primera fila que se va a ocultar.                 |
| **totalRows**   | integer | query     | Número de filas consecutivas que se van a ocultar, comenzando desde **startrow**. |
| **folder**      | string  | query     | Carpeta en el almacenamiento donde se encuentra el libro.                   |
| **storageName** | string  | query     | Nombre del servicio de almacenamiento.                                      |

La [Especificación de OpenAPI](https://apireference.aspose.cloud/cells/#/Cells/PostHideWorksheetRows) proporciona una interfaz de programación públicamente accesible que permite realizar interacciones REST directamente desde un navegador web.

Puede utilizar la herramienta de línea de comandos **cURL** para llamar a los servicios web de Aspose.Cells. La API requiere un token JWT Bearer obtenido del endpoint OAuth de Aspose Cloud; inclúyalo en la cabecera `Authorization`. El ejemplo siguiente demuestra cómo ocultar una fila mediante cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Solicitud" tabName2="Respuesta" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/cells/rows/hide?startrow=1&totalRows=1" \
  -X POST \
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

**Códigos de estado de respuesta**

| Código | Descripción                              |
|--------|------------------------------------------|
| 200    | Éxito – filas ocultas                    |
| 400    | Solicitud incorrecta – parámetros no válidos |
| 401    | No autorizado – token JWT faltante o inválido |
| 404    | No encontrado – el libro o la hoja de cálculo no existen |
| 500    | Error del servidor – fallo interno de procesamiento |

Una llamada exitosa devuelve un objeto JSON que contiene los campos `Code` y `Status`. En caso de error, la respuesta incluye campos adicionales como `Message` y los códigos de estado HTTP apropiados (por ejemplo, 400, 401, 404, 500).

**Notas:** Asegúrese de que el valor de `startrow` esté dentro del rango de filas de la hoja de cálculo; de lo contrario, la API devolverá un error 400. Los índices de fila son de base cero, por lo que `startrow=0` se refiere a la primera fila.

## Familia de SDK en la nube

Utilizar un SDK es la forma más rápida de integrar esta funcionalidad en su aplicación. Los SDK manejan los detalles de bajo nivel, para que pueda centrarse en la lógica de negocio. Consulte el [repositorio de GitHub](https://github.com/aspose-cells-cloud) para ver una lista completa de los SDK de Aspose.Cells Cloud.

Los siguientes ejemplos de código muestran cómo ocultar filas mediante varios SDK. (Los nombres de los archivos de ejemplo hacen referencia a “Unhide” debido a una nomenclatura heredada; el código incluido en cada fragmento realiza la operación **Ocultar**).

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostUnhideWorksheetRows.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostUnhideWorksheetRows.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostUnhideWorksheetRows.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostUnhideWorksheetRows.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostUnhideWorksheetRows.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostUnhideWorksheetRows.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostUnhideWorksheetRows.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostUnhideWorksheetRows.go" >}}

{{< /tab >}}

{{< /tabs >}}