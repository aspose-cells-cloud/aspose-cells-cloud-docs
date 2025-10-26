---
title: Aspose.Cells Cloud Webb API - Agregar una hoja de trabajo a una hoja de cálculo
second_title: Documen
ArticleTitle: Add a Worksheet to a Spreadshee
linktitle: Agregar hoja de trabajo a la hoja de cálculo
type: docs
url: /es/add-worksheet-to-spreadsheet/
keywords: Aspose.Cells Cloud Web API, Add Worksheet, Spreadsheet Management, RES
description: La versión Aspose.Cells de Cloud Web API permite a los desarrolladores añadir eficientemente una nueva hoja de cálculo a un libro, lo que permite controlar su tipo, posición y nombre. Esta funcionalidad mejora la gestión y la flexibilidad del libro.
weight: 100
kwords: Excel, Office Nube, REST, Hoja de cálculo, PDF, CSV, JSON, Markdown, Administrar Excel Hojas de trabajo, Creación dinámica de hojas de cálculo
---
Agregar una hoja de trabajo a la hoja de cálculo, especificando el tipo y la ubicación de la hoja de trabajo.

|**Tipo de hoja de trabajo** | Descripción|
|:- |:- |
|**VB** | Módulo de Visual Basic|
|**Hoja de trabajo** | Hoja de trabajo|
|**Cuadro** | Hoja de gráficos|
|**BIFF4Macro** | Hoja de macros BIFF4|
|**Macro internacional** | Hoja macroeconómica internacional|
|**Otro** | Hoja macroeconómica internacional|
|**Diálogo** | Hoja de trabajo de diálogo|

## **Agregar hoja de trabajo a hoja de cálculo API**

```http
PUT http://api.aspose.cloud/v4.0/cells/spreadsheet/add/worksheet
```

### **Parámetros de la solicitud:**

| Nombre del parámetro| Tipo| Ruta/Cadena de consulta/HTTPBody| Descripción|
|:- |:- |:- |:- |
|Hoja de cálculo|Archivo|Datos del formulario|Subir archivo de hoja de cálculo.|
|tipo de hoja|Cadena|Consulta|Especifica el nombre de la nueva hoja de cálculo. Si no se proporciona, se asignará un nombre predeterminado.|
|posición|Entero|Consulta|Especifica la posición donde se debe insertar la nueva hoja de cálculo. Si no se proporciona, la hoja de cálculo se añadirá al final del libro.|
|nombreHoja|Cadena|Consulta|Especifica el tipo de hoja de cálculo que se agregará. Si no se proporciona, se utilizará un tipo de hoja de cálculo predeterminado.|
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

## ¿Dónde debemos utilizar la función Agregar hoja de trabajo a la hoja de cálculo API?

Cuando necesite agregar una hoja de trabajo para una hoja de cálculo, puede utilizar este API.

## ¿Por qué debería utilizar la opción Agregar hoja de trabajo a la hoja de cálculo API?

- Agregue una hoja de trabajo a la hoja de cálculo, especificando el tipo y la ubicación de la hoja de trabajo.
- El desarrollo se puede completar rápidamente a través del SDK existente.

## Cómo usar la función Agregar hoja de cálculo a hoja de cálculo API con SDK

### Agregar hoja de trabajo a la hoja de cálculo API Especificación

 El[Agregar hoja de trabajo a la hoja de cálculo API Especificación](https://reference.aspose.cloud/cells/#/ManagementController/AddWorksheetToSpreadsheet) define una interfaz de programación de acceso público y le permite realizar interacciones REST directamente desde un navegador web.

### Utilice los SDK de la nube Aspose.Cells

Usar el SDK es la forma más rápida de desarrollar, ya que abstrae los detalles de bajo nivel y permite agregar una hoja de trabajo a una hoja de cálculo con código corto.
 Por favor, consulte el[Repositorio de GitHub](https://github.com/aspose-cells-cloud) para obtener una lista completa de Aspose.Cells SDK en la nube.

Los siguientes ejemplos de código demuestran cómo realizar llamadas API a servicios web Aspose.Cells utilizando varios SDK:

{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_AddWorksheet.cs" >}}
{{< /tab >}}
{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_AddWorksheet.java" >}}
{{< /tab >}}
{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_AddWorksheet.php" >}}
{{< /tab >}}
{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_AddWorksheet.rb" >}}
{{< /tab >}}
{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_AddWorksheet.ts" >}}
{{< /tab >}}
{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_AddWorksheet.py" >}}
{{< /tab >}}
{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_AddWorksheet.pl" >}}
{{< /tab >}}
{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_AddWorksheet.go" >}}
{{< /tab >}}
{{< /tabs >}}
