---
title: "Aspose.Cells Cloud – Unir, dividir e importar datos de hojas de cálculo"
second_title: "Documento"
ArticleTitle: "Procesamiento de datos de hojas de cálculo – Unir, dividir e importar"
linktitle: "Procesamiento de datos"
type: docs
url: /es/data-processing/
keywords: "Aspose.Cells Cloud, procesamiento de datos de hojas de cálculo, unir Excel, dividir Excel, importar CSV, importar JSON, API"
description: "Guía detallada para importar datos CSV/JSON, unir libros de Excel remotos y dividir hojas de cálculo grandes utilizando la API REST de Aspose.Cells Cloud, incluyendo ejemplos de solicitudes y respuestas."
weight: 30
---

**Aspose.Cells Cloud** – un servicio basado en REST que permite manipular archivos de Excel programáticamente en la nube. Admite la importación de datos desde diversos formatos, la unión de libros y la división de hojas de cálculo grandes.

La sección **Procesamiento de datos** de la API de Aspose.Cells Cloud le permite importar, unir y dividir datos de hojas de cálculo programáticamente. Utilice los puntos de conexión que se indican a continuación para manejar importaciones de CSV/JSON, combinar libros o dividir archivos grandes en piezas manejables.

## Importación y gestión de datos

- **[Importar datos CSV, JSON y XML a archivos de Excel](https://docs.aspose.cloud/cells/import-data-into-spreadsheet/)**  

La operación de importación acepta cargas útiles en formato CSV, JSON o XML y crea una nueva hoja de cálculo (o actualiza una existente) en el libro de destino.

**Detalles del punto de conexión**

| Método HTTP | Punto de conexión | Cuerpo de la solicitud | Respuesta correcta |
|-------------|-------------------|------------------------|--------------------|
| POST | `https://api.aspose.cloud/v3.0/cells/{fileName}/import` | `application/json` o `text/csv` (según el formato) | `200 OK` con JSON que contiene los metadatos del libro actualizado |
| GET | `https://api.aspose.cloud/v3.0/cells/{fileName}?format=excel` | *ninguno* | Devuelve el archivo de libro procesado |

**Ejemplo de solicitud cURL (importación CSV)**

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/MyWorkbook.xlsx/import" \
     -H "Authorization: Bearer {access_token}" \
     -H "Content-Type: text/csv" \
     --data-binary @data.csv
```

**Ejemplo de respuesta JSON**

```json
{
  "Code": 200,
  "Status": "OK",
  "Workbook": {
    "FileName": "MyWorkbook.xlsx",
    "Worksheets": 3
  }
}
```

> **Requisitos previos**: Se requiere un token de acceso OAuth2. El archivo de origen debe residir en el almacenamiento de Aspose Cloud o proporcionarse mediante una carga multipart.

## Operación de unión de archivos

- **[Unir archivos de Excel remotos en un libro especificado](https://docs.aspose.cloud/cells/merge-remote-spreadsheet/)**
- **[Unir varios archivos de Excel en un único libro](https://docs.aspose.cloud/cells/merge-spreadsheets/)**
- **[Unir archivos de Excel que coincidan en una carpeta remota](https://docs.aspose.cloud/cells/merge-spreadsheets-in-remote-folder/)**  

La unión combina dos o más libros en un único libro de destino. La API admite tanto listas explícitas de archivos como fusiones basadas en patrones dentro de una carpeta de almacenamiento.

**Detalles del punto de conexión**

| Método HTTP | Punto de conexión | Parámetros | Respuesta correcta |
|-------------|-------------------|------------|--------------------|
| POST | `https://api.aspose.cloud/v3.0/cells/merge` | `files` (matriz de nombres de archivos), `target` (nombre opcional del libro de destino) | `200 OK` con JSON que describe el libro fusionado |
| POST | `https://api.aspose.cloud/v3.0/cells/merge/remote` | `sourceFolder`, `pattern`, `target` | `200 OK` con metadatos del libro fusionado |

**Ejemplo de solicitud cURL (unir lista explícita)**

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/merge" \
     -H "Authorization: Bearer {access_token}" \
     -H "Content-Type: application/json" \
     -d '{
           "files": ["Book1.xlsx", "Book2.xlsx"],
           "target": "Combined.xlsx"
         }'
```

**Ejemplo de respuesta JSON**

```json
{
  "Code": 200,
  "Status": "OK",
  "MergedWorkbook": {
    "FileName": "Combined.xlsx",
    "Worksheets": 10
  }
}
```

> **Requisitos previos**: Todos los libros de origen deben estar almacenados en la misma ubicación del almacenamiento en la nube y el llamador debe tener permisos de lectura/escritura.

## Operación de división de archivos

- **[Dividir un archivo de Excel en varios archivos según hojas de cálculo](https://docs.aspose.cloud/cells/split-remote-spreadsheet/)**
- **[Dividir archivo de Excel según reglas personalizadas](https://docs.aspose.cloud/cells/split-spreadsheet/)**  

La división extrae hojas de cálculo individuales o grupos de filas/columnas en archivos de libro separados.

**Detalles del punto de conexión**

| Método HTTP | Punto de conexión | Parámetros | Respuesta correcta |
|-------------|-------------------|------------|--------------------|
| POST | `https://api.aspose.cloud/v3.0/cells/{fileName}/split` | `splitBy` (por ejemplo, `worksheet`), `outputFolder` | `200 OK` con lista de URLs de los archivos generados |
| POST | `https://api.aspose.cloud/v3.0/cells/{fileName}/split/custom` | JSON de regla personalizada (tamaño de página, rango de filas, etc.) | `200 OK` con detalles de los archivos divididos |

**Ejemplo de solicitud cURL (dividir por hoja de cálculo)**

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/BigReport.xlsx/split" \
     -H "Authorization: Bearer {access_token}" \
     -H "Content-Type: application/json" \
     -d '{
           "splitBy": "worksheet",
           "outputFolder": "Splits/"
         }'
```

**Ejemplo de respuesta JSON**

```json
{
  "Code": 200,
  "Status": "OK",
  "Splits": [
    {"FileName": "BigReport_Sheet1.xlsx", "Url": "https://storage.aspose.cloud/..."},
    {"FileName": "BigReport_Sheet2.xlsx", "Url": "https://storage.aspose.cloud/..."}
  ]
}
```

> **Requisitos previos**: El libro de origen debe estar accesible en el almacenamiento de Aspose Cloud, y el llamador debe tener permiso de escritura en la carpeta de destino.