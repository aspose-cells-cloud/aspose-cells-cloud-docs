---
title: "Convertir un archivo de Excel a diferentes formatos"
ArticleTitle: "Convertir un archivo de Excel a diferentes formatos"
second_title: "Documento"
linktype: "Convertir Excel"
type: docs
url: /es/convert-an-excel-file-to-different-formats/
aliases:
  [
    /convert-excel-workbook-to-different-file-formats/,
    /convert/excel-to-different-formats/,
  ]
keywords: "Aspose.Cells Cloud, conversión de Excel, conversión de formatos de archivo, API REST, SDK, CSV, PDF, HTML, JSON, Markdown"
description: "Convierta libros de Excel a formatos como CSV, PDF, HTML, JSON, Markdown y otros mediante la API REST de Aspose.Cells Cloud."
weight: 10
---

Antes de llamar a este punto final, asegúrese de haber obtenido un token JWT válido y de que el libro de trabajo de origen esté almacenado en una ubicación compatible (por ejemplo, Aspose Cloud Storage). Incluya el token en el encabezado `Authorization` y, si es necesario, especifique el parámetro de consulta `storageName`.

Esta API REST convierte un archivo de Excel a varios formatos de salida.

## API PutConvertWorkBook

```http
PUT https://api.aspose.cloud/v3.0/cells/convert
```

La solicitud es un **PUT** HTTP con contenido multipart (consulte [RFC 2046](https://tools.ietf.org/html/rfc2046#page-17) o [RFC 1341](https://www.w3.org/Protocols/rfc1341/7_2_Multipart.html)).  
La primera parte del cuerpo multipart contiene el **archivo de datos**, y la segunda parte contiene las **opciones de guardado**.

### **Seguridad y autenticación**

Las API de Aspose.Cells Cloud son seguras y requieren <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">autenticación basada en token JWT</a>.

### Parámetros de consulta

| Nombre del parámetro    | Tipo   | Descripción                                                                                                                |
| ----------------------- | ------ | -------------------------------------------------------------------------------------------------------------------------- |
| `format`                | string | Formato de archivo de destino (por ejemplo, CSV, XLS, HTML, PDF, XML, TXT, TIFF, PNG, JPG, GIF, EMF, BMP, MD, Numbers, WMF, SVG, etc.). |
| `password`              | string | Contraseña necesaria para abrir el archivo de Excel de origen.                                                            |
| `outPath`               | string | Ruta completa (incluyendo nombre de archivo y extensión) para un único archivo de salida, o una ruta de carpeta cuando se generan varios archivos. |
| `storageName`           | string | Nombre del almacenamiento donde reside el archivo de origen.                                                              |
| `checkExcelRestriction` | bool   | Si es **true**, valida las restricciones de Excel antes de modificar celdas u objetos relacionados.                      |
| `streamFormat`          | string | Formato del flujo de archivo de entrada.                                                                                  |
| `region`                | string | Configuración regional aplicada al libro de trabajo.                                                                       |
| `pageWideFitOnPerSheet` | bool   | Ajusta el ancho de página para que quepa en cada hoja de cálculo al convertir a PDF.                                      |
| `pageTallFitOnPerSheet` | bool   | Ajusta la altura de página para que quepa en cada hoja de cálculo al convertir a PDF.                                     |
| `sheetName`             | string | Nombre de la hoja de cálculo a convertir.                                                                                 |
| `pageIndex`             | string | Índice de la página a convertir (requiere `sheetName`).                                                                    |
| `onePagePerSheet`       | bool   | Si es **true**, genera una página PDF por hoja de cálculo.                                                                |
| `AutoRowsFit`           | bool   | Ajusta automáticamente todas las filas del libro de trabajo.                                                              |
| `AutoColumnsFit`        | bool   | Ajusta automáticamente el ancho de las columnas del libro de trabajo.                                                     |

### Parámetros del cuerpo de solicitud

| Nombre del parámetro | Tipo      | Descripción                                                    |
| -------------------- | --------- | -------------------------------------------------------------- |
| `datafile`           | data file | El archivo de Excel ubicado en la primera parte del cuerpo multipart. |
| `SaveOptions`        | object    | Opciones de guardado ubicadas en la segunda parte del cuerpo multipart. |

### **Respuesta**

```json
{
    "Name": "ResponseFile",
    "DataType": {
        "Identifier": "File",
        "Reference": "Stream",
        "Name": "file"
    }
}
```

**Códigos de estado HTTP**

| Código | Significado                | Descripción                                             |
| ------ | -------------------------- | ------------------------------------------------------- |
| 200    | OK                         | Filtro aplicado correctamente; la respuesta contiene los detalles de la operación. |
| 400    | Solicitud incorrecta       | Parámetros faltantes o no válidos (por ejemplo, tipo de archivo no admitido). |
| 401    | No autorizado              | Token JWT no válido o faltante.                         |
| 413    | Carga útil demasiado grande | El archivo cargado supera el límite de tamaño.         |
| 500    | Error interno del servidor | Error inesperado en el servidor.                        |

## Cómo usar la API PutConvertWorkBook con SDK

### Especificación de la API PutConvertWorkBook

La [Especificación OpenAPI](https://apireference.aspose.cloud/cells/#/Workbook/PutConvertWorkBook) define una interfaz accesible públicamente que permite interacciones REST directas desde un navegador web.

### Ejemplo con cURL

```bash
curl -X PUT "https://api.aspose.cloud/v3.0/cells/convert?format=html" \
     -H "accept: multipart/form-data" \
     -H "Content-Type: multipart/form-data" \
     -H "x-aspose-client: Containerize.Swagger" \
     -d '{"File":{}}'
```

### Uso de los SDK de Aspose.Cells Cloud

El uso de un SDK acelera el desarrollo al manejar los detalles de bajo nivel, permitiéndole centrarse en la lógica de negocio. Consulte el [repositorio de GitHub](https://github.com/aspose-cells-cloud) para obtener una lista completa de los SDK de Aspose.Cells Cloud.

Los siguientes ejemplos de código muestran cómo llamar a los servicios web de Aspose.Cells con diversos SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePutConvertWorkbook.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PutConvertWorkbook.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "ExamplePutConvertWorkbook.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "ExamplePutConvertWorkbook.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "ExamplePutConvertWorkbook.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "ExamplePutConvertWorkbook.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "ExamplePutConvertWorkbook.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "ExamplePutConvertWorkbook.go" >}}

{{< /tab >}}

{{< /tabs >}}
---