---
title: "Aspose.Cells Cloud Web API: Convertir hoja de cálculo a JSON"
second_title: "Document"
ArticleTitle: "Cómo convertir una hoja de cálculo de una hoja de cálculo a JSON mediante la API de Aspose.Cells Cloud"
linktitle: "Convertir hoja de cálculo a JSON"
type: docs
url: /convert-worksheet-to-json/
keywords: "Aspose.Cells, hoja de cálculo a JSON, conversión de Excel, API en la nube, API v4, exportación de datos"
description: "Guía paso a paso para convertir una hoja de cálculo de Excel a JSON mediante la API de Aspose.Cells Cloud, incluidos los parámetros de solicitud, el manejo de respuestas, los códigos de error y ejemplos de SDK."
weight: 100
---

El endpoint **ConvertWorksheetToJson** lee un archivo de hoja de cálculo desde el sistema de archivos local, extrae la hoja especificada y devuelve su contenido como un archivo JSON. La conversión se realiza completamente en los servidores de Aspose.Cells Cloud, por lo que no se requiere ninguna carga ni almacenamiento intermedio. Admite libros protegidos con contraseña, ubicaciones personalizadas de fuentes y configuraciones regionales, ofreciendo una solución rápida y nativa en la nube para exportar datos de hojas a JSON, listos para su procesamiento posterior.

## **API para convertir hoja de cálculo a JSON**

### API web

```http
PUT https://api.aspose.cloud/v4.0/cells/convert/worksheet/json
```

### **Seguridad y autenticación**

Las APIs de Aspose.Cells Cloud son seguras y requieren <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">autenticación basada en token JWT</a>.

### **Parámetros de solicitud:**

| Nombre del parámetro | Tipo   | Ubicación    | Obligatorio / Opcional | Descripción                                                                                                                                                                         |
| :------------------- | :----- | :----------- | :-------------------- | :---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Spreadsheet          | archivo | FormData     | Obligatorio           | El libro de Excel que se procesará. Debe estar en un formato admitido (xls, xlsx, csv, etc.). Se envía como multipart/form-data. Ejemplo: `Spreadsheet=@C:\Docs\Sample.xlsx`.      |
| worksheet            | cadena | Query        | Obligatorio           | Nombre exacto de la hoja que se convertirá (distingue mayúsculas y minúsculas). Si se omite o no se encuentra, la API devuelve un error. Ejemplo: `worksheet=Sheet1`.               |
| outPath              | cadena | Query        | Opcional              | Carpeta de destino en el almacenamiento en la nube configurado donde se guardará el archivo JSON generado. Si no se proporciona, el JSON se devuelve directamente en el flujo de respuesta. Ejemplo: `outPath=/converted/`. |
| outStorageName       | cadena | Query        | Opcional              | Nombre del almacenamiento de destino (por ejemplo, "MyStorage") que contiene `outPath`. Usa el almacenamiento predeterminado si se omite.                                          |
| fontsLocation        | cadena | Query        | Opcional              | Carpeta en el servidor que contiene las fuentes personalizadas necesarias para representar correctamente el texto en la hoja. Ejemplo: `fontsLocation=/fonts/custom/`.             |
| region               | cadena | Query        | Opcional              | Identificador cultural/regional que influye en el formato de números, fechas y monedas en el JSON generado (por ejemplo, `es-ES`, `fr-FR`).                                        |
| password             | cadena | Query        | Opcional              | Contraseña para abrir un libro cifrado. Si el libro no está protegido con contraseña, omita este parámetro.                                                                         |

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

| Código | Significado             | Descripción                                                       |
| ------ | ----------------------- | ----------------------------------------------------------------- |
| 200    | Correcto                | Filtro aplicado correctamente; la respuesta contiene detalles de la operación. |
| 400    | Solicitud incorrecta    | Parámetros faltantes o no válidos (por ejemplo, tipo de archivo no admitido). |
| 401    | No autorizado           | Token JWT inválido o ausente.                                      |
| 413    | Payload demasiado grande | El archivo cargado excede el límite de tamaño.                   |
| 500    | Error interno del servidor | Error inesperado del servidor.                                    |

## ¿Dónde debemos usar la API para convertir hoja de cálculo a JSON?

- **Paneles web (dashboards)** – Exportar datos de la hoja a JSON para bibliotecas de gráficos del lado cliente (por ejemplo, Chart.js, D3.js).
- **Migración de datos** – Mover datos de Excel antiguos a bases de datos NoSQL o servicios REST que consumen JSON.
- **Aplicaciones móviles o sin conexión** – Convertir contenido de hojas a JSON en el servidor y luego sincronizar la carga ligera en dispositivos móviles.
- **Cadenas de procesamiento de informes** – Alimentar directamente los datos de la hoja a motores de análisis que aceptan entrada JSON, sin necesidad de pasos intermedios en CSV.

## ¿Por qué debería usar la API para convertir hoja de cálculo a JSON?

- **Flujo de trabajo sin carga previa** – Procesar archivos locales en la nube sin cargarlos previamente al almacenamiento, ahorrando ancho de banda y costos de almacenamiento.
- **Conversión completa** – Admite libros protegidos con contraseña, fuentes personalizadas y formato regional para una representación precisa de los datos.
- **Ejecución rápida y escalable** – Aprovecha el motor de alto rendimiento de Aspose.Cells en infraestructura en la nube, manejando eficientemente hojas grandes.
- **Integración simplificada** – Una única llamada PUT devuelve un archivo JSON listo para usar o lo almacena directamente, reduciendo la complejidad del código en las aplicaciones cliente.

## Cómo usar la API para convertir hoja de cálculo a JSON con SDK

### Especificación de la API para convertir hoja de cálculo a JSON

La <a href="https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Conversion/ConvertWorksheetToJson" rel="noopener noreferrer">Especificación de la API para convertir hoja de cálculo a JSON</a> proporciona una interfaz de programación accesible públicamente para ejecutar interacciones REST directamente desde un navegador web.

Puede usar la herramienta de línea de comandos cURL para acceder fácilmente a los servicios web de Aspose.Cells. El siguiente ejemplo muestra cómo realizar llamadas a la API en la nube con cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Solicitud" tabName12="Respuesta" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/convert/worksheet/json?worksheet=Sheet1" \
  -H "Authorization: Bearer {access_token}" \
  -F "Spreadsheet=@myWorkbook.xlsx" \
  -o converted.json
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

Usar los SDK es la forma más rápida de desarrollar, ya que abstrae los detalles de bajo nivel y permite trabajar con hojas de cálculo mediante código conciso. Consulte el <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">repositorio de GitHub</a> para obtener una lista completa de los SDK de Aspose.Cells Cloud.  
Los siguientes ejemplos de código muestran cómo interactuar con los servicios web de Aspose.Cells mediante diversos SDK:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example_v40_ConvertWorksheetToJson.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_v40_ConvertWorksheetToJson.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_v40_ConvertWorksheetToJson.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_v40_ConvertWorksheetToJson.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_v40_ConvertWorksheetToJson.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_v40_ConvertWorksheetToJson.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_v40_ConvertWorksheetToJson.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_v40_ConvertWorksheetToJson.go" >}}
{{</tab>}}
{{< /tabs >}}