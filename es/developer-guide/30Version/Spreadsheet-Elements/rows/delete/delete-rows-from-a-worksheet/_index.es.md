---
title: "Eliminar varias filas de una hoja de cálculo de Excel"
second_title: "Documento"
linktitle: "Filas"
type: docs
url: /rows/delete/rows/
keywords: "Aspose.Cells Cloud, eliminar filas, eliminar varias filas, hoja de cálculo de Excel, API REST, SDK"
description: "Aprenda cómo eliminar una o más filas de una hoja de cálculo de Excel utilizando la API REST de Aspose.Cells Cloud. Incluye detalles del endpoint, parámetros, un ejemplo con cURL y ejemplos de código SDK para varios lenguajes."
weight: 80
ArticleTitle: "Eliminar varias filas de una hoja de cálculo de Excel mediante la API de Aspose.Cells Cloud"
---

Esta API REST elimina varias filas **de** una hoja de cálculo de Excel.

**Requisitos previos:** Para llamar a este endpoint debe poseer un token de acceso JWT válido obtenido mediante la autenticación de Aspose Cloud y los permisos adecuados de almacenamiento para el libro.

## DeleteWorksheetRows API

```http
DELETE https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/rows
```

### **Seguridad y autenticación**

Las APIs de Aspose.Cells Cloud son seguras y requieren <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">autenticación basada en token JWT</a>.

### **Parámetros de solicitud**

| Nombre del parámetro | Tipo    | Ruta / Cadena de consulta / Cuerpo HTTP | Descripción                                                        |
| --------------------- | ------- | --------------------------------------- | ------------------------------------------------------------------ |
| name                  | string  | path                                    | Nombre del libro.                                                  |
| sheetName             | string  | path                                    | Nombre de la hoja de cálculo.                                      |
| startrow              | integer | query                                   | Índice de base cero de la primera fila a eliminar (por ejemplo, `0` = primera fila). |
| totalRows             | integer | query                                   | Número de filas a eliminar.                                        |
| updateReference       | boolean | query                                   | Indica si se deben actualizar las referencias tras la eliminación (`true`/`false`). |
| folder                | string  | query                                   | Carpeta del documento.                                             |
| storageName           | string  | query                                   | Nombre del almacenamiento.                                         |

La [Especificación OpenAPI](https://apireference.aspose.cloud/cells/#/Cells/DeleteWorksheetRows) define una interfaz de programación públicamente accesible y le permite realizar interacciones REST directamente desde un navegador web.

Puede utilizar la herramienta de línea de comandos cURL para acceder fácilmente a los servicios web de Aspose.Cells. El siguiente ejemplo muestra cómo realizar llamadas a la API en la nube con cURL. **Todos los endpoints requieren HTTPS; HTTP está obsoleto.**

{{< tabs tabTotal="2" tabID="1" tabName1="Solicitud" tabName2="Respuesta" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/cells/rows?startrow=1&totalRows=1&updateReference=true" \
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

{{< /tab >}}

{{< /tabs >}}

**Códigos de respuesta posibles**

| Estado HTTP | Descripción                                        |
|-------------|----------------------------------------------------|
| 200         | Filas eliminadas correctamente.                   |
| 400         | Solicitud incorrecta: parámetros no válidos.      |
| 401         | No autorizado: token JWT faltante o no válido.    |
| 404         | No encontrado: el libro o la hoja de cálculo no existen. |
| 500         | Error interno del servidor: condición inesperada. |

## Familia de SDK en la nube

Utilizar un SDK es la mejor forma de acelerar el desarrollo. Un SDK gestiona los detalles de bajo nivel y le permite centrarse en las tareas de su proyecto. Consulte el [repositorio de GitHub](https://github.com/aspose-cells-cloud) para obtener una lista completa de los SDK de Aspose.Cells Cloud.

Los siguientes ejemplos de código muestran cómo realizar llamadas a los servicios web de Aspose.Cells mediante diversos SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleDeleteWorksheetRows.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_DeleteWorksheetRows.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_DeleteWorksheetRows.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_DeleteWorksheetRows.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_DeleteWorksheetRows.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_DeleteWorksheetRows.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_DeleteWorksheetRows.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_DeleteWorksheetRows.go" >}}

{{< /tab >}}

{{< /tabs >}}