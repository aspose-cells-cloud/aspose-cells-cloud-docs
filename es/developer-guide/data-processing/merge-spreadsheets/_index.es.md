---
title: Aspose.Cells Cloud Web API - Fusionar varias hojas de cálculo en una sola
second_title: Documen
ArticleTitle: Merge multiple Spreadsheets into a single spreadsheet
linktitle: Fusionar hoja de cálculo
type: docs
url: /es/merge-spreadsheets/
keywords: Merge spreadsheets, data merging, file format conversion, REST, XLSX, CSV, PD
description: Combine fácilmente archivos de hojas de cálculo locales en varios formatos (XLSX, CSV, PDF) utilizando Excel API
weight: 100
kwords: Excel API, Combinar hojas de cálculo, Office Nube, REST API, Combinar hojas de cálculo, Formato CSV, JSON, Markdow
---
Fusiona múltiples archivos de hojas de cálculo locales en un solo archivo, al mismo tiempo que admite la salida en más de 30 formatos de archivo.

## **Fusionar hoja de cálculo API**

```http
PUT http://api.aspose.cloud/v4.0/cells/merge/spreadsheet
```

### **Parámetros de la solicitud:**

| Nombre del parámetro| Tipo| Ruta/Cadena de consulta/Cuerpo HTTP| Descripción|
|:- |:- |:- |:- |
| Hoja de cálculo| Archivo| Datos del formulario| Sube el archivo de hoja de cálculo.|
| formato de salida| Cadena| Consulta| Especifique el formato del archivo de salida.|
| fusionar en una hoja| Booleano| Consulta| Indique si desea combinar todos los datos en una sola hoja de cálculo.|
| Ruta de salida| Cadena| Consulta| (Opcional) Ruta de la carpeta del libro de salida. El valor predeterminado es nulo.|
|nombreAlmacenamientoExterno| Cadena| Consulta| Especifique el nombre de almacenamiento del archivo de salida.|
| Ubicación de fuentes| Cadena| Consulta| Define fuentes personalizadas que se utilizarán.|
| región| Cadena| Consulta| Establecer la región de la hoja de cálculo.|
| contraseña| Cadena| Consulta| Proporcione la contraseña para abrir el archivo de hoja de cálculo.|

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

### Códigos de error

- **400 Solicitud incorrecta**: URI de nube Apose.Cells no válido API.
- **401 No autorizado**Token de acceso no válido. O ID de cliente y secreto no válidos.
- **404 No encontrado**:El archivo de hoja de cálculo no es accesible.
- **Error de servidor 500**:La hoja de cálculo ha encontrado una anomalía al obtener los datos de cálculo.

## ¿Dónde debemos utilizar la hoja de cálculo Merge Local API?

Cuando necesite fusionar varios archivos de datos, puede utilizar este API.

## ¿Por qué debería utilizar la hoja de cálculo Merge Local API?

- No necesita espacio de almacenamiento en la nube, simplemente fusione directamente.
- El desarrollo se puede completar rápidamente a través del SDK existente.

## Cómo utilizar la hoja de cálculo Merge Local API con SDK

### Especificación OpenAPI

 El[Especificación OpenAPI](https://reference.aspose.cloud/cells/#/DataProcessingController/MergeSpreadsheets)Proporciona una interfaz de programación de acceso público, que permite a los usuarios realizar interacciones REST directamente desde un navegador web.

### Utilice los SDK de la nube Aspose.Cells

Usar el SDK es la forma más rápida de desarrollar, ya que abstrae los detalles de bajo nivel y permite fusionar varias hojas de cálculo en una hoja de cálculo con código corto.
 Por favor, consulte el[Repositorio de GitHub](https://github.com/aspose-cells-cloud) para obtener una lista completa de Aspose.Cells SDK en la nube.

Los siguientes ejemplos de código ilustran cómo realizar llamadas a los servicios web Aspose.Cells utilizando varios SDK:
{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_MergeSpreadsheets.cs" >}}
{{< /tab >}}
{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_MergeSpreadsheets.java" >}}
{{< /tab >}}
{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_MergeSpreadsheets.php" >}}
{{< /tab >}}
{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_MergeSpreadsheets.rb" >}}
{{< /tab >}}
{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_MergeSpreadsheets.ts" >}}
{{< /tab >}}
{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_MergeSpreadsheets.py" >}}
{{< /tab >}}
{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_MergeSpreadsheets.pl" >}}
{{< /tab >}}
{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_MergeSpreadsheets.go" >}}
{{< /tab >}}
{{< /tabs >}}
