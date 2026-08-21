---
title: "Obtener la descripción de una fila en una hoja de cálculo de Excel"
second_title: "Document"
linktype: "Row"
type: docs
url: /rows/get/row/
aliases: [/get-row-from-a-worksheet/]
keywords: "Aspose.Cells Cloud, API de filas de Excel, Obtener fila de hoja de cálculo, API REST, SDK de .NET, SDK de Java, SDK de Python"
description: "Recuperar información detallada (altura, estilo, estado oculto, etc.) para una fila específica en una hoja de cálculo de Excel utilizando la API REST de Aspose.Cells Cloud. Incluye ejemplo con cURL, fragmentos de SDK y manejo de errores."
weight: 10
ArticleTitle: "Obtener la descripción de una fila en una hoja de cálculo de Excel – API de Aspose.Cells Cloud"
---

**Requisitos previos:**  
- Obtener un token de acceso JWT válido e incluirlo en el encabezado `Authorization: Bearer <jwt token>`.  
- Asegurarse de que el libro esté almacenado en el almacenamiento de Aspose Cloud o especificar la ruta de la carpeta donde se encuentra.  
- Utilizar la versión de la API **v3.0**, tal como se muestra en la URL del endpoint.

Esta API REST recupera datos de fila mediante su índice en una hoja de cálculo de Excel.

## API GetWorksheetRow

```http
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/rows/{rowIndex}
```

### **Seguridad y autenticación**

Las API de Aspose.Cells Cloud son seguras y requieren <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">autenticación mediante token JWT</a>.

### **Parámetros de solicitud**

| Nombre del parámetro | Tipo    | Ubicación | Descripción                                           |
| --------------------- | ------- | --------- | ----------------------------------------------------- |
| name                  | string  | path      | Nombre del archivo del libro.                         |
| sheetName             | string  | path      | Nombre de la hoja de cálculo dentro del libro.       |
| rowIndex              | integer | path      | Índice de base cero de la fila que se va a recuperar.|
| folder                | string  | query     | Carpeta que contiene el libro.                        |
| storageName           | string  | query     | Nombre del almacenamiento donde reside el libro.     |

La [Especificación OpenAPI](https://apireference.aspose.cloud/cells/#/Cells/GetWorksheetRow) define una interfaz de programación públicamente accesible y permite realizar interacciones REST directamente desde un navegador web.

Puede utilizar la herramienta de línea de comandos cURL para acceder fácilmente a los servicios web de Aspose.Cells. El siguiente ejemplo muestra cómo realizar llamadas a la API en la nube con cURL. Incluya el encabezado `Authorization: Bearer <jwt token>` para autenticar la solicitud.

{{< tabs tabTotal="2" tabID="1" tabName1="Solicitud" tabName2="Respuesta" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/cells/rows/0" \
  -X GET \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Row": {
    "GroupLevel": 0,
    "Height": 13.5,
    "Index": 0,
    "IsBlank": false,
    "IsHeightMatched": true,
    "IsHidden": false,
    "Style": {
      "link": {
        "Href": "/style",
        "Rel": "self"
      }
    },
    "link": {
      "Href": "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/cells/rows/0",
      "Rel": "self"
    }
  },
  "Code": 200,
  "Status": "OK"
}
```

**Esquema de respuesta**

| Propiedad         | Tipo    | Descripción                                                         |
|-------------------|---------|----------------------------------------------------------------------|
| `GroupLevel`      | integer | Nivel de agrupación (usado para agrupaciones).                      |
| `Height`          | number  | Altura de la fila en puntos.                                        |
| `Index`           | integer | Índice de base cero de la fila devuelta.                            |
| `IsBlank`         | boolean | Indica si la fila contiene algún dato.                              |
| `IsHeightMatched`| boolean | `true` si la altura de la fila coincide con la altura predeterminada.|
| `IsHidden`        | boolean | `true` si la fila está oculta.                                      |
| `Style`           | object  | Objeto que contiene información de estilo para la fila.            |
| `link`            | object  | Referencia de hipervínculo al recurso de fila.                      |
| `Code`            | integer | Código de estado HTTP de la respuesta.                              |
| `Status`          | string  | Descripción textual del estado (por ejemplo, “OK”).                |

{{< /tab >}}

{{< /tabs >}}

**Notas / Manejo de errores:** La API puede devolver los siguientes códigos de estado HTTP:

- **200** – Éxito; se devuelve la información de la fila.  
- **401** – No autorizado; el token JWT falta o no es válido.  
- **404** – No encontrado; el libro, hoja de cálculo o fila especificados no existen.  
- **500** – Error interno del servidor; se produjo una condición inesperada.

| Código | Descripción                                      | Solución                                     |
|--------|--------------------------------------------------|----------------------------------------------|
| 200    | Éxito – se devuelve la información de la fila.   | –                                            |
| 401    | No autorizado – token JWT ausente o no válido.   | Proporcione un token JWT válido.             |
| 404    | No encontrado – libro, hoja de cálculo o fila ausentes.| Verifique los nombres y el índice de fila. |
| 500    | Error interno del servidor – condición inesperada.| Póngase en contacto con el soporte de Aspose.|

Para obtener una lista completa de códigos de error, consulte la documentación de [Códigos de error](https://docs.aspose.cloud/cells/) de Aspose.Cells Cloud.

## Familia de SDK en la nube

Utilizar un SDK es la forma más rápida de desarrollar. Un SDK abstracta los detalles de bajo nivel para que pueda centrarse en las tareas de su proyecto. Consulte el [repositorio de GitHub](https://github.com/aspose-cells-cloud) para obtener una lista completa de los SDK de Aspose.Cells Cloud.

Los siguientes ejemplos de código muestran cómo llamar a los servicios web de Aspose.Cells utilizando varios SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetWorksheetRow.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetWorksheetRow.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetWorksheetRow.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetWorksheetRow.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_GetWorksheetRow.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetWorksheetRow.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetWorksheetRow.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetWorksheetRow.go" >}}

{{< /tab >}}

{{< /tabs >}}