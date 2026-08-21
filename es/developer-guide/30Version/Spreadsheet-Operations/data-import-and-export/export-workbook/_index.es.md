---
title: "Exportar Libro de Trabajo"
second_title: "Documento"
linktitle: "Libro de Trabajo"
type: docs
url: /export-excel-to-different-formats/
aliases: [/export/excel-to-different-formats/]
keywords: "Aspose.Cells Cloud, exportación de Excel, conversión de libro de trabajo, PDF, CSV, JSON, formatos de imagen, API de hojas de cálculo, XLSX, ODS, PNG"
description: "Una guía paso a paso sobre cómo exportar libros de trabajo de Excel a múltiples formatos, incluyendo PDF, CSV, JSON y varios tipos de imagen, utilizando la API REST y los SDK de Aspose.Cells Cloud."
weight: 20
---

Puede exportar libros de trabajo a cualquiera de los siguientes formatos: [XLS](https://docs.fileformat.com/spreadsheet/xls/), [XLSX](https://docs.fileformat.com/spreadsheet/xlsx/), [XLSB](https://docs.fileformat.com/spreadsheet/xlsb/), [CSV](https://docs.fileformat.com/spreadsheet/csv/), [TSV](https://docs.fileformat.com/spreadsheet/tsv/), [XLSM](https://docs.fileformat.com/spreadsheet/xlsm/), [ODS](https://docs.fileformat.com/spreadsheet/ods/), [TXT](https://docs.fileformat.com/word-processing/txt/), [PDF](https://docs.fileformat.com/pdf/), [OTS](https://docs.fileformat.com/spreadsheet/ots/), [XPS](https://docs.fileformat.com/page-description-language/xps/), [DIF](https://docs.fileformat.com/spreadsheet/dif/), [PNG](https://docs.fileformat.com/Image/png/), [JPEG](https://docs.fileformat.com/image/jpeg/), [BMP](https://docs.fileformat.com/image/bmp/), [SVG](https://docs.fileformat.com/page-description-language/svg/), [TIFF](https://docs.fileformat.com/image/tiff/), [EMF](https://docs.fileformat.com/image/emf/), [NUMBERS](https://docs.fileformat.com/spreadsheet/numbers/), [FODS](https://docs.fileformat.com/spreadsheet/fods/).

## API REST


```bash
POST https://api.aspose.cloud/v3.0/cells/export
```

### **Seguridad y Autenticación**

Las API de Aspose.Cells Cloud son seguras y requieren <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">autenticación basada en token JWT</a>.


### Parámetros de Solicitud

| Nombre del Parámetro | Tipo    | Ruta/Cadena de Consulta/Cuerpo HTTP | Obligatorio | Descripción |
|----------------------|---------|-------------------------------------|-------------|-------------|
| file                 | archivo | formData                            | Sí          | Archivo a cargar |
| objectType           | string  | query                               | Sí          | Tipo de objeto a exportar. Para exportar gráficos use `chart`. Otros valores posibles son `worksheet`, `picture`, etc. |
| format               | string  | query                               | Sí          | Formato de salida deseado. Valores admitidos: `png`, `jpeg`, `gif`, `bmp`, `svg`, `tiff`, `emf`, `wmf`, `pdf`. |


### **Respuesta**

```json
{
  "Files": [
    {
      "Filename": "Book1_xlsx.tif",
      "FileSize": 274022,
      "FileContent": "-----Base64String--------"
    },
    {
      "Filename": "myDocument_xlsx.tif",
      "FileSize": 348126,
      "FileContent": "-----Base64String--------"
    }
  ]
}
```


**Códigos de Estado HTTP**

| Código | Significado           | Descripción |
|--------|-----------------------|-------------|
| 200    | OK                    | Formas exportadas correctamente; la respuesta contiene la lista de archivos. |
| 400    | Solicitud Incorrecta  | Parámetros faltantes o inválidos. |
| 401    | No Autorizado         | Token de acceso inválido o faltante. |
| 413    | Carga Demasiado Grande| El archivo cargado supera el límite de tamaño. |
| 500    | Error Interno del Servidor | Error inesperado en el servidor. |


## Cómo Usar la API PostExport con SDK

### Especificación de la API PostExport


La [Especificación OpenAPI](https://apireference.aspose.cloud/cells/#/LightCells/PostExport) define una interfaz de programación accesible públicamente que le permite realizar interacciones REST directamente desde un navegador web.

Puede utilizar la herramienta de línea de comandos **cURL** para acceder fácilmente a los servicios web de Aspose.Cells. El siguiente ejemplo muestra cómo llamar a la API en la nube mediante cURL.

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/export?objectType=workbook&format=tiff" \
     -H "accept: multipart/form-data" \
     -H "Content-Type: multipart/form-data" \
     -H "x-aspose-client: Containerize.Swagger" \
     -d '{"File":{}}'
```

### Uso de los SDK de Aspose.Cells Cloud

El uso de un SDK acelera el desarrollo al manejar los detalles de bajo nivel, permitiéndole centrarse en la lógica de negocio. Una lista completa de los SDK de Aspose.Cells Cloud está disponible en el [repositorio de GitHub](https://github.com/aspose-cells-cloud).

Los siguientes ejemplos de código muestran cómo llamar al servicio web de Aspose.Cells utilizando diversos SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostExport.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostExport.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostExport.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostExport.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostExport.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostExport.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostExport.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostExport.go" >}}

{{< /tab >}}

{{< /tabs >}}