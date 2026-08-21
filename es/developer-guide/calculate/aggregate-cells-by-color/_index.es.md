---
title: "Aspose.Cells Cloud Web API: Sumar y Contar por Color en Excel"
second_title: "Documento"
ArticleTitle: "Sumar, Contar, Promediar, Encontrar Valor Máximo y Mínimo por Color en Hoja de Cálculo/Excel"
LinkTitle: "Agrupar Celdas por Color"
type: docs
url: /es/aggregate-cells-by-color/
keywords: "Aspose, Cells, Excel, API, agrupar, color, sumar, contar, promediar, mínimo, máximo"
description: "Agrupe celdas de Excel por color de fondo o de fuente (sumar, contar, promediar, mínimo, máximo) utilizando la API en la nube de Aspose.Cells. Aprenda sobre el punto de conexión, los parámetros, la autenticación y ejemplos de SDK."
weight: 100
---

## Descripción general

La API puede realizar cálculos de datos basados en el **color** de las celdas. Permite sumar, contar, calcular promedios y también encontrar los valores máximo y mínimo en una hoja de cálculo de Excel según el color de relleno o de fuente de las celdas.

| Operación de cálculo | Descripción                                                  |
| :------------------ | :----------------------------------------------------------- |
| Contar              | Determina el número de celdas con el mismo color.          |
| Sumar               | Calcula el valor total de las celdas con el mismo color.   |
| Valor máximo        | Identifica el valor más alto entre las celdas con el mismo color. |
| Valor mínimo        | Encuentra el valor más bajo entre las celdas con el mismo color. |
| Valor promedio      | Calcula el valor medio de las celdas con el mismo color.   |

## API web

```http
PUT https://api.aspose.cloud/v4.0/cells/calculate/aggregate/color
```

### **Seguridad y autenticación**

Las API de Aspose.Cells Cloud son seguras y requieren <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">autenticación basada en token JWT</a>.

### Parámetros de la solicitud

| Nombre del parámetro | Tipo   | Ubicación | Descripción                                                      |
| :------------------- | :----- | :-------- | :--------------------------------------------------------------- |
| Spreadsheet          | File   | FormData  | El libro de Excel que se va a procesar.                         |
| Worksheet            | String | Query     | Nombre de la hoja de cálculo que contiene el rango.             |
| Range                | String | Query     | Rango en estilo A‑1 (por ejemplo, `A1:B10`).                    |
| Operation            | String | Query     | Método de cálculo: `Sum`, `Count`, `Average`, `Min` o `Max`.   |
| ColorPosition        | String | Query     | Determina qué color evaluar: `Background` (fondo) o `Font` (fuente). |
| Region               | String | Query     | Configuración de región de la hoja de cálculo (por ejemplo, `us-east-1`). |
| Password             | String | Query     | Contraseña para abrir un libro protegido (opcional).            |

#### Enumeraciones

- **ColorPosition**

  | Valor      | Significado                     |
  | :--------- | :------------------------------ |
  | Background | Usa el color de relleno de la celda. |
  | Font       | Usa el color de fuente de la celda. |

**Ejemplo de solicitud multipart/form‑data**

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/calculate/aggregate/color?Worksheet=Sheet1&Range=A1:B10&Operation=Sum&ColorPosition=Background" \
  -H "Authorization: Bearer <access_token>" \
  -F "Spreadsheet=@/path/to/workbook.xlsx"
```

### Respuesta

El esquema siguiente describe el objeto de respuesta. A continuación del esquema se muestra un ejemplo concreto.

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
      "DataType": { "Identifier": "Integer" }
    },
    {
      "Name": "Status",
      "DataType": { "Identifier": "String" }
    }
  ]
}
```

**Ejemplo de respuesta (valores reales)**

```json
{
  "Code": 200,
  "Status": "OK",
  "AggregateResults": [
    {
      "Color": "#FF0000",
      "Count": 12,
      "Sum": 345.67,
      "Average": 28.8,
      "Min": 5.0,
      "Max": 80.0
    },
    {
      "Color": "#00FF00",
      "Count": 7,
      "Sum": 210.0,
      "Average": 30.0,
      "Min": 10.0,
      "Max": 50.0
    }
  ]
}
```

**Códigos de estado HTTP**

| Código | Significado           | Descripción                                                       |
| ------ | --------------------- | ----------------------------------------------------------------- |
| 200    | OK                    | Filtro aplicado correctamente; la respuesta contiene detalles de la operación. |
| 400    | Solicitud incorrecta  | Parámetros faltantes o no válidos (por ejemplo, tipo de archivo no admitido). |
| 401    | No autorizado         | Token JWT inválido o faltante.                                    |
| 413    | Carga demasiado grande | El archivo subido supera el límite de tamaño.                    |
| 500    | Error interno del servidor | Error inesperado en el servidor.                                 |

## ¿Dónde debemos usar la API de Agrupación por Color?

En una hoja de cálculo, los datos de diferentes categorías suelen estar codificados por colores. Esta API le permite sumar, contar, promediar o encontrar los valores mínimo y máximo para cada grupo de colores, simplificando así el análisis de datos basado en color.

## ¿Por qué debería utilizar la API de Agrupación por Color?

La API proporciona una forma rápida y fiable de realizar cálculos basados en color sin tener que escribir lógica personalizada de análisis. Se integra perfectamente con los SDK de Aspose.Cells Cloud, lo que permite a los desarrolladores implementar la agrupación por color con tan solo unas pocas líneas de código.

## Cómo usar la API de Agrupación por Color con SDK

### Especificación de la API de Agrupación por Color

La <a href="https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Calculate/AggregateCellsByColor" rel="noopener noreferrer">especificación de la API de Agrupación por Color</a> define una interfaz de programación pública accesible y permite realizar interacciones REST directamente desde un navegador web.

### Utilizar los SDK de Aspose.Cells Cloud

Utilizar los SDK es la forma más rápida de desarrollar, ya que oculta los detalles de bajo nivel, permitiendo agrupar cálculos por color de celda con tan solo un fragmento breve de código.  
Consulte el <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">repositorio de GitHub</a> para obtener una lista completa de los SDK de Aspose.Cells Cloud.

Los siguientes ejemplos de código muestran cómo realizar llamadas a los servicios web de Aspose.Cells mediante diversos SDK:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_AggregateCellsByColor.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_AggregateCellsByColor.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_AggregateCellsByColor.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_AggregateCellsByColor.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_AggregateCellsByColor.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_AggregateCellsByColor.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_AggregateCellsByColor.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_AggregateCellsByColor.go" >}}
{{</tab>}}
{{< /tabs >}}

**Notas:**

- Al trabajar con libros protegidos, incluya el parámetro de consulta opcional `Password`; de lo contrario, la solicitud fallará con un error 401.
- El tamaño máximo de solicitud para el archivo `Spreadsheet` es de 100 MB. Si necesita procesar archivos más grandes, considere subir primero el libro al almacenamiento en la nube de Aspose Cloud y hacer referencia a él mediante el parámetro `Path` (no se muestra aquí).