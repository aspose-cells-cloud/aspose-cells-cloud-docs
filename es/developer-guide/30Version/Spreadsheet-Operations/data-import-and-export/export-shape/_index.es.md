---
title: "Exportar Formas"
second_title: "Documento"
linktitle: "Forma"
type: docs
url: /export-excel-shape-to-different-formats/
aliases: [/export/excel-shape-to-different-formats/]
keywords: "Exportar Formas, Aspose.Cells Cloud, Exportación de formas de Excel, Formatos de imagen, API REST, SDK"
description: "Aprenda cómo exportar formas de Excel a diversos formatos de imagen (PNG, GIF, JPEG, BMP, SVG, TIFF, EMF, WMF) utilizando la API REST y SDK de Aspose.Cells Cloud."
weight: 20
ArticleTitle: "Exportar Formas – Aspose.Cells Cloud"
---

Exportar formas desde Excel permite reutilizar contenido diagramático en múltiples plataformas y aplicaciones. **Prerrequisitos:** un token de acceso JWT válido y el archivo de Excel de origen para subir.

Puede exportar formas a los siguientes formatos: **PNG**, **GIF**, **JPEG**, **BMP**, **SVG**, **TIFF**, **EMF**, **WMF**.

## API PostExport

```http
PUT https://api.aspose.cloud/v3.0/cells/export
```

### **Seguridad y autenticación**

Las API de Aspose.Cells Cloud son seguras y requieren <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">autenticación basada en token JWT</a>.


### Parámetros de la solicitud

| Nombre del parámetro | Tipo   | Ruta / Cadena de consulta / Cuerpo HTTP | Obligatorio | Descripción |
|----------------------|--------|-----------------------------------------|-------------|-------------|
| file                 | archivo | formData                                | Sí          | Archivo a subir |
| objectType           | string | query                                   | Sí          | Tipo de objeto a exportar. Para exportar gráficos, utilice `chart`. Los valores válidos incluyen `shape`, `worksheet`, `picture`, etc. |
| format               | string | query                                   | Sí          | Formato de salida deseado. Valores admitidos: `png`, `jpeg`, `gif`, `bmp`, `svg`, `tiff`, `emf`, `wmf`, `pdf`. |

### **Ejemplo de solicitud**

```bash
curl -X PUT "https://api.aspose.cloud/v3.0/cells/export?objectType=shape&format=tiff" \
     -H "accept: multipart/form-data" \
     -H "Content-Type: multipart/form-data" \
     -H "Authorization: Bearer <your_access_token>" \
     -H "x-aspose-client: Containerize.Swagger" \
     -d '{"File":{}}'
```

### Respuesta

```json
{
  "Files": [
    {
      "Filename": "Book1_xlsx_Sheet1_Shapes_0.tif",
      "FileSize": 390,
      "FileContent": "-----Base64String--------"
    }
    // ... objetos de archivo adicionales ...
  ]
}
```

*Las cargas útiles de archivos codificadas en Base64 suelen oscilar entre unos pocos cientos de bytes y varios megabytes, según las dimensiones y el formato de la imagen.*

**Códigos de estado HTTP**

| Código | Significado              | Descripción |
|--------|--------------------------|-------------|
| 200    | OK                       | Formas exportadas correctamente; la respuesta contiene la lista de archivos. |
| 400    | Solicitud incorrecta     | Parámetros ausentes o inválidos. |
| 401    | No autorizado            | Token de acceso inválido o ausente. |
| 413    | Payload demasiado grande  | El archivo subido excede el límite de tamaño. |
| 500    | Error interno del servidor | Error inesperado en el servidor. |


## Cómo utilizar la API PostExport con SDK

### Especificación de la API PostExport

La [Especificación OpenAPI](https://apireference.aspose.cloud/cells/#/LightCells/PostExport) define una interfaz de programación públicamente accesible y permite realizar interacciones REST directamente desde un navegador web.

Puede utilizar la herramienta de línea de comandos **cURL** para acceder fácilmente a los servicios web de Aspose.Cells. El siguiente ejemplo muestra cómo llamar a la API en la nube utilizando cURL.

```bash
curl -X PUT "https://api.aspose.cloud/v3.0/cells/export?objectType=shape&format=tiff" \
     -H "accept: multipart/form-data" \
     -H "Content-Type: multipart/form-data" \
     -H "Authorization: Bearer <your_access_token>" \
     -H "x-aspose-client: Containerize.Swagger" \
     -d '{"File":{}}'
```

### Utilizar los SDK de Aspose.Cells Cloud

Utilizar un SDK es la forma más rápida de desarrollar contra Aspose.Cells Cloud. Un SDK abstracta los detalles de bajo nivel, permitiéndole centrarse en la lógica de negocio. Consulte el [repositorio de GitHub](https://github.com/aspose-cells-cloud) para obtener una lista completa de los SDK de Aspose.Cells Cloud.

Los siguientes ejemplos de código muestran cómo llamar a los servicios web de Aspose.Cells utilizando diversos SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostExportShape.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostExportShape.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostExportShape.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostExportShape.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostExportShape.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostExportShape.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostExportShape.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostExportShape.go" >}}

{{< /tab >}}

{{< /tabs >}}