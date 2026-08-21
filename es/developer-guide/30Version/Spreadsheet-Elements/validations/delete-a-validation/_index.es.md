---
title: "Eliminar validación de hoja de cálculo – Aspose.Cells Cloud"
second_title: "Documento"
linktitle: "Eliminar"
type: docs
url: /es/validations/delete/
keywords: "Eliminar, validación de hoja de cálculo, Aspose.Cells Cloud, API de Excel"
description: "Aprenda a eliminar una validación de hoja de cálculo de un archivo de Excel mediante la API REST de Aspose.Cells Cloud. Incluye el punto de conexión, parámetros, detalles de autenticación, ejemplo con cURL, manejo de errores y fragmentos de código de SDK."
weight: 10
---

Esta API REST elimina una validación de hoja de cálculo mediante su índice basado en cero en una hoja de cálculo de Excel.

## API REST

```bash
DELETE https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/validations/{validationIndex}
```

### **Parámetros de la solicitud**

| Nombre del parámetro | Tipo    | Ubicación | Descripción                                        |
| --------------------- | ------- | --------- | -------------------------------------------------- |
| name                  | string  | path      | El nombre del archivo de Excel.                   |
| sheetName             | string  | path      | El nombre de la hoja de cálculo.                  |
| validationIndex       | integer | path      | El índice basado en cero de la validación que se va a eliminar. |
| folder                | string  | query     | La carpeta que contiene el documento.             |
| storageName           | string  | query     | El nombre del servicio de almacenamiento.         |

La [Especificación OpenAPI](https://apireference.aspose.cloud/cells/#/WorksheetValidations/DeleteWorksheetValidation) define una interfaz de programación públicamente accesible y le permite realizar interacciones REST directamente desde un navegador web.

Puede utilizar la herramienta de línea de comandos cURL para invocar el servicio web de Aspose.Cells. El ejemplo siguiente muestra cómo eliminar una validación con cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Solicitud" tabName2="Respuesta" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/myWorkBook.xlsx/worksheets/Sheet1/validations/0" \
  -X DELETE \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt-token>"
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

**Códigos de estado HTTP**

| Código | Significado                 | Descripción                                      |
|--------|-----------------------------|--------------------------------------------------|
| 200    | Correcto                    | Filtro aplicado correctamente; la respuesta contiene los detalles de la operación. |
| 400    | Solicitud incorrecta        | Parámetros ausentes o no válidos (p. ej., tipo de archivo no admitido). |
| 401    | No autorizado               | Token JWT no válido o ausente. |
| 413    | Payload demasiado grande     | El archivo cargado supera el límite de tamaño. |
| 500    | Error interno del servidor  | Error inesperado en el servidor. |

## Familia de SDK en la nube

Utilizar un SDK es la forma más rápida de integrar esta operación en su aplicación. Los SDK gestionan los detalles de bajo nivel para que usted se enfoque en la lógica de negocio. Consulte el [repositorio de GitHub](https://github.com/aspose-cells-cloud) para ver una lista completa de los SDK de Aspose.Cells Cloud.

Los siguientes ejemplos de código muestran cómo eliminar una validación de hoja de cálculo mediante diversos SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleDeleteWorksheetValidation.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_DeleteWorksheetValidation.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_DeleteWorksheetValidation.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_DeleteWorksheetValidation.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_DeleteWorksheetValidation.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_DeleteWorksheetValidation.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_DeleteWorksheetValidation.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_DeleteWorksheetValidation.go" >}}

{{< /tab >}}

{{< /tabs >}}