---
title: "Exportar Tabla – API de Aspose.Cells Cloud | Convertir Excel a PDF, PNG, CSV"
second_title: "Documento"
ArticleTitle: "Cómo exportar una tabla de hoja de cálculo remota a otro formato: Guía paso a paso"
linktitle: "Exportar Tabla al Formato Especificado"
type: docs
url: /es/export-table-as-format/
keywords: "Aspose.Cells, Exportar Tabla, Excel a PDF, API en la nube, REST"
description: "Exporta una tabla de Excel almacenada en la nube a PDF, PNG, CSV, JSON u otros formatos mediante la API de Aspose.Cells Cloud. Punto final HTTPS seguro con autenticación JWT y ejemplos de SDK."
weight: 100
---

Exporta una tabla de hoja de cálculo (Excel) almacenada en la nube a un archivo en otro formato.

## **API de Exportar Tabla a Formato**

### API Web

```http
GET https://api.aspose.cloud/v4.0/cells/{name}/worksheets/{worksheet}/tables/{tableName}
```

### **Seguridad y Autenticación**

Las API de Aspose.Cells Cloud son seguras y requieren <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">autenticación basada en token JWT</a>.

```bash
-H "Authorization: Bearer {access_token}"
```

### **Parámetros de Solicitud:**

| Nombre del Parámetro | Tipo   | Ruta / Cadena de Consulta / Cuerpo HTTP | Descripción                                                                                                                                       |
| :------------------- | :----- | :-------------------------------------- | :------------------------------------------------------------------------------------------------------------------------------------------------ |
| name                 | String | Ruta                                    | **Obligatorio.** Nombre del archivo del libro que se va a recuperar.                                                                            |
| worksheet            | String | Ruta                                    | Nombre de la hoja de cálculo.                                                                                                                     |
| tableName            | String | Ruta                                    | Nombre de la tabla.                                                                                                                               |
| format               | String | Consulta                                | **Obligatorio.** Formato de salida deseado (por ejemplo, “png”, “pdf”, “svg”).                                                                   |
| folder               | String | Consulta                                | Opcional. Ruta de la carpeta donde se almacena el libro. Por defecto es `null`.                                                                  |
| storageName          | String | Consulta                                | Opcional. Nombre del almacenamiento si se utiliza un almacenamiento en la nube personalizado. Usa el almacenamiento predeterminado si se omite. |
| outPath              | String | Consulta                                | Opcional. Ruta de la carpeta para el almacenamiento de salida. Por defecto es `null`.                                                            |
| outStorageName       | String | Consulta                                | Opcional. Nombre del almacenamiento del archivo de salida.                                                                                       |
| fontsLocation        | String | Consulta                                | Opcional. Ubicación de fuentes personalizadas.                                                                                                   |
| region               | String | Consulta                                | Opcional. Configuración regional/idioma de la hoja de cálculo (por ejemplo, `es-ES`, `fr-FR`). Afecta el formato numérico, el análisis de fechas y el comportamiento específico de la configuración regional. |
| password             | String | Consulta                                | Opcional. Contraseña para abrir el archivo de la hoja de cálculo.                                                                                |

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

**Códigos de Estado HTTP**

| Código | Significado             | Descripción                                                       |
| ------ | ----------------------- | ----------------------------------------------------------------- |
| 200    | Correcto                | Filtro aplicado correctamente; la respuesta contiene detalles de la operación. |
| 400    | Solicitud Incorrecta    | Parámetros faltantes o inválidos (por ejemplo, tipo de archivo no admitido).    |
| 401    | No Autorizado           | Token JWT inválido o faltante.                                    |
| 413    | Payload Demasiado Grande| El archivo cargado excede el límite de tamaño.                   |
| 500    | Error Interno del Servidor | Error inesperado del servidor.                                   |

## **¿Dónde Debería Utilizar la API de Exportar Tabla a Otro Formato?**

- **Migración de Sistemas Heredados**: Convierte miles de archivos XLS heredados a XLSX para sistemas modernos.
- **Estandarización de Archivo**: Normaliza diversos formatos de hojas de cálculo (XLS, XLSM, ODS, CSV) a un único formato para archivo.
- **Interoperabilidad con Suites de Oficina**: Convierte archivos de Excel a formatos compatibles con LibreOffice, Google Sheets o Apple Numbers.
- **Normalización de Fuentes de Datos**: Convierte diversos formatos de hojas de cálculo a CSV o JSON para su ingestión en bases de datos.
- **Publicación Web**: Convierte modelos financieros a HTML para su visualización web.

## ¿Por Qué Debería Utilizar la API de Exportar Tabla a Otro Formato?

- **Amigable para Desarrolladores**: Aspose.Cells Cloud ofrece bibliotecas SDK en múltiples lenguajes, lo que permite un desarrollo rápido y viene acompañado de documentación completa. En comparación con la construcción de soluciones personalizadas de renderizado de gráficos, esto reduce significativamente la carga de trabajo de desarrollo.
- **Reducción de Costos de Mano de Obra**: Disminuye la necesidad de asignar personal exclusivamente a la consolidación de documentos.
- **Pago por Uso**: Sin inversión inicial; solo paga por las llamadas a la API que realmente utiliza.
- **Costos de Mantenimiento Cero**: No es necesario mantener servidores, actualizar software ni lidiar con problemas de compatibilidad.
- **La API devuelve únicamente los datos brutos de la tabla, sin ningún estilo del libro.**

## ¿Cómo Utilizar la API de Exportar Tabla de Hoja de Cálculo a Formato con SDK?

### Especificación de la API de Exportar Tabla a Formato

La <a href="https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Conversion/ExportTableAsFormat" target="_blank" rel="noopener noreferrer">Especificación de la API Exportar Tabla a Formato</a> define una interfaz de programación públicamente accesible y le permite realizar interacciones REST directamente desde un navegador web.

Puede utilizar la herramienta de línea de comandos cURL para acceder fácilmente a los servicios web de Aspose.Cells. El siguiente ejemplo muestra cómo realizar llamadas a la API en la nube con cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Solicitud" tabName12="Respuesta" >}}

{{< tab tabNum="11" >}}

```bash
curl -X GET "https://api.aspose.cloud/v4.0/cells/MyWorkbook.xlsx/worksheets/Sheet1/tables/Table1?format=pdf" \
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

### Utilizar los SDK de Aspose.Cells Cloud

Usar el SDK es la forma más rápida de desarrollar, ya que abstrae los detalles de bajo nivel, permitiéndole exportar una tabla de hoja de cálculo a un archivo en otro formato con un código breve. Consulte el <a href="https://github.com/aspose-cells-cloud" target="_blank" rel="noopener noreferrer">repositorio de GitHub</a> para ver una lista completa de los SDK de Aspose.Cells Cloud.

Los siguientes ejemplos de código muestran cómo realizar llamadas a los servicios web de Aspose.Cells utilizando diversos SDK:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_ExportTableAsFormat.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_ExportTableAsFormat.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_ExportTableAsFormat.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_ExportTableAsFormat.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_ExportTableAsFormat.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_ExportTableAsFormat.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_ExportTableAsFormat.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_ExportTableAsFormat.go" >}}
{{</tab>}}
{{< /tabs >}}

---