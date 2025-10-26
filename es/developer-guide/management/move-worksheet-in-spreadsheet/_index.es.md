---
title: Aspose.Cells Cloud Web API - Mover una hoja de cálculo a una nueva posición en la hoja de cálculo
second_title: Documen
ArticleTitle: Move worksheet to new position in Spreadshee
linktitle: Mover hoja de trabajo en hoja de cálculo
type: docs
url: /es/move-worksheet-in-spreadsheet/
keywords: Move Worksheet, Aspose.Cells Cloud Web API, Spreadsheet Management, Worksheet Positioning, Workbook Organization, Excel AP
description: MoveWorksheet API permite a los usuarios reposicionar eficientemente una hoja de cálculo específica dentro de un libro, mejorando así la organización y accesibilidad de los datos de la hoja de cálculo.
weight: 100
kwords: Excel, Office Nube, REST API, Hoja de cálculo, Mover hoja de cálculo, Organización del libro de trabajo, PDF, CSV, JSON, Markdown
---
Mover una hoja de trabajo a una nueva posición en una hoja de cálculo.

## **Mover hoja de cálculo desde Hoja de cálculo API**

```http
PUT http://api.aspose.cloud/v4.0/cells/spreadsheet/move/worksheet
```

### **Parámetros de la solicitud:**

| Nombre del parámetro| Tipo| Ruta/Cadena de consulta/HTTPBody| Descripción|
|:- |:- |:- |:- |
|Hoja de cálculo|Archivo|Datos del formulario|Sube el archivo de hoja de cálculo.|
|hoja de trabajo|Cadena|Consulta|El nombre actual de la hoja de trabajo que se va a mover.|
|posición|Entero|Consulta|La nueva posición de la hoja de trabajo.|
|Ruta de salida|Cadena|Consulta|(Opcional) La ruta de la carpeta donde se almacena el libro. El valor predeterminado es nulo.|
|nombreAlmacenamientoExterno|Cadena|Consulta|Nombre de almacenamiento del archivo de salida.|
|región|Cadena|Consulta|La configuración de la región de la hoja de cálculo.|
|contraseña|Cadena|Consulta|La contraseña para abrir el archivo de hoja de cálculo.|

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

## ¿Dónde debemos utilizar la hoja de trabajo Mover en la hoja de cálculo API?

Cuando necesite mover una hoja de cálculo a una nueva posición en las hojas de cálculo, puede utilizar este API.

## ¿Por qué debería utilizar la hoja de trabajo Mover en la hoja de cálculo API?

- Mueva rápidamente hojas de trabajo desde hojas de cálculo.
- El desarrollo se puede completar rápidamente a través del SDK existente.

## Cómo usar la hoja de cálculo "Mover" en la hoja de cálculo API con SDK

### Mover hoja de trabajo en hoja de cálculo API Especificación

 El[Mover hoja de trabajo en hoja de cálculo API Especificación](https://reference.aspose.cloud/cells/#/ManagementController/MoveWorksheetInSpreadsheet) Proporciona una interfaz de programación de acceso público para facilitar interacciones REST directas desde un navegador web.

### Utilice los SDK de la nube Aspose.Cells

Usar el SDK es la forma más rápida de desarrollar, ya que abstrae los detalles de bajo nivel y permite mover la hoja de trabajo en la hoja de cálculo con un código corto.
 Por favor, consulte el[Repositorio de GitHub](https://github.com/aspose-cells-cloud) para obtener una lista completa de Aspose.Cells SDK en la nube.
Los siguientes ejemplos de código demuestran cómo llamar a los servicios web Aspose.Cells utilizando varios SDK:

{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_MoveWorksheet.cs" >}}
{{< /tab >}}
{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_MoveWorksheet.java" >}}
{{< /tab >}}
{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_MoveWorksheet.php" >}}
{{< /tab >}}
{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_MoveWorksheet.rb" >}}
{{< /tab >}}
{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_MoveWorksheet.ts" >}}
{{< /tab >}}
{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_MoveWorksheet.py" >}}
{{< /tab >}}
{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_MoveWorksheet.pl" >}}
{{< /tab >}}
{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_MoveWorksheet.go" >}}
{{< /tab >}}
{{< /tabs >}}
