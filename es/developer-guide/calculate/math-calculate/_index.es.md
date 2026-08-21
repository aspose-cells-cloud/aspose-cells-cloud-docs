---
title: "Aspose.Cells Cloud – API de cálculo matemático (Suma, Resta, Multiplicación, División, %)"
second_title: "Documento"
ArticleTitle: "Suma, Resta, Multiplicación, División y Porcentajes en hojas de cálculo/Excel"
linktype: "docs"
url: /math-calculate/
keywords: "API de cálculo matemático, Aspose.Cells Cloud, cálculos en Excel, suma, resta, multiplicación, división, porcentaje, procesamiento por lotes de Excel, API REST"
description: "Aprenda a utilizar la API de cálculo matemático de Aspose.Cells Cloud para aplicar por lotes operaciones de suma, resta, multiplicación, división o porcentaje a rangos en Excel. Incluye el formato de solicitud, código de ejemplo y manejo de errores."
weight: 100
---

## **Introducción**: Cálculo rápido en hojas de cálculo – Fórmulas de suma, multiplicación, resta, división y porcentaje en una única API en ejecución

_Elaborar cálculos por lotes en columnas, filas o tablas completas sin escribir fórmulas._

- **Matemáticas básicas**: sume, reste, multiplique o divida todas las celdas de un rango por cualquier número
- **Porcentajes**: aumente/disminuya según un %, o calcule el % de un número (por ejemplo, +15%, -8%, 20% de…)
- **Procesamiento por lotes**: aplique cambios instantáneamente a miles de celdas — sin relleno por arrastre, sin fórmulas matriciales ni VBA

| **Operación de cálculo** | Descripción |
| :---------------------- | :---------- |
| **Suma**                | +           |
| **Resta**               | -           |
| **Multiplicación**      | \*          |
| **División**            | /           |
| **Porcentaje**          | %           |

## **API de cálculo matemático**

```http
PUT https://api.aspose.cloud/v4.0/cells/calculate/math
```

### **Seguridad y autenticación**

Las API de Aspose.Cells Cloud son seguras y requieren <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">autenticación basada en token JWT</a>.

### **Parámetros de solicitud:**

| Nombre del parámetro | Tipo   | Ruta/cadena de consulta/cuerpo HTTP | Descripción                                                                                      |
| :------------------- | :----- | :---------------------------------- | :----------------------------------------------------------------------------------------------- |
| Spreadsheet (hoja de cálculo) | Archivo | FormData                            | Suba el archivo de hoja de cálculo para procesarlo.                                              |
| operation (operación) | Cadena | Consulta                            | La operación matemática a realizar (Suma, Resta, Multiplicación, División y Porcentaje).         |
| value (valor)        | Cadena | Consulta                            | Un valor a utilizar en el cálculo, si corresponde.                                               |
| worksheet (hoja)     | Cadena | Consulta                            | El nombre de la hoja en la que realizar la operación.                                           |
| range (rango)        | Cadena | Consulta                            | El rango de celdas a incluir en el cálculo.                                                     |
| region (región)      | Cadena | Consulta                            | La configuración de región de la hoja de cálculo.                                               |
| password (contraseña) | Cadena | Consulta                            | La contraseña para abrir el archivo de hoja de cálculo, si está protegido.                       |

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

**Códigos de estado HTTP**

| Código | Significado             | Descripción                                                        |
| ------ | ----------------------- | ------------------------------------------------------------------ |
| 200    | OK                      | Filtro aplicado correctamente; la respuesta contiene detalles de la operación. |
| 400    | Solicitud incorrecta    | Parámetros ausentes o no válidos (por ejemplo, tipo de archivo no admitido). |
| 401    | No autorizado           | Token JWT inválido o ausente.                                      |
| 413    | Payload demasiado grande | El archivo subido excede el límite de tamaño.                     |
| 500    | Error interno del servidor | Error inesperado en el servidor.                                  |

## ¿Dónde debemos utilizar la API de cálculo matemático?

- **Finanzas**: sume un 13% de IVA a toda una columna de precios de compra.
- **Inventario**: multiplique la columna de kg por 2,2046 para convertir por lotes a libras.
- **Nómina**: sume una bonificación fija de 1.000 a la columna de bonificaciones para todo el personal.
- **Conversión de divisas**: divida la columna de ventas por el tipo de cambio actual para obtener importes en USD.
- **Calificación**: reste 5 puntos a la puntuación de cada estudiante como penalización por asistencia.
- **Comercio electrónico**: aplique un descuento promocional del 15% reduciendo los precios de los productos con un solo clic.

## ¿Por qué debería utilizar la API de cálculo matemático?

- **Cálculos rápidos en Excel**: termine los informes mensuales en segundos.
- **Aumento porcentual por lotes en Excel**: actualice precios, previsiones, comisiones con un solo clic.
- **Sumar el mismo número a toda una columna**: inventario, conversión de divisas, conversión de unidades.
- **Excel sin fórmulas**: los usuarios no técnicos valoran su simplicidad.
- **El desarrollo puede completarse rápidamente mediante el SDK existente**.

**Notas**  
El tamaño máximo de archivo admitido es de 200 MB. El parámetro `range` debe ser una dirección válida de Excel (por ejemplo, A1:B10). Las hojas de cálculo muy grandes pueden requerir más tiempo de procesamiento.

## Cómo utilizar la API de cálculo matemático con SDK

### Especificación de la API de cálculo matemático

La [especificación de la API de cálculo matemático](https://reference.aspose.cloud/cells/#/CalculateController/MathCalculate) define una interfaz de programación pública accesible, lo que permite a los desarrolladores interactuar directamente con la API desde un navegador web.

### Utilice los SDK de Aspose.Cells Cloud

Utilizar los SDK es la forma más rápida de desarrollar, ya que oculta los detalles de bajo nivel, permitiéndole realizar cálculos matemáticos por celda con solo un código breve.  
Consulte los [SDK de Aspose.Cells Cloud en GitHub](https://github.com/aspose-cells-cloud) para obtener una lista completa.

Los siguientes ejemplos de código muestran cómo realizar llamadas a los servicios web de Aspose.Cells mediante diversos SDK:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_MathCalculate.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_MathCalculate.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_MathCalculate.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_MathCalculate.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_MathCalculate.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_MathCalculate.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_MathCalculate.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_MathCalculate.go" >}}
{{</tab>}}
{{< /tabs >}}