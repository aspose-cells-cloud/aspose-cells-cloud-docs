---
title: "Establecer fondo en una hoja de cálculo de Excel"
ArticleTitle: "Establecer fondo en una hoja de cálculo de Excel – Guía de la API de Aspose.Cells Cloud"
second_title: "Documentos"
linktitle: "Agregar"
type: docs
url: /es/worksheets/background/add/
aliases: [  /es/set-background-or-watermark-for-excel-worksheet/ ]
keywords: "Aspose.Cells, Excel, hoja de cálculo, fondo, API REST, SDK, agregar imagen"
description: "Aprenda cómo agregar una imagen de fondo (PNG, JPEG, BMP) a una hoja de cálculo de Excel mediante la API REST de Aspose.Cells Cloud. Incluye el punto de conexión, los parámetros obligatorios, los pasos de autenticación, un ejemplo con cURL y ejemplos de código del SDK."
weight: 180
---

Esta API REST agrega una imagen de fondo a una hoja de cálculo.

## Seguridad y autenticación
Las API de Aspose.Cells Cloud son seguras y requieren [autenticación basada en token JWT](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/).

## API REST

```bash
PUT http://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/background
```

### **Parámetros de la solicitud**

| Nombre del parámetro | Tipo   | Ubicación | Descripción                                                     |
| --------------------- | ------ | --------- | --------------------------------------------------------------- |
| name                  | string | path      | Nombre del libro de Excel.                                      |
| sheetName             | string | path      | Nombre de la hoja de cálculo a la que se aplica la imagen.      |
| imageFile             | file   | body      | Archivo de imagen binario (PNG, JPEG, BMP, etc.) para establecer como fondo. |
| folder                | string | query     | Carpeta en el almacenamiento donde se encuentra el libro.       |
| storageName           | string | query     | Nombre del almacenamiento de Aspose Cloud.                      |

**Formatos admitidos y límites**

- Extensiones de imagen aceptadas: **PNG, JPEG, BMP, GIF**.
- Tamaño máximo de archivo: **5 MB**.
- La imagen se repite (mosaico) para cubrir todo el fondo de la hoja de cálculo.

La [Especificación OpenAPI](https://apireference.aspose.cloud/cells/#/Worksheets/PutWorksheetBackground) define una interfaz de programación públicamente accesible y le permite realizar interacciones REST directamente desde un navegador web.

Puede utilizar la herramienta de línea de comandos cURL para acceder fácilmente a los servicios web de Aspose.Cells. El siguiente ejemplo muestra cómo realizar una llamada a la API en la nube con cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Solicitud" tabName2="Respuesta" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/myWorkbook.xlsx/worksheets/Sheet1/background" \
  -X PUT \
  -F "imageFile=@Creative.jpg" \
  -H "Content-Type: multipart/form-data" \
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

_Posibles respuestas de error_

| Código HTTP | Descripción                                                  |
| ----------- | ------------------------------------------------------------ |
| 400         | Solicitud incorrecta: parámetros faltantes o no válidos.     |
| 401         | No autorizado: token JWT inválido o caducado.                |
| 404         | No encontrado: el libro o la hoja de cálculo no existen.     |
| 500         | Error interno del servidor: condición inesperada en el servidor. |

{{< /tab >}}

{{< /tabs >}}

## Familia de SDK en la nube

Utilizar un SDK es la mejor forma de acelerar el desarrollo. Un SDK gestiona los detalles de bajo nivel y le permite centrarse en las tareas de su proyecto. Consulte el [repositorio de GitHub](https://github.com/aspose-cells-cloud) para obtener una lista completa de los SDK de Aspose.Cells Cloud.

Los siguientes ejemplos de código muestran cómo llamar a los servicios web de Aspose.Cells utilizando varios SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePutWorkbookBackground.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PutWorkbookBackground.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PutWorkbookBackground.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PutWorkbookBackground.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PutWorkbookBackground.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PutWorkbookBackground.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PutWorkbookBackground.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PutWorkbookBackground.go" >}}

{{< /tab >}}

{{< /tabs >}}