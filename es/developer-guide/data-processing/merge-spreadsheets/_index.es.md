---
title: "Fusionar varios archivos de Excel en una hoja de cálculo única – API de Aspose.Cells Cloud"
second_title: "Documentación"
ArticleTitle: "Combinar varios archivos de Excel en uno solo – Fusionar por lotes hojas de cálculo en más de 30 formatos"
linktype: "Fusionar hojas de cálculo"
type: docs
url: /merge-spreadsheets/
keywords: "Aspose.Cells, fusionar hojas de cálculo, API de Excel, hoja de cálculo en la nube, fusión por lotes, conversión a PDF, fusión CSV, fusión ODS, referencia de API, SDK"
description: "Combine varios archivos locales de Excel, CSV u ODS en un único libro y convierta el resultado en más de 30 formatos (PDF, HTML, etc.) mediante Aspose.Cells Cloud. Incluye el punto de conexión, parámetros, guía de autenticación y ejemplos de SDK."
weight: 100
---

Fusione varios archivos locales de Excel, CSV u ODS en un único libro y conviértalo en más de 30 formatos de salida con la API de Aspose.Cells Cloud.

### API web

```http
PUT https://api.aspose.cloud/v4.0/cells/merge/spreadsheet
```

### **Seguridad y autenticación**

Las API de Aspose.Cells Cloud son seguras y requieren <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">autenticación mediante token JWT</a>.

### **Parámetros de solicitud**

| Nombre del parámetro | Tipo    | Ubicación       | Descripción                                                                                      |
| --------------------- | ------- | --------------- | ------------------------------------------------------------------------------------------------ |
| Spreadsheet           | File    | FormData        | Archivo local de hoja de cálculo para cargar. Admite XLSX, XLS, CSV, ODS, etc.                 |
| outFormat             | String  | Query           | Formato de salida deseado (p. ej., `XLSX`, `PDF`, `CSV`, `HTML`). Admite más de 30 formatos.   |
| mergeInOneSheet       | Boolean | Query           | `true` → todos los datos fusionados en una única hoja de cálculo; `false` → cada hoja original se conserva. |
| outPath               | String  | Query (opcional)| Ruta de carpeta en la nube donde se guardará el archivo fusionado. Si se omite, se usa la ubicación predeterminada. |
| outStorageName        | String  | Query           | Nombre del almacenamiento en la nube que se usará (predeterminado o personalizado).            |
| fontsLocation         | String  | Query (opcional)| Carpeta en la nube que contiene fuentes personalizadas para una correcta generación de PDF o imágenes. |
| region                | String  | Query (opcional)| Configuración regional para el formato de números, fechas y monedas (p. ej., `es-ES`, `zh-CN`).  |
| password              | String  | Query (opcional)| Contraseña para abrir una hoja de cálculo protegida.                                           |

### **Respuesta**

```json
{
  "Name": "ResponseFile",
  "DataType": {
    "Identifier": "File",
    "Reference": "Stream"
  }
}
```

El archivo se puede descargar directamente o guardarse en la ubicación especificada por `outPath`.

**Detalles de la respuesta correcta**

| Código de estado | Tipo de contenido          | Descripción                              |
| ---------------- | -------------------------- | ---------------------------------------- |
| 200 OK           | `application/octet-stream` | Secuencia binaria del archivo del libro fusionado. |

**Códigos de estado HTTP**

| Código | Significado              | Descripción                                                       |
| ------ | ------------------------ | ----------------------------------------------------------------- |
| 200    | OK                       | Filtro aplicado correctamente; la respuesta contiene los detalles de la operación. |
| 400    | Solicitud incorrecta     | Parámetros ausentes o no válidos (p. ej., tipo de archivo no admitido). |
| 401    | No autorizado            | Token JWT inválido o ausente.                                     |
| 413    | Carga demasiado grande    | El archivo cargado supera el límite de tamaño.                   |
| 500    | Error interno del servidor | Error inesperado en el servidor.                                  |

## ¿Dónde se debe utilizar la API de fusión de hojas de cálculo?

### **Educación y aplicaciones académicas**

- **Calificación de tareas estudiantiles** – Fusionar varios archivos de tareas estudiantiles para comentar y calificar de forma unificada.
- **Recopilación de datos de investigación** – Consolidar hojas de cálculo de datos procedentes de distintos grupos experimentales.
- **Creación de materiales docentes** – Combinar ejercicios de varios capítulos en un único libro de banco de preguntas.

### **Procesamiento y análisis de datos**

- **Integración de conjuntos de datos pequeños** – Fusionar archivos CSV o Excel exportados desde fuentes distintas.
- **Preprocesamiento para análisis de datos** – Combinar archivos de datos relevantes antes de realizar el análisis.
- **Relleno de plantillas de datos** – Rellenar plantillas de informes predefinidas con datos fusionados.

### **Desarrollo y soporte técnico**

- **Preparación de datos de prueba** – Fusionar varios archivos de casos de prueba para pruebas automatizadas.
- **Análisis de archivos de registro** – Consolidar informes de registro del sistema en Excel procedentes de distintos periodos.
- **Gestión de configuraciones** – Fusionar varias hojas de configuración en un único archivo unificado.

## ¿Por qué debería utilizar la API de fusión de hojas de cálculo?

- **Fácil de usar para desarrolladores** – SDK disponibles para múltiples lenguajes, lo que reduce el esfuerzo de desarrollo frente a una solución personalizada.
- **Reducción de costes de mano de obra** – Elimina la necesidad de personal dedicado para consolidar documentos manualmente.
- **Pago por uso** – Solo pague por las llamadas a la API que realmente realice; sin inversión inicial.
- **Cero costes de mantenimiento** – No hay servidores que mantener, ni actualizaciones de software ni preocupaciones por compatibilidad.

## Cómo utilizar la API de fusión de hojas de cálculo con SDK

### Especificación OpenAPI

La <a href="https://reference.aspose.cloud/cells/#/DataProcessingController/MergeSpreadsheets" rel="noopener noreferrer">especificación OpenAPI</a> proporciona una descripción legible por máquinas de la API, lo que permite interacciones REST directas.

Puede utilizar la herramienta de línea de comandos cURL para acceder fácilmente a los servicios web de Aspose.Cells. El siguiente ejemplo muestra cómo realizar llamadas a la API en la nube mediante cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Solicitud" tabName12="Respuesta" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/merge/spreadsheet?outFormat=PDF&mergeInOneSheet=true" \
  -H "Authorization: Bearer {access_token}" \
  -F "Spreadsheet=@/ruta/a/Book1.xlsx" \
  -F "Spreadsheet=@/ruta/a/Book2.xlsx"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```
{
  "type": "FileContentResult",
  "fileContents": "byte[] (codificado en Base64)",
  "contentType": "tipo MIME",
  "fileDownloadName": "nombre de archivo opcional"
}
```

{{< /tab >}}

{{< /tabs >}}

### Utilizar los SDK de Aspose.Cells Cloud

Utilizar los SDK es la forma más rápida de desarrollar, ya que ocultan los detalles de bajo nivel y permite importar datos en una hoja de cálculo con un código breve. Consulte el <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">repositorio de GitHub</a> para obtener una lista completa de los SDK de Aspose.Cells Cloud.

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_MergeSpreadsheets.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_MergeSpreadsheets.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_MergeSpreadsheets.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_MergeSpreadsheets.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_MergeSpreadsheets.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_MergeSpreadsheets.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_MergeSpreadsheets.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_MergeSpreadsheets.go" >}}
{{</tab>}}
{{< /tabs >}}

---