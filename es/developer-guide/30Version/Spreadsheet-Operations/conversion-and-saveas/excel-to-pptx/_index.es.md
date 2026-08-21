---
title: "Convertir Excel a PPTX mediante la API de Aspose.Cells Cloud v3.0"
second_title: "Documento"
linktitle: "Excel a PPTX"
type: docs
url: /convert-excel-file-to-pptx-file/
keywords: "Aspose, Cells, Excel, PPTX, conversión, API REST, nube"
description: "Aprenda cómo convertir libros de Excel a presentaciones PPTX mediante la API REST de Aspose.Cells Cloud v3.0. Incluye solicitud cURL, ejemplos de código con SDK, autenticación y manejo de errores."
weight: 90
ArticleTitle: "Convertir Excel a PPTX mediante la API de Aspose.Cells Cloud v3.0"
---

Esta API REST convierte un archivo de hoja de cálculo al formato PPTX.

## API PostConvertWorkbookToPptx

```http
POST https://api.aspose.cloud/v3.0/cells/convert/pptx
```

### **Seguridad y autenticación**

Las API de Aspose.Cells Cloud son seguras y requieren <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">autenticación basada en token JWT</a>.

### Parámetros de consulta

| Nombre del parámetro    | Tipo   | Descripción                                                                                  |
| ----------------------- | ------ | -------------------------------------------------------------------------------------------- |
| `password`              | string | Contraseña necesaria para abrir el libro de Excel.                                           |
| `storageName`           | string | Nombre del almacenamiento donde se encuentra el archivo de origen.                           |
| `checkExcelRestriction` | bool   | Indica si se deben aplicar restricciones de archivo de Excel al modificar objetos relacionados con celdas. |

### Parámetro del cuerpo de solicitud

| Nombre del parámetro | Tipo      | Descripción                                                            |
| -------------------- | --------- | ---------------------------------------------------------------------- |
| `datafile`           | data file | El archivo Excel incluido en la primera parte del cuerpo de solicitud multipart. |

**Ejemplo de cuerpo de solicitud multipart (simplificado):**

```
--boundary
Content-Disposition: form-data; name="File"; filename="input.xlsx"
Content-Type: application/vnd.openxmlformats-officedocument.spreadsheetml.sheet

<contenido binario de input.xlsx>
--boundary
Content-Disposition: form-data; name="password"

MyPwd
--boundary--
```

### Respuesta

La API devuelve un objeto **FileInfo** que contiene el archivo pptx generado.

| Campo           | Tipo   | Descripción                                      |
| --------------- | ------ | ------------------------------------------------ |
| **Filename**    | string | Nombre del archivo pptx (por ejemplo, `ejemplo.pptx`). |
| **FileSize**    | int    | Tamaño del archivo en bytes.                     |
| **FileContent** | string | Contenido del archivo pptx codificado en Base64. |

[FileInfo](/cells/file-info/)


**Códigos de estado HTTP**

| Código | Significado                 | Descripción                                               |
|--------|-----------------------------|-----------------------------------------------------------|
| 200    | Correcto                    | Filtro aplicado correctamente; la respuesta contiene los detalles de la operación. |
| 400    | Solicitud incorrecta        | Parámetros ausentes o no válidos (por ejemplo, tipo de archivo no admitido). |
| 401    | No autorizado               | Token JWT no válido o ausente. |
| 413    | Payload demasiado grande     | El archivo cargado supera el límite de tamaño. |
| 500    | Error interno del servidor  | Error inesperado en el servidor. |

*Notas:* El punto de conexión admite formatos comunes de Excel (`.xlsx`, `.xls`, `.xlsm`). El tamaño máximo del archivo está limitado a 50 MB. La conversión podría estar restringida para libros que contengan macros o hojas protegidas, a menos que se proporcionen los parámetros adecuados.

## Cómo usar la API PostConvertWorkbookToPptx con SDK

### Especificación de la API PostConvertWorkbookToPptx

La <a href="https://reference.aspose.cloud/cells/#/Conversion/PostConvertWorkbookToPptx" rel="noopener noreferrer">Especificación OpenAPI</a> define una interfaz de programación públicamente accesible y le permite realizar interacciones REST directamente desde un navegador web.

Puede utilizar la herramienta de línea de comandos **cURL** para acceder fácilmente a los servicios web de Aspose.Cells. El ejemplo siguiente muestra cómo invocar la API en la nube mediante cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Solicitud" tabName12="Respuesta" >}}

{{< tab tabNum="11" >}}

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/convert/pptx?storageName=MyStorage" \
     -H "Authorization: Bearer {access_token}" \
     -H "accept: multipart/form-data" \
     -H "Content-Type: multipart/form-data" \
     -F "File=@/ruta/hacia/input.xlsx" \
     -F "password=MiContraseña"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Filename": "ejemplo.pptx",
  "FileSize": 123456,
  "FileContent": "Contenido del archivo: cadena_codificada_en_base64"
}
```

{{< /tab >}}

{{< /tabs >}}

### Utilizar los SDK de Aspose.Cells Cloud

Usar un SDK es la forma más rápida de desarrollar. Un SDK abstracta los detalles de bajo nivel para que pueda centrarse en su proyecto. Consulte el [repositorio de GitHub](https://github.com/aspose-cells-cloud" rel="noopener noreferrer") para obtener una lista completa de los SDK de Aspose.Cells Cloud.

Los siguientes ejemplos de código muestran cómo invocar los servicios web de Aspose.Cells mediante diversos SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example_PostConvertWorkbookToPptx.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostConvertWorkbookToPptx.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostConvertWorkbookToPptx.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostConvertWorkbookToPptx.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostConvertWorkbookToPptx.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1c" "Example_PostConvertWorkbookToPptx.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostConvertWorkbookToPptx.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostConvertWorkbookToPptx.go" >}}

{{< /tab >}}

{{< /tabs >}}

## Otras API que implementan esta función

- **[POST /cells/convert/pdf](https://apireference.aspose.cloud/cells/#/Conversion/PostConvertWorkbookToPdf)** – Convierte un archivo de Excel a PDF.
- **[POST /cells/convert/png](https://apireference.aspose.cloud/cells/#/Conversion/PostConvertWorkbookToPng)** – Convierte un archivo de Excel a imágenes PNG.
- **[POST /cells/convert/svg](https://apireference.aspose.cloud/cells/#/Conversion/PostConvertWorkbookToSvg)** – Convierte un archivo de Excel al formato SVG.
---