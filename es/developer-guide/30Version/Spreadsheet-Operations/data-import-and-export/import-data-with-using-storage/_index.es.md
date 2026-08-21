---
title: "Importar datos mediante almacenamiento"
second_title: "Documentos"
linktype: "import-data-with-using-storage"
type: docs
url: /es/import-data-with-using-storage/
aliases:
  - /import-data-into-excel-worksheet/
  - /import-data-into-worksheet/
  - /import-data-in-excel-worksheet/
  - /import-data/
  - /import/with-using-storage/
description: "Importar datos mediante almacenamiento: Importe datos en una hoja de cálculo de Excel mediante la API de Aspose.Cells Cloud desde diversas fuentes de almacenamiento. Admite formatos JSON, CSV y otros a través de HTTPS."
keywords: "Aspose.Cells Cloud, Excel, importar datos, API REST, almacenamiento en la nube, JSON, CSV, PDF, Markdown, HTTPS"
weight: 10
ArticleTitle: "Importar datos mediante almacenamiento — Documentación de la API de Aspose.Cells Cloud"
---

Esta API REST importa datos en un archivo de Excel.

## API PostImportData

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/importdata
```

### **Seguridad y autenticación**

Las API de Aspose.Cells Cloud son seguras y requieren <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">autenticación basada en token JWT</a>.

### Los parámetros de la solicitud son

| Nombre del parámetro | Tipo   | Ubicación | Descripción                                           |
| --------------------- | ------ | --------- | ----------------------------------------------------- |
| name                  | string | path      | Nombre del archivo de Excel.                          |
| folder                | string | query     | Ruta de la carpeta en el almacenamiento donde reside el archivo. |
| storageName           | string | query     | Nombre del servicio de almacenamiento.                |
| importData            | object | body      | Objeto JSON que contiene los datos que se van a importar. |

**Los parámetros de opción de importación de datos** se describen en [el enlace de referencia](/cells/import/#import-data-option-parameter).

**Requisitos previos:** Debe proporcionar un token JWT válido en el encabezado `Authorization` y asegurarse de que el libro de destino ya exista en la ubicación de almacenamiento especificada.

### Respuesta

```json
{
  "Status":"OK",
  "Code":200
}
```

**Códigos de estado HTTP**

| Código | Significado                 | Descripción                                              |
| ------ | --------------------------- | -------------------------------------------------------- |
| 200    | OK                          | Filtro aplicado correctamente; la respuesta contiene los detalles de la operación. |
| 400    | Solicitud incorrecta        | Parámetros ausentes o no válidos (por ejemplo, tipo de archivo no admitido). |
| 401    | No autorizado               | Token JWT no válido o ausente. |
| 413    | Carga útil demasiado grande | El archivo subido supera el límite de tamaño. |
| 500    | Error interno del servidor  | Error inesperado en el servidor. |

## Cómo utilizar la API PostImportData con SDK

### Especificación de la API PostImportData

La <a href="https://apireference.aspose.cloud/cells/#/Workbook/PostImportData" rel="noopener noreferrer">Especificación OpenAPI</a> define una interfaz de programación accesible públicamente y le permite realizar interacciones REST directamente desde un navegador web.

Puede utilizar la herramienta de línea de comandos cURL para acceder fácilmente a los servicios web de Aspose.Cells. El siguiente ejemplo muestra cómo invocar la API en la nube mediante cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Solicitud" tabName2="Respuesta" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/importdata" \
     -X POST \
     -d '{"Data":[1,2,4],"DestinationWorksheet":"Sheet1","FirstRow":1,"FirstColumn":2,"IsVertical":true,"IsInsert":true,"importDataType":"IntArray"}' \
     -H "Content-Type: application/json" \
     -H "Accept: application/json" \
     -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

### Utilizar los SDK de Aspose.Cells Cloud

Usar un SDK es la mejor manera de acelerar el desarrollo. Un SDK abstracta los detalles de bajo nivel, permitiéndole centrarse en su lógica de negocio. Consulte el [repositorio de GitHub](https://github.com/aspose-cells-cloud) para obtener una lista completa de los SDK de Aspose.Cells Cloud.

El siguiente ejemplo de código demuestra cómo invocar el servicio web de Aspose.Cells mediante el SDK de PHP:
---