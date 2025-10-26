---
title: Aspose.Cells Cloud Web API - Intercambio de rango en hoja de cálculo
second_title: Documen
ArticleTitle: Swap Range Data in a Spreadshee
linktitle: Intercambio de rango
type: docs
url: /es/swap-range/
keywords: Aspose.Cells Cloud Web API, Swap Ranges, Office Cloud, RES
description: La función Intercambiar rangos para Excel API proporciona una potente herramienta para intercambiar dos columnas, filas, rangos o celdas individuales dentro de un archivo Excel. Esta función API permite a los usuarios reorganizar sus tablas de forma eficiente, garantizando que se conserve el formato original de los datos y que todas las fórmulas existentes sigan funcionando correctamente. Al aprovechar esta función API, los usuarios pueden optimizar sus tareas de manipulación de datos y mantener la integridad de sus hojas de cálculo.
weight: 100
kwords: Excel, Office Nube, REST, PDF, CSV, Json, Markdown
---
Intercambiar datos entre dos columnas, filas, rangos o celdas individuales en un archivo Excel.

## **Rango de intercambio API**

```http
PUT http://api.aspose.cloud/v4.0/cells/swap/range
```

### **Parámetros de la solicitud:**

| Nombre del parámetro| Tipo| Ruta/Cadena de consulta/HTTPBody| Descripción|
|:- |:- |:- |:- |
|Hoja de cálculo|Archivo|Datos del formulario|Sube el archivo de hoja de cálculo.|
|hoja de trabajo1|Cadena|Consulta|Especifique la hoja de trabajo que es la fuente del área de datos de intercambio.|
|rango1|Cadena|Consulta|Especifique la fuente de los datos de intercambio.|
|hoja de trabajo2|Cadena|Consulta|Especifique la hoja de trabajo que es el destino del área de datos de intercambio.|
|rango2|Cadena|Consulta|Especifique el destino de los datos de intercambio.|
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

## ¿Dónde debemos utilizar el rango Swap API?

Cuando necesite intercambiar datos de rango en una hoja de cálculo, puede utilizar este API.

## ¿Por qué debería utilizar el rango Swap API?

- Intercambie rápidamente datos de rango en una hoja de cálculo Excel.
- El desarrollo se puede completar rápidamente a través del SDK existente.

## Cómo utilizar el rango de intercambio API con SDK

### Especificación del rango de intercambio API

 El[Especificación del rango de intercambio API](https://reference.aspose.cloud/cells/#/TransformController/SwapRange) define una interfaz de programación de acceso público y le permite realizar interacciones REST directamente desde un navegador web.

### Utilice los SDK de la nube Aspose.Cells

Usar el SDK es la forma más rápida de desarrollar, ya que abstrae los detalles de bajo nivel y permite intercambiar rangos con código corto.
 Por favor, consulte el[Repositorio de GitHub](https://github.com/aspose-cells-cloud) para obtener una lista completa de Aspose.Cells SDK en la nube.

Los siguientes ejemplos de código demuestran cómo realizar llamadas a los servicios web Aspose.Cells utilizando varios SDK:

{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_SwapRange.cs" >}}
{{< /tab >}}
{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_SwapRange.java" >}}
{{< /tab >}}
{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_SwapRange.php" >}}
{{< /tab >}}
{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_SwapRange.rb" >}}
{{< /tab >}}
{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_SwapRange.ts" >}}
{{< /tab >}}
{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_SwapRange.py" >}}
{{< /tab >}}
{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_SwapRange.pl" >}}
{{< /tab >}}
{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_SwapRange.go" >}}
{{< /tab >}}
{{< /tabs >}}
