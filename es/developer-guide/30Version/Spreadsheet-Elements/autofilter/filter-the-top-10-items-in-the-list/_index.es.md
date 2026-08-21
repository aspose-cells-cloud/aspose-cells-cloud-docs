---
title: "Agregar filtro superior 10 a una hoja de cálculo de Excel (Aspose.Cells Cloud)"
ArticleTitle: "Agregar filtro superior 10 a una hoja de cálculo de Excel – Aspose.Cells Cloud"
second_title: "Documento"
linktitle: "Agregar filtro superior 10"
type: docs
url: /autofilter/add-top-10-filter/
aliases:
  [/filter-the-top-10-items-in-the-list/, /autofilter/add-a-top-10-filter/]
keywords: "Aspose.Cells, AutoFilter, Filtro superior 10, API de Excel"
description: "Aprenda a aplicar un filtro superior 10 en una hoja de cálculo de Excel mediante la API REST de Aspose.Cells Cloud. Incluye el punto de conexión, parámetros, un ejemplo con cURL por HTTPS, detalles de autenticación, manejo de errores y fragmentos de código de SDK para C#, Java, Python y más."
weight: 65
---

Esta API REST filtra los **10 elementos superiores** en una lista.

> **Requisitos previos**  
> • Obtenga un token JWT válido mediante la autenticación de Aspose.Cells Cloud.  
> • Cargue el libro de Excel en su almacenamiento de Aspose Cloud (o especifique el almacenamiento/carpeta donde se encuentra).  
> • Conozca el nombre de la hoja de cálculo y el rango de celdas que desea filtrar.

## API PutWorksheetFilterTop10

```http
PUT https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/autoFilter/filterTop10
```

### **Seguridad y autenticación**

Las API de Aspose.Cells Cloud son seguras y requieren <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">autenticación basada en token JWT</a>.

### Parámetros de solicitud

| Nombre del parámetro | Tipo    | Ubicación | Obligatorio | Valor predeterminado | Descripción                                                                 |
| --------------------- | ------- | --------- | ----------- | -------------------- | --------------------------------------------------------------------------- |
| **name**              | string  | path      | Sí          | —                    | Nombre del archivo de Excel.                                                |
| **sheetName**         | string  | path      | Sí          | —                    | Nombre de la hoja de cálculo que contiene los datos.                        |
| **range**             | string  | query     | Sí          | —                    | Rango de celdas al que se aplica el filtro (por ejemplo, `A1:B10`).         |
| **fieldIndex**        | integer | query     | Sí          | —                    | Índice de columna (base cero) sobre el que se aplica el filtro.             |
| **isTop**             | boolean | query     | Sí          | `true`               | `true` para filtrar los elementos superiores; `false` para los inferiores.  |
| **isPercent**         | boolean | query     | No          | `false`              | `true` para tratar `itemCount` como un porcentaje; `false` para una cantidad absoluta. |
| **itemCount**         | integer | query     | No          | `10`                 | Número de elementos que se incluirán en el filtro.                          |
| **matchBlanks**       | boolean | query     | No          | `false`              | `true` para incluir celdas en blanco en los resultados del filtro.         |
| **refresh**           | boolean | query     | No          | `false`              | `true` para actualizar el filtro tras aplicarlo.                            |
| **folder**            | string  | query     | No          | —                    | Carpeta en el almacenamiento donde se encuentra el archivo de Excel.        |
| **storageName**       | string  | query     | No          | —                    | Nombre del almacenamiento de Aspose Cloud.                                  |

### **Respuesta**

```json
{
    "Status":"OK",
    "Code":200
}
```

**Respuestas de error típicas**

```json
{
    "Code":400,
    "Message":"Solicitud incorrecta: parámetros ausentes o no válidos."
}
```

```json
{
    "Code":401,
    "Message":"No autorizado: token JWT no válido o ausente."
}
```

```json
{
    "Code":413,
    "Message":"Solicitud demasiado grande: el archivo cargado supera el tamaño permitido."
}
```

```json
{
    "Code":500,
    "Message":"Error interno del servidor: condición inesperada del servidor."
}
```

**Códigos de estado HTTP**

| Código | Significado                 | Descripción                                              |
|--------|-----------------------------|----------------------------------------------------------|
| 200    | OK                          | Filtro aplicado correctamente; la respuesta contiene los detalles de la operación. |
| 400    | Solicitud incorrecta        | Parámetros ausentes o no válidos (por ejemplo, tipo de archivo no admitido). |
| 401    | No autorizado               | Token JWT no válido o ausente.                           |
| 413    | Solicitud demasiado grande   | El archivo cargado supera el límite de tamaño.          |
| 500    | Error interno del servidor  | Error inesperado del servidor.                           |

## Cómo utilizar la API PutWorksheetFilterTop10 con SDK

### Especificación de la API PutWorksheetFilterTop10

La [Especificación OpenAPI](https://apireference.aspose.cloud/cells/#/AutoFilter/PutWorksheetFilterTop10) define una interfaz de programación públicamente accesible y le permite realizar interacciones REST directamente desde un navegador web.

Puede utilizar la herramienta de línea de comandos cURL para acceder fácilmente a los servicios web de Aspose.Cells. El siguiente ejemplo muestra cómo llamar a la API con cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Solicitud" tabName12="Respuesta" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/autoFilter/filterTop10?range=A1:B10&fieldIndex=0&isTop=true&itemCount=10" \
  -X PUT \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

### Utilizar los SDK de Aspose.Cells Cloud

Utilizar un SDK es la forma más rápida de desarrollar. Un SDK gestiona los detalles de bajo nivel para que usted pueda centrarse en su proyecto. Consulte el [repositorio de GitHub](https://github.com/aspose-cells-cloud) para obtener una lista completa de los SDK de Aspose.Cells Cloud.

Los siguientes ejemplos de código muestran cómo llamar a los servicios web de Aspose.Cells mediante diversos SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePutWorksheetFilterTop10.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PutWorksheetFilterTop10.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PutWorksheetFilterTop10.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PutWorksheetFilterTop10.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PutWorksheetFilterTop10.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PutWorksheetFilterTop10.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PutWorksheetFilterTop10.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PutWorksheetFilterTop10.go" >}}

{{< /tab >}}

{{< /tabs >}}