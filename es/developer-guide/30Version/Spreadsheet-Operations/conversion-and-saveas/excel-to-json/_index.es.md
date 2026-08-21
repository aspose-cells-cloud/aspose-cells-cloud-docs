---
title: "Excel a JSON"
second_title: "Documento"
linktitle: "Excel a JSON"
type: docs
url: /convert-excel-file-to-json-file/
keywords: "Aspose.Cells, Excel a JSON, API en la nube, conversión de hojas de cálculo, API REST"
description: "Aprenda a convertir hojas de cálculo de Excel a archivos JSON mediante la API REST de Aspose.Cells Cloud. Incluye un ejemplo con cURL, fragmentos de código para SDK (C#, Java, Python), parámetros requeridos, autenticación y formato de respuesta."
weight: 100
ArticleTitle: "Convertir Excel a JSON usando la API de Aspose.Cells Cloud – Guía rápida"
---


## API REST

Esta API REST convierte un archivo de hoja de cálculo en un archivo con formato JSON.  


```http
POST https://api.aspose.cloud/v3.0/cells/convert/json
```

### Seguridad y autenticación

Las API de Aspose.Cells Cloud son seguras y requieren [autenticación basada en token JWT](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/).

### Solicitud

**Parámetros de consulta**

| Nombre del parámetro      | Tipo   | Descripción                                                                |
| ------------------------- | ------ | -------------------------------------------------------------------------- |
| `password`                | string | Contraseña necesaria para abrir el archivo de Excel (opcional).            |
| `storageName`             | string | Nombre del almacenamiento donde se encuentra el archivo (opcional).        |
| `checkExcelRestriction`   | bool   | Aplica restricciones específicas de Excel al modificar celdas (opcional).  |

**Parámetro del cuerpo de la solicitud**

| Nombre del parámetro | Tipo | Descripción                                                                                               |
| -------------------- | ---- | --------------------------------------------------------------------------------------------------------- |
| `datafile`           | file | El archivo de Excel que se va a cargar. Debe enviarse como la primera parte de una solicitud `multipart/form-data`. |

#### Ejemplo de llamada con cURL

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/convert/json" \
     -H "Authorization: Bearer $ACCESS_TOKEN" \
     -H "accept: application/json" \
     -H "Content-Type: multipart/form-data" \
     -F "File=@myWorkbook.xlsx"
```

### Respuesta

El servicio devuelve un objeto **FileInfo**. Los campos más importantes se describen a continuación:

| Campo         | Tipo    | Descripción                                                                 |
| ------------- | ------- | --------------------------------------------------------------------------- |
| `Filename`    | string  | Nombre del archivo JSON generado (por ejemplo, `myWorkbook.json`).         |
| `FileSize`    | integer | Tamaño del archivo generado en bytes.                                      |
| `FileContent` | string  | Contenido del archivo JSON en codificación Base64. Decodifíquelo para obtener el JSON real. |

**Ejemplo de respuesta**

```json
{
  "Filename": "myWorkbook.json",
  "FileSize": 8423,
  "FileContent": "eyJmb3JtYXR0ZWRfZGF0YSI6IH ... (cadena en base64) ..."
}
```

#### Manejo de errores

Si la solicitud falla, la API devuelve un objeto de error con la siguiente estructura:

| Campo     | Tipo   | Descripción                                |
| --------- | ------ | ------------------------------------------ |
| `Code`    | string | Identificador legible por máquinas del error. |
| `Message` | string | Descripción legible por humanos del error.    |

Códigos de estado HTTP comunes:

- **400** – Solicitud incorrecta (por ejemplo, archivo faltante o parámetros no válidos).
- **401** – No autorizado (token de acceso no válido o faltante).
- **500** – Error interno del servidor.

**Códigos de estado HTTP**

| Código | Significado                 | Descripción                                            |
|--------|-----------------------------|--------------------------------------------------------|
| 200    | OK                          | Filtro aplicado correctamente; la respuesta contiene detalles de la operación. |
| 400    | Solicitud incorrecta        | Parámetros faltantes o no válidos (por ejemplo, tipo de archivo no admitido). |
| 401    | No autorizado               | Token JWT no válido o faltante.                        |
| 413    | Carga demasiado grande       | El archivo cargado supera el límite de tamaño.        |
| 500    | Error interno del servidor  | Error inesperado en el servidor.                       |
## Cómo usar la API PostConvertWorkbookToJson con SDK

### Especificación de la API PostConvertWorkbookToJson


La <a href="https://reference.aspose.cloud/cells/#/Conversion/PostConvertWorkbookToJson" rel="noopener noreferrer" title="Especificación OpenAPI de Aspose.Cells – Convertir libro a JSON">Especificación OpenAPI</a> define una interfaz de programación accesible públicamente y permite realizar interacciones REST directamente desde un navegador web.

Puede utilizar la herramienta de línea de comandos **cURL** para acceder fácilmente a los servicios web de Aspose.Cells. El siguiente ejemplo muestra cómo realizar llamadas a la API en la nube mediante cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Solicitud" tabName12="Respuesta" >}}

{{< tab tabNum="11" >}}

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/convert/json" \
     -H "Authorization: Bearer $ACCESS_TOKEN" \
     -H "accept: application/json" \
     -H "Content-Type: multipart/form-data" \
     -F "File=@myWorkbook.xlsx"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Filename": "myWorkbook.json",
  "FileSize": 8423,
  "FileContent": "eyJmb3JtYXR0ZWRfZGF0YSI6IH... (cadena en base64)"
}
```

{{< /tab >}}

{{< /tabs >}}

### Utilizar los SDK de Aspose.Cells Cloud

Usar un SDK es la mejor forma de acelerar el desarrollo. Un SDK se encarga de los detalles de bajo nivel, para que usted pueda centrarse en las tareas de su proyecto. Consulte el <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer" title="SDK de Aspose.Cells Cloud en GitHub">repositorio de GitHub</a> para ver una lista completa de los SDK de Aspose.Cells Cloud.

Los siguientes ejemplos de código muestran cómo realizar llamadas a los servicios web de Aspose.Cells utilizando diversos SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example_PostConvertWorkbookToJson.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostConvertWorkbookToJson.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostConvertWorkbookToJson.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostConvertWorkbookToJson.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostConvertWorkbookToJson.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostConvertWorkbookToJson.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostConvertWorkbookToJson.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostConvertWorkbookToJson.go" >}}

{{< /tab >}}

{{< /tabs >}}

## Otras API que implementan funcionalidades similares

- **[POST /cells/{name}/saveAs](https://apireference.aspose.cloud/cells/#/SaveAs/PostDocumentSaveAs)** – Guarda un archivo de Excel como archivo HTML con configuraciones adicionales y almacena el resultado en el almacenamiento especificado.
- **[PUT /cells/convert](https://apireference.aspose.cloud/cells/#/Workbook/PutConvertWorkBook)** – Convierte un archivo de Excel en archivo HTML con configuraciones adicionales y devuelve el resultado en la respuesta.
- **[GET /cells/{name}](https://apireference.aspose.cloud/cells/#/Workbook/GetWorkBook)** – Recupera un archivo de Excel; puede usarse con parámetros de consulta para obtener el archivo en formato HTML.