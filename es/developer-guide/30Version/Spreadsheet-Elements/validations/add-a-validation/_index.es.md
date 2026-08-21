---
title: "Agregar una validación de hoja de cálculo a una hoja de cálculo de Excel"
second_title: "Documento"
linktitle: "Agregar"
type: docs
url: /es/validations/add/
keywords: "Agregar validación de hoja de cálculo, Excel, Aspose.Cells Cloud, API REST, hoja de cálculo, regla de validación"
description: "Utilice la API REST de Aspose.Cells Cloud para agregar una validación de hoja de cálculo a un archivo de Excel. Los SDK están disponibles para C#, Java, PHP, Ruby, Node.js, Python, Perl, Go y Swift."
weight: 10
---

Esta API REST agrega una validación de hoja de cálculo a una hoja de cálculo de Excel.

## API REST

```bash
PUT http://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/validations
```

### **Parámetros de la solicitud**

| Nombre del parámetro | Tipo   | Ubicación | Descripción                                                      |
| -------------------- | ------ | --------- | ---------------------------------------------------------------- |
| name                 | string | path      | Nombre del documento de Excel.                                  |
| sheetName            | string | path      | Nombre de la hoja de cálculo.                                   |
| range                | string | query     | Rango de celdas al que se aplica la validación (por ejemplo, A1:B10). |
| validation           | object | body      | Definición de la regla de validación.                           |
| folder               | string | query     | Carpeta que contiene el documento.                              |
| storageName          | string | query     | Nombre del servicio de almacenamiento.                          |

La [Especificación de OpenAPI](https://apireference.aspose.cloud/cells/#/WorksheetValidations/PutWorksheetValidation) define una interfaz de programación accesible públicamente y le permite realizar interacciones REST directamente desde un navegador web.

Puede utilizar la herramienta de línea de comandos cURL para acceder fácilmente a los servicios web de Aspose.Cells. El siguiente ejemplo muestra cómo realizar llamadas a la API en la nube mediante cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Solicitud" tabName2="Respuesta" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "http://api.aspose.cloud/v3.0/cells/myWorkBook.xlsx/worksheets/Sheet1/validations" \
-X PUT \
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

## Familia de SDK en la nube

Utilizar un SDK es la mejor forma de acelerar el desarrollo. Un SDK gestiona los detalles de bajo nivel y le permite centrarse en las tareas de su proyecto. Consulte el [repositorio de GitHub](https://github.com/aspose-cells-cloud) para obtener una lista completa de los SDK de Aspose.Cells Cloud.

Los siguientes ejemplos de código muestran cómo invocar los servicios web de Aspose.Cells utilizando diversos SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePutWorksheetValidation.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PutWorksheetValidation.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PutWorksheetValidation.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PutWorksheetValidation.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2b4189bc27ae92abf73c36b4df0" "Example_PutWorksheetValidation.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PutWorksheetValidation.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PutWorksheetValidation.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PutWorksheetValidation.go" >}}

{{< /tab >}}

{{< /tabs >}}