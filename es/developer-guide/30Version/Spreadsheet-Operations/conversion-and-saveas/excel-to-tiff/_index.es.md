---
title: "Excel a TIFF"
second_title: "Documentos"
linketitle: "Excel a TIFF"
type: docs
url: /es/convert-excel-file-to-tiff-file/
aliases: [  /es/convert-excel-file-to-tiff-in-cloud/ , /es/convert/excel-to-tiff/ ]
keywords: "Aspose.Cells Cloud, conversión de Excel a TIFF, API REST, cURL, SDK, .NET, Java, Python, exportación de imágenes"
description: "Aprenda cómo convertir libros de Excel en imágenes TIFF de alta calidad mediante la API de Aspose.Cells Cloud. Comandos detallados de cURL, ejemplos de SDK (C#, Java, Python, etc.), pasos de autenticación y manejo de errores."
weight: 90
---

Los puntos finales **Convert**, **SaveAs** y **Export** de Aspose.Cells Cloud le permiten transformar un libro de Excel en una imagen TIFF.  
Puede invocar estos puntos finales directamente mediante **cURL** o a través de uno de los SDK admitidos.

## API REST

| **API**                | **Método** | **Finalidad**                                                                                   | **Enlace Swagger**                                                                          |
| ---------------------- | ---------- | ----------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------- |
| `/cells/convert`       | PUT        | Convierte un libro suministrado en el cuerpo de la solicitud al formato especificado (TIFF).   | [PutConvertWorkBook](https://apireference.aspose.cloud/cells/#/Workbook/PutConvertWorkBook) |
| `/cells/{name}`        | GET        | Exporta el libro indicado a otro formato (TIFF) y devuelve el resultado en la respuesta.      | [GetWorkBook](https://apireference.aspose.cloud/cells/#/Workbook/GetWorkBook)               |
| `/cells/{name}/saveAs` | POST       | Guarda el libro en un formato elegido (TIFF) y almacena el resultado en el almacenamiento en la nube. | [PostDocumentSaveAs](https://apireference.aspose.cloud/cells/#/SaveAs/PostDocumentSaveAs)   |

Estos puntos finales son accesibles públicamente y pueden invocarse directamente desde un navegador web o cualquier cliente HTTP.

### Ejemplos con cURL

{{< tabs tabTotal="3" tabID="11" tabName11="convert" tabName12="saveas" tabName13="export">}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/convert?format=tiff" \
     -X PUT \
     -d '{"File":{"Name":"book1.xlsx","Data":"<contenido-base64>"},"SaveFormat":"tiff"}' \
     -H "Content-Type: application/json" \
     -H "Accept: application/json" \
     -H "Authorization: Bearer <token jwt>"
```

{{< /tab >}}
{{< tab tabNum="12" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/book1.xlsx/saveas?newfilename=book1.tiff" \
     -X POST \
     -d '{"SaveFormat":"tiff","ImageFormat":"tiff"}' \
     -H "Content-Type: application/json" \
     -H "Accept: application/json" \
     -H "Authorization: Bearer <token jwt>"
```

{{< /tab >}}
{{< tab tabNum="13" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/book1.xlsx?format=tiff" \
     -X GET \
     -H "Authorization: Bearer <token jwt>"
```

{{< /tab >}}
{{< /tabs >}}

> **Nota:**
>
> - El cuerpo de la solicitud **Convert** debe contener el archivo (o una referencia a un archivo almacenado) y el `SaveFormat` deseado.
> - La solicitud **Export** no requiere cuerpo; el formato se especifica mediante la cadena de consulta (`format=tiff`).

## Manejo de errores

| **Código de estado** | **Significado**       | **Causa típica**                            |
| -------------------- | --------------------- | ------------------------------------------- |
| 200                  | Correcto              | La imagen TIFF se devuelve (flujo binario). |
| 400                  | Solicitud incorrecta  | Parámetros faltantes o con formato incorrecto. |
| 401                  | No autorizado         | Token JWT inválido o ausente.               |
| 404                  | No encontrado         | El libro especificado no existe.            |
| 500                  | Error interno del servidor | Condición inesperada del lado del servidor. |

Cuando se produce un error, la API devuelve una carga útil JSON con los campos `Code`, `Message` y, opcionalmente, `Description`.

## Familia de SDK en la nube

Utilizar un SDK es la forma más rápida de desarrollar. Un SDK gestiona los detalles de bajo nivel para que usted pueda centrarse en su proyecto. Consulte el [repositorio de GitHub](https://github.com/aspose-cells-cloud) para obtener una lista completa de los SDK de Aspose.Cells Cloud.

Los siguientes ejemplos de código muestran cómo invocar los servicios web de Aspose.Cells mediante diversos SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePutConvertWorkbookToTiff.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PutConvertWorkbookToTiff.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PutConvertWorkbookToTiff.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PutConvertWorkbookToTiff.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PutConvertWorkbookToTiff.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PutConvertWorkbookToTiff.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PutConvertWorkbookToTiff.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PutConvertWorkbookToTiff.go" >}}

{{< /tab >}}

{{< /tabs >}}

---