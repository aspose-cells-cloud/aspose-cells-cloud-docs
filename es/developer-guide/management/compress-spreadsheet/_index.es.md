---
title: Aspose.Cells Cloud Web API - Comprimir el tamaño de la hoja de cálculo
second_title: Documen
ArticleTitle: Compress the size of the Spreadshee
linktitle: Comprimir hoja de cálculo
type: docs
url: /es/compress-spreadsheet/
keywords: Spreadsheet Compression, Reduce File Size, Aspose.Cells Cloud Web AP
description: La herramienta Compress Spreadsheet API permite a los usuarios reducir de manera eficiente el tamaño de los archivos de hojas de cálculo aplicando niveles de compresión específicos, optimizando el almacenamiento y mejorando el rendimiento.
weight: 100
kwords: Excel, Office Nube, REST, Compresión de hojas de cálculo, Optimización del tamaño de archivo, PDF, CSV, JSON, Markdow
---
Comprimir el tamaño de la hoja de cálculo.

## **Comprimir hoja de cálculo API**

```http
PUT http://api.aspose.cloud/v4.0/cells/spreadsheet/compress
```

### **Parámetros de la solicitud:**

| Nombre del parámetro| Tipo| Ruta/Cadena de consulta/Cuerpo HTTP| Descripción|
|:- |:- |:- |:- |
|Hoja de cálculo|Archivo|Datos del formulario|Sube el archivo de hoja de cálculo que desea comprimir.|
|nivel|Entero|Consulta|Especifica el nivel de compresión que se aplicará, desde 0 (sin compresión) a 9 (compresión máxima).|
|Ruta de salida|Cadena|Consulta|(Opcional) Ruta de la carpeta donde se almacenará el libro comprimido. El valor predeterminado es nulo.|
|nombreAlmacenamientoExterno|Cadena|Consulta|Nombre de almacenamiento del archivo de salida.|
|región|Cadena|Consulta|La configuración de la región de la hoja de cálculo.|
|contraseña|Cadena|Consulta|La contraseña necesaria para abrir el archivo de hoja de cálculo.|

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

## ¿Dónde debemos utilizar la hoja de cálculo Compress API?

Cuando necesite reducir el tamaño de las hojas de cálculo, puede utilizar este API.

## ¿Por qué debería utilizar la hoja de cálculo Compress API?

- La hoja de cálculo es demasiado grande y es necesario reducir el tamaño del archivo.
- El desarrollo se puede completar rápidamente a través del SDK existente.

## Cómo usar la hoja de cálculo Comprimir API con SDK

### Especificación de la hoja de cálculo Comprimir API

 El[Especificación de la hoja de cálculo Comprimir API](https://reference.aspose.cloud/cells/#/ManagementController/CompressSpreadsheet) Proporciona una interfaz de acceso público para interacciones REST, permitiendo llamadas directas al API desde un navegador web.

### Utilice los SDK de la nube Aspose.Cells

Usar el SDK es la forma más rápida de desarrollar, ya que abstrae los detalles de bajo nivel y permite comprimir el tamaño de la hoja de cálculo con código corto.
 Por favor, consulte el[Repositorio de GitHub](https://github.com/aspose-cells-cloud) para obtener una lista completa de Aspose.Cells SDK en la nube.

Los siguientes ejemplos de código demuestran cómo interactuar con los servicios web Aspose.Cells utilizando varios SDK:

{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_CompressSpreadsheet.cs" >}}
{{< /tab >}}
{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_CompressSpreadsheet.java" >}}
{{< /tab >}}
{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_CompressSpreadsheet.php" >}}
{{< /tab >}}
{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_CompressSpreadsheet.rb" >}}
{{< /tab >}}
{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_CompressSpreadsheet.ts" >}}
{{< /tab >}}
{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_CompressSpreadsheet.py" >}}
{{< /tab >}}
{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_CompressSpreadsheet.pl" >}}
{{< /tab >}}
{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_CompressSpreadsheet.go" >}}
{{< /tab >}}
{{< /tabs >}}
