---
title: "Eliminar columnas en blanco de Excel con la API de Aspose.Cells Cloud – Ejemplo rápido de REST"
second_title: "Documento"
ArticleTitle: "Cómo eliminar columnas en blanco en Excel – Automatice la limpieza de columnas"
linktitle: "Eliminar columnas en blanco"
type: docs
url: /es/delete-spreadsheet-blank-columns/
keywords: "eliminar columnas en blanco API de Excel, Aspose.Cells Cloud, API REST, limpieza de Excel, automatización de hojas de cálculo"
description: "Aprenda a eliminar columnas vacías de archivos de Excel mediante la API REST de Aspose.Cells Cloud. Incluye el endpoint, autenticación, ejemplos de solicitud y respuesta, y código de SDK en C#, Java, Python y más."
weight: 100
---

Utilice la API de Aspose.Cells Cloud para eliminar automáticamente todas las columnas en blanco de las hojas de cálculo de Excel. Nuestra API inteligente detecta y elimina columnas cuyas celdas no contienen datos, fórmulas, comentarios, gráficos ni objetos. La API admite procesamiento por lotes, automatización en la nube e integración REST fluida para flujos de trabajo de limpieza de hojas de cálculo a nivel empresarial.

**Antecedentes:**  
Las columnas en blanco suelen aparecer tras importaciones de datos, generación de plantillas o migraciones de archivos heredados. Eliminar estas columnas vacías mejora el tamaño del archivo, el rendimiento de representación y la precisión del procesamiento posterior de datos. La API *Eliminar columnas en blanco de la hoja de cálculo* ofrece una forma rápida y del lado del servidor para limpiar hojas de cálculo sin editarlas manualmente.

## **API DeleteSpreadsheetBlankColumns**

### API web

```http
PUT https://api.aspose.cloud/v4.0/cells/delete/blank-columns
```

### **Seguridad y autenticación**

Las API de Aspose.Cells Cloud son seguras y requieren <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">autenticación basada en token JWT</a>.

```bash
-H "Authorization: Bearer {access_token}"
```

### Parámetros de solicitud

| Nombre del parámetro | Tipo   | Ubicación              | Descripción                                                                                                                  |
| --------------------- | ------ | ---------------------- | ---------------------------------------------------------------------------------------------------------------------------- |
| **Spreadsheet**       | Archivo | Form‑Data (multipart)  | El libro de Excel que se va a procesar.                                                                                      |
| **outPath**           | Cadena | Consulta               | Opcional. Carpeta de destino en el almacenamiento en la nube para el archivo limpio. Si se omite, el resultado se devuelve en el cuerpo de la respuesta. |
| **outStorageName**    | Cadena | Consulta               | Opcional. Nombre del almacenamiento en la nube donde se debe guardar el resultado.                                          |
| **region**            | Cadena | Consulta               | Opcional. Identificador de configuración regional (por ejemplo, `es-ES`, `fr-FR`).                                          |
| **password**          | Cadena | Consulta               | Opcional. Contraseña para abrir un libro protegido.                                                                          |

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

### Códigos de error

- **400 Bad Request** – Parámetros de solicitud no válidos o URI con formato incorrecto.
- **401 Unauthorized** – Token de acceso ausente o no válido.
- **404 Not Found** – No se pudo encontrar la hoja de cálculo especificada.
- **500 Server Error** – Se produjo una condición inesperada que impidió que la API procesara el archivo.

## Cuándo utilizar la API Delete Spreadsheet Blank Columns

- **Flujos de trabajo de importación y limpieza de datos** – Elimine columnas en blanco finales o estructurales inmediatamente después de cargar datos desde CSV, bases de datos o API web.
- **Generación de informes y paneles** – Asegure que los informes finales tengan un diseño limpio sin columnas vacías innecesarias.
- **Tuberías ETL** – Preprocese archivos de Excel antes de cargarlos en almacenes de datos como Snowflake o BigQuery.
- **Integración de sistemas** – Normalice archivos de Excel proporcionados por socios antes de su procesamiento posterior.
- **Automatización por lotes de documentos** – Elimine columnas de marcador de posición de plantillas generadas en lote.
- **Contenido generado por usuarios** – Limite las cargas de Excel desde portales web antes del almacenamiento o análisis.
- **Migración de datos heredados** – Simplifique archivos antiguos de hojas de cálculo eliminando columnas históricamente vacías.

## ¿Por qué utilizar esta API?

- **Amigable para desarrolladores** – SDK disponibles para C#, Java, Python, PHP, Ruby, Node.js, Go y más, reduciendo el esfuerzo de desarrollo.
- ** rentable** – Precios por uso eliminan los costos iniciales de infraestructura.
- **Cero mantenimiento** – Sin servidores que gestionar; el servicio se actualiza continuamente por Aspose.

## Cómo utilizar la API Delete Spreadsheet Blank Columns con SDK

### Especificación de la API

La [Especificación de la API Delete Spreadsheet Blank Columns](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Transform/RemoveSpreadsheetBlankColumns) proporciona la definición OpenAPI completa y ejemplos.

### Uso de los SDK de Aspose.Cells Cloud

El SDK abstracte los detalles HTTP de bajo nivel, permitiéndole eliminar columnas en blanco con solo unas pocas líneas de código. Consulte el repositorio oficial de GitHub para obtener una lista completa de los lenguajes admitidos: <https://github.com/aspose-cells-cloud>.

Los siguientes ejemplos de código muestran cómo llamar a la API mediante varios SDK:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_DeleteSpreadsheetBlankColumns.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_DeleteSpreadsheetBlankColumns.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_DeleteSpreadsheetBlankColumns.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_DeleteSpreadsheetBlankColumns.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_DeleteSpreadsheetBlankColumns.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_DeleteSpreadsheetBlankColumns.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_DeleteSpreadsheetBlankColumns.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_DeleteSpreadsheetBlankColumns.go" >}}
{{</tab>}}
{{< /tabs >}}
---