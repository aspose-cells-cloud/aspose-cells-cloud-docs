---
title: "Borrar Hipervínculos"
type: docs
url: /hyperlinks/clear/
aliases: [/add-hyperlinks-to-excel-worksheet/]
keywords: "Aspose.Cells Cloud, Excel, borrar hipervínculos, eliminar hipervínculos, REST API, hoja de cálculo, SDK"
description: "Aprenda cómo eliminar todos los hipervínculos de una hoja de cálculo de Excel usando la API REST de Aspose.Cells Cloud o cualquier SDK compatible (C#, Java, Python, Node.js, Go, PHP, Ruby, Perl, etc.)."
weight: 40
ArticleTitle: "Borrar Hipervínculos – Documentación de la API de Aspose.Cells Cloud"
---

Esta API REST elimina **todos los hipervínculos** en una hoja de cálculo de Excel.

## Seguridad y Autenticación
Las API de Aspose.Cells Cloud son seguras y requieren [autenticación basada en token JWT](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/).

## API REST

```bash
DELETE https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/hyperlinks
```

### Parámetros de la solicitud

| Nombre del parámetro | Tipo   | Ubicación | Descripción                                    |
| ------------------- | ------ | --------- | --------------------------------------------- |
| name                | string | path      | El nombre del archivo de Excel.               |
| sheetName           | string | path      | El nombre de la hoja de cálculo.              |
| folder              | string | query     | La carpeta que contiene el documento.         |
| storageName         | string | query     | El nombre del servicio de almacenamiento.     |

### Respuestas de error

| Código HTTP | Motivo                                              | Cuerpo de ejemplo                                                   |
| ----------- | --------------------------------------------------- | ------------------------------------------------------------------- |
| **400**     | Solicitud incorrecta – parámetros ausentes o inválidos. | `{ "Code":"400", "Message":"Valor de parámetro no válido." }`      |
| **401**     | No autorizado – token JWT ausente o inválido.        | `{ "Code":"401", "Message":"El token de acceso está ausente o es inválido." }` |
| **404**     | No encontrado – libro de trabajo o hoja de cálculo no existe. | `{ "Code":"404", "Message":"Archivo no encontrado." }`             |
| **500**     | Error interno del servidor – fallo inesperado del servidor. | `{ "Code":"500", "Message":"Se produjo un error inesperado." }`    |

La [Especificación OpenAPI](https://apireference.aspose.cloud/cells/#/Hyperlinks/DeleteWorksheetHyperlinks) define una interfaz de programación accesible públicamente, lo que le permite realizar interacciones REST directamente desde un navegador web.

Puede utilizar la herramienta de línea de comandos **cURL** para invocar los servicios web de Aspose.Cells. El ejemplo siguiente muestra cómo eliminar todos los hipervínculos de una hoja de cálculo.

{{< tabs tabTotal="2" tabID="11" tabName11="Solicitud" tabName12="Respuesta" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test1.xlsx/worksheets/Sheet1/hyperlinks" \
  -X DELETE \
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

## Familia de SDK en la nube

Utilizar un SDK acelera el desarrollo al manejar automáticamente los detalles de bajo nivel. Para obtener una lista completa de los SDK de Aspose.Cells Cloud, visite el [repositorio de GitHub](https://github.com/aspose-cells-cloud).

Los siguientes ejemplos de código muestran cómo eliminar los hipervínculos de una hoja de cálculo con diversos SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleDeleteWorksheetHyperlinks.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_DeleteWorksheetHyperlinks.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_DeleteWorksheetHyperlinks.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_DeleteWorksheetHyperlinks.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_DeleteWorksheetHyperlinks.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_DeleteWorksheetHyperlinks.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_DeleteWorksheetHyperlinks.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_DeleteWorksheetHyperlinks.go" >}}

{{< /tab >}}

{{< /tabs >}}
---