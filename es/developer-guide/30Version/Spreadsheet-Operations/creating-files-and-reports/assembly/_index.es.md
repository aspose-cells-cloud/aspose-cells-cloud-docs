---
title: "Ensamblaje de datos para la creación de un informe de Excel"
second_title: "Documento"
linktitle: "Ensamblaje de datos"
type: docs
url: /assembly-data-for-the-creation-of-an-excel-report/
aliases: [/assembly/]
keywords: "Aspose.Cells, informe de Excel, ensamblaje de datos, API en la nube, REST, SDK, cURL, PDF, ODS"
description: "Aprenda a utilizar la API de ensamblaje de Aspose.Cells Cloud para integrar datos en informes de Excel (XLSX, PDF, ODS). Incluye endpoint, parámetros, ejemplo con cURL, código de SDK, guía de autenticación y manejo de errores."
weight: 40
---

Esta API REST ensambla datos **dentro** de un archivo de Excel.

## API REST

```bash
POST https://api.aspose.cloud/v3.0/cells/assembly
```

### **Seguridad y autenticación**

Las API de Aspose.Cells Cloud son seguras y requieren <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">autenticación basada en token JWT</a>.

### Parámetros de solicitud


| Nombre del parámetro | Tipo   | Ubicación                | Descripción                                                                 |
|----------------------|--------|--------------------------|-----------------------------------------------------------------------------|
| file                 | file   | formData (cuerpo multiparte) | El archivo de hoja de cálculo que se cargará.                              |
| DataSource           | string | cadena de consulta       | Identificador de la fuente de datos que aporta los datos para el ensamblaje. |
| format               | string | cadena de consulta       | Formato de salida deseado (por ejemplo, `xlsx`, `pdf`).                    |

### **Respuesta**

```json
{
    "Status" : "OK",
    "Code" : 200,
    "Filename" : "[nombre del archivo2]",
    "Filesize" : [tamaño del archivo],
    "FileContent" : "[Cadena en Base64]"
}
```

**Códigos de estado HTTP**

| Código | Significado                 | Descripción                                                                 |
|--------|-----------------------------|-----------------------------------------------------------------------------|
| 200    | OK                          | Filtro aplicado correctamente; la respuesta contiene detalles de la operación. |
| 400    | Solicitud incorrecta        | Parámetros ausentes o no válidos (por ejemplo, tipo de archivo no admitido). |
| 401    | No autorizado               | Token JWT no válido o ausente.                                              |
| 413    | Carga demasiado grande       | El archivo cargado excede el límite de tamaño.                             |
| 500    | Error interno del servidor  | Error inesperado en el servidor.                                            |

## Cómo utilizar la API PostAssemble con SDK

### Especificación de la API PostAssemble

La [Especificación OpenAPI](https://apireference.aspose.cloud/cells/#/LightCells/PostAssemble) define una interfaz de programación públicamente accesible y permite realizar interacciones REST directamente desde un navegador web.

Puede utilizar la herramienta de línea de comandos cURL para acceder fácilmente a los servicios web de Aspose.Cells. El siguiente ejemplo muestra cómo realizar llamadas a la API en la nube mediante cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Solicitud" tabName12="Respuesta" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/assembly?DataSource=ds&format=pdf" \
  -X POST \
  -H "Content-Type: multipart/form-data" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <token jwt>" \
  -F 'template=@template.xlsx' \
  -F 'data=@data.json'
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Files": [
    {
      "Filename": "report1",
      "FileSize": 274022,
      "FileContent": "-----Cadena en Base64--------"
    },
    {
      "Filename": "report2",
      "FileSize": 274022,
      "FileContent": "-----Cadena en Base64--------"
    }
  ]
}
```

{{< /tab >}}

{{< /tabs >}}

### Utilizar los SDK de Aspose.Cells Cloud

Utilizar un SDK es la forma más rápida de desarrollar contra la API. Un SDK abstracta los detalles de bajo nivel, permitiéndole centrarse en su lógica de negocio. Consulte el [repositorio de GitHub](https://github.com/aspose-cells-cloud) para obtener una lista completa de los SDK de Aspose.Cells Cloud.

Los siguientes ejemplos de código muestran cómo invocar los servicios web de Aspose.Cells mediante distintos SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostAssemble.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostAssemble.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostAssemble.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostAssemble.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostAssemble.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostAssemble.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostAssemble.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostAssemble.go" >}}

{{< /tab >}}

{{< /tabs >}}