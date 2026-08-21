---
title: "Refrescar un Filtro Automático en una Hoja de Cálculo de Excel"
second_title: "Document"
linktype: "Refresh auto filter"
type: docs
url: /es/autofilter/refresh/
aliases: [  /es/refresh-an-autofilter/ ]
weight: 100
keywords: "Aspose.Cells, AutoFilter, refrescar, Excel, API, REST"
description: "Refresque un filtro automático existente en una hoja de cálculo de Excel utilizando la API REST de Aspose.Cells Cloud. Incluye ejemplos en cURL y SDK para C#, Java, Python y más."
ArticleTitle: "Refrescar un Filtro Automático en una Hoja de Cálculo de Excel"
---

### ¿Qué hace el método **Refrescar**?

Llamar al punto de conexión vuelve a aplicar los criterios de filtrado actuales tras haber cambiado los datos de la hoja de cálculo (por ejemplo, al agregar o eliminar filas). Esta operación no modifica la definición del filtro; simplemente actualiza la vista y devuelve una respuesta de estado.

### API REST

Esta API REST refresca un filtro automático en una hoja de cálculo de Excel (versión de la API: **v3.0**).

```bash
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/autoFilter/refresh
```

### **Seguridad y autenticación**

Las API de Aspose.Cells Cloud son seguras y requieren <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">autenticación mediante token JWT</a>.

### **Respuesta**

```json
{
    "Status":"OK",
    "Code":200
}
```

**Códigos de estado HTTP**

| Código | Significado                 | Descripción                                                      |
|--------|-----------------------------|------------------------------------------------------------------|
| 200    | OK                          | Filtro aplicado correctamente; la respuesta contiene detalles de la operación. |
| 400    | Solicitud incorrecta        | Parámetros faltantes o no válidos (por ejemplo, tipo de archivo no admitido). |
| 401    | No autorizado               | Token JWT inválido o ausente. |
| 413    | Carga demasiado grande       | El archivo cargado supera el límite de tamaño. |
| 500    | Error interno del servidor  | Error inesperado en el servidor. |

*Ejemplos de respuestas de error*  

```json
// 400 Bad Request (Solicitud incorrecta)
{
    "Code": 400,
    "Message": "Parámetro inválido: sheetName no encontrado."
}

// 401 Unauthorized (No autorizado)
{
    "Code": 401,
    "Message": "Falló la autenticación. El token JWT está ausente o es inválido."
}

// 413 Payload Too Large (Carga demasiado grande)
{
    "Code": 413,
    "Message": "El archivo cargado supera el tamaño máximo permitido."
}

// 500 Internal Server Error (Error interno del servidor)
{
    "Code": 500,
    "Message": "Ocurrió un error inesperado en el servidor."
}
```

## Cómo utilizar la API PostWorksheetAutoFilterRefresh con SDK

### Especificación de la API PostWorksheetAutoFilterRefresh

La [Especificación OpenAPI](https://apireference.aspose.cloud/cells/#/AutoFilter/PostWorksheetAutoFilterRefresh) define una interfaz de programación públicamente accesible y permite llevar a cabo interacciones REST directamente desde un navegador web.

Puede utilizar la herramienta de línea de comandos cURL para acceder fácilmente a los servicios web de Aspose.Cells. El siguiente ejemplo muestra cómo realizar llamadas a la API en la nube con cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Solicitud" tabName12="Respuesta" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/autoFilter/refresh" \
  -X POST \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <your-jwt-token>"
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

### Utilizar SDK de Aspose.Cells Cloud

Utilizar un SDK es la mejor forma de acelerar el desarrollo. Un SDK gestiona los detalles de bajo nivel y le permite centrarse en las tareas de su proyecto. Consulte el [repositorio de GitHub](https://github.com/aspose-cells-cloud) para obtener una lista completa de los SDK de Aspose.Cells Cloud.

Los siguientes ejemplos de código muestran cómo realizar llamadas a los servicios web de Aspose.Cells utilizando diversos SDK:
{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostWorksheetAutoFilterRefresh.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostWorksheetAutoFilterRefresh.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostWorksheetAutoFilterRefresh.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostWorksheetAutoFilterRefresh.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostWorksheetAutoFilterRefresh.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostWorksheetAutoFilterRefresh.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostWorksheetAutoFilterRefresh.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostWorksheetAutoFilterRefresh.go" >}}

{{< /tab >}}

{{< /tabs >}}