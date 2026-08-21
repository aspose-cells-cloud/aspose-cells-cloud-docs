---
title: "Exportar gráfico de Excel"
second_title: "Documento"
linktitle: "Gráfico"
type: docs
url: /export-excel-chart-to-different-formats/
aliases: [/export/excel-chart-to-different-formats/]
description: "Exporte objetos de gráfico de Excel a formatos populares como PNG, JPEG, PDF, SVG, TIFF, EMF, WMF y más utilizando la API REST de Aspose.Cells Cloud o los SDK. Incluye autenticación, un ejemplo con cURL y ejemplos de código para múltiples lenguajes."
keywords: "Aspose.Cells, exportar gráfico, exportación de gráfico de Excel, API REST, cURL, PDF, PNG, JPEG, SVG, TIFF, EMF, WMF, SDK, formatos de gráfico, Aspose Cells Cloud"
weight: 20
ArticleTitle: "Exportar gráfico de Excel – Documento"
---

Exportar objetos de gráfico desde un libro de Excel a diversos formatos de imagen y documento es un requisito común para informes y publicaciones. Aspose.Cells Cloud proporciona un endpoint REST simple que convierte gráficos directamente a formatos populares como PNG, JPEG, PDF, SVG, TIFF, EMF, WMF y más.

Puede exportar gráficos a los siguientes formatos: [PNG](https://docs.fileformat.com/Image/png/), [GIF](https://docs.fileformat.com/image/gif/), [JPEG](https://docs.fileformat.com/image/jpeg/), [BMP](https://docs.fileformat.com/image/bmp/), [SVG](https://docs.fileformat.com/page-description-language/svg/), [TIFF](https://docs.fileformat.com/image/tiff/), [EMF](https://docs.fileformat.com/image/emf/), [WMF](https://docs.fileformat.com/image/Wmf/), y [PDF](https://docs.fileformat.com/pdf/).

**Requisitos previos:**  
- Una cuenta válida de Aspose.Cells Cloud con una suscripción activa.  
- Un token OAuth 2.0 Bearer (JWT) obtenido mediante el flujo de autenticación.  
- El archivo de libro que se va a cargar (tamaño máximo < 50 MB).  

## **API REST**

```bash
POST https://api.aspose.cloud/v3.0/cells/export
```

### **Seguridad y autenticación**

Las API de Aspose.Cells Cloud son seguras y requieren <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">autenticación basada en token JWT</a>.

### Parámetros de solicitud

| Nombre del parámetro | Tipo   | Ruta/Cadena de consulta/Cuerpo HTTP | Obligatorio | Descripción                                                                                                                     |
|----------------------|--------|-------------------------------------|-------------|---------------------------------------------------------------------------------------------------------------------------------|
| file                 | archivo | formData                            | Sí          | Archivo que se va a cargar                                                                                                      |
| objectType           | cadena | query                               | Sí          | Tipo de objeto que se va a exportar. Para exportar gráficos utilice `chart`. Otros valores posibles son `worksheet`, `picture`, etc. |
| format               | cadena | query                               | Sí          | Formato de salida deseado. Valores admitidos: `png`, `jpeg`, `gif`, `bmp`, `svg`, `tiff`, `emf`, `wmf`, `pdf`.                 |

### **Respuesta**

```json
{
  "Files": [
    {
      "Filename": "Book1_xlsx_Sheet4_Charts_0.tif",
      "FileSize": 10040,
      "FileContent": "-----Base64String--------"
    },
    {
      "Filename": "Book1_xlsx_Sheet4_Charts_1.tif",
      "FileSize": 12978,
      "FileContent": "-----Base64String--------"
    },
    {
      "Filename": "Book1_xlsx_Sheet4_Charts_2.tif",
      "FileSize": 7002,
      "FileContent": "-----Base64String--------"
    },
    {
      "Filename": "Book1_xlsx_Sheet4_Charts_3.tif",
      "FileSize": 11532,
      "FileContent": "-----Base64String--------"
    },
    {
      "Filename": "Book1_xlsx_Sheet6_Charts_0.tif",
      "FileSize": 8270,
      "FileContent": "-----Base64String--------"
    },
    {
      "Filename": "myDocument_xlsx_Sheet3_Charts_0.tif",
      "FileSize": 42570,
      "FileContent": "-----Base64String--------"
    },
    {
      "Filename": "myDocument_xlsx_Sheet3_Charts_1.tif",
      "FileSize": 12102,
      "FileContent": "-----Base64String--------"
    },
    {
      "Filename": "myDocument_xlsx_Sheet3_Charts_2.tif",
      "FileSize": 8290,
      "FileContent": "-----Base64String--------"
    }
  ]
}
```

**Códigos de estado HTTP**

| Código | Significado                 | Descripción                                              |
|--------|-----------------------------|----------------------------------------------------------|
| 200    | OK                          | Filtro aplicado correctamente; la respuesta contiene detalles de la operación. |
| 400    | Solicitud incorrecta        | Parámetros faltantes o no válidos (por ejemplo, tipo de archivo no admitido). |
| 401    | No autorizado               | Token JWT no válido o ausente.                           |
| 413    | Payload demasiado grande     | El archivo cargado supera el límite de tamaño.         |
| 500    | Error interno del servidor  | Error inesperado en el servidor.                         |

## Cómo usar la API PostExport con SDK

### Especificación de la API PostExport

La [Especificación OpenAPI](https://apireference.aspose.cloud/cells/#/LightCells/PostExport) define una interfaz de programación públicamente accesible y permite realizar interacciones REST directamente desde un navegador web.

Todas las solicitudes deben incluir un token OAuth 2.0 Bearer válido en el encabezado `Authorization`. El siguiente ejemplo muestra cómo llamar a la API mediante **cURL** y cargar un libro mediante multipart/form‑data.

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/export?objectType=chart&format=tiff" \
  -H "Authorization: Bearer {access_token}" \
  -H "Accept: multipart/form-data" \
  -H "Content-Type: multipart/form-data" \
  -H "x-aspose-client: Containerize.Swagger" \
  -F "File=@/path/to/your/workbook.xlsx"
```

### Utilizar los SDK de Aspose.Cells Cloud

Utilizar un SDK es la mejor manera de acelerar el desarrollo. Un SDK se encarga de los detalles de bajo nivel y le permite centrarse en las tareas de su proyecto. Consulte el [repositorio de GitHub](https://github.com/aspose-cells-cloud) para obtener una lista completa de los SDK de Aspose.Cells Cloud.

Los siguientes ejemplos de código muestran cómo realizar llamadas a los servicios web de Aspose.Cells mediante diversos SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostExportChart.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostExportChart.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostExportChart.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostExportChart.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostExportChart.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostExportChart.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostExportChart.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostExportChart.go" >}}

{{< /tab >}}

{{< /tabs >}}