---
title: "Obtener el eje de categorías de un gráfico"
type: docs
url: /charts/category-axis/get/
weight: 60
keywords: "Aspose.Cells, eje de categorías de gráfico, Excel, API REST, almacenamiento en la nube, OAuth2, documentación de API"
description: "Recupera el eje de categorías de un gráfico en una hoja de cálculo de Excel mediante la API REST de Aspose.Cells Cloud."
ArticleTitle: "Obtener el eje de categorías de un gráfico – Documentación de la API de Aspose.Cells Cloud"
---

Esta API REST recupera el **eje de categorías** de un gráfico.  
Para llamar a este punto final, debe proporcionar un token de acceso válido de OAuth 2.0, y el libro de trabajo debe estar almacenado en el almacenamiento de Aspose Cloud.

**Requisitos previos**  
Antes de usar este punto final, asegúrese de que:  

- Se ha obtenido y es válido un token OAuth 2.0 para los servicios de Aspose Cloud.  
- El archivo del libro de trabajo se ha cargado en el almacenamiento de Aspose Cloud (predeterminado o una carpeta especificada).  
- Está utilizando la versión **v3.0** de la API, como se muestra en la URL de la solicitud.  
- La aplicación que realiza la llamada tiene permiso para leer el libro de trabajo y acceder a sus hojas de cálculo.

## API GetChartCategoryAxis

```http
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/charts/{chartIndex}/categoryaxis
```

**Antecedentes**: eliminar todos los gráficos de una hoja de cálculo es útil cuando necesita restablecer el diseño visual de una hoja, reemplazar visualizaciones desactualizadas o preparar un libro de trabajo para su reutilización sin conservar los datos de gráficos anteriores.

### **Seguridad y autenticación**

Las API de Aspose.Cells Cloud son seguras y requieren <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">autenticación basada en token JWT</a>.

### Parámetros de solicitud

| Nombre del parámetro | Tipo    | Ubicación | Descripción                                                |
| --------------------- | ------- | --------- | ---------------------------------------------------------- |
| name                  | string  | path      | Nombre del archivo del libro de trabajo.                  |
| sheetName             | string  | path      | Nombre de la hoja de cálculo que contiene el gráfico.     |
| chartIndex            | integer | path      | Índice de base cero del gráfico cuyo eje se solicita.     |
| folder                | string  | query     | Ruta de la carpeta en el almacenamiento donde reside el libro de trabajo. |
| storageName           | string  | query     | Nombre del servicio de almacenamiento (si no es el predeterminado). |

### **Respuesta**

```json
{
  "Code": 200,
  "Status": "OK",
  "CategoryAxis": {
    "AxisBetweenCategories": true,
    "AxisLine": {
      "IsVisible": true,
      "Weight": 1.0
    },
    "MajorTickMark": "Cross",
    "MinorTickMark": "None",
    "Title": {
      "Text": "Category Axis",
      "IsVisible": true
    },
    "Labels": {
      "IsAutoRotation": false,
      "RotationAngle": 0,
      "IsVisible": true
    }
  }
}
```

**Códigos de estado HTTP**

| Código | Significado                 | Descripción                                          |
|--------|-----------------------------|------------------------------------------------------|
| 200    | OK                          | Filtro aplicado correctamente; la respuesta contiene los detalles de la operación. |
| 400    | Solicitud incorrecta        | Parámetros ausentes o no válidos (por ejemplo, tipo de archivo no admitido). |
| 401    | No autorizado               | Token JWT no válido o ausente. |
| 413    | Carga útil demasiado grande | El archivo cargado excede el límite de tamaño. |
| 500    | Error interno del servidor  | Error inesperado en el servidor. |

## Cómo usar la API GetChartCategoryAxis con SDK

### Especificación de la API GetChartCategoryAxis

La <a href="https://apireference.aspose.cloud/cells/#/Charts/GetChartCategoryAxis" rel="noopener noreferrer">Especificación OpenAPI</a> define una interfaz de programación accesible públicamente y le permite realizar interacciones REST directamente desde un navegador web.

Puede utilizar la herramienta de línea de comandos cURL para acceder fácilmente a los servicios web de Aspose.Cells. El siguiente ejemplo muestra cómo realizar una llamada a la API en la nube con cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Solicitud" tabName2="Respuesta" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/charts/{chartIndex}/categoryaxis" \
-X GET \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Code": 200,
  "Status": "OK",
  "CategoryAxis": {
    "AxisBetweenCategories": true,
    "AxisLine": {
      "IsVisible": true,
      "Weight": 1.0
    },
    "MajorTickMark": "Cross",
    "MinorTickMark": "None",
    "Title": {
      "Text": "Category Axis",
      "IsVisible": true
    },
    "Labels": {
      "IsAutoRotation": false,
      "RotationAngle": 0,
      "IsVisible": true
    }
  }
}
```

{{< /tab >}}

{{< /tabs >}}

### Utilizar los SDK de Aspose.Cells Cloud

Usar un SDK es la mejor forma de acelerar el desarrollo. Un SDK maneja los detalles de bajo nivel y le permite centrarse en las tareas de su proyecto. Consulte el <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">repositorio de GitHub</a> para ver una lista completa de los SDK de Aspose.Cells Cloud.

Los siguientes ejemplos de código muestran cómo llamar a los servicios web de Aspose.Cells utilizando diversos SDK:

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

<!-- C# example placeholder -->

{{< /tab >}}

{{< tab tabNum="2" >}}

<!-- Java example placeholder -->

{{< /tab >}}

{{< tab tabNum="3" >}}

<!-- PHP example placeholder -->

{{< /tab >}}

{{< tab tabNum="4" >}}

<!-- Ruby example placeholder -->

{{< /tab >}}

{{< tab tabNum="5" >}}

<!-- Python example placeholder -->

{{< /tab >}}

{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example-Get-ChartCategoryAxis.js" >}}
{{< /tab >}}

{{< tab tabNum="7" >}}

<!-- Android example placeholder -->

{{< /tab >}}

{{< tab tabNum="8" >}}

<!-- Swift example placeholder -->

{{< /tab >}}

{{< tab tabNum="9" >}}

<!-- Perl example placeholder -->

{{< /tab >}}

{{< tab tabNum="10" >}}

<!-- Go example placeholder -->

{{< /tab >}}

{{< /tabs >}}