---
title: "Conversión avanzada de archivo Excel"
second_title: "Documentos"
linktype: "Conversión avanzada"
type: docs
url: /es/advanced-convert-excel/
keywords: "Aspose.Cells, conversión de Excel, API en la nube, SDK"
description: "La API REST de Aspose.Cells Cloud ofrece potentes funcionalidades para convertir libros de Excel a una amplia gama de formatos, configurar la configuración de página, opciones de guardado e configuraciones de impresión. Los SDK están disponibles para Android, C#, Go, Java, Node.js, Perl, PHP, Python, Ruby y Swift, lo que permite una integración fluida en múltiples plataformas."
weight: 50
ArticleTitle: "Conversión avanzada de archivo Excel – Guía de la API de Aspose.Cells Cloud"
---

## API en la nube avanzada para conversión de Excel

La operación de Conversión avanzada le permite transformar un libro de Excel en diversos formatos de salida (PDF, HTML, CSV, etc.), ofreciéndole un control detallado sobre la configuración de página, las opciones de guardado y las configuraciones de impresión.

**Prerrequisitos / Autenticación**  
Para utilizar este punto de conexión, debe obtener un token de acceso de Aspose.Cells Cloud e incluirlo en el encabezado `Authorization` como un token Bearer.

**Referencia de la API**  
- **Método:** `PUT`  
- **Punto de conexión:** `/cells/convert`  
- **Parámetros:**  
  - `format` (cadena, obligatorio) – Formato de salida deseado (por ejemplo, `pdf`, `html`).  
  - `outPath` (cadena, opcional) – Ruta en el almacenamiento en la nube donde se guardará el archivo convertido.  
  - `options` (objeto, opcional) – Objeto JSON que contiene opciones avanzadas de conversión, como `pageSetup`, `saveOptions` y `printSettings`.  
- **Ejemplo de cuerpo de solicitud:**  
  ```json
  {
    "format": "pdf",
    "outPath": "output/converted.pdf",
    "options": {
      "pageSetup": {
        "orientation": "Landscape",
        "paperSize": "A4"
      },
      "saveOptions": {
        "compress": true
      },
      "printSettings": {
        "printHeadings": false
      }
    }
  }
  ```  
- **Respuesta:**  
  - `200 OK` – Conversión exitosa; la respuesta contiene el flujo del archivo convertido o una referencia al archivo guardado.  
  - `400 Bad Request` – Parámetros inválidos o cuerpo de solicitud mal formado.  
  - `401 Unauthorized` – Autenticación fallida o token ausente.  
  - `500 Internal Server Error` – Error del servidor durante la conversión.  

**Códigos de estado HTTP**

| Código | Significado                | Descripción                                           |
|--------|----------------------------|-------------------------------------------------------|
| 200    | OK                         | Filtro aplicado correctamente; la respuesta contiene detalles de la operación. |
| 400    | Bad Request                | Parámetros faltantes o inválidos (por ejemplo, tipo de archivo no admitido). |
| 401    | Unauthorized               | Token JWT inválido o ausente. |
| 413    | Payload Too Large          | El archivo subido excede el límite de tamaño. |
| 500    | Internal Server Error      | Error inesperado del servidor. |

**Notas**  
* Algunos formatos de salida tienen limitaciones específicas (por ejemplo, la conversión a HTML no preserva las macros). Consulte la documentación específica por formato para obtener detalles.

### Posibilidad de cargar archivos de hojas de cálculo desde múltiples fuentes de datos

### Configuración de página y opciones de guardado

## Familia de SDK en la nube

El uso de un SDK acelera el desarrollo al manejar los detalles de bajo nivel, permitiéndole enfocarse en las tareas de su proyecto. Consulte el <a href="https://github.com/aspose-cells-cloud" target="_blank" rel="noopener noreferrer">repositorio de GitHub</a> para obtener una lista completa de los SDK de Aspose.Cells Cloud.

Los siguientes ejemplos de código muestran cómo realizar llamadas a los servicios web de Aspose.Cells mediante diversos SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePutConvertWorkbook.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PutConvertWorkbook.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PutConvertWorkbook.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PutConvertWorkbook.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PutConvertWorkbook.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PutConvertWorkbook.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PutConvertWorkbook.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PutConvertWorkbook.go" >}}

{{< /tab >}}

{{< /tabs >}}

<script type="application/ld+json">
{
  "@context":"https://schema.org",
  "@type":"WebAPI",
  "name":"Aspose.Cells Cloud Conversión avanzada",
  "description":"Convierta un libro de Excel a PDF/HTML/CSV con opciones avanzadas.",
  "url":"https://api.aspose.cloud/v3.0/cells/convert",
  "documentation":"https://docs.aspose.cloud/cells/advanced-convert-excel/",
  "endpointDescription":"PUT /cells/convert",
  "input":{
    "@type":"PropertyValueSpecification",
    "valueRequired":true,
    "valueName":"format",
    "description":"Formato de salida deseado (pdf, html, csv, …)"
  },
  "target":{
    "@type":"EntryPoint",
    "urlTemplate":"https://api.aspose.cloud/v3.0/cells/convert?format={format}",
    "httpMethod":"PUT"
  }
}
</script>