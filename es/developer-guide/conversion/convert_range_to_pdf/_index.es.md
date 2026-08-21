---
title: "ConvertRangeToPdf"
ArticleTitle: "Convertir rango a PDF – Aspose.Cells Cloud API"
second_title: "Document"
linktitle: "ConvertRangeToPdf"
type: docs
url: /es/cells/convert/range/pdf
aliases: []
keywords: "Aspose.Cells, convertir rango a PDF, API"
description: "Convierte un rango especificado de una hoja de cálculo a PDF mediante Aspose.Cells Cloud."
weight: 1
---

## ConvertRangeToPdf de los servicios web de Aspose.Cells Cloud

Convierte un rango de una hoja de cálculo ubicada en una unidad local a un archivo PDF.

### Punto de conexión de la API web

```http
PUT https://api.aspose.cloud/v4.0/cells/convert/range/pdf
```

### **Seguridad y autenticación**

Las API de Aspose.Cells Cloud son seguras y requieren <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">autenticación basada en token JWT</a>.

### Parámetros de la solicitud

| Nombre del parámetro | Tipo   | Ruta / Cadena de consulta / Cuerpo HTTP | Descripción                                                                                                                                    |
|----------------------|--------|------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| Spreadsheet          | File   | FormData                                 | Cargar archivo de hoja de cálculo.                                                                                                             |
| worksheet            | String | Query                                    | Nombre de la hoja de cálculo.                                                                                                                  |
| range                | String | Query                                    | Área de celdas, por ejemplo, A1:C10                                                                                                            |
| outPath              | String | Query                                    | (Opcional) Ruta de la carpeta donde se almacena el libro de trabajo. El valor predeterminado es null.                                          |
| outStorageName       | String | Query                                    | Nombre del almacenamiento para el archivo de salida.                                                                                           |
| fontsLocation        | String | Query                                    | Utilizar fuentes personalizadas.                                                                                                               |
| AutoRowsFit          | Boolean| Query                                    | (Opcional) Ajusta automáticamente todas las filas en las hojas de cálculo.                                                                    |
| AutoColumnsFit       | Boolean| Query                                    | (Opcional) Ajusta automáticamente todas las columnas en las hojas de cálculo.                                                                 |
| region               | String | Query                                    | Configuración regional/idioma de la hoja de cálculo (por ejemplo, `es-ES`, `fr-FR`). Influye en el formato numérico, el análisis de fechas y el comportamiento específico de la configuración regional. |
| password             | String | Query                                    | Contraseña para abrir el archivo de hoja de cálculo.                                                                                           |

### Parámetro del cuerpo de la solicitud

| Nombre del parámetro | Tipo | Descripción                 |
|----------------------|------|-----------------------------|
| Spreadsheet          | File | Cargar archivo de hoja de cálculo. |

### **Respuesta**

```json
{
  "file": "<contenido binario PDF>"
}
```

**Códigos de estado de la respuesta**

| Código | Significado            | Descripción                                                                 |
|--------|------------------------|-----------------------------------------------------------------------------|
| 200    | OK (Correcto)          | Conversión correcta; devuelve el flujo del archivo PDF generado.           |
| 400    | Bad Request (Solicitud incorrecta) | URL inválida.                                                              |
| 401    | Unauthorized (No autorizado) | La autenticación falló o no se proporcionaron credenciales.               |
| 413    | Payload Too Large (Carga demasiado grande) | El archivo cargado supera el límite de tamaño permitido.              |
| 500    | Internal Server Error (Error interno del servidor) | La hoja de cálculo ha presentado una anomalía al obtener los datos de conversión. |

## Cómo usar ConvertRangeToPdf con SDK

### Especificación de ConvertRangeToPdf

La [Especificación de la API ConvertRangeToPdf](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Conversion/ConvertRangeToPdf) define una interfaz de programación pública accesible y permite realizar interacciones REST directamente desde un navegador web.

Puede utilizar la herramienta de línea de comandos cURL para acceder fácilmente a los servicios web de Aspose Cells Cloud. El siguiente ejemplo muestra cómo realizar llamadas a la API en la nube mediante cURL.

{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}

{< tab tabNum="1" >}

```bash
# Utilizar HTTPS para una conexión segura
curl -v "https://api.aspose.cloud/v4.0/cells/convert/range/pdf?worksheet=Sheet1&range=A1:C10" \
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

### Utilizar los SDK de Aspose Cells Cloud

Utilizar un SDK es la forma más rápida de acelerar el desarrollo. Un SDK abstracta los detalles de bajo nivel, permitiéndole centrarse en las tareas de su proyecto. Consulte el <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">repositorio de GitHub</a> para obtener una lista completa de los SDK de Aspose.Cells Cloud.

Los siguientes ejemplos de código muestran cómo llamar a los servicios web de Aspose Cells Cloud utilizando varios SDK:

```csharp
// Código de ejemplo del SDK para C#
var apiInstance = new ConversionApi();
var file = File.OpenRead("sample.xlsx");
var result = apiInstance.ConvertRangeToPdf(file, "Sheet1", "A1:C10", outPath: null, outStorageName: null, fontsLocation: null, autoRowsFit: null, autoColumnsFit: null, region: null, password: null);
File.WriteAllBytes("output.pdf", result);
```

```java
// Código de ejemplo del SDK para Java
ConversionApi api = new ConversionApi();
File file = new File("sample.xlsx");
byte[] result = api.convertRangeToPdf(file, "Sheet1", "A1:C10", null, null, null, null, null, null, null);
Files.write(Paths.get("output.pdf"), result);
```

```python
# Código de ejemplo del SDK para Python
api_instance = conversion_api.ConversionApi()
with open("sample.xlsx", "rb") as f:
    result = api_instance.convert_range_to_pdf(f, worksheet="Sheet1", range="A1:C10")
    with open("output.pdf", "wb") as out_file:
        out_file.write(result)
```

```javascript
// Código de ejemplo del SDK para JavaScript/Node.js
const fs = require('fs');
const { ConversionApi } = require('asposecellscloud');
const apiInstance = new ConversionApi();

let file = fs.createReadStream('sample.xlsx');
apiInstance.convertRangeToPdf(file, { worksheet: 'Sheet1', range: 'A1:C10' })
    .then((result) => {
        fs.writeFileSync('output.pdf', result);
    })
    .catch((error) => console.error(error));
```

`[TBD]`
---