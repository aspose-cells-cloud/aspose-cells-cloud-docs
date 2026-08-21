---
title: "Eliminar varias hojas de cálculo de Excel"
second_title: "Document"
linktype: "Varias hojas de cálculo"
type: docs
url: /es/worksheets/delete-multiple/
aliases: [  /es/delete-excel-worksheets/ ]
keywords: "Aspose.Cells Cloud, eliminar varias hojas de cálculo, API de Excel, API REST, v3.0, eliminar hojas de cálculo"
description: "Aprenda cómo eliminar varias hojas de cálculo de un libro de Excel utilizando la API REST de Aspose.Cells Cloud (v3.0). Incluye un endpoint HTTPS seguro, los parámetros requeridos, un ejemplo corregido de cURL y fragmentos de SDK para múltiples lenguajes de programación."
weight: 20
ArticleTitle: "Eliminar varias hojas de cálculo de Excel mediante la API REST de Aspose.Cells Cloud"
---

Esta API REST elimina varias hojas de cálculo de un libro.

## Seguridad y autenticación
Las API de Aspose.Cells Cloud son seguras y requieren [autenticación basada en token JWT](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/).

## API REST

```bash
DELETE https://api.aspose.cloud/v3.0/cells/{name}/worksheets
```

### **Parámetros de la solicitud**

| Nombre del parámetro | Tipo   | Ubicación | Descripción                                                                 |
| -------------------- | ------ | --------- | --------------------------------------------------------------------------- |
| name                 | string | path      | Nombre del archivo de Excel.                                                |
| matchCondition       | object | body      | Objeto `MatchConditionRequest` que especifica qué hojas de cálculo eliminar. |
| folder               | string | query     | Ruta de carpeta en el almacenamiento donde se encuentra el archivo.         |
| storageName          | string | query     | Nombre del servicio de almacenamiento.                                      |

**Propiedades de MatchConditionRequest**

| Nombre              | Tipo     | Descripción                                  | Notas    |
| ------------------- | -------- | -------------------------------------------- | -------- |
| RegexPattern        | string   | Expresión regular para coincidir con nombres de hojas de cálculo. | opcional |
| FullMatchConditions | string[] | Nombres exactos de las hojas de cálculo que se van a eliminar. | opcional |

La [Especificación OpenAPI](https://apireference.aspose.cloud/cells/#/Worksheets/DeleteWorksheets) define una interfaz de programación accesible públicamente y le permite realizar interacciones REST directamente desde un navegador web.

Puede utilizar la herramienta de línea de comandos cURL para acceder fácilmente a los servicios web de Aspose.Cells. El siguiente ejemplo muestra cómo realizar llamadas a la API en la nube con cURL. **Se requiere un token JWT válido en el encabezado `Authorization`.**

{{< tabs tabTotal="2" tabID="1" tabName1="Solicitud" tabName2="Respuesta" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets?folder=Temp" \
  -X DELETE \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt_token>" \
  -d '{"FullMatchConditions":["Sheet1","Sheet2","Sheet3"]}'
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

La solicitud también puede devolver respuestas de error comunes, por ejemplo:

| Estado HTTP | Significado                                      | Carga útil de ejemplo                                    |
| ----------- | ------------------------------------------------ | -------------------------------------------------------- |
| 400         | Solicitud incorrecta: JSON o parámetros no válidos | `{"Code":400,"Message":"Invalid request payload."}`      |
| 401         | No autorizado: token JWT ausente o no válido     | `{"Code":401,"Message":"Authentication failed."}`        |
| 403         | Prohibido: permisos insuficientes                | `{"Code":403,"Message":"Access denied."}`                |
| 404         | No encontrado: el archivo o la hoja de cálculo no existe | `{"Code":404,"Message":"Resource not found."}`           |
| 500         | Error interno del servidor                       | `{"Code":500,"Message":"An unexpected error occurred."}` |

{{< /tab >}}

{{< /tabs >}}

## Familia de SDK en la nube

Utilizar un SDK es la mejor forma de acelerar el desarrollo. Un SDK maneja los detalles de bajo nivel para que usted pueda centrarse en las tareas de su proyecto. Consulte el [repositorio de GitHub](https://github.com/aspose-cells-cloud) para ver una lista completa de los SDK de Aspose.Cells Cloud.

Los siguientes ejemplos de código muestran cómo realizar llamadas a los servicios web de Aspose.Cells mediante diversos SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleDeleteWorksheets.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_DeleteWorksheets.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_DeleteWorksheets.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_DeleteWorksheets.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_DeleteWorksheets.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_DeleteWorksheets.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_DeleteWorksheets.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_DeleteWorksheets.go" >}}

{{< /tab >}}

{{< /tabs >}}

**Consulte también:**  
- [Eliminar una sola hoja de cálculo](https://docs.aspose.cloud/cells/worksheets/delete/)  
- [Copiar hoja de cálculo](https://docs.aspose.cloud/cells/worksheets/copy/)  
- [Mover hoja de cálculo](https://docs.aspose.cloud/cells/worksheets/move/)  
---