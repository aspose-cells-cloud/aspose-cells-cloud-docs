---
title: "Agregar marca de agua a archivos de Excel"
second_title: "Documento"
linktitle: "Agregar marca de agua a archivos de Excel"
type: docs
url: /add-watermark-into-excel-files/
aliases: [/watermark/]
keywords: "agregar marca de agua a Excel, Aspose.Cells Cloud, API REST, SDK, C#, Java, PHP, Ruby, Node.js, Python, Perl, Go"
description: "Aprenda cómo agregar una marca de agua de texto a libros de Excel utilizando la API REST de Aspose.Cells Cloud (v3.0). Incluye un ejemplo con cURL, parámetros requeridos y detalles de respuesta."
weight: 39
ArticleTitle: "Agregar marca de agua a archivos de Excel – Documentación de Aspose.Cells Cloud"
---

Esta API REST agrega una **marca de agua** a archivos de Excel.

**Requisitos previos:** Debe obtener un token de acceso JWT válido y asegurarse de que el archivo de Excel esté en un formato compatible (por ejemplo, `.xlsx`, `.xls`).  
**Antecedentes:** Una marca de agua es una superposición de texto semitransparente aplicada a cada hoja de cálculo para indicar propiedad o confidencialidad.

## API PostWatermark

```http
POST https://api.aspose.cloud/v3.0/cells/watermark
```

### **Seguridad y autenticación**

Las API de Aspose.Cells Cloud son seguras y requieren <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">autenticación basada en token JWT</a>.

### **Parámetros de solicitud**

| Nombre del parámetro | Tipo   | Ubicación                          | Descripción                                                  |
|----------------------|--------|------------------------------------|--------------------------------------------------------------|
| `file`               | archivo | formData (cuerpo multipart)        | El archivo de Excel al que se aplicará la marca de agua.    |
| `text`               | cadena | consulta                           | El texto de la marca de agua que se mostrará.               |
| `color`              | cadena | consulta                           | El color de la marca de agua en formato hexadecimal ARGB (por ejemplo, `004433ff`). |

### **Respuesta**

La respuesta JSON contiene un array **Files**. Para cada objeto de archivo:

- **Filename** – nombre del libro de trabajo procesado.  
- **FileSize** – tamaño del archivo en bytes.  
- **FileContent** – contenido codificado en Base64 del archivo de Excel con marca de agua; decodifíquelo para obtener el archivo real.

```json
{
    "Status" : "OK",
    "Code" : 200,
    "Files": [
        {
            "Filename" : "[nombre_archivo1]",
            "Filesize" : [tamaño_archivo],
            "FileContent" : "[CadenaBase64]"
        },        {
            "Filename" : "[nombre_archivo2]",
            "Filesize" : [tamaño_archivo],
            "FileContent" : "[CadenaBase64]"
        },        {
            "Filename" : "[nombre_archivo3]",
            "Filesize" : [tamaño_archivo],
            "FileContent" : "[CadenaBase64]"
        }
    ]
}
```

**Códigos de estado HTTP**

| Código | Significado                 | Descripción                                                    |
|--------|-----------------------------|----------------------------------------------------------------|
| 200    | OK                          | Filtro aplicado correctamente; la respuesta contiene detalles de la operación. |
| 400    | Solicitud incorrecta        | Parámetros faltantes o no válidos (por ejemplo, tipo de archivo no admitido). |
| 401    | No autorizado               | Token JWT inválido o faltante. |
| 413    | Payload demasiado grande     | El archivo subido excede el límite de tamaño. |
| 500    | Error interno del servidor  | Error inesperado en el servidor. |

## Cómo usar la API PostWatermark con SDK

### Especificación de la API PostWatermark

La [Especificación OpenAPI](https://apireference.aspose.cloud/cells/#/LightCells/PostWatermark) define una interfaz de programación públicamente accesible y le permite realizar interacciones REST directamente desde un navegador web.

Puede utilizar la herramienta de línea de comandos **cURL** para llamar a los servicios web de Aspose.Cells. El siguiente ejemplo muestra una solicitud completa, incluida la cabecera de autenticación requerida. Reemplace `<your-jwt-token>` por un token de acceso JWT válido obtenido del punto de conexión de autenticación de Aspose.

{{< tabs tabTotal="2" tabID="1" tabName1="Solicitud" tabName2="Respuesta" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/watermark?text=aspose.cells.cloud&color=004433ff" \
  -X POST \
  -H "Content-Type: multipart/form-data" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <your-jwt-token>" \
  -F "file=@Sample.xlsx"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Files": [
    {
      "Filename": "Sample_watermarked.xlsx",
      "FileSize": 274022,
      "FileContent": "-----CadenaBase64--------"
    }
  ]
}
```

{{< /tab >}}

{{< /tabs >}}

### Utilizar los SDK de Aspose.Cells Cloud

Utilizar un SDK es la forma más rápida de desarrollar. Un SDK abstracta los detalles de bajo nivel, permitiéndole centrarse en la lógica de negocio. Consulte el [repositorio de GitHub](https://github.com/aspose-cells-cloud) para obtener una lista completa de los SDK de Aspose.Cells Cloud.

Los siguientes ejemplos de código demuestran cómo invocar los servicios web de Aspose.Cells utilizando diversos SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostWatermark.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostWatermark.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostWatermark.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostWatermark.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostWatermark.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostWatermark.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostWatermark.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostWatermark.go" >}}

{{< /tab >}}

{{< /tabs >}}