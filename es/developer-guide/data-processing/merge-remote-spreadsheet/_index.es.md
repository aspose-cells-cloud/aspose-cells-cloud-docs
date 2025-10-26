---
title: Aspose.Cells Cloud Web API - Fusionar una hoja de cálculo en otra.
second_title: Aspose.Cells Cloud"
ArticleTitle: Merge one spreadsheet into anothe
linktitle: Fusionar hoja de cálculo remota
type: docs
url: /es/merge-remote-spreadsheet/
keywords: Merge spreadsheets, cloud storage, Aspose.Cells Cloud Web API, spreadsheet merging, XLSX, CSV, PD
description: Combine un archivo de hoja de cálculo almacenado en un almacenamiento en la nube con otra hoja de cálculo y podrá especificar el formato y la ubicación de la salida de datos.
weight: 100
kwords: Excel, Office Nube, REST API, Hoja de cálculo, PDF, CSV, JSON, Markdown, combinar celdas en blanco, procesamiento en la nube
---
Combine un archivo de hoja de cálculo almacenado en un almacenamiento en la nube con otra hoja de cálculo y podrá especificar el formato y la ubicación de la salida de datos.

## **Fusionar hoja de cálculo remota API**

```http
PUT http://api.aspose.cloud/v4.0/cells/{name}/merge/spreadsheet
```

### **Parámetros de la solicitud:**

| Nombre del parámetro| Tipo| Ruta/Cadena de consulta/HTTPBody| Descripción|
|:- |:- |:- |:- |
|nombre|Cadena|Camino|El nombre del archivo del libro de trabajo que se va a fusionar.|
|hoja de cálculo fusionada|Cadena|Consulta|La lista de archivos de hojas de cálculo para fusionar.|
|carpeta|Cadena|Consulta|La ruta de la carpeta donde se almacena el libro de trabajo.|
|formato de salida|Cadena|Consulta|El formato del archivo de salida (por ejemplo, XLSX, PDF).|
|fusionar en una hoja|Booleano|Consulta|Si se deben combinar todos los datos en una sola hoja de cálculo.|
|nombreDeAlmacenamiento|Cadena|Consulta|(Opcional) El nombre del almacenamiento si se utiliza un almacenamiento en la nube personalizado. Si se omite, se usará el almacenamiento predeterminado.|
|Ruta de salida|Cadena|Consulta|(Opcional) Ruta de la carpeta del libro fusionado. El valor predeterminado es nulo.|
|nombreAlmacenamientoExterno|Cadena|Consulta|El nombre del almacenamiento para el archivo de salida.|
|Ubicación de fuentes|Cadena|Consulta|Ubicación de fuente personalizada.|
|región|Cadena|Consulta|La configuración de la región de la hoja de cálculo.|
|contraseña|Cadena|Consulta|La contraseña para acceder al archivo de hoja de cálculo.|

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

## ¿Dónde debemos utilizar la hoja de cálculo Merge Remote API?

- Cuando necesita fusionar varios archivos de datos en el almacenamiento en la nube.


## ¿Por qué debería utilizar la hoja de cálculo Merge Remote API?

- Los archivos de almacenamiento en la nube no necesitan descargarse y se pueden fusionar directamente en la nube.
- El desarrollo se puede completar rápidamente a través del SDK existente.

## Cómo utilizar la hoja de cálculo remota Merge API con SDK

### Especificación de la hoja de cálculo remota Merge API

 El[Especificación de la hoja de cálculo remota Merge API](https://reference.aspose.cloud/cells/#/DataProcessingController/MergeRemoteSpreadsheet) Proporciona una interfaz de programación de acceso público para ejecutar interacciones REST directamente desde un navegador web.

## Excel API SDK

### Utilice los SDK de la nube Aspose.Cells

Usar el SDK es la forma más rápida de desarrollar, ya que abstrae los detalles de bajo nivel y permite fusionar una hoja de cálculo en otra con un código corto.
 Por favor, consulte el[Repositorio de GitHub](https://github.com/aspose-cells-cloud) para obtener una lista completa de Aspose.Cells SDK en la nube.
Los siguientes ejemplos de código demuestran cómo interactuar con los servicios web Aspose.Cells utilizando varios SDK:

{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_MergeRemoteSpreadsheet.cs" >}}
{{< /tab >}}
{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_MergeRemoteSpreadsheet.java" >}}
{{< /tab >}}
{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_MergeRemoteSpreadsheet.php" >}}
{{< /tab >}}
{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_MergeRemoteSpreadsheet.rb" >}}
{{< /tab >}}
{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_MergeRemoteSpreadsheet.ts" >}}
{{< /tab >}}
{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_MergeRemoteSpreadsheet.py" >}}
{{< /tab >}}
{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_MergeRemoteSpreadsheet.pl" >}}
{{< /tab >}}
{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_MergeRemoteSpreadsheet.go" >}}
{{< /tab >}}
{{< /tabs >}}
