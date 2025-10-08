---
title: Aspose.Cells Cloud Web API - Fusionar archivos de hojas de cálculo coincidentes en un archivo en una carpeta remota
second_title: Documen
ArticleTitle: Merge matching spreadsheet files into a file in a remote Folder
linktitle: Fusionar hojas de cálculo en carpetas remotas
type: docs
url: /es/merge-spreadsheets-in-remote-folder/
keywords: Merge spreadsheets, cloud storage, Excel API, remote processing, spreadsheet formats, REST AP
description: Combine los archivos de hojas de cálculo almacenados en el almacenamiento en la nube en un solo archivo, y el formato de archivo admite 30 formatos de salida, como PDF, Csv, Json y otros formatos comunes.
weight: 100
kwords: Excel, Office Nube, REST API, Hoja de cálculo, PDF, CSV, JSON, Markdown, Combinar hojas de cálculo, Procesamiento en la nube, Manejo remoto de archivos
---
Fusiona archivos de hojas de cálculo coincidentes en archivos en una carpeta remota, el formato de archivo de salida admite más de 30 formatos como PDF, Csv, Json y otros formatos comunes.


## **Fusionar hojas de cálculo en una carpeta remota API**

```http
PUT http://api.aspose.cloud/v4.0/cells/merge/remote-spreadsheets
```

### **Parámetros de la solicitud:**

| Nombre del parámetro| Tipo| Ruta/Cadena de consulta/HTTPBody| Descripción|
|:- |:- |:- |:- |
| carpeta| Cadena| Consulta|La carpeta donde se almacenarán los archivos fusionados.|
| expresión de coincidencia de archivo| Cadena| Consulta| Expresión para hacer coincidir archivos para fusionar.|
| formato de salida| Cadena| Consulta| El formato de archivo de salida deseado.|
| fusionar en una hoja| Booleano| Consulta| Indica si se deben combinar todos los datos en una sola hoja de cálculo.|
| nombreDeAlmacenamiento| Cadena| Consulta| (Opcional) El nombre del almacenamiento en la nube personalizado; si se omite, el valor predeterminado es el almacenamiento predeterminado.|
| Ruta de salida| Cadena| Consulta| (Opcional) La ruta de la carpeta para almacenar el libro de trabajo; el valor predeterminado es nulo.|
|nombreAlmacenamientoExterno| Cadena| Consulta| El nombre del almacenamiento para el archivo de salida.|
| Ubicación de fuentes| Cadena| Consulta| Especifica fuentes personalizadas.|
| región| Cadena| Consulta| Establece la región de la hoja de cálculo.|
| contraseña| Cadena| Consulta| La contraseña para abrir el archivo de hoja de cálculo.|

## **Respuesta**

```json
[
    {
        "Name": "ResponseFile",
        "DataType": {
        "Identifier": "File",
        "Reference": "Stream",
        "Name": "file"
        }
    }
]
```

### Códigos de error

- **400 Solicitud incorrecta**: URI de nube Apose.Cells no válido API.
- **401 No autorizado**Token de acceso no válido. O ID de cliente y secreto no válidos.
- **404 No encontrado**:El archivo de hoja de cálculo no es accesible.
- **Error de servidor 500**:La hoja de cálculo ha encontrado una anomalía al obtener los datos de cálculo.

## ¿Dónde debemos utilizar la hoja de cálculo de combinación en la carpeta remota API?

Cuando necesite fusionar varios archivos de datos, puede utilizar este API.

## ¿Por qué debería utilizar la hoja de cálculo de combinación en la carpeta remota API?

- Los archivos de almacenamiento en la nube no necesitan descargarse y se pueden fusionar directamente en la nube.
- Fusiona por lotes varios archivos de hojas de cálculo. Admite expresiones coincidentes.
- El desarrollo se puede completar rápidamente a través del SDK existente.

## Cómo usar la hoja de cálculo de combinación en la carpeta remota API con SDK

### Combinar hoja de cálculo en carpeta remota API Especificación

 El[Combinar hoja de cálculo en carpeta remota API Especificación](https://reference.aspose.cloud/cells/#/DataProcessingController/MergeSpreadsheetsInRemoteFolder) Proporciona una interfaz de programación de acceso público que permite interacciones REST directamente desde un navegador web.

### Utilice los SDK de la nube Aspose.Cells

Usar el SDK es la forma más rápida de desarrollar, ya que abstrae los detalles de bajo nivel y permite fusionar archivos de hojas de cálculo coincidentes en archivos en una carpeta remota con código corto.
 Por favor, consulte el[Repositorio de GitHub](https://github.com/aspose-cells-cloud) para obtener una lista completa de Aspose.Cells SDK en la nube.

Los siguientes ejemplos de código ilustran cómo interactuar con los servicios web Aspose.Cells utilizando varios SDK:
{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_MergeSpreadsheetsInRemoteFolder.cs" >}}
{{< /tab >}}
{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_MergeSpreadsheetsInRemoteFolder.java" >}}
{{< /tab >}}
{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_MergeSpreadsheetsInRemoteFolder.php" >}}
{{< /tab >}}
{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_MergeSpreadsheetsInRemoteFolder.rb" >}}
{{< /tab >}}
{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_MergeSpreadsheetsInRemoteFolder.ts" >}}
{{< /tab >}}
{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_MergeSpreadsheetsInRemoteFolder.py" >}}
{{< /tab >}}
{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_MergeSpreadsheetsInRemoteFolder.pl" >}}
{{< /tab >}}
{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_MergeSpreadsheetsInRemoteFolder.go" >}}
{{< /tab >}}
{{< /tabs >}}
