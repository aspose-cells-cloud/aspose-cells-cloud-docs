---
title: "Aspose.Cells Cloud Web API: Convertir datos de una tabla de hoja de cálculo a un archivo CSV - Herramienta gratuita en línea"
second_title: "Documentación"
ArticleTitle: "Cómo convertir datos de una tabla de hoja de cálculo a un archivo CSV: Guía paso a paso"
linktitle: "Convertir tabla a CSV"
type: docs
url: /convert-table-to-csv/
keywords: "Aspose.Cells Cloud, tabla a CSV, conversión de hojas de cálculo, Excel a CSV, API, REST, exportación de datos"
description: "Convierta rápidamente una tabla de una hoja de cálculo de Excel a un archivo CSV utilizando la API de Aspose.Cells Cloud."
weight: 100
---

Exporte datos de una tabla desde un archivo local de Excel a un archivo CSV utilizando la API en la nube.

## **API para convertir tabla a CSV**

### API web

```http
PUT http://api.aspose.cloud/v4.0/cells/convert/table/csv
```

### **Seguridad y autenticación**

Las API de Aspose.Cells Cloud son seguras y requieren <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">autenticación basada en token JWT</a>.

```bash
-H "Authorization: Bearer {access_token}"
```

### **Parámetros de solicitud:**

| Nombre del parámetro | Tipo   | Ruta/cadena de consulta/cuerpo HTTP | Descripción                                                                                                                             |
| --------------------- | ------ | ----------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------- |
| Spreadsheet           | Archivo | FormData                            | Cargar el archivo de hoja de cálculo.                                                                                                   |
| worksheet             | Cadena  | Consulta                            | Nombre de la hoja de cálculo dentro del libro.                                                                                          |
| tableName             | Cadena  | Consulta                            | Nombre de la tabla que se va a convertir.                                                                                               |
| outPath               | Cadena  | Consulta                            | (Opcional) Ruta de carpeta donde se guarda el libro; el valor predeterminado es null.                                                   |
| outStorageName        | Cadena  | Consulta                            | Nombre del almacenamiento para el archivo de salida.                                                                                    |
| fontsLocation         | Cadena  | Consulta                            | Ruta para utilizar fuentes personalizadas.                                                                                              |
| region                | Cadena  | Consulta                            | Configuración regional/idioma de la hoja de cálculo (por ejemplo, `es-ES`, `fr-FR`). Influye en el formato de números, el análisis de fechas y el comportamiento específico de la configuración regional. |
| password              | Cadena  | Consulta                            | Contraseña para abrir el archivo de hoja de cálculo.                                                                                    |

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

| Código | Significado               | Descripción                                                        |
| ------ | ------------------------- | ------------------------------------------------------------------ |
| 200    | Correcto                  | Filtro aplicado correctamente; la respuesta contiene detalles de la operación. |
| 400    | Solicitud incorrecta      | Parámetros faltantes o no válidos (por ejemplo, tipo de archivo no admitido). |
| 401    | No autorizado             | Token JWT inválido o faltante.                                     |
| 413    | Payload demasiado grande   | El archivo cargado excede el límite de tamaño.                    |
| 500    | Error interno del servidor | Error inesperado en el servidor.                                   |

## **¿Dónde debería utilizar la API de conversión de tabla a CSV?**

- **Migración de bases de datos**: Convertir tablas de Excel a CSV para importación masiva en bases de datos SQL (MySQL, PostgreSQL, SQL Server).
- **Carga en almacenes de datos**: Transformar tablas de informes basadas en Excel a CSV para cargarlas en Snowflake, Redshift o BigQuery.
- **Cargas útiles por lotes en APIs**: Convertir datos de tablas de Excel a CSV para cargas masivas en servicios REST.
- **Comunicación entre servicios**: Utilizar CSV como formato ligero para intercambio de datos entre microservicios.
- **Preparación de datos para aprendizaje automático**: Convertir tablas de características desde Excel a CSV para bibliotecas de aprendizaje automático en Python/R.
- **Análisis estadístico**: Transformar tablas de datos de investigación a CSV para importarlos en SPSS, SAS o Stata.
- **Migración de contenido**: Mover contenido estructurado desde Excel a sistemas de gestión de contenidos (CMS) mediante CSV.

## ¿Por qué debería utilizar la API de conversión de tabla a CSV?

- **Fácil de usar para desarrolladores**: Aspose.Cells Cloud ofrece bibliotecas SDK en múltiples lenguajes, lo que permite un desarrollo rápido, y viene con documentación completa. En comparación con la creación de soluciones personalizadas, esto reduce significativamente la carga de desarrollo.
- **Rentable**: Puede convertir datos de tablas sin necesidad de cargar previamente el libro, lo que ahorra espacio de almacenamiento y reduce costos.
- **Extracción pura de datos sin formato de estilo**.
- **CSV es compatible prácticamente con todos los sistemas**:
  - Bases de datos (todos los SGBD principales)
  - Lenguajes de programación (todos incluyen analizadores nativos)
  - Herramientas de inteligencia empresarial (Tableau, Power BI, Looker)
  - Software de hojas de cálculo (Excel, Google Sheets, LibreOffice)
  - Herramientas de línea de comandos (awk, sed, grep)

## ¿Cómo utilizar la API de conversión de tabla a CSV con SDK?

### Especificación de la API para convertir tabla a CSV

La [Especificación de la API para convertir tabla a CSV](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Conversion/ConvertTableToCSV) proporciona una interfaz de programación accesible públicamente, lo que permite interacciones REST directamente desde un navegador web.
Puede utilizar la herramienta de línea de comandos cURL para acceder fácilmente a los servicios web de Aspose.Cells. El siguiente ejemplo muestra cómo realizar llamadas a la API en la nube mediante cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Solicitud" tabName12="Respuesta" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/convert/table/csv?worksheet=Sheet1&tableName=Table1" \
  -H "Authorization: Bearer {access_token}" \
  -F "Spreadsheet=@myWorkbook.xlsx" \
  -o converted.csv
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

Utilizar los SDK es la forma más rápida de desarrollar, ya que ocultan los detalles de bajo nivel, permitiéndole convertir datos de tablas de hojas de cálculo a un archivo CSV con un código mínimo. Consulte el [repositorio de GitHub](https://github.com/aspose-cells-cloud) para obtener una lista completa de los SDK de Aspose.Cells Cloud.

Los siguientes ejemplos de código muestran cómo realizar llamadas a los servicios web de Aspose.Cells utilizando diversos SDK:
{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_ConvertTableToCSV.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_ConvertTableToCSV.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_ConvertTableToCSV.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_ConvertTableToCSV.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_ConvertTableToCSV.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_ConvertTableToCSV.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_ConvertTableToCSV.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_ConvertTableToCSV.go" >}}
{{</tab>}}
{{< /tabs >}}