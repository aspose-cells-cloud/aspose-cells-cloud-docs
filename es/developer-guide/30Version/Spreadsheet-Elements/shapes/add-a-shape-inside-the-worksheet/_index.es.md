---
title: "Agregar una forma a una hoja de cálculo de Excel"
second_title: "Document"
linktype: "Add"
type: docs
url: /shapes/add/
aliases: [/add-a-shape-inside-the-worksheet/]
keywords: "Aspose.Cells, agregar forma, Excel, API REST, SDK en la nube, shapeDTO, tipo de dibujo"
description: "Aprenda cómo agregar formas (arco, línea, rectángulo, etc.) a una hoja de cálculo de Excel mediante la API REST de Aspose.Cells Cloud v3.0. Incluye sintaxis de solicitud, parámetros obligatorios, pasos de autenticación y código de ejemplo del SDK."
weight: 30
ArticleTitle: "Agregar una forma a una hoja de cálculo de Excel mediante la API de Aspose.Cells Cloud"
---

Esta API REST agrega una forma a una hoja de cálculo de Excel.  
El punto de conexión pertenece a la **versión de la API v3.0**; asegúrese de utilizar un token de acceso JWT obtenido a través del flujo OAuth2 de Aspose Cloud (client-id/client-secret) e incluirlo en el encabezado `Authorization: Bearer <token>`.

### **Seguridad y autenticación**

Las API de Aspose.Cells Cloud son seguras y requieren <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">autenticación basada en token JWT</a>.

## API PutWorksheetShape

```http
PUT https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/shapes
```

### **Parámetros de la solicitud**

| Nombre del parámetro | Tipo    | Ubicación | Descripción                                                                                           |
| --------------------- | ------- | --------- | ----------------------------------------------------------------------------------------------------- |
| name                  | string  | path      | Nombre del documento.                                                                                 |
| sheetName             | string  | path      | Nombre de la hoja de cálculo.                                                                         |
| shapeDTO              | object  | body      | Objeto JSON que describe la forma a agregar (consulte la especificación OpenAPI para el esquema completo). |
| drawingType           | string  | query     | Tipo de objeto de forma (por ejemplo, `arc`, `line`, `rectangle`).                                   |
| upperLeftRow          | integer | query     | Índice de fila superior izquierdo de la forma.                                                        |
| upperLeftColumn       | integer | query     | Índice de columna superior izquierdo de la forma.                                                     |
| top                   | integer | query     | Desplazamiento vertical de la forma desde su borde superior, en píxeles.                              |
| left                  | integer | query     | Desplazamiento horizontal de la forma desde su borde izquierdo, en píxeles.                           |
| width                 | integer | query     | Ancho de la forma, en píxeles.                                                                        |
| height                | integer | query     | Alto de la forma, en píxeles.                                                                         |
| folder                | string  | query     | Carpeta que contiene el documento.                                                                    |
| storageName           | string  | query     | Nombre del almacenamiento.                                                                            |

La [Especificación OpenAPI](https://apireference.aspose.cloud/cells/#/Shapes/PutWorksheetShape) define una interfaz de programación públicamente accesible y permite realizar interacciones REST directamente desde un navegador web.

Puede utilizar la herramienta de línea de comandos cURL para acceder fácilmente a los servicios web de Aspose.Cells. El siguiente ejemplo muestra cómo realizar una llamada a la API en la nube con cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Solicitud" tabName2="Respuesta" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/shapes?DrawingType=arc&upperLeftRow=1&upperLeftColumn=1&top=1&left=1&width=100&height=100" \
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
  "Status": "OK",
  "ShapeId": 5
}
```

_La respuesta correcta devuelve el código de estado HTTP, un texto de estado y el identificador de la forma recién creada (`ShapeId`)._

{{< /tab >}}

{{< /tabs >}}

**Códigos de estado HTTP**

| Código | Significado                 | Descripción                                                  |
|--------|-----------------------------|--------------------------------------------------------------|
| 200    | OK                          | Filtro aplicado correctamente; la respuesta contiene los detalles de la operación. |
| 400    | Solicitud incorrecta        | Parámetros ausentes o no válidos (por ejemplo, tipo de archivo no admitido). |
| 401    | No autorizado               | Token JWT no válido o ausente.                               |
| 413    | Carga útil demasiado grande | El archivo subido excede el límite de tamaño.               |
| 500    | Error interno del servidor  | Error inesperado del servidor.                               |

Las respuestas de error típicas incluyen:

- **400 Solicitud incorrecta** – parámetros ausentes o no válidos.  
- **401 No autorizado** – token JWT no válido o ausente.  
- **404 No encontrado** – la hoja de cálculo o el documento especificados no existen.

Cada error se devuelve como un objeto JSON que contiene los campos `Code` y `Message`.

## Familia de SDK en la nube

Utilizar un SDK es la mejor manera de acelerar el desarrollo. Un SDK gestiona los detalles de bajo nivel para que usted pueda centrarse en las tareas de su proyecto. Consulte el [repositorio de GitHub](https://github.com/aspose-cells-cloud) para obtener una lista completa de los SDK de Aspose.Cells Cloud.

Los siguientes ejemplos de código muestran cómo invocar los servicios web de Aspose.Cells mediante varios SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePutWorksheetShape.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PutWorksheetShape.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PutWorksheetShape.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PutWorksheetShape.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PutWorksheetShape.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PutWorksheetShape.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PutWorksheetShape.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PutWorksheetShape.go" >}}

{{< /tab >}}

{{< /tabs >}}