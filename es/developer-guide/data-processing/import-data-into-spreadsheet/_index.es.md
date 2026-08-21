---
title: "API de importación de datos de Aspose.Cells Cloud: una solución en la nube para importar automáticamente datos CSV, JSON y XML en hojas de cálculo de Excel."
second_title: "Documento"
ArticleTitle: "Plataforma de integración de datos de múltiples fuentes para Excel – API de importación y transformación automática de datos de Aspose.Cells Cloud."
linktitle: "Importar datos en hoja de cálculo"
type: docs
url: /es/import-data-into-spreadsheet/
keywords: "Aspose Cells, API de importación de datos, CSV a Excel, JSON a Excel, XML a Excel, hoja de cálculo en la nube, API REST"
description: "Importe datos CSV, JSON o XML en hojas de cálculo de Excel mediante la API REST de Aspose.Cells Cloud. Aprenda sobre el formato de solicitud, parámetros, código de ejemplo con SDK y manejo de errores."
weight: 100
---

## Características principales

### Soporte para datos en múltiples formatos

- **<a href="https://docs.fileformat.com/spreadsheet/csv/" rel="noopener noreferrer">Importación de datos CSV</a>**: admite diversos delimitadores y detecta automáticamente la codificación.
- **<a href="https://docs.fileformat.com/web/json/" rel="noopener noreferrer">Gestión de datos JSON</a>**: aplanar estructuras JSON complejas en tablas de Excel.
- **<a href="https://docs.fileformat.com/web/xml/" rel="noopener noreferrer">Conversión de archivos XML</a>**: asigna datos de nodos a la estructura de filas y columnas de Excel.

## Descripción de la API de importación de datos en hoja de cálculo

### API web

```http
PUT https://api.aspose.cloud/v4.0/cells/import/data
```

### **Seguridad y autenticación**

Las API de Aspose.Cells Cloud son seguras y requieren <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">autenticación basada en token JWT</a>.

### Parámetros de solicitud

| Nombre del parámetro | Tipo   | Ubicación         | Descripción                                                                 |
| -------------------- | ------ | ----------------- | --------------------------------------------------------------------------- |
| datafile             | File   | FormData          | El archivo de datos (CSV, JSON o XML) que se va a importar.                |
| spreadsheet          | File   | FormData          | El libro de trabajo de destino que recibirá los datos importados.          |
| worksheet            | string | Query             | Nombre de la hoja de cálculo donde se colocarán los datos.                 |
| startCell            | string | Query             | Celda superior izquierda (por ejemplo, `A1`) que marca la posición inicial para la importación. |
| insert               | bool   | Query             | `true` para insertar filas; `false` para sobrescribir los datos existentes. |
| convertNumericData   | bool   | Query             | `true` para convertir cadenas numéricas en números durante la importación. |
| splitter             | string | Query             | Delimitador CSV de un solo carácter (el valor predeterminado es `,`).      |
| outPath              | string | Query (opcional)  | Ruta de carpeta donde se guardará el libro de trabajo actualizado.        |
| outStorageName       | string | Query (opcional)  | Nombre de la ubicación de almacenamiento para el archivo de salida.       |
| fontsLocation        | string | Query (opcional)  | Ruta a una carpeta personalizada de fuentes, si es necesario.              |
| region               | string | Query (opcional)  | Configuración regional de la hoja de cálculo (por ejemplo, `es-ES`).       |
| password             | string | Query (opcional)  | Contraseña para abrir un libro de trabajo protegido.                       |

### Respuesta

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

| Código | Significado             | Descripción                                                     |
| ------ | ----------------------- | --------------------------------------------------------------- |
| 200    | Correcto                | Filtro aplicado correctamente; la respuesta contiene detalles de la operación. |
| 400    | Solicitud incorrecta    | Parámetros ausentes o no válidos (por ejemplo, tipo de archivo no admitido). |
| 401    | No autorizado           | Token JWT no válido o ausente.                                  |
| 413    | Carga útil demasiado grande | El archivo cargado excede el límite de tamaño.              |
| 500    | Error interno del servidor | Error inesperado del servidor.                                |

## Por qué debería utilizar esta API

- **Carga eficiente de datos**: permite importar grandes conjuntos de datos directamente en un libro de trabajo sin crear archivos intermedios.
- **Amplia compatibilidad con SDK**: proporciona bibliotecas cliente para .NET, Java, PHP, Ruby, Node.js, Python, Go y Perl, facilitando la integración.
- **Procesamiento en memoria**: realiza transformaciones en memoria, lo que reduce los requisitos de almacenamiento temporal.

## Cómo usar la API de importación de datos en hoja de cálculo con SDK

**Notas / limitaciones**: la API admite hasta 1 000 000 de filas por importación. El delimitador CSV predeterminado es únicamente la coma; se pueden especificar otros delimitadores de un solo carácter mediante el parámetro `splitter`. Los archivos XML grandes pueden aumentar el tiempo de procesamiento.

Para operaciones relacionadas, como exportar datos o convertir formatos de libro de trabajo, consulte la documentación sobre **Exportar datos** y **Convertir libro de trabajo**.

### Especificación de la API de importación de datos en hoja de cálculo

La <a href="https://reference.aspose.cloud/cells/#/DataProcessingController/ImportDataIntoSpreadsheet" rel="noopener noreferrer">Especificación de la API de importación de datos en hoja de cálculo</a> proporciona una interfaz de programación accesible públicamente, lo que permite interacciones REST directamente desde su navegador web.
Puede utilizar la herramienta de línea de comandos cURL para acceder fácilmente a los servicios web de Aspose.Cells. El siguiente ejemplo muestra cómo realizar llamadas a la API en la nube con cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Solicitud" tabName12="Respuesta" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/import/data?worksheet=Sheet1&startCell=A1&insert=true" \
  -H "Authorization: Bearer {access_token}" \
  -F "datafile=@/path/to/data.csv" \
  -F "spreadsheet=@/path/to/workbook.xlsx"
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

### Utilizar SDK de Aspose.Cells Cloud

Utilizar el SDK es la forma más rápida de desarrollar, ya que abstracta los detalles de bajo nivel, permitiéndole importar datos en una hoja de cálculo con un código breve. Consulte el <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">repositorio de GitHub</a> para obtener una lista completa de SDK de Aspose.Cells Cloud.