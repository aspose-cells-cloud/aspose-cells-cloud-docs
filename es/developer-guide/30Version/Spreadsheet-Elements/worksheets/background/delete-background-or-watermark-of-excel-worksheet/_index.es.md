---
title: "Eliminar el fondo en una hoja de cálculo de Excel"
second_title: "Document"
linktype: "Delete"
type: docs
url: /es/worksheets/background/delete/
aliases: [  /es/delete-background-or-watermark-of-excel-worksheet/ ]
keywords: "Aspose.Cells Cloud, Eliminar fondo de hoja de cálculo, Excel, REST API, SDK, C#, Java, PHP, Ruby, Node.js, Python, Perl, Go"
description: "Utilice la API REST de Aspose.Cells Cloud para eliminar la imagen de fondo de una hoja de cálculo de Excel. Los SDK están disponibles para C#, Java, PHP, Ruby, Node.js, Python, Perl y Go."
weight: 210
ArticleTitle: "Eliminar el fondo en una hoja de cálculo de Excel mediante la API de Aspose.Cells Cloud"
---

Esta API REST elimina la imagen de fondo de una hoja de cálculo.

**Prerrequisitos:** Debe tener el libro almacenado en el almacenamiento de Aspose Cloud y poseer un token de acceso JWT válido para la autenticación.

## API REST

```bash
DELETE https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/background
```

### **Parámetros de la solicitud**

| Nombre del parámetro | Tipo   | Ubicación | Descripción                                           |
| --------------------- | ------ | --------- | ----------------------------------------------------- |
| name                  | string | path      | El nombre del archivo de Excel.                      |
| sheetName             | string | path      | El nombre de la hoja de cálculo cuyo fondo se elimina. |
| folder                | string | query     | La carpeta en el almacenamiento donde se encuentra el archivo. |
| storageName           | string | query     | El nombre del almacenamiento (si no es el almacenamiento predeterminado). |

La [Especificación OpenAPI](https://apireference.aspose.cloud/cells/#/Worksheets/DeleteWorksheetBackground) define una interfaz de programación accesible públicamente y le permite realizar interacciones REST directamente desde un navegador web.

Puede utilizar la herramienta de línea de comandos cURL para acceder fácilmente a los servicios web de Aspose.Cells. Todas las solicitudes requieren un token JWT válido. Obtenga el token a través del endpoint de token OAuth2, como se describe en la guía de autenticación.

{{< tabs tabTotal="2" tabID="1" tabName1="Solicitud" tabName2="Respuesta" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/WorkSheetBackground_Sample_Test_Book.xls/worksheets/Sheet1/background" \
  -X DELETE \
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

**Códigos de estado HTTP**

| Código | Significado                 | Descripción                                            |
| ------ | --------------------------- | ------------------------------------------------------ |
| 200    | OK                          | Filtro aplicado correctamente; la respuesta contiene detalles de la operación. |
| 400    | Solicitud incorrecta        | Parámetros faltantes o no válidos (por ejemplo, tipo de archivo no admitido). |
| 401    | No autorizado               | Token JWT inválido o faltante.                         |
| 413    | Payload demasiado grande     | El archivo cargado excede el límite de tamaño.        |
| 500    | Error interno del servidor  | Error inesperado del servidor.                         |

{{< /tab >}}

{{< /tabs >}}

## Familia de SDK en la nube

Utilizar un SDK es la mejor forma de acelerar el desarrollo. Un SDK maneja los detalles de bajo nivel y le permite centrarse en las tareas de su proyecto. Consulte el [repositorio de GitHub](https://github.com/aspose-cells-cloud) para ver una lista completa de los SDK de Aspose.Cells Cloud.

Los siguientes ejemplos de código muestran cómo realizar llamadas a los servicios web de Aspose.Cells mediante varios SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleDeleteWorkbookBackground.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_DeleteWorkbookBackground.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_DeleteWorkbookBackground.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_DeleteWorkbookBackground.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_DeleteWorkbookBackground.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_DeleteWorkbookBackground.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_DeleteWorkbookBackground.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_DeleteWorkbookBackground.go" >}}

{{< /tab >}}

{{< /tabs >}}