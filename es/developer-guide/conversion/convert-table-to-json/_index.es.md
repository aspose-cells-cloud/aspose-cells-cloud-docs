---
title: Aspose.Cells Cloud Web API - Convertir los datos de una tabla de hoja de cálculo a un archivo JSON
second_title: Documen
ArticleTitle: Convert a Spreadsheet Table data to a Json file
linktitle: Convertir tabla a JSO
type: docs
url: /es/convert-table-to-json/
keywords: Excel API, JSON conversion, spreadsheet to JSON, cloud file conversion, REST API, Aspose.Cell
description: Convierta una tabla de hoja de cálculo local a formato JSON de manera eficiente usando Excel API. Este método permite un procesamiento de archivos sin problemas, sin necesidad de almacenamiento en la nube.
weight: 100
kwords: Excel API, conversión JSON, conversión de archivos en la nube, hoja de cálculo, REST API, Aspose.Cells, procesamiento de unidad local, conversión de formato de archivo
---
Convierta una tabla de hoja de cálculo local/Excel a un archivo json con Aspose.Cells Cloud Web API.

## **Convertir tabla a JSON API**

```http
PUT http://api.aspose.cloud/v4.0/cells/convert/table/json
```

### **Parámetros de la solicitud:**

| Nombre del parámetro| Tipo| Ruta/Cadena de consulta/Cuerpo HTTP| Descripción|
|-------------|-|-----------------------|----------------------------------------------|
| Hoja de cálculo| Archivo| Datos del formulario| Sube el archivo de hoja de cálculo.|
| hoja de trabajo|Cadena| Consulta| Especifique el nombre de la hoja de cálculo.|
| nombre de la tabla|Cadena| Consulta| Proporcione el nombre de la tabla a convertir.|
| Ruta de salida|Cadena| Consulta| (Opcional) La ruta de la carpeta donde se almacena el libro de trabajo; el valor predeterminado es nulo.|
| nombreAlmacenamientoExterno|Cadena| Consulta| Especifique el nombre de almacenamiento del archivo de salida.|
| Ubicación de fuentes|Cadena| Consulta| Utilice fuentes personalizadas para la conversión.|
| región|Cadena| Consulta|Define la configuración regional para la hoja de cálculo.|
| contraseña|Cadena| Consulta| La contraseña necesaria para abrir el archivo de hoja de cálculo.|

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

## ¿Por qué debería utilizar la función Convertir tabla a Json API?

- No necesita almacenamiento en la nube, lo que reduce la carga sobre los recursos de la nube.
- El desarrollo se puede completar rápidamente a través del SDK existente.

## ¿Cómo utilizar la tabla de conversión a Json API con SDK?

### Especificación API para convertir tablas a JSON

 El[Especificación API para convertir tablas a JSON](https://reference.aspose.cloud/cells/#/ConversionController/ConvertTableToJson) Proporciona una interfaz de programación de acceso público, que permite interacciones REST directamente desde un navegador web.

### Utilice los SDK de la nube Aspose.Cells

Usar el SDK es la forma más rápida de desarrollar, ya que abstrae los detalles de bajo nivel y le permite convertir los datos de una tabla de una hoja de cálculo en un archivo json con código corto.
 Por favor, consulte el[Repositorio de GitHub](https://github.com/aspose-cells-cloud) para obtener una lista completa de Aspose.Cells SDK en la nube.

Los siguientes ejemplos de código demuestran cómo interactuar con los servicios web Aspose.Cells utilizando varios SDK:
{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_ConvertTableToJson.cs" >}}
{{< /tab >}}
{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_ConvertTableToJson.java" >}}
{{< /tab >}}
{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_ConvertTableToJson.php" >}}
{{< /tab >}}
{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_ConvertTableToJson.rb" >}}
{{< /tab >}}
{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_ConvertTableToJson.ts" >}}
{{< /tab >}}
{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_ConvertTableToJson.py" >}}
{{< /tab >}}
{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_ConvertTableToJson.pl" >}}
{{< /tab >}}
{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_ConvertTableToJson.go" >}}
{{< /tab >}}
{{< /tabs >}}
