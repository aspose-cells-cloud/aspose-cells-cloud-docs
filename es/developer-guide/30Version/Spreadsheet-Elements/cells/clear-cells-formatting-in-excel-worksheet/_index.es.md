---
title: "Borrar formato de celdas en una hoja de cálculo de Excel"
type: docs
url: /es/clear-cells-formatting-in-excel-worksheet/
weight: 100
keywords: "Aspose.Cells Cloud, Excel, Borrar formato de celdas, API REST, C#, Java, PHP, Ruby, Node.js, Python, Perl, Go"
description: "Utilice la API REST de Aspose.Cells Cloud para borrar el formato de celdas en una hoja de cálculo de Excel. Incluye detalles de la solicitud, un ejemplo con cURL y fragmentos de código de SDK para múltiples lenguajes."
ArticleTitle: "Borrar formato de celdas en una hoja de cálculo de Excel - API de Aspose.Cells Cloud"
---

**Nota:** Todas las llamadas a la API de Aspose.Cells Cloud deben realizarse a través de **HTTPS**. Las direcciones HTTP están obsoletas y pueden ser bloqueadas por los navegadores.

- **Método:** POST  
- **Punto de conexión:** `https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/clearformats`

Esta API REST borra el formato de celdas en un archivo de Excel y forma parte del conjunto Aspose.Cells Cloud para borrar el formato de celdas en hojas de cálculo de Excel.

## API PostClearFormats

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/clearformats
```

### **Seguridad y autenticación**

Las API de Aspose.Cells Cloud son seguras y requieren <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">autenticación basada en token JWT</a>.

### **Respuesta**

```json
{
    "Status":"OK",
    "Code":200
}
```

**Esquema de respuesta**

| Campo  | Tipo    | Descripción                                               |
|--------|---------|-----------------------------------------------------------|
| Code   | integer | Código de estado HTTP devuelto por la API (por ejemplo, 200). |
| Status | string  | Resultado de la operación (`OK` para operación exitosa).   |

**Códigos de estado HTTP**

| Código | Significado                 | Descripción                                                 |
|--------|-----------------------------|-------------------------------------------------------------|
| 200  | OK                          | Filtro aplicado correctamente; la respuesta contiene detalles de la operación. |
| 400  | Solicitud incorrecta        | Parámetros faltantes o no válidos (por ejemplo, tipo de archivo no admitido). |
| 401  | No autorizado               | Token JWT inválido o faltante. |
| 413  | Payload demasiado grande     | El archivo subido excede el límite de tamaño. |
| 500  | Error interno del servidor  | Error inesperado en el servidor. |

## Cómo utilizar la API PostClearFormats con SDK

### Especificación de la API PostClearFormats

La <a href="https://apireference.aspose.cloud/cells/#/Cells/PostClearFormats" rel="noopener noreferrer">Especificación OpenAPI</a> define una interfaz de programación accesible públicamente y le permite realizar interacciones REST directamente desde un navegador web.

Puede utilizar la herramienta de línea de comandos cURL para acceder fácilmente a los servicios web de Aspose.Cells. El siguiente ejemplo muestra cómo realizar una llamada a la API en la nube utilizando cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Solicitud" tabName12="Respuesta" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/cells/clearformats?range=a1%3Aa10&startRow=1&startColumn=1&endRow=10&endColumn=10" \
  -X POST \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
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

### Uso de los SDK de Aspose.Cells Cloud

Utilizar un SDK es la forma más rápida de desarrollar. Un SDK maneja los detalles de bajo nivel, lo que le permite centrarse en las tareas de su proyecto. Consulte el [repositorio de GitHub](https://github.com/aspose-cells-cloud) para ver una lista completa de los SDK de Aspose.Cells Cloud.

Los siguientes ejemplos de código muestran cómo llamar a los servicios web de Aspose.Cells utilizando diversos SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostClearFormats.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostClearFormats.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostClearFormats.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostClearFormats.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostClearFormats.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostClearFormats.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostClearFormats.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostClearFormats.go" >}}

{{< /tab >}}

{{< /tabs >}}

**Consulte también**

- [Borrar contenido y estilos de celdas](https://docs.aspose.cloud/cells/clear-contents-and-styles)  
- [Establecer estilo de celda](https://docs.aspose.cloud/cells/set-cell-style)
---