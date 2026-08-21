---
title: "Guardar libro de Excel: API de Aspose.Cells Cloud"
second_title: "Documentos"
linktitle: "Guardar como"
type: docs
url: /es/guardar-un-libro-de-excel-en-otros-formatos-de-archivo/
aliases:
  - /convertir-libro-de-excel-a-diferentes-formatos-de-archivo/
  - /guardar-como-otros-formatos/
keywords: "Aspose Cells, Excel, Guardar como, PDF, CSV, JSON, Markdown, API REST"
description: "Guarde libros de Excel en formatos PDF, CSV, JSON, Markdown y otros mediante la API REST de Aspose.Cells Cloud."
weight: 30
---

Esta API REST le permite **guardar** un archivo de Excel en distintos formatos.  
Antes de llamar a este endpoint, asegúrese de tener un token de acceso OAuth 2.0 válido y de que el libro de trabajo origen esté almacenado en su almacenamiento de Aspose Cloud.

**Requisitos previos**  
1. Obtenga un token de acceso JWT e inclúyalo en el encabezado `Authorization: Bearer <token>` de cada solicitud.  
2. Cargue el libro de trabajo origen en el almacenamiento de Aspose Cloud (o confirme que ya existe).  
3. Conozca el nombre del almacenamiento y la ruta de la carpeta donde se encuentra el libro de trabajo.

## API PostWorkbookSaveAs

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/saveAs
```

### **Seguridad y autenticación**

Las API de Aspose.Cells Cloud son seguras y requieren <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">autenticación basada en token JWT</a>.

### **Parámetro de ruta**

| Nombre del parámetro | Tipo   | Descripción                             |
| ---------------------| ------ | --------------------------------------- |
| name                 | string | Nombre del archivo de Excel.            |

### **Parámetro de consulta**

| Nombre del parámetro      | Tipo   | Descripción                                                                                     |
| --------------------------| ------ | ----------------------------------------------------------------------------------------------- |
| newfilename               | string | Nuevo nombre de archivo para el documento guardado.                                             |
| isAutoFitRows             | string | Si es `true`, ajusta automáticamente todas las filas del libro de trabajo. El valor predeterminado es `false`. |
| isAutoFitColumns          | string | Si es `true`, ajusta automáticamente el ancho de las columnas del libro de trabajo. El valor predeterminado es `false`. |
| folder                    | string | Carpeta que contiene el libro de trabajo original.                                              |
| storageName               | string | Nombre del almacenamiento donde se encuentra el archivo de origen.                             |
| outStorageName            | string | Nombre del almacenamiento donde se guardará el archivo de salida.                              |
| checkExcelRestriction     | bool   | Especifica si se deben aplicar restricciones de Excel al modificar celdas u objetos relacionados. |
| region                    | string | Configuración regional aplicada al libro de trabajo.                                            |
| pageWideFitOnPerSheet     | bool   | Ajusta el ancho de página a cada hoja de cálculo durante la conversión.                         |
| pageTallFitOnPerSheet     | bool   | Ajusta la altura de página a cada hoja de cálculo durante la conversión.                        |
| sheetName                 | string | Nombre de la hoja de cálculo que se va a convertir.                                             |
| pageIndex                 | string | Índice de la página que se va a convertir dentro de la hoja especificada (requiere `sheetName`). |
| onePagePerSheet           | bool   | Al convertir a PDF, genera una página por hoja de cálculo.                                      |

### **Parámetro del cuerpo de solicitud**

| Nombre del parámetro | Tipo   | Descripción                                                    |
| ---------------------| ------ | -------------------------------------------------------------- |
| SaveOptions          | Object | Opciones de guardado proporcionadas en la segunda parte de la solicitud multipart. |

**Ejemplo de cuerpo de solicitud (parte JSON de la solicitud multipart)**

```json
{
  "SaveOptions": {
    "SaveFormat": "pdf",
    "CompressionLevel": 9
  }
}
```

### Respuesta

La API devuelve un objeto `SaveResponse`.

```json
{
  "Status": "OK",
  "Code": 200,
  "SaveResult": {
    "Documents": [
      {
        "Name": "sample.pdf",
        "Size": 10240,
        "Folder": "output",
        "Storage": "MyStorage"
      }
    ]
  }
}
```

**Códigos de estado HTTP**

| Código | Significado                 | Descripción                                                    |
|--------|-----------------------------|----------------------------------------------------------------|
| 200    | OK                          | Filtro aplicado correctamente; la respuesta contiene detalles de la operación. |
| 400    | Solicitud incorrecta        | Parámetros ausentes o no válidos (por ejemplo, tipo de archivo no admitido). |
| 401    | No autorizado               | Token JWT inválido o ausente.                                  |
| 413    | Payload demasiado grande     | El archivo cargado supera el límite de tamaño.                 |
| 500    | Error interno del servidor  | Error inesperado del servidor.                                 |

## Cómo usar la API PostWorkbookSaveAs con SDK

### Especificación de la API PostWorkbookSaveAs

La [Especificación OpenAPI](https://reference.aspose.cloud/cells/#/Conversion/PostWorkbookSaveAs) define una interfaz de programación accesible públicamente y le permite realizar interacciones REST directamente desde un navegador web.

Puede utilizar **cURL** para acceder fácilmente a los servicios web de Aspose.Cells. El ejemplo siguiente muestra cómo llamar a la API en la nube con cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Solicitud" tabName12="Respuesta" >}}

{{< tab tabNum="11" >}}

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/sampleBook.xlsx/SaveAs?newfilename=sample.pdf&isAutoFitRows=true&isAutoFitColumns=true" \
  -H "accept: multipart/form-data" \
  -H "Authorization: Bearer <your_jwt_token>"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "SaveResult": {
    "Documents": [
      {
        "Name": "sample.pdf",
        "Size": 10240,
        "Folder": "output",
        "Storage": "MyStorage"
      }
    ]
  },
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

### Utilizar los SDK de Aspose.Cells Cloud

Utilizar un SDK es la mejor manera de acelerar el desarrollo. Un SDK gestiona los detalles de bajo nivel, para que usted pueda centrarse en las tareas de su proyecto. Consulte el <a href="https://github.com/aspose-cells-cloud" target="_blank" rel="noopener noreferrer">repositorio de GitHub</a> para ver una lista completa de los SDK de Aspose.Cells Cloud.

Los siguientes ejemplos de código muestran cómo llamar a los servicios web de Aspose.Cells mediante diversos SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostWorkbookSaveAs.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostWorkbookSaveAs.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostWorkbookSaveAs.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostWorkbookSaveAs.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostWorkbookSaveAs.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostWorkbookSaveAs.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostWorkbookSaveAs.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostWorkbookSaveAs.go" >}}

{{< /tab >}}

{{< /tabs >}}

Para otros escenarios de conversión, consulte las guías [Convertir Excel a PDF](/convertir-excel-a-pdf/) y [Exportar Excel a CSV](/exportar-excel-a-csv/).
---