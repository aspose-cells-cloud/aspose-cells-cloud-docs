---
title: Aspose.Cells Cloud Web API - Suma, recuento, valor promedio, etc. por color en hoja de cálculo/Exce
second_title: Documen
ArticleTitle: Sum, Count, Average Value, etc by color in Spreadsheet/Exce
LinkTitle: Aggregate Cells by Colo
type: docs
url: /es/aggregate-cells-by-color/
keywords: Sum, Count, Average Value, Max Value, Min Value, Excel REST API, Spreadsheet Operations, Aspose.Cells, Excel Cloud AP
description: La nube web Aspose.Cells Cloud Web API (Excel Cloud API) puede realizar cálculos de datos, sumas y promedios, y también puede encontrar los valores máximos y mínimos en una hoja de cálculo Excel según el relleno o el color de fuente de las celdas.
weight: 100
kwords: Suma, Conteo, Valor promedio, Valor máximo, Valor mínimo, Excel REST API, Operaciones de hoja de cálculo, Aspose.Cells, Excel Nube API
---
El API puede realizar cálculos de datos, sumas y promedios, y también puede encontrar los valores máximos y mínimos en una hoja de cálculo Excel según el relleno o el color de fuente de las celdas.

| Calcular operación| Descripción|
|:- |:- |
| Contar| Determinar el número de celdas con el mismo color.|
| Suma| Calcula el valor total de celdas con el mismo color.|
| Valor máximo| Identifica el valor más alto entre las celdas con el mismo color.|
| Valor mínimo| Encuentra el valor más bajo entre las celdas con el mismo color.|
|Valor promedio| Calcular el valor medio de las celdas con el mismo color.|

## **Agregando Cells por Color API**

```http
PUT http://api.aspose.cloud/v4.0/cells/calculate/aggregate/color
```

### **Parámetros de la solicitud:**

| Nombre del parámetro| Tipo| Ruta/Cadena de consulta/HTTPBody| Descripción|
|:- |:- |:- |:- |
| Hoja de cálculo| Archivo| Datos del formulario| Subir archivo de hoja de cálculo.|
| Hoja de trabajo| Cadena| Consulta| Especifica la hoja de trabajo.|
| Rango| Cadena| Consulta| Especifica el rango.|
| Operación| Cadena| Consulta| Especifique los métodos de operación de cálculo, incluidos Suma, Conteo, Promedio, Mínimo y Máximo.|
| Posición del color| Cadena| Consulta| Indica el contenido a sumar y contar según el color de fondo y/o el color de fuente.|
| Región| Cadena| Consulta| La configuración de la región de la hoja de cálculo.|
| Contraseña| Cadena| Consulta| La contraseña para abrir el archivo de hoja de cálculo.|

### **Respuesta**

```json
{
  "Name": "AggregateResultByColorResponse",
  "Type": "Class",
  "ParentName": "CellsCloudResponse",
  "IsAbstract": false,
  "Properties": [
    {
      "Name": "AggregateResults",
      "DataType": {
        "Identifier": "Array",
        "Reference": "AggregateResultByColor",
        "ElementDataType": {
          "Reference": "AggregateResultByColor"
        }
      }
    },
    {
      "Name": "Code",
      "DataType": {
        "Identifier": "Integer",
      }
    },
    {
      "Name": "Status",
      "DataType": {
        "Identifier": "String",
      }
    }
  ]
}
```

### Códigos de error

- **400 Solicitud incorrecta**: URI de nube Apose.Cells no válido API.
- **401 No autorizado**Token de acceso no válido. O ID de cliente y secreto no válidos.
- **404 No encontrado**:El archivo de hoja de cálculo no es accesible.
- **Error de servidor 500**:La hoja de cálculo ha encontrado una anomalía al obtener los datos de cálculo.

## ¿Donde debemos utilizar el Agregado por Color API?

En una hoja de cálculo, los datos de diferentes categorías se muestran en diferentes colores, lo que permite realizar operaciones como sumar, contar, calcular promedios y encontrar valores máximos y mínimos según el color.

## ¿Por qué debería utilizar el Agregado por Color API?

- Proporcionar métodos para el análisis de datos de color.
- Clasifique y calcule datos según el color para proporcionar datos fundamentales para el análisis de datos.
- El desarrollo se puede completar rápidamente a través del SDK existente.

## Cómo usar la función Agregado por color API con SDK

### Agregado por color API Especificación

 El[Agregado por color API Especificación](https://reference.aspose.cloud/cells/#/CalculateController/AggregateCellsByColor) define una interfaz de programación de acceso público y le permite realizar interacciones REST directamente desde un navegador web.

### Utilice los SDK de la nube Aspose.Cells

Usar el SDK es la forma más rápida de desarrollar, ya que abstrae los detalles de bajo nivel y permite agregar cálculos por color de celda con solo un pequeño fragmento de código.
 Por favor, consulte el[Repositorio de GitHub](https://github.com/aspose-cells-cloud) para obtener una lista completa de Aspose.Cells SDK en la nube.

Los siguientes ejemplos de código demuestran cómo realizar llamadas a los servicios web Aspose.Cells utilizando varios SDK:

{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_AggregateCellsByColor.cs" >}}
{{< /tab >}}
{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_AggregateCellsByColor.java" >}}
{{< /tab >}}
{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_AggregateCellsByColor.php" >}}
{{< /tab >}}
{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_AggregateCellsByColor.rb" >}}
{{< /tab >}}
{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_AggregateCellsByColor.ts" >}}
{{< /tab >}}
{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_AggregateCellsByColor.py" >}}
{{< /tab >}}
{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_AggregateCellsByColor.pl" >}}
{{< /tab >}}
{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_AggregateCellsByColor.go" >}}
{{< /tab >}}
{{< /tabs >}}
