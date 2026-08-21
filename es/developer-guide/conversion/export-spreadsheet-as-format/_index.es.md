---
title: "Aspose.Cells Cloud Web API: Exportar hoja de cálculo en la nube a otros formatos - Herramienta gratuita en línea"
second_title: "Documentos"
ArticleTitle: "Cómo exportar la hoja de cálculo en la nube a otros formatos: Guía paso a paso"
linktitle: "Exportar hoja de cálculo como formato"
type: docs
url: /es/export-spreadsheet-as-format/
keywords: "Aspose.Cells, conversión de hojas de cálculo, API, exportar, PDF, CSV, JSON, XLSX"
description: "Convierta libros de Excel almacenados en Aspose Cloud a PDF, XLSX, CSV, JSON o HTML mediante un único punto final REST. Aprenda la sintaxis de la solicitud, los parámetros y vea ejemplos de SDK en C#, Java, Python y más."
weight: 100
---

Exporte una hoja de cálculo en la nube (Excel) a otro formato de archivo.

## **API para exportar hoja de cálculo como formato**

### API web

```http
GET https://api.aspose.cloud/v4.0/cells/{name}?format={format}&folder={folder}&storageName={storageName}&outPath={outPath}&outStorageName={outStorageName}&fontsLocation={fontsLocation}&region={region}&password={password}
```

### **Seguridad y autenticación**

Las API de Aspose.Cells Cloud son seguras y requieren <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">autenticación basada en token JWT</a>.

### **Parámetros de solicitud:**

| Nombre del parámetro | Tipo   | Ruta / Cadena de consulta / Cuerpo HTTP | Descripción                                                                                                                                        |
| :------------------- | :----- | :-------------------------------------- | :------------------------------------------------------------------------------------------------------------------------------------------------- |
| name                 | String | Ruta                                    | (Obligatorio) Nombre del archivo del libro que se va a recuperar.                                                                                   |
| format               | String | Cadena de consulta                        | (Obligatorio) Formato de salida deseado (por ejemplo, “Xlsx”, “PDF”, “CSV”).                                                                       |
| folder               | String | Cadena de consulta                        | (Opcional) Ruta de la carpeta donde se almacena el libro. El valor predeterminado es null.                                                         |
| storageName          | String | Cadena de consulta                        | (Opcional) Nombre del almacenamiento si se utiliza un almacenamiento en la nube personalizado. Se utiliza el almacenamiento predeterminado si se omite. |
| outPath              | String | Cadena de consulta                        | (Opcional) Ruta de la carpeta donde se guardará el libro. El valor predeterminado es null.                                                         |
| outStorageName       | String | Cadena de consulta                        | (Opcional) Nombre del almacenamiento del archivo de salida.                                                                                        |
| fontsLocation        | String | Cadena de consulta                        | (Opcional) Ubicación personalizada de las fuentes.                                                                                                 |
| region               | String | Cadena de consulta                        | (Opcional) Configuración regional/idioma de la hoja de cálculo (por ejemplo, `es-ES`, `fr-FR`). Afecta el formato de números, el análisis de fechas y el comportamiento específico de la configuración regional. |
| password             | String | Cadena de consulta                        | (Opcional) Contraseña para abrir el archivo de hoja de cálculo.                                                                                    |

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

La respuesta contiene un único objeto que representa el flujo del archivo convertido.

**Códigos de estado HTTP**

| Código | Significado                | Descripción                                                     |
| ------ | -------------------------- | --------------------------------------------------------------- |
| 200    | Correcto                   | Filtro aplicado correctamente; la respuesta contiene detalles de la operación. |
| 400    | Solicitud incorrecta       | Parámetros faltantes o no válidos (por ejemplo, tipo de archivo no admitido). |
| 401    | No autorizado              | Token JWT inválido o faltante.                                   |
| 413    | Carga demasiado grande      | El archivo cargado excede el límite de tamaño.                  |
| 500    | Error interno del servidor | Error inesperado en el servidor.                                |

## ¿Dónde debería utilizarse la API para exportar hoja de cálculo como otro formato?

- **Migración de sistemas heredados**: Convertir miles de archivos XLS heredados a XLSX para sistemas modernos.
- **Estandarización de archivos**: Normalizar diversos formatos de hojas de cálculo (XLS, XLSM, ODS, CSV) a un único formato para archivado.
- **Interoperabilidad con suites ofimáticas**: Convertir archivos de Excel a formatos compatibles con LibreOffice, Google Sheets o Apple Numbers.
- **Normalización de fuentes de datos**: Convertir diversos formatos de hojas de cálculo a CSV o JSON para su ingesta en bases de datos.
- **Publicación web**: Convertir modelos financieros a HTML para su visualización en la web.

## ¿Por qué debería utilizar la API para exportar hoja de cálculo como otro formato?

- **Amigable para desarrolladores**: Aspose.Cells Cloud ofrece bibliotecas SDK en múltiples lenguajes, lo que permite un desarrollo rápido y cuenta con una documentación completa. Comparado con la creación de soluciones personalizadas para renderizado de gráficos, esto reduce significativamente la carga de desarrollo.
- **Reducción de costos laborales**: Reduce la necesidad de asignar personal específicamente a la consolidación de documentos.
- **Pago por uso**: Sin inversión inicial; solo paga por las llamadas a la API que realmente se utilicen.
- **Sin necesidad de mantenimiento del lado del servidor**: No es necesario mantener servidores, actualizar software ni lidiar con problemas de compatibilidad.
- **Soporte integral de formatos**: Convierta entre más de 20 formatos de hojas de cálculo.
- **Preservación de la fidelidad y el formato de los datos**: Mantiene el diseño original, las fórmulas y el estilo durante la conversión.

## ¿Cómo utilizar la API para exportar hoja de cálculo como formato con SDK?

### Especificación de la API para exportar hoja de cálculo como formato

La <a href="https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Conversion/ExportSpreadsheetAsFormat" rel="noopener noreferrer">Especificación de la API para exportar hoja de cálculo como formato</a> proporciona una interfaz de programación accesible públicamente para realizar interacciones REST sin problemas.

Puede utilizar la herramienta de línea de comandos cURL para acceder fácilmente a los servicios web de Aspose.Cells. El siguiente ejemplo muestra cómo realizar llamadas a la API en la nube con cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Solicitud" tabName12="Respuesta" >}}

{{< tab tabNum="11" >}}

```bash
curl -X GET "https://api.aspose.cloud/v4.0/cells/MyWorkbook.xlsx/worksheets?format=pdf" \
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

Utilizar un SDK es la forma más rápida de desarrollar, ya que abstracta los detalles de bajo nivel, permitiéndole exportar una hoja de cálculo a un archivo de formato con un código breve.  
Antes de llamar a la API, obtenga un token de acceso OAuth 2.0 e inclúyalo en el encabezado `Authorization: Bearer <token>`.

Consulte el <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">repositorio de GitHub</a> para obtener una lista completa de los SDK de Aspose.Cells Cloud.

Los siguientes ejemplos de código ilustran cómo interactuar con los servicios web de Aspose.Cells mediante varios SDK:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_ExportSpreadsheetAsFormat.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_ExportSpreadsheetAsFormat.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_ExportSpreadsheetAsFormat.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_ExportSpreadsheetAsFormat.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_ExportSpreadsheetAsFormat.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_ExportSpreadsheetAsFormat.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_ExportSpreadsheetAsFormat.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_ExportSpreadsheetAsFormat.go" >}}
{{</tab>}}
{{< /tabs >}}