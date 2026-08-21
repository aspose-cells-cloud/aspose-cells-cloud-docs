---
title: "Excel a SQL"
second_title: "Documento"
linktitle: "Excel a SQL"
type: docs
url: /convert-excel-file-to-sql-file/
keywords: "Aspose.Cells, Excel a SQL, API en la nube, conversión de hojas de cálculo, REST"
description: "Utilice la API REST de Aspose.Cells Cloud para convertir hojas de cálculo de Excel en archivos SQL. Admite múltiples SDK y lenguajes de programación para una integración fluida en sus aplicaciones."
weight: 100
ArticleTitle: "Convertir Excel a SQL – Aspose.Cells Cloud API"
---

Esta API REST convierte un archivo de hoja de cálculo a un archivo en formato SQL.

**Prerrequisitos**  
Para utilizar este punto de conexión, debe tener un token JWT válido generado según lo descrito en la guía de <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">autenticación basada en token JWT</a>. La API admite archivos de Excel hasta los límites de tamaño definidos en la documentación del servicio y puede manejar libros protegidos con contraseña cuando se proporciona el parámetro de consulta `password`.

## API PostConvertWorkbookToSQL

```http
POST https://api.aspose.cloud/v3.0/cells/convert/sql
```

### **Seguridad y autenticación**

Las API de Aspose.Cells Cloud son seguras y requieren <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">autenticación basada en token JWT</a>.

### **Parámetro de consulta**

| Nombre del parámetro  | Tipo   | Descripción                                                                                      |
| --------------------- | ------ | ------------------------------------------------------------------------------------------------ |
| password              | string | Contraseña necesaria para abrir el archivo de Excel.                                             |
| storageName           | string | Nombre del almacenamiento donde se guarda el archivo.                                            |
| checkExcelRestriction | bool   | Indica si se deben verificar las restricciones del archivo de Excel al modificar objetos relacionados con celdas. |

### **Parámetro del cuerpo de solicitud**

| Nombre del parámetro | Tipo      | Descripción                                                                      |
| -------------------- | --------- | -------------------------------------------------------------------------------- |
| datafile             | data file | El archivo de hoja de cálculo que se va a convertir, incluido como la primera parte de la solicitud. |

### Respuesta

La API devuelve un objeto **FileInfo** que contiene el archivo SQL generado.

| Campo           | Tipo   | Descripción                                   |
| --------------- | ------ | --------------------------------------------- |
| **Filename**    | string | Nombre del archivo SQL (por ejemplo, `ejemplo.sql`). |
| **FileSize**    | int    | Tamaño del archivo en bytes.                  |
| **FileContent** | string | Contenido del archivo SQL codificado en Base64.      |

[FileInfo](/cells/file-info/)

**Códigos de estado HTTP**

| Código | Significado                 | Descripción                                                                 |
| ------ | --------------------------- | --------------------------------------------------------------------------- |
| 200    | Correcto                    | Filtro aplicado correctamente; la respuesta contiene detalles de la operación. |
| 400    | Solicitud incorrecta        | Parámetros faltantes o no válidos (por ejemplo, tipo de archivo no admitido). |
| 401    | No autorizado               | Token JWT inválido o faltante.                                              |
| 413    | Payload demasiado grande     | El archivo cargado excede el límite de tamaño.                             |
| 500    | Error interno del servidor  | Error inesperado en el servidor.                                            |

## Cómo utilizar la API PostConvertWorkbookToSQL con SDK

### Especificación de la API PostConvertWorkbookToSQL

La <a href="https://reference.aspose.cloud/cells/#/Conversion/PostConvertWorkbookToSQL" rel="noopener noreferrer">Especificación OpenAPI</a> define una interfaz de programación accesible públicamente y le permite realizar interacciones REST directamente desde un navegador web.

Puede utilizar la herramienta de línea de comandos **cURL** para acceder fácilmente a los servicios web de Aspose.Cells. El siguiente ejemplo muestra cómo realizar llamadas a la API en la nube con cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Solicitud" tabName12="Respuesta" >}}

{{< tab tabNum="11" >}}

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/convert/sql" \
     -H "accept: multipart/form-data" \
     -H "Content-Type: multipart/form-data" \
     -H "x-aspose-client: curl" \
     -d '{"File":{}}'
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Filename": "ejemplo.sql",
  "FileSize": 1024,
  "FileContent": "cadena_codificada_en_base64"
}
```

{{< /tab >}}

{{< /tabs >}}

### Utilizar los SDK de Aspose.Cells Cloud

Utilizar un SDK es la mejor forma de acelerar el desarrollo. Un SDK maneja los detalles de bajo nivel, lo que le permite centrarse en las tareas de su proyecto. Consulte el <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">repositorio de GitHub</a> para obtener una lista completa de los SDK de Aspose.Cells Cloud.

Los siguientes ejemplos de código muestran cómo llamar a los servicios web de Aspose.Cells utilizando diversos SDK:
{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example_PostConvertWorkbookToSQL.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostConvertWorkbookToSQL.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostConvertWorkbookToSQL.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostConvertWorkbookToSQL.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostConvertWorkbookToSQL.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostConvertWorkbookToSQL.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostConvertWorkbookToSQL.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostConvertWorkbookToSQL.go" >}}

{{< /tab >}}

{{< /tabs >}}

## Otras API que implementan esta función

- **[POST /cells/{name}/saveAs](https://apireference.aspose.cloud/cells/#/SaveAs/PostDocumentSaveAs)** – Guarda un libro en otro formato y almacena el resultado en el almacenamiento especificado.

- **[PUT /cells/convert](https://apireference.aspose.cloud/cells/#/Workbook/PutConvertWorkBook)** – Convierte un libro a otro formato con configuraciones opcionales y devuelve el resultado en la respuesta.

- **[GET /cells/{name}](https://apireference.aspose.cloud/cells/#/Workbook/GetWorkBook)** – Recupera un libro con configuraciones de conversión opcionales.

**Notas**  
- Al convertir archivos de Excel protegidos con contraseña, asegúrese de proporcionar el parámetro de consulta `password`; de lo contrario, la conversión fallará con un error 400.  
- El servicio devuelve el contenido del archivo SQL en Base64; decodifíquelo antes de guardarlo como un archivo `.sql`.  

**Archivos de ejemplo**  
Descargue un libro de Excel de ejemplo [aquí](https://example.com/sample.xlsx) y un resultado SQL pregenerado [aquí](https://example.com/sample.sql) para probar rápidamente la API.