---
title: "Convertir Tabla a PDF"
ArticleTitle: "Convertir Tabla a PDF – Aspose.Cells Cloud API"
second_title: "Documento"
linktitle: "Convertir Tabla a PDF"
type: docs
url: /cells/convert/table/pdf
aliases: []
keywords: "Convertir Tabla a PDF, Aspose.Cells, API"
description: "Convierte una tabla de una hoja de cálculo ubicada en un disco local en un archivo PDF utilizando Aspose.Cells Cloud."
weight: 1000
---

## La conversión de Tabla a PDF de los Servicios Web de Aspose.Cells Cloud

Esta operación lee un archivo de hoja de cálculo desde el sistema de archivos local, convierte la tabla especificada en un documento PDF y devuelve el resultado convertido. Todo el proceso se realiza completamente en el servidor en la nube, por lo que no es necesario cargar previamente el archivo al almacenamiento en la nube. La API admite parámetros opcionales para la ubicación de salida, fuentes personalizadas, ajuste automático de filas/columnas, configuraciones regionales y libros protegidos con contraseña.

### Punto de acceso de la API web

```http
PUT https://api.aspose.cloud/v4.0/cells/convert/table/pdf
```

### **Seguridad y autenticación**

Las API de Aspose.Cells Cloud son seguras y requieren <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">autenticación basada en token JWT</a>.

### Parámetros de la solicitud

| Nombre del parámetro | Tipo | Ruta/Cadena de consulta/Cuerpo HTTP | Descripción |
|----------------------|------|-------------------------------------|-------------|
| Spreadsheet | Archivo | FormData | Archivo de hoja de cálculo a cargar. |
| worksheet | Cadena | Consulta | Nombre de la hoja de cálculo. |
| tableName | Cadena | Consulta | Nombre de la tabla. |
| outPath | Cadena | Consulta | (Opcional) Ruta de la carpeta donde se almacenará el libro. Por defecto es null. |
| outStorageName | Cadena | Consulta | Nombre del almacenamiento para el archivo de salida. |
| fontsLocation | Cadena | Consulta | Utilizar fuentes personalizadas. |
| AutoRowsFit | Booleano | Consulta | (Opcional) Ajustar automáticamente todas las filas en las hojas de cálculo. |
| AutoColumnsFit | Booleano | Consulta | (Opcional) Ajustar automáticamente todas las columnas en las hojas de cálculo. |
| region | Cadena | Consulta | Configuración regional/idioma de la hoja de cálculo (por ejemplo, `es-ES`, `fr-FR`). Afecta el formato de números, el análisis de fechas y el comportamiento específico de la configuración regional. |
| password | Cadena | Consulta | Contraseña para abrir el archivo de hoja de cálculo. |

### Parámetro del cuerpo de solicitud

| Nombre del parámetro | Tipo | Descripción |
|----------------------|------|-------------|
| *Ninguno* | *Ninguno* | *No se requiere cuerpo JSON; el archivo se envía mediante multipart/form-data.* |

### **Respuesta**

```json
{
  "file": "<contenido binario PDF>"
}
```

**Códigos de estado de respuesta**

| Código | Significado | Descripción |
|--------|-------------|-------------|
| 200 | Correcto | La tabla se convirtió correctamente a PDF; el cuerpo de la respuesta contiene el flujo del archivo PDF. |
| 400 | Solicitud incorrecta | Parámetros de solicitud inválidos o URL mal formada. |
| 401 | No autorizado | La autenticación falló o no se proporcionaron credenciales. |
| 404 | No encontrado | El archivo de origen no es accesible o no se encontró la hoja de cálculo o la tabla. |
| 413 | Payload demasiado grande | La hoja de cálculo cargada excede el límite de tamaño permitido. |
| 500 | Error interno del servidor | Se produjo un error durante la conversión de la hoja de cálculo a PDF. |

## Cómo usar la conversión de Tabla a PDF con SDK

### Especificación de conversión de Tabla a PDF

La [Especificación de la API de Conversión de Tabla a PDF](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Conversion/ConvertTableToPdf) define una interfaz de programación accesible públicamente y permite realizar interacciones REST directamente desde un navegador web.

Puede utilizar la herramienta de línea de comandos cURL para acceder fácilmente a los servicios web de Aspose.Cells Cloud. El siguiente ejemplo muestra cómo realizar llamadas a la API en la nube con cURL.

{< tabs tabTotal="2" tabID="1" tabName1="Solicitud" tabName2="Respuesta" >}

{< tab tabNum="1" >}

```bash
# Utilizar HTTPS para una conexión segura
curl -v "https://api.aspose.cloud/v4.0/cells/convert/table/pdf?worksheet={worksheet}&tableName={tableName}&outPath={outPath}&outStorageName={outStorageName}&fontsLocation={fontsLocation}&AutoRowsFit={AutoRowsFit}&AutoColumnsFit={AutoColumnsFit}&region={region}&password={password}" \
  -X PUT \
  -H "Content-Type: multipart/form-data" \
  -H "Accept: application/pdf" \
  -H "Authorization: Bearer <jwt token>" \
  -F "Spreadsheet=@sample.xlsx"
```

{< /tab >}

{< tab tabNum="2" >}

```json
{
  "file": "<contenido binario PDF>"
}
```

{< /tab >}

{< /tabs >}

### Utilizar SDK de Aspose Cells Cloud

Utilizar un SDK es la forma más rápida de acelerar el desarrollo. Un SDK abstracta los detalles de bajo nivel, permitiéndole centrarse en las tareas de su proyecto. Consulte el <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">repositorio de GitHub</a> para obtener una lista completa de los SDK de Aspose.Cells Cloud.

Los siguientes ejemplos de código demuestran cómo llamar a los servicios web de Aspose.Cells Cloud utilizando diversos SDK:

```csharp
// Código de ejemplo del SDK para C#
var apiInstance = new ConversionApi();
var file = File.ReadAllBytes("sample.xlsx");
var response = apiInstance.ConvertTableToPdf(
    file,
    worksheet: "Sheet1",
    tableName: "Table1",
    outPath: null,
    outStorageName: null,
    fontsLocation: null,
    AutoRowsFit: null,
    AutoColumnsFit: null,
    region: null,
    password: null);
File.WriteAllBytes("output.pdf", response);
```

```java
// Código de ejemplo del SDK para Java
ConversionApi apiInstance = new ConversionApi();
byte[] file = Files.readAllBytes(Paths.get("sample.xlsx"));
byte[] result = apiInstance.convertTableToPdf(
    file,
    "Sheet1",
    "Table1",
    null,
    null,
    null,
    null,
    null,
    null,
    null);
Files.write(Paths.get("output.pdf"), result);
```

```python
# Código de ejemplo del SDK para Python
api_instance = conversion_api.ConversionApi()
with open("sample.xlsx", "rb") as f:
    file_bytes = f.read()
pdf_bytes = api_instance.convert_table_to_pdf(
    file=file_bytes,
    worksheet="Sheet1",
    table_name="Table1")
with open("output.pdf", "wb") as out_file:
    out_file.write(pdf_bytes)
```

`[TBD]`
---