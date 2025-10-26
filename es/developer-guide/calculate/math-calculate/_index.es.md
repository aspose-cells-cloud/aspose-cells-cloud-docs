---
title: Aspose.Cells Cloud Web API - Sumar, Restar, Multiplicar, Dividir y Porcentaje en un rango de Hojas de Cálculo/Excel
second_title: Documen
ArticleTitle: Add, Minus, Multiply, Divide and Percentage in Spreadsheet/Exce
linktitle: Cálculo matemático
type: docs
url: /es/math-calculate/
keywords: Math calculation,Cloud REST API, Add, Minus, Multiply, Divide, Percentage, Office Cloud, Aspose.Cell
description: Guía completa para usar la función Math Calculate API para realizar cálculos en hojas de cálculo Excel
weight: 100
kwords: Cálculo matemático, Cloud REST API, Sumar, Restar, Multiplicar, Dividir, Porcentaje, Office Cloud, Aspose.Cells
---
Los desarrolladores pueden usar este API para realizar cálculos de suma, resta, multiplicación, división y porcentajes en rangos específicos de hojas de cálculo/Excel.

|**Calcular operación** | Descripción|
|:- |:- |
|**Agregar** |+ |
|**Menos** |-  |
|**Multiplicar** |*  |
|**Dividir** |/ |
|**Porcentaje** |% |

## **Calcular matemáticas API**

```http
PUT http://api.aspose.cloud/v4.0/cells/calculate/math
```

### **Parámetros de la solicitud:**

| Nombre del parámetro| Tipo| Ruta/Cadena de consulta/Cuerpo HTTP| Descripción|
|:- |:- |:- |:- |
| Hoja de cálculo| Archivo| Datos del formulario| Sube el archivo de hoja de cálculo para su procesamiento.|
| operación| Cadena| Consulta| La operación matemática a realizar (Suma, Resta, Multiplicación, División y Porcentaje).|
| valor| Cadena| Consulta| Un valor a utilizar en el cálculo, si corresponde.|
| hoja de trabajo| Cadena| Consulta| El nombre de la hoja de trabajo sobre la que se va a operar.|
| rango| Cadena| Consulta| El rango de celdas a incluir en el cálculo.|
| región| Cadena| Consulta|Define la región específica de la hoja de cálculo.|
| contraseña| Cadena| Consulta| La contraseña para abrir el archivo de hoja de cálculo, si está protegido.|

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

## ¿Dónde debemos utilizar el cálculo matemático API?

El cálculo matemático API es adecuado para cálculos por lotes en hojas de cálculo.

## ¿Por qué deberías utilizar el cálculo matemático API?

- Realizar cálculos matemáticos por lotes.
- El desarrollo se puede completar rápidamente a través del SDK existente.

## Cómo usar la función matemática Calculate API con SDK

### Especificación de cálculo matemático API

 El[Especificación de cálculo matemático](https://reference.aspose.cloud/cells/#/CalculateController/MathCalculate) define una interfaz de programación de acceso público, que permite a los desarrolladores interactuar con API directamente desde un navegador web.

### Utilice los SDK de la nube Aspose.Cells

Usar el SDK es la forma más rápida de desarrollar, ya que abstrae los detalles de bajo nivel y permite realizar cálculos matemáticos por celda con solo un código corto.
 Por favor, consulte el[Repositorio de GitHub](https://github.com/aspose-cells-cloud) para obtener una lista completa de Aspose.Cells SDK en la nube.

Los siguientes ejemplos de código demuestran cómo realizar llamadas a los servicios web Aspose.Cells utilizando varios SDK:

{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_MathCalculate.cs" >}}
{{< /tab >}}
{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_MathCalculate.java" >}}
{{< /tab >}}
{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_MathCalculate.php" >}}
{{< /tab >}}
{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_MathCalculate.rb" >}}
{{< /tab >}}
{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_MathCalculate.ts" >}}
{{< /tab >}}
{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_MathCalculate.py" >}}
{{< /tab >}}
{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_MathCalculate.pl" >}}
{{< /tab >}}
{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_MathCalculate.go" >}}
{{< /tab >}}
{{< /tabs >}}
