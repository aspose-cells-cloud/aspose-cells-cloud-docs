---
title: Aspose.Cells Cloud Web API - Desproteger hoja de cálculo con contraseña
second_title: Documen
ArticleTitle: Unprotect the Spreadsheet with passwor
linktitle: Desproteger la hoja de cálculo
type: docs
url: /es/unprotect-spreadsheet/
keywords: Excel API, Unprotect Spreadsheet, Password Removal, Encryption, Office Cloud, REST API, Spreadsheet Security, Excel File Managemen
description: Elimina de forma eficiente la protección de contraseña de doble capa de las hojas de cálculo Excel, admitiendo tanto la apertura como la modificación de contraseñas con técnicas de cifrado avanzadas.
weight: 100
kwords: Excel, Office Nube, REST API, Hoja de cálculo, PDF, CSV, JSON, Markdown, Coincidir con todas las celdas en blanco en una hoja de cálculo Excel
---
Aplica la protección de Excel hojas de cálculo con contraseña, admitiendo tanto la apertura como la modificación de contraseñas.

## **Desproteger hoja de cálculo API**

```http
PUT http://api.aspose.cloud/v4.0/cells/unprotection/spreadsheet
```

### **Parámetros de la solicitud:**

| Nombre del parámetro| Tipo| Ruta/Cadena de consulta/Cuerpo HTTP| Descripción|
|:- |:- |:- |:- |
|Hoja de cálculo|Archivo|Datos del formulario|Sube el archivo de hoja de cálculo que desea desproteger.|
|contraseña|Cadena|Consulta|La contraseña de cifrado para el archivo de hoja de cálculo.|
|modificarContraseña|Cadena|Consulta|La contraseña necesaria para modificar el archivo protegido.|
|Ruta de salida|Cadena|Consulta|(Opcional) Ruta de la carpeta donde se almacenará el libro desprotegido. El valor predeterminado es nulo.|
|nombreAlmacenamientoExterno|Cadena|Consulta|Especifica el nombre de almacenamiento del archivo de salida.|
|región|Cadena|Consulta|Define la configuración de la región de la hoja de cálculo.|

### **Respuesta**

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

## ¿Dónde debemos utilizar la función Eliminar columnas en blanco de la hoja de cálculo API?

Cuando necesites transformar datos, puedes utilizar este API.

## ¿Por qué debería utilizar la función Eliminar columnas en blanco de la hoja de cálculo API?

- Elimine rápidamente todas las columnas en blanco que no contengan datos u otros objetos de una hoja de cálculo Excel.
- El desarrollo se puede completar rápidamente a través del SDK existente.

## Cómo usar la función Eliminar columnas en blanco de la hoja de cálculo API con SDK

### Especificación OpenAPI

 El[Especificación OpenAPI](https://reference.aspose.cloud/cells/#/ProtectionController/UnprotectSpreadsheet) define una interfaz de programación de acceso público que le permite realizar interacciones REST directamente desde un navegador web.

### Utilice los SDK de la nube Aspose.Cells

Usar el SDK es la mejor manera de acelerar el desarrollo. El SDK gestiona los detalles subyacentes, lo que permite implementar fácilmente la eliminación de columnas en blanco en las celdas de las hojas de cálculo con un mínimo de código.
 Por favor, consulte el[Repositorio de GitHub](https://github.com/aspose-cells-cloud) para obtener una lista completa de Aspose.Cells SDK en la nube.

Los siguientes ejemplos de código ilustran cómo llamar a los servicios web Aspose.Cells utilizando varios SDK:

{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_UnprotectSpreadsheet.cs" >}}
{{< /tab >}}
{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_UnprotectSpreadsheet.java" >}}
{{< /tab >}}
{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_UnprotectSpreadsheet.php" >}}
{{< /tab >}}
{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_UnprotectSpreadsheet.rb" >}}
{{< /tab >}}
{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_UnprotectSpreadsheet.ts" >}}
{{< /tab >}}
{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_UnprotectSpreadsheet.py" >}}
{{< /tab >}}
{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_UnprotectSpreadsheet.pl" >}}
{{< /tab >}}
{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_UnprotectSpreadsheet.go" >}}
{{< /tab >}}
{{< /tabs >}}
