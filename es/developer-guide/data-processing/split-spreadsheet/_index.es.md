---
title: Aspose.Cells Cloud WEb API - Dividir la hoja de cálculo en archivos separados
second_title: Documen
ArticleTitle: Split the Spreadsheet into separate files
linktitle: Hoja de cálculo dividida
type: docs
url: /es/split-spreadsheet/
keywords: Excel API, Split Spreadsheet, Spreadsheet Management, Cloud Processing, File Formats, REST API, XLSX, CSV, PDF, JSON, Markdow
description: Divida una hoja de cálculo local en varios archivos en varios formatos sin necesidad de almacenamiento en la nube
weight: 100
kwords: Excel API, Office Nube, REST API, Hoja de cálculo, PDF, CSV, JSON, Markdown, Hoja de cálculo local dividida, Procesamiento en la nube, Gestión de archivos, Manejo de errores
---
Divida la hoja de cálculo local en archivos separados con 30 formatos de archivos de salida sin necesidad de almacenamiento en la nube.

## **Hoja de cálculo dividida API**

```http
PUT http://api.aspose.cloud/v4.0/cells/split/spreadsheet
```

### **Parámetros de la solicitud:**

| Nombre del parámetro| Tipo| Ruta/Cadena de consulta/HTTPBody| Descripción|
|:- |:- |:- |:- |
| Hoja de cálculo| Archivo| Datos del formulario| Sube el archivo de hoja de cálculo que deseas dividir.|
| de| Entero| Consulta| Especifique el índice de la hoja de trabajo inicial.|
| a| Entero| Consulta| Especifique el índice de la hoja de trabajo final.|
| formato de salida| Cadena| Consulta| Define el formato del archivo de salida.|
| Ruta de salida| Cadena| Consulta| (Opcional) Ruta de la carpeta donde se almacena el libro de salida. El valor predeterminado es nulo.|
|nombreAlmacenamientoExterno| Cadena| Consulta| Define el nombre de almacenamiento del archivo de salida.|
| Ubicación de fuentes| Cadena| Consulta| Especifique fuentes personalizadas si es necesario.|
| regresar| Cadena| Consulta| Establecer la región de la hoja de cálculo.|
| contraseña| Cadena| Consulta| Proporcione la contraseña para acceder al archivo de hoja de cálculo.|

## **Respuesta**

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

## ¿Dónde debemos utilizar la hoja de cálculo dividida API?

Cuando necesite dividir una hoja de cálculo en más archivos, puede utilizar este API.

## ¿Por qué debería utilizar la hoja de cálculo dividida API?

- No necesita espacio de almacenamiento en la nube, solo divídalo directamente.
- El desarrollo se puede completar rápidamente a través del SDK existente.

## Cómo utilizar la hoja de cálculo dividida API con SDK

### Especificación de la hoja de cálculo dividida API

 El[Especificación de la hoja de cálculo dividida API](https://reference.aspose.cloud/cells/#/DataProcessingController/SplitSpreadsheet) Proporciona una interfaz de programación de acceso público para realizar interacciones REST directamente desde un navegador web.

### Utilice los SDK de la nube Aspose.Cells

Usar el SDK es la forma más rápida de desarrollar, ya que abstrae los detalles de bajo nivel y permite dividir la hoja de cálculo en archivos separados con código corto.
 Por favor, consulte el[Repositorio de GitHub](https://github.com/aspose-cells-cloud) para obtener una lista completa de Aspose.Cells SDK en la nube.

Los siguientes ejemplos de código ilustran cómo invocar servicios web Aspose.Cells utilizando diferentes SDK:

{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_SplitLocalFile.cs" >}}
{{< /tab >}}
{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_SplitLocalFile.java" >}}
{{< /tab >}}
{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_SplitLocalFile.php" >}}
{{< /tab >}}
{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_SplitLocalFile.rb" >}}
{{< /tab >}}
{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_SplitLocalFile.ts" >}}
{{< /tab >}}
{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_SplitLocalFile.py" >}}
{{< /tab >}}
{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_SplitLocalFile.pl" >}}
{{< /tab >}}
{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_SplitLocalFile.go" >}}
{{< /tab >}}
{{< /tabs >}}
