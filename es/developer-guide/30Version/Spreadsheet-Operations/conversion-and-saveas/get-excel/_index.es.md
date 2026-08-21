---
title: "Aspose.Cells Cloud: Convertir libro de Excel a PDF, CSV, HTML y más (GET /cells/{name})"
second_title: "Documento"
linktitle: "Convertir Excel"
type: docs
url: /es/get-different-formats-files/
aliases:
  - /export-excel-workbook-to-different-file-formats/
  - /export-different-formats/
keywords: "Aspose.Cells, conversión de Excel, convertir Excel, PDF, CSV, HTML, ODS, JSON, formatos de imagen, exportación de hojas de cálculo, API, REST"
description: "Aprenda cómo recuperar un libro de Excel en cualquier formato (PDF, CSV, HTML, PNG, etc.) mediante la API REST de Aspose.Cells Cloud. Incluye ejemplos con cURL, SDK, autenticación y detalles de respuesta."
weight: 10
ArticleTitle: "Aspose.Cells Cloud: Convertir libro de Excel a PDF, CSV, HTML y más (GET /cells/{name})"
---

Esta API REST recupera un libro de Excel en un formato diferente.

## API GetWorkBook

```http
GET https://api.aspose.cloud/v3.0/cells/{name}
```

### **Seguridad y autenticación**

Las API de Aspose.Cells Cloud son seguras y requieren <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">autenticación mediante token JWT</a>.

### **Parámetros de consulta**

| Nombre del parámetro    | Tipo   | Descripción                                                                                                                                                                          | Valor predeterminado |
| ----------------------- | ------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------- |
| format                  | string | Formato de archivo de destino (por ejemplo, CSV, XLS, HTML, MHTML, ODS, PDF, XML, TXT, TIFF, XLSB, XLSM, XLSX, XLTM, XLTX, XPS, PNG, JPG, GIF, EMF, BMP, MD, Numbers, WMF, SVG, etc.). | –                   |
| password                | string | Contraseña necesaria para abrir el archivo de Excel.                                                                                                                                | –                   |
| isAutoFit               | bool   | Ajusta automáticamente el ancho de filas y columnas.                                                                                                                               | false               |
| onlySaveTable           | bool   | Si es **true**, solo se guarda la información de la tabla. Acepta `true` o `false`.                                                                                                 | false               |
| outPath                 | string | Ruta donde guardar el resultado. Para un solo archivo, incluya el nombre y extensión del archivo; para varios archivos, especifique únicamente la carpeta.                          | –                   |
| outStorageName          | string | Nombre del almacenamiento donde se guardará el archivo de salida.                                                                                                                  | –                   |
| checkExcelRestriction   | bool   | Verifica las restricciones de Excel al modificar celdas u objetos relacionados.                                                                                                    | false               |
| region                  | string | Configuración regional aplicada al libro de trabajo.                                                                                                                               | –                   |
| pageWideFitOnPerSheet   | bool   | Ajusta el ancho de página a cada hoja de cálculo al convertir a PDF.                                                                                                                | false               |
| pageTallFitOnPerSheet   | bool   | Ajusta la altura de página a cada hoja de cálculo al convertir a PDF.                                                                                                               | false               |
| onePagePerSheet         | bool   | Genera una página PDF por hoja de cálculo.                                                                                                                                         | false               |
| folder                  | string | Ruta de la carpeta donde se encuentra el libro de trabajo original.                                                                                                                 | –                   |
| storageName           | string | Nombre del almacenamiento donde se encuentra el archivo fuente.                                                                                                                    | –                   |

### Respuesta

**Éxito (200)**

- La API devuelve un objeto **[Workbook](/es/cells/workbook/)** que contiene información sobre la estructura del libro cuando se omite el parámetro de consulta `format`.

- La API devuelve el archivo convertido en el formato solicitado cuando el parámetro de consulta `format` especifica un tipo de archivo.

```http
HTTP/1.1 200 OK
Content-Type: application/pdf
Content-Disposition: attachment; filename="book1.pdf"
Content-Length: 123456

(datos binarios del PDF)
```

**Códigos de estado HTTP**

| Código | Significado                 | Descripción                                              |
|--------|-----------------------------|----------------------------------------------------------|
| 200    | Correcto                    | Filtro aplicado correctamente; la respuesta contiene detalles de la operación. |
| 400    | Solicitud incorrecta        | Parámetros faltantes o no válidos (por ejemplo, tipo de archivo no admitido). |
| 401    | No autorizado               | Token JWT inválido o ausente.                            |
| 413    | Carga demasiado grande       | El archivo cargado supera el límite de tamaño.          |
| 500    | Error interno del servidor  | Error inesperado en el servidor.                         |

> **Notas:**  
> - Los libros de trabajo grandes pueden tardar más en convertirse; considere aumentar el tiempo de espera de la solicitud.  
> - Algunos formatos (por ejemplo, `ODS`) no son compatibles con ciertas características de Excel, como macros.

## Cómo usar la API GetWorkBook con SDK

> **Requisitos previos:**  
> - Un **token de acceso JWT** válido obtenido mediante el flujo de autenticación de Aspose.Cells.  
> - El libro de trabajo fuente debe estar almacenado en un almacenamiento admitido por Aspose o proporcionarse directamente en la solicitud.  
> - Asegúrese de que la versión de la API (`v3.0`) coincida con la versión más reciente publicada.

### Especificación de la API GetWorkBook

La <a href="https://apireference.aspose.cloud/cells/#/Workbook/GetWorkBook" rel="noopener noreferrer">Especificación OpenAPI</a> define una interfaz de programación accesible públicamente y le permite realizar interacciones REST directamente desde un navegador web.

### Ejemplo de solicitud

Puede utilizar la herramienta de línea de comandos **cURL** para acceder a los servicios web de Aspose.Cells. El siguiente ejemplo muestra una solicitud GET correcta con el encabezado de autorización requerido.

{{< tabs tabTotal="1" tabID="11" tabName11="Solicitud" >}}

{{< tab tabNum="11" >}}

```bash
curl -X GET "https://api.aspose.cloud/v3.0/cells/book1.xlsx?format=pdf" \
     -H "Authorization: Bearer <access_token>" \
     -H "accept: multipart/form-data" \
     -H "Content-Type: multipart/form-data" \
     -H "x-aspose-client: Containerize.Swagger"
```

{{< /tab >}}

{{< /tabs >}}

### Utilizar los SDK de Aspose.Cells Cloud

Utilizar un SDK es la forma más rápida de desarrollar. Un SDK abstracta los detalles de bajo nivel para que pueda centrarse en las tareas de su proyecto. Consulte el <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">repositorio de GitHub</a> para ver la lista completa de SDK de Aspose.Cells Cloud.

Los siguientes ejemplos de código muestran cómo llamar a los servicios web de Aspose.Cells mediante diversos SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetWorkbook.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetWorkbook.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetWorkbook.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetWorkbook.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_GetWorkbook.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetWorkbook.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetWorkbook.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetWorkbook.go" >}}

{{< /tab >}}

{{< /tabs >}}

**Consulte también**

- <a href="https://apireference.aspose.cloud/cells/#/Workbook/ConvertWorkbook" rel="noopener noreferrer">Convertir libro de trabajo (POST)</a>  
- <a href="https://apireference.aspose.cloud/cells/#/Workbook/SaveAs" rel="noopener noreferrer">Guardar como (GET)</a>

---

_Ultima actualización: 2024-12-01_

<script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@type": "TechArticle",
  "headline": "Aspose.Cells Cloud: Convertir libro de Excel a PDF, CSV, HTML y más (GET /cells/{name})",
  "description": "Documentación para el punto de conexión GET /cells/{name} de Aspose.Cells Cloud, que convierte libros de Excel a diversos formatos como PDF, CSV, HTML y más.",
  "author": {
    "@type": "Organization",
    "name": "Aspose"
  },
  "datePublished": "2024-12-01",
  "keywords": "Aspose.Cells, conversión de Excel, PDF, CSV, HTML, API, REST, nube",
  "url": "https://docs.aspose.cloud/es/cells/get-different-formats-files/",
  "publisher": {
    "@type": "Organization",
    "name": "Aspose"
  }
}
</script>
---