---
title: "Generar informes de Excel con plantillas de marcadores inteligentes"
second_title: "Documentos"
linktype: "SmartMarker"
type: docs
url: /es/build-report-with-smart-marker/
aliases:
  - /create-excel-workbook-from-a-smartmarker-template/
  - /workbook/smartmarker/
  - /workbook/create/smartmarker/
keywords: "Excel, marcador inteligente, Aspose.Cells Cloud, API REST, libro de cálculo, SDK, API, generación de informes"
description: "Aprenda a generar libros de cálculo de Excel a partir de plantillas de marcadores inteligentes mediante la API REST de Aspose.Cells Cloud. Incluye detalles de solicitud y respuesta, ejemplo con cURL, requisitos previos, notas y ejemplos de código SDK."
weight: 40
ArticleTitle: "Generar informes de Excel con plantillas de marcadores inteligentes – Guía de la API de Aspose.Cells Cloud"
---

Esta API REST crea un libro de cálculo utilizando una plantilla de marcador inteligente.

## API SmartMarker para libros de cálculo

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/smartmarker
```

### **Seguridad y autenticación**

Las API de Aspose.Cells Cloud son seguras y requieren <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">autenticación basada en token JWT</a>.

### **¿Qué es un marcador inteligente?**

Un marcador inteligente es una sintaxis de marcador de posición que asigna campos de datos en un archivo XML (o JSON) a celdas de una plantilla de Excel. En tiempo de ejecución, Aspose.Cells reemplaza los marcadores con los datos correspondientes, permitiéndole generar informes completamente rellenados de forma programática.

### **Parámetros de consulta**

| Nombre del parámetro | Tipo   | Descripción                                                  |
| -------------------- | ------ | ------------------------------------------------------------ |
| outPath              | string | Ruta de destino donde se guardará el libro generado.       |
| folder               | string | Carpeta que contiene el libro original.                      |
| storageName          | string | Nombre del servicio de almacenamiento a utilizar.           |

### **Parámetro del cuerpo de solicitud**

| Nombre del parámetro | Tipo | Descripción                                           |
| -------------------- | ---- | ----------------------------------------------------- |
| xmlFile              | file | Archivo XML con datos del marcador inteligente subido con la solicitud. |

### **Respuesta**

```json
{
    "Name": "ResponseFile",
    "DataType": {
        "Identifier": "File",
        "Reference": "Stream",
        "Name": "file"
    }
}
```

**Notas / Limitaciones:**  
- La API admite archivos de Excel de hasta **50 MB**.  
- Los formatos aceptados son únicamente **.xlsx**, **.xlsm** y **.xlsb**.  
- Se aplica un límite de velocidad de **20 solicitudes por segundo** por cuenta.

**Códigos de estado HTTP**

| Código | Significado                 | Descripción                                                  |
| ------ | --------------------------- | ------------------------------------------------------------ |
| 200    | OK                          | Filtro aplicado correctamente; la respuesta contiene detalles de la operación. |
| 400    | Solicitud incorrecta        | Parámetros faltantes o no válidos (por ejemplo, tipo de archivo no admitido). |
| 401    | No autorizado               | Token JWT inválido o ausente. |
| 413    | Carga útil demasiado grande | El archivo subido supera el límite de tamaño. |
| 500    | Error interno del servidor  | Error inesperado en el servidor. |

## Cómo usar la API SmartMarker para libros de cálculo

### Especificación de la API SmartMarker para libros de cálculo

La [Especificación OpenAPI](https://apireference.aspose.cloud/cells/#/Workbook/PostWorkbookGetSmartMarkerResult) define una interfaz de programación accesible públicamente y le permite realizar interacciones REST directamente desde un navegador web.

### Uso de los SDK de Aspose.Cells Cloud

Puede utilizar la herramienta de línea de comandos **cURL** para acceder fácilmente a los servicios web de Aspose.Cells. El siguiente ejemplo muestra cómo realizar llamadas a la API en la nube con cURL.

**Ejemplo rápido en una sola línea**

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/{name}/smartmarker?outPath={outPath}" -H "Authorization: Bearer {access_token}" -F "xmlFile=@Sample_SmartMarker_Data.xml"
```

{{< tabs tabTotal="2" tabID="1" tabName1="Solicitud" tabName2="Respuesta" >}}

{{< tab tabNum="1" >}}

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/newworkbook_14.xlsx/smartmarker?outPath=GeneratedReport.xlsx" \
    -H "accept: multipart/form-data" \
    -H "x-aspose-client: Containerize.Swagger" \
    -F "xmlFile=@Sample_SmartMarker_Data.xml"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```text
HTTP/1.1 200 OK
Content-Type: application/json

{
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

### **Manejo de errores**

| Código de estado HTTP | Descripción           | Causa típica                                               |
| --------------------- | --------------------- | ---------------------------------------------------------- |
| 400                   | Solicitud incorrecta  | Plantilla ausente, XML con formato incorrecto o parámetros no válidos. |
| 401                   | No autorizado         | Token de autenticación inválido o ausente.                 |
| 404                   | No encontrado         | El libro especificado o la ubicación del almacenamiento no existe. |
| 500                   | Error interno del servidor | Fallo inesperado del lado del servidor.                  |

**Ejemplo de respuesta de error (400)**

```json
{
  "Code": 400,
  "Message": "El archivo de datos XML está ausente o tiene un formato incorrecto."
}
```

## Familia de SDK en la nube

Utilizar un SDK es la mejor forma de acelerar el desarrollo. Un SDK maneja los detalles de bajo nivel para que usted se enfoque en las tareas de su proyecto. Consulte el [repositorio de GitHub](https://github.com/aspose-cells-cloud) para obtener una lista completa de los SDK de Aspose.Cells Cloud.

Los siguientes ejemplos de código muestran cómo llamar a los servicios web de Aspose.Cells mediante diversos SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePutWorkbookCreate.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PutWorkbookCreate.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PutWorkbookCreate.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PutWorkbookCreate.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PutWorkbookCreate.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PutWorkbookCreate.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PutWorkbookCreate.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PutWorkbookCreate.go" >}}

{{< /tab >}}

{{< /tabs >}}