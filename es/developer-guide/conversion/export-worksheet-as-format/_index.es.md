---
title: "Exportar hoja de cálculo – API de Aspose.Cells Cloud v4 (PDF, PNG, SVG, CSV)"
second_title: "Document"
ArticleTitle: "Cómo exportar una hoja de cálculo remota a otro formato: guía paso a paso"
linktype: "docs"
url: /es/export-worksheet-as-format/
keywords: "Aspose Cells, exportar hoja de cálculo, API en la nube, PDF, PNG, CSV, conversión de Excel"
description: "Convierta una hoja de cálculo almacenada en Aspose.Cells Cloud a PDF, PNG, SVG, CSV u otros formatos mediante una única solicitud GET. Incluye ejemplos de código para C#, Java, Python y más."
weight: 100
---

Exporte una hoja de cálculo/Excel en la nube a otro formato de archivo mediante la API web de Aspose.Cells Cloud.

## **API para exportar hoja de cálculo a otro formato**

### API web

```http
GET https://api.aspose.cloud/v4.0/cells/{name}/worksheets/{worksheet}
```

### **Seguridad y autenticación**

Las API de Aspose.Cells Cloud son seguras y requieren <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">autenticación basada en token JWT</a>.

```bash
-H "Authorization: Bearer {access_token}"
```

### **Parámetros de solicitud**

| Nombre del parámetro | Tipo   | Ruta / Cadena de consulta / Cuerpo HTTP | Descripción                                                                                                                                          |
| :------------------- | :----- | :-------------------------------------- | :--------------------------------------------------------------------------------------------------------------------------------------------------- |
| **name**             | String | Ruta                                    | (Obligatorio) Nombre del archivo de libro que se va a recuperar.                                                                                     |
| **worksheet**        | String | Ruta                                    | (Obligatorio) Hoja de cálculo específica que se va a convertir.                                                                                      |
| **format**           | String | Consulta                                | (Obligatorio) Formato de salida deseado (por ejemplo, `png`, `pdf`, `svg`).                                                                          |
| **folder**           | String | Consulta                                | (Opcional) Ruta de la carpeta donde se almacena el libro. El valor predeterminado es `null`.                                                        |
| **storageName**      | String | Consulta                                | (Opcional) Nombre del almacenamiento en la nube personalizado. Se utiliza el almacenamiento predeterminado si se omite.                             |
| **outPath**          | String | Consulta                                | (Opcional) Ruta de la carpeta de salida. El valor predeterminado es `null`.                                                                          |
| **outStorageName**   | String | Consulta                                | (Opcional) Nombre del almacenamiento para el archivo de salida.                                                                                      |
| **fontsLocation**    | String | Consulta                                | (Opcional) Especifique fuentes personalizadas si es necesario.                                                                                       |
| **region**           | String | Consulta                                | (Opcional) Configuración regional/idioma de la hoja de cálculo (por ejemplo, `es-ES`, `fr-FR`). Afecta el formato numérico, el análisis de fechas y el comportamiento específico de la configuración regional. |
| **password**         | String | Consulta                                | (Opcional) Contraseña para acceder al archivo de hoja de cálculo.                                                                                    |

### **Respuesta**

```json
[
  {
    "Name": "ResponseFile",
    "DataType": {
      "Identifier": "File",
      "Reference": "Stream"
    }
  }
]
```

**Códigos de estado HTTP**

| Código | Significado             | Descripción                                                      |
| ------ | ----------------------- | ---------------------------------------------------------------- |
| 200    | OK                      | Filtro aplicado correctamente; la respuesta contiene detalles de la operación. |
| 400    | Solicitud incorrecta    | Parámetros faltantes o no válidos (por ejemplo, tipo de archivo no admitido).   |
| 401    | No autorizado           | Token JWT inválido o faltante.                                   |
| 413    | Carga útil demasiado grande | El archivo subido supera el límite de tamaño.                     |
| 500    | Error interno del servidor | Error inesperado en el servidor.                                  |

## **¿Dónde debería usar la API para exportar una hoja de cálculo a otro formato?**

- **Migración de sistemas heredados** – Convierta miles de archivos XLS heredados a XLSX para sistemas modernos.
- **Estandarización de archivos para archivar** – Normalice diversos formatos de hojas de cálculo (XLS, XLSM, ODS, CSV) a un único formato para archivar.
- **Interoperabilidad con suites ofimáticas** – Convierta archivos de Excel a formatos compatibles con LibreOffice, Google Sheets o Apple Numbers.
- **Normalización de fuentes de datos** – Convierta diversos formatos de hojas de cálculo a CSV o JSON para su ingestión en bases de datos.
- **Publicación web** – Convierta modelos financieros a HTML para su visualización en la web.

## ¿Por qué usar la API para exportar una hoja de cálculo a otro formato?

- **Soporte de SDK multilenguaje** – Proporciona bibliotecas cliente para varios lenguajes de programación, lo que permite a los desarrolladores invocar la API directamente desde su entorno preferido.
- **Conversión directa sin carga intermedia** – Permite convertir una hoja de cálculo almacenada en almacenamiento en la nube al formato solicitado sin necesidad de descargar y volver a subir el archivo.
- **Extracción de solo datos** – Devuelve el contenido de la hoja de cálculo en el formato seleccionado sin conservar el estilo visual.

## ¿Cómo usar la API para exportar una hoja de cálculo a otro formato con SDK?

### Especificación de la API para exportar hoja de cálculo a otro formato

La [especificación de la API para exportar hoja de cálculo a otro formato](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Conversion/ExportWorksheetAsFormat) proporciona una interfaz de programación pública accesible para realizar interacciones REST directamente desde un navegador web.

Puede utilizar la herramienta de línea de comandos cURL para acceder fácilmente a los servicios web de Aspose.Cells. El siguiente ejemplo muestra cómo realizar llamadas a la API en la nube con cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Solicitud" tabName12="Respuesta" >}}

{{< tab tabNum="11" >}}

```bash
curl -X GET "https://api.aspose.cloud/v4.0/cells/MyWorkbook.xlsx/worksheets/Sheet1?format=pdf" \
     -H "Authorization: Bearer {access_token}" \
     -H "Accept: application/octet-stream"
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

### Uso de los SDK de Aspose.Cells Cloud

Utilizar el SDK es la forma más rápida de desarrollar, ya que oculta los detalles de bajo nivel, permitiéndole exportar una hoja de cálculo a un archivo en otro formato con un código breve.  
Consulte el [repositorio de GitHub](https://github.com/aspose-cells-cloud) para obtener una lista completa de los SDK de Aspose.Cells Cloud.

Los siguientes ejemplos de código muestran cómo realizar llamadas a los servicios web de Aspose.Cells utilizando diversos SDK:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_ExportWorksheetAsFormat.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_ExportWorksheetAsFormat.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_ExportWorksheetAsFormat.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_ExportWorksheetAsFormat.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_ExportWorksheetAsFormat.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_ExportWorksheetAsFormat.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_ExportWorksheetAsFormat.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_ExportWorksheetAsFormat.go" >}}
{{</tab>}}
{{< /tabs >}}