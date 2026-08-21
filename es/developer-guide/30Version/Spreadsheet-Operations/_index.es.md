---
title: "Operaciones de hojas de cálculo"
second_title: "Documento"
type: docs
url: /es/spreadsheet-operations/
keywords: "Aspose Cells Cloud, Excel API, operaciones de hojas de cálculo, ajuste automático, procesamiento por lotes, protección de archivos, conversión, importación y exportación, procesamiento de texto"
description: "Aprenda a realizar operaciones en hojas de cálculo, como ajuste automático, conversión por lotes, protección, fusión y búsqueda-reemplazo, utilizando la API REST de Aspose.Cells Cloud. Incluye notas breves de uso y orientación con ejemplos de código."
weight: 100
ArticleTitle: "Operaciones de hojas de cálculo – Guía de la API de Aspose.Cells Cloud"
---

Las **Operaciones de hojas de cálculo** ofrecen una guía concisa sobre las acciones más comunes que puede realizar en libros de Excel con **Aspose.Cells Cloud** (v3.0). Ya sea que necesite ajustar automáticamente el ancho de columnas, procesar archivos por lotes, proteger hojas de cálculo o manipular texto, la API REST dispone de puntos de conexión dedicados que funcionan en lenguajes como Python, C# y Java. La lista siguiente enlaza a la documentación detallada de cada operación e incluye una breve nota de uso para ayudarle a comenzar rápidamente.

**Prerrequisitos**: Para invocar estos puntos de conexión, debe tener una clave válida de la API de Aspose.Cells Cloud e incluir el encabezado `Authorization` (`Bearer <access-token>`). Los ejemplos asumen la versión de la API v3.0.

- **[Opciones de ajuste automático](/cells/auto-fitter-options/)** – Ajusta automáticamente el ancho de columnas y la altura de filas. `POST /cells/{file}/worksheets/{sheet}/autoFitColumns`  
  ```http
  POST https://api.aspose.cloud/v3.0/cells/MyWorkbook.xlsx/worksheets/Sheet1/autoFitColumns
  Authorization: Bearer {access-token}
  Content-Type: application/json

  {
    "autoFitOptions": {
      "autoFitType": "All",
      "autoFitMergedCells": true
    }
  }
  ```
- **[Procesamiento por lotes de archivos de Excel: conversión, bloqueo, protección, división y desbloqueo](/cells/batch/)** – Realiza acciones masivas (conversión, bloqueo, protección, división y desbloqueo) en hasta 100 archivos por solicitud. `POST /cells/batch`  
  ```http
  POST https://api.aspose.cloud/v3.0/cells/batch
  Authorization: Bearer {access-token}
  Content-Type: application/json

  {
    "tasks": [
      { "file": "Book1.xlsx", "action": "convert", "format": "pdf" },
      { "file": "Book2.xlsx", "action": "protect", "password": "Secret123" }
    ]
  }
  ```
- **[Compresión y reparación de archivos de Excel](/cells/compress-and-repair-excel-files/)** – Reduce el tamaño del archivo y corrige problemas estructurales. `POST /cells/{file}/compressAndRepair`  
  ```http
  POST https://api.aspose.cloud/v3.0/cells/Report.xlsx/compressAndRepair
  Authorization: Bearer {access-token}
  ```
- **[Conversión de un archivo de Excel a otro formato o guardado en otro formato](/cells/conversion-and-save-as/)** – Convierte Excel a PDF, CSV, HTML, etc., o cambia el formato de salida. `GET /cells/{file}/saveAs`  
  ```http
  GET https://api.aspose.cloud/v3.0/cells/Financials.xlsx/saveAs?format=pdf
  Authorization: Bearer {access-token}
  ```
- **[Opciones de conversión de libro](/cells/convert-workbook-options/)** – Ajusta finamente configuraciones de conversión como tamaño de página, opciones de renderizado y protección por contraseña. `POST /cells/{file}/convert`  
  ```http
  POST https://api.aspose.cloud/v3.0/cells/Presentation.xlsx/convert
  Authorization: Bearer {access-token}
  Content-Type: application/json

  {
    "format": "pdf",
    "options": {
      "pageSetup": { "orientation": "landscape" },
      "pdfSaveOptions": { "compressImages": true }
    }
  }
  ```
- **[Creación de archivos de Excel y generación de informes](/cells/creating-files-and-reports/)** – Genera nuevos libros desde cero o a partir de plantillas. `PUT /cells/{newFile}`  
  ```http
  PUT https://api.aspose.cloud/v3.0/cells/NewReport.xlsx
  Authorization: Bearer {access-token}
  Content-Type: application/json

  {
    "templateFile": "Template.xlsx",
    "dataSource": { "name": "Q1 Sales", "value": 12345 }
  }
  ```
- **[Importación de datos en archivos de Excel y exportación de datos desde archivos de Excel](/cells/data-import-and-export/)** – Carga datos desde CSV, JSON o bases de datos y exporta datos de hojas de cálculo. `POST /cells/{file}/importData`  
  ```http
  POST https://api.aspose.cloud/v3.0/cells/Orders.xlsx/importData
  Authorization: Bearer {access-token}
  Content-Type: application/json

  {
    "importOptions": {
      "source": "json",
      "jsonData": [{ "OrderId": 1, "Amount": 250.0 }]
    }
  }
  ```
- **[Cifrado, descifrado y firma digital de archivos de Excel](/cells/protect/)** – Aplica protección por contraseña, cifrado o firmas digitales. `POST /cells/{file}/encrypt`  
  ```http
  POST https://api.aspose.cloud/v3.0/cells/Sensitive.xlsx/encrypt
  Authorization: Bearer {access-token}
  Content-Type: application/json

  {
    "password": "StrongPass!23",
    "encryptionType": "Standard"
  }
  ```
- **[Información del archivo](/cells/file-info/)** – Recupera metadatos como tamaño, formato y fecha de creación. `GET /cells/{file}/info`  
  ```http
  GET https://api.aspose.cloud/v3.0/cells/Archive.xlsx/info
  Authorization: Bearer {access-token}
  ```
- **[Fusión y división de archivos de Excel](/cells/merge-and-split/)** – Combina múltiples libros en uno solo o divide un libro en archivos independientes. `POST /cells/merge` / `POST /cells/split`  
  ```http
  POST https://api.aspose.cloud/v3.0/cells/merge
  Authorization: Bearer {access-token}
  Content-Type: application/json

  {
    "files": ["Q1.xlsx", "Q2.xlsx"],
    "outputFile": "FullYear.xlsx"
  }
  ```
- **[Búsqueda y reemplazo de contenido de texto en archivos de Excel](/cells/search-and-replace/)** – Busca y reemplaza cadenas en varias hojas de cálculo. `POST /cells/{file}/searchReplace`  
  ```http
  POST https://api.aspose.cloud/v3.0/cells/Report.xlsx/searchReplace
  Authorization: Bearer {access-token}
  Content-Type: application/json

  {
    "text": "Draft",
    "newText": "Final",
    "options": { "matchCase": false }
  }
  ```
- **[Procesamiento de texto en Excel: agregar texto, eliminar caracteres, recortar texto, modificar mayúsculas y minúsculas, y más](/cells/text-processing/)** – Realiza manipulaciones avanzadas sobre valores de celdas. `POST /cells/{file}/textProcessing`  
  ```http
  POST https://api.aspose.cloud/v3.0/cells/Notes.xlsx/textProcessing
  Authorization: Bearer {access-token}
  Content-Type: application/json

  {
    "operations": [
      { "type": "trim", "range": "A1:A10" },
      { "type": "toUpper", "range": "B1:B5" }
    ]
  }
  ```
- **[Inserción de marcas de agua o configuración de fondos en archivos de Excel](/cells/watermark-and-background/)** – Agrega marcas de agua de imagen o texto y establece fondos de hoja de cálculo. `POST /cells/{file}/watermark`  
  ```http
  POST https://api.aspose.cloud/v3.0/cells/Presentation.xlsx/watermark
  Authorization: Bearer {access-token}
  Content-Type: application/json

  {
    "type": "text",
    "text": "Confidential",
    "fontSize": 36,
    "color": "FF0000"
  }
  ```
- **[Trabajo con archivos de Excel: cálculo de fórmulas, ajuste automático, limpieza de objetos, etc.](/cells/workbook/)** – Ejecuta tareas comunes en libros como cálculo de fórmulas, limpieza de objetos y ajuste automático. `POST /cells/{file}/workbookOperations`  
  ```http
  POST https://api.aspose.cloud/v3.0/cells/Analytics.xlsx/workbookOperations
  Authorization: Bearer {access-token}
  Content-Type: application/json

  {
    "operations": [
      { "type": "calculateFormula" },
      { "type": "clearObjects", "objectType": "charts" }
    ]
  }
  ```