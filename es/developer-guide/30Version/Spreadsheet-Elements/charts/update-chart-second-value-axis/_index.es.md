---
title: "Actualizar el segundo eje de valores de un gráfico"
ArticleTitle: "Actualizar el segundo eje de valores de un gráfico – Aspose.Cells Cloud REST API"
type: docs
url: /charts/second-value-axis/update/
weight: 160
keywords: "Aspose.Cells, API de gráficos, segundo eje de valores, Excel, REST, SDK en la nube"
description: "Actualiza el segundo eje de valores de un gráfico en una hoja de cálculo de Excel mediante la API REST de Aspose.Cells Cloud. Incluye ejemplos de solicitudes, códigos de respuesta y requisitos previos."
---

Esta API REST actualiza el segundo eje de valores de un gráfico.

**Requisitos previos:**  
- Un token de acceso JWT válido (consulte la [guía de autenticación](https://docs.aspose.cloud/cells/authentication/)).  
- El archivo de Excel de destino debe estar almacenado en el almacenamiento de Aspose Cloud (proporcione `folder` y, opcionalmente, `storageName`).  
- Se utiliza la versión de la API v3.0; asegúrese de que la URL base sea `https://api.aspose.cloud/v3.0`.

## API PostChartSecondValueAxis

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/charts/{chartIndex}/secondvalueaxis
```

### **Seguridad y autenticación**

Las API de Aspose.Cells Cloud son seguras y requieren <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">autenticación basada en token JWT</a>.

### Parámetros de la solicitud

| Nombre del parámetro | Tipo   | Ubicación | Descripción                                           |
| --------------------- | ------ | --------- | ----------------------------------------------------- |
| name                  | string | path      | Nombre del archivo de Excel.                          |
| sheetName             | string | path      | Nombre de la hoja de cálculo que contiene el gráfico. |
| chartIndex            | integer| path      | Índice de base cero del gráfico que se va a modificar.|
| axis                  | object | body      | Configuración del segundo eje de valores.             |
| folder                | string | query     | Ruta de la carpeta en el almacenamiento donde se encuentra el archivo. |
| storageName           | string | query     | Nombre del servicio de almacenamiento.                |

**Ejemplo de cuerpo de solicitud (JSON):**

```json
{
  "IsAutomaticMajorUnit": true,
  "Maximum": 100,
  "Minimum": 0,
  "MajorUnit": 10,
  "MinorUnit": 2,
  "Title": {
    "Text": "Eje secundario"
  }
}
```

La [Especificación OpenAPI](https://apireference.aspose.cloud/cells/#/Charts/PostChartSecondValueAxis) define una interfaz de programación accesible públicamente y permite realizar interacciones REST directamente desde un navegador web.

Puede utilizar la herramienta de línea de comandos cURL para acceder fácilmente a los servicios web de Aspose.Cells. El siguiente ejemplo muestra cómo realizar llamadas a la API en la nube mediante cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Solicitud" tabName2="Respuesta" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/charts/{chartIndex}/secondvalueaxis" \
-X POST \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

**Códigos de estado HTTP**

| Código | Significado               | Descripción                                         |
|--------|---------------------------|-----------------------------------------------------|
| 200    | OK                        | Filtro aplicado correctamente; la respuesta contiene detalles de la operación. |
| 400    | Solicitud incorrecta      | Parámetros ausentes o no válidos (por ejemplo, tipo de archivo no admitido). |
| 401    | No autorizado             | Token JWT no válido o ausente. |
| 413    | Carga útil demasiado grande | El archivo cargado supera el límite de tamaño. |
| 500    | Error interno del servidor | Error inesperado en el servidor. |

**Consulte también:**  
- [Obtener el segundo eje de valores de un gráfico](https://docs.aspose.cloud/cells/charts/second-value-axis/get/)  
- [Actualizar el eje de valores de un gráfico](https://docs.aspose.cloud/cells/charts/value-axis/update/)

## Familia de SDK en la nube

Utilizar un SDK es la mejor forma de acelerar el desarrollo. Un SDK se encarga de los detalles de bajo nivel y le permite centrarse en las tareas de su proyecto. Consulte el [repositorio de GitHub](https://github.com/aspose-cells-cloud) para obtener una lista completa de los SDK de Aspose.Cells Cloud.

Los siguientes ejemplos de código muestran cómo realizar llamadas a los servicios web de Aspose.Cells utilizando diversos SDK:

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

```csharp
// Ejemplo en C# para actualizar el segundo eje de valores
var api = new CellsApi("clientId", "clientSecret");
var axis = new Axis { IsAutomaticMajorUnit = true, Maximum = 100 };
api.PostChartSecondValueAxis(name, sheetName, chartIndex, axis);
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java
// Ejemplo en Java para actualizar el segundo eje de valores
CellsApi api = new CellsApi("clientId", "clientSecret");
Axis axis = new Axis();
axis.setIsAutomaticMajorUnit(true);
axis.setMaximum(100.0);
api.postChartSecondValueAxis(name, sheetName, chartIndex, axis);
```

{{< /tab >}}

{{< tab tabNum="3" >}}

```php
// Ejemplo en PHP para actualizar el segundo eje de valores
$api = new CellsApi($clientId, $clientSecret);
$axis = new Axis();
$axis->setIsAutomaticMajorUnit(true);
$axis->setMaximum(100);
$api->postChartSecondValueAxis($name, $sheetName, $chartIndex, $axis);
```

{{< /tab >}}

{{< tab tabNum="4" >}}

```ruby
# Ejemplo en Ruby para actualizar el segundo eje de valores
api = AsposeCellsCloud::ApiClient.new(client_id, client_secret)
axis = Axis.new(is_automatic_major_unit: true, maximum: 100)
api.post_chart_second_value_axis(name, sheet_name, chart_index, axis)
```

{{< /tab >}}

{{< tab tabNum="5" >}}

```python
# Ejemplo en Python para actualizar el segundo eje de valores
api = asposecellscloud.ApiClient(client_id, client_secret)
axis = Axis(is_automatic_major_unit=True, maximum=100)
api.post_chart_second_value_axis(name, sheet_name, chart_index, axis)
```

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example-Post-ChartSecondValueAxis.js" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

```java
// Ejemplo en Android (Java): idéntico al fragmento anterior en Java
```

{{< /tab >}}

{{< tab tabNum="8" >}}

```swift
// Ejemplo en Swift para actualizar el segundo eje de valores
let api = CellsApi(clientId: "clientId", clientSecret: "clientSecret")
var axis = Axis()
axis.isAutomaticMajorUnit = true
axis.maximum = 100
api.postChartSecondValueAxis(name: name, sheetName: sheetName, chartIndex: chartIndex, axis: axis)
```

{{< /tab >}}

{{< tab tabNum="9" >}}

```perl
# Ejemplo en Perl para actualizar el segundo eje de valores
my $api = AsposeCellsCloud::ApiClient->new(client_id => $client_id, client_secret => $client_secret);
my $axis = AsposeCellsCloud::Object::Axis->new(isAutomaticMajorUnit => 1, maximum => 100);
$api->post_chart_second_value_axis(name => $name, sheet_name => $sheet_name, chart_index => $chart_index, axis => $axis);
```

{{< /tab >}}

{{< tab tabNum="10" >}}

```go
// Ejemplo en Go para actualizar el segundo eje de valores
api := cells.NewApiClient("clientId", "clientSecret")
axis := cells.Axis{IsAutomaticMajorUnit: true, Maximum: 100}
api.PostChartSecondValueAxis(name, sheetName, chartIndex, axis)
```

{{< /tab >}}

{{< /tabs >}}