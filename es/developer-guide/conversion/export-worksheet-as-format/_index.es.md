---
title: Aspose.Cells Cloud Web API - Exportar una hoja de cálculo como un archivo de formato
second_title: Documen
ArticleTitle: Export a Spreadsheet Worksheet as a Format fil
linktitle: Hoja de trabajo de exportación
type: docs
url: /es/export-worksheet-as-format/
keywords: Export worksheet, Cloud storage conversion, File format transformation, API for spreadsheet
description: Convierte de manera eficiente una hoja de cálculo del almacenamiento en la nube a varios formatos como PDF, CSV e imágenes.
weight: 100
kwords: Exportar hoja de cálculo, Conversión a la nube, PDF, Formatos de imagen, Excel, REST API, CSV, JSON, Markdown, Manejo de celdas en blanco en Excel
---
Exporte una hoja de cálculo en la nube/Excel a un archivo de otro formato con Aspose.Cells Cloud Web API.

## **Exportar hoja de cálculo como formato API**

```http
GET http://api.aspose.cloud/v4.0/cells/{name}/worksheets/{worksheet}
```

### **Parámetros de la solicitud:**

| Nombre del parámetro| Tipo| Ruta/Cadena de consulta/HTTPBody| Descripción|
|:- |:- |:- |:- |
|nombre|Cadena|Camino|(Obligatorio) El nombre del archivo del libro de trabajo que se recuperará.|
|hoja de trabajo|Cadena|Camino|(Obligatorio) La hoja de trabajo específica a convertir.|
|formato|Cadena|Consulta|(Obligatorio) El formato de salida deseado (por ejemplo, "png", "pdf", "svg").|
|carpeta|Cadena|Consulta|(Opcional) La ruta de la carpeta donde se almacena el libro. El valor predeterminado es nulo.|
|nombreDeAlmacenamiento|Cadena|Consulta|(Opcional) El nombre del almacenamiento en la nube personalizado. Si se omite, utilice el almacenamiento predeterminado.|
|Ruta de salida|Cadena|Consulta|(Opcional) Ruta de la carpeta de salida. El valor predeterminado es nulo.|
|nombreAlmacenamientoExterno|Cadena|Consulta|(Opcional) Nombre de almacenamiento del archivo de salida.|
|Ubicación de fuentes|Cadena|Consulta|(Opcional) Especifique fuentes personalizadas si es necesario.|
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

## ¿Por qué debería utilizar la hoja de cálculo de exportación como formato API?

- Puede convertir archivos en la nube a diferentes formatos en cualquier momento y en cualquier lugar.
- El desarrollo se puede completar rápidamente a través del SDK existente.

## ¿Cómo utilizar la hoja de cálculo de exportación como formato API con SDK?

### Exportar hoja de cálculo como formato API Especificación

 El[Exportar hoja de cálculo como formato API Especificación](https://reference.aspose.cloud/cells/#/ConversionController/ExportWorksheetAsFormat) Proporciona una interfaz de programación de acceso público para realizar interacciones REST directamente desde un navegador web.

### Utilice los SDK de la nube Aspose.Cells

Usar el SDK es la forma más rápida de desarrollar, ya que abstrae los detalles de bajo nivel y permite exportar una hoja de cálculo a un archivo de formato con código corto.
 Por favor, consulte el[Repositorio de GitHub](https://github.com/aspose-cells-cloud) para obtener una lista completa de Aspose.Cells SDK en la nube.

Los siguientes ejemplos de código demuestran cómo realizar llamadas a los servicios web Aspose.Cells utilizando varios SDK:

{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_ExportWorksheetAsFormat.cs" >}}
{{< /tab >}}
{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_ExportWorksheetAsFormat.java" >}}
{{< /tab >}}
{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_ExportWorksheetAsFormat.php" >}}
{{< /tab >}}
{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_ExportWorksheetAsFormat.rb" >}}
{{< /tab >}}
{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_ExportWorksheetAsFormat.ts" >}}
{{< /tab >}}
{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_ExportWorksheetAsFormat.py" >}}
{{< /tab >}}
{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_ExportWorksheetAsFormat.pl" >}}
{{< /tab >}}
{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_ExportWorksheetAsFormat.go" >}}
{{< /tab >}}
{{< /tabs >}}
