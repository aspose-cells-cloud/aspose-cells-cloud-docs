---
title: "Obtener todas las validaciones de hoja de cálculo de una hoja de Excel"
second_title: "Document"
linktitle: "Obtener todas"
type: docs
url: /validations/get-all/
keywords: "Aspose.Cells Cloud, Excel, validaciones de hoja de cálculo, API REST, obtener todas las validaciones, SDKs"
description: "Recuperar todas las validaciones de hoja de cálculo de una hoja de Excel mediante la API REST de Aspose.Cells Cloud. Admite múltiples SDKs (C#, Java, PHP, Ruby, Node.js, Python, Perl, Go) para una integración rápida."
weight: 10
---

Las validaciones de hoja de cálculo permiten definir reglas que restringen el tipo o rango de datos que se puede introducir en celdas. Se utilizan comúnmente para garantizar la integridad de los datos, por ejemplo, limitando las entradas a una lista de valores, fechas dentro de un rango específico o límites numéricos.

Esta API REST recupera todas las validaciones de una hoja de cálculo de Excel.

## API REST

```bash
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/validations
```

### **Parámetros de la solicitud**

| Nombre del parámetro | Tipo   | Ubicación | Descripción                                     |
| ---------------------|--------|-----------|-------------------------------------------------|
| name                 | string | path      | Nombre del documento de Excel.                 |
| sheetName            | string | path      | Nombre de la hoja de cálculo.                  |
| folder               | string | query     | Ruta de la carpeta donde se almacena el documento. |
| storageName          | string | query     | Nombre del servicio de almacenamiento.         |

**Códigos de estado de la respuesta**

| Código | Descripción                                   |
|--------|-----------------------------------------------|
| 200    | Solicitud correcta – lista de validaciones   |
| 401    | No autorizado – token no válido o ausente    |
| 404    | No encontrado – documento o hoja de cálculo ausente |
| 500    | Error interno del servidor                    |

La [Especificación OpenAPI](https://apireference.aspose.cloud/cells/#/WorksheetValidations/GetWorksheetValidations) define una interfaz de programación públicamente accesible y le permite realizar interacciones REST directamente desde un navegador web.

Puede utilizar la herramienta de línea de comandos cURL para acceder fácilmente a los servicios web de Aspose.Cells Cloud. **Requisito previo:** debe incluir un token JWT válido en el encabezado `Authorization`.

{{< tabs tabTotal="2" tabID="1" tabName1="Solicitud" tabName2="Respuesta" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/myWorkBook.xlsx/worksheets/Sheet1/validations" \
-X GET \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "validations": [
    {
      "name": "Validation1",
      "type": "WholeNumber",
      "operator": "Between",
      "formula1": "1",
      "formula2": "100",
      "showErrorMessage": true,
      "errorMessage": "El valor debe estar comprendido entre 1 y 100."
    },
    {
      "name": "Validation2",
      "type": "List",
      "formula1": "\"Opción1,Opción2,Opción3\"",
      "showErrorMessage": true,
      "errorMessage": "Seleccione un valor de la lista."
    }
  ]
}
```

{{< /tab >}}

{{< /tabs >}}

## Familia de SDKs en la nube

Utilizar un SDK es la mejor manera de acelerar el desarrollo. Un SDK gestiona los detalles de bajo nivel, permitiéndole centrarse en las tareas de su proyecto. Consulte el [repositorio de GitHub](https://github.com/aspose-cells-cloud) para obtener una lista completa de los SDKs de Aspose.Cells Cloud.

Los siguientes ejemplos de código muestran cómo llamar a los servicios web de Aspose.Cells utilizando diversos SDKs:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetWorksheetValidations.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetWorksheetValidations.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetWorksheetValidations.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetWorksheetValidations.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_GetWorksheetValidations.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetWorksheetValidations.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetWorksheetValidations.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetWorksheetValidations.go" >}}

{{< /tab >}}

{{< /tabs >}}