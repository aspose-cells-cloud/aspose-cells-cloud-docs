---
title: Aspose.Cells Cloud Web API - Cambiar el nombre de la hoja de cálculo en la hoja de cálculo
second_title: Documen
ArticleTitle: Rename worksheet in Spreadshee
linktitle: Cambiar el nombre de la hoja de cálculo en la hoja de cálculo
type: docs
url: /es/rename-worksheet-in-spreadsheet/
keywords: Excel API, Rename Worksheet, Workbook Management, REST API, Spreadsheet Organizatio
description: El punto final Web API permite a los usuarios cambiar el nombre de una hoja de cálculo específica dentro de un libro, lo que mejora la organización y la legibilidad.
weight: 100
kwords: Excel API, Cambiar nombre de hoja de cálculo, Gestión de libros, REST API, Hoja de cálculo, PDF, CSV, JSON, Markdown, Coincidir con todas las celdas en blanco en una hoja de cálculo Excel
---
Cambiar el nombre de la hoja de trabajo en una hoja de cálculo.

## **Cambiar el nombre de la hoja de cálculo en la hoja de cálculo API**

```http
PUT http://api.aspose.cloud/v4.0/cells/spreadsheet/rename/worksheet
```

### **Parámetros de la solicitud:**

| Nombre del parámetro| Tipo| Ruta/Cadena de consulta/HTTPBody| Descripción|
|:- |:- |:- |:- |
|Hoja de cálculo|Archivo|Datos del formulario|Sube el archivo de hoja de cálculo.|
|nombreDeFuente|Cadena|Consulta|Nombre actual de la hoja de trabajo que se va a renombrar.|
|nombreDeObjetivo|Cadena|Consulta|Nuevo nombre para la hoja de trabajo.|
|Ruta de salida|Cadena|Consulta|(Opcional) Ruta de la carpeta donde se almacena el libro. El valor predeterminado es nulo.|
|nombreAlmacenamientoExterno|Cadena|Consulta|Nombre de almacenamiento del archivo de salida.|
|región|Cadena|Consulta|Configuración de la región de la hoja de cálculo.|
|contraseña|Cadena|Consulta|Contraseña para abrir el archivo de hoja de cálculo.|

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

## ¿Dónde debemos utilizar la hoja de trabajo Cambiar nombre en la hoja de cálculo API?

Cuando necesite cambiar el nombre de una hoja de trabajo en hojas de cálculo, puede utilizar este API.

## ¿Por qué debería utilizar la hoja de trabajo Cambiar nombre en la hoja de cálculo API?

- Cambie rápidamente el nombre de las hojas de trabajo desde las hojas de cálculo.
- El desarrollo se puede completar rápidamente a través del SDK existente.

## Cómo usar la hoja de cálculo "Cambiar nombre" en la hoja de cálculo API con SDK

### Especificación OpenAPI

 El[Especificación OpenAPI](https://reference.aspose.cloud/cells/#/ManagementController/RenameWorksheetInSpreadsheet)detalla una interfaz de programación de acceso público, que permite interacciones REST directamente desde un navegador web.

### Utilice los SDK de la nube Aspose.Cells

Usar el SDK es la mejor manera de acelerar el desarrollo. El SDK gestiona los detalles subyacentes, lo que permite implementar fácilmente el cambio de nombre de la hoja de cálculo para las celdas con un mínimo de código.
 Por favor, consulte el[Repositorio de GitHub](https://github.com/aspose-cells-cloud) para obtener una lista completa de Aspose.Cells SDK en la nube.

Los siguientes ejemplos de código ilustran cómo llamar a los servicios web Aspose.Cells utilizando varios SDK:

{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_RenameWorksheet.cs" >}}
{{< /tab >}}
{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_RenameWorksheet.java" >}}
{{< /tab >}}
{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_RenameWorksheet.php" >}}
{{< /tab >}}
{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_RenameWorksheet.rb" >}}
{{< /tab >}}
{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_RenameWorksheet.ts" >}}
{{< /tab >}}
{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_RenameWorksheet.py" >}}
{{< /tab >}}
{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_RenameWorksheet.pl" >}}
{{< /tab >}}
{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_RenameWorksheet.go" >}}
{{< /tab >}}
{{< /tabs >}}
