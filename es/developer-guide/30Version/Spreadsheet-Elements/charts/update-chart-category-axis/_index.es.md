---
title: "Actualizar el eje de categorías de un gráfico"
type: docs
url: /es/charts/category-axis/update/
weight: 160
keywords: "Aspose.Cells, gráfico, eje de categorías, API REST, Excel, SDK en la nube"
description: "Actualiza el eje de categorías de un gráfico en una hoja de cálculo de Excel mediante la API REST de Aspose.Cells Cloud."
ArticleTitle: "Actualizar el eje de categorías de un gráfico – Aspose.Cells Cloud API"
---

Esta API REST actualiza el eje de categorías de un gráfico.

## API PostChartCategoryAxis

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/charts/{chartIndex}/categoryaxis
```

### **Seguridad y autenticación**

Las API de Aspose.Cells Cloud son seguras y requieren <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">autenticación basada en token JWT</a>.

### Parámetros de la solicitud

| Nombre del parámetro | Tipo    | Ubicación | Descripción |
| -------------------- | ------- | --------- | ----------- |
| name                 | string  | path      | Nombre del archivo de Excel. |
| sheetName            | string  | path      | Nombre de la hoja de cálculo que contiene el gráfico. |
| chartIndex           | integer | path      | Índice de base cero del gráfico que se va a actualizar. |
| axis                 | object  | body      | Objeto JSON que define las propiedades del eje de categorías. |
| folder               | string  | query     | Carpeta en el almacenamiento en la nube donde se encuentra el archivo (opcional). |
| storageName          | string  | query     | Nombre del almacenamiento (opcional). |

**Esquema del cuerpo de solicitud – objeto `axis`**

| Propiedad                  | Tipo    | Descripción |
|----------------------------|---------|-------------|
| IsAutomaticMajorUnit       | boolean | Determina si la unidad mayor se calcula automáticamente. |
| MajorUnit                  | number  | Valor de la unidad mayor cuando `IsAutomaticMajorUnit` es `false`. |
| IsAutomaticMinorUnit       | boolean | Determina si la unidad menor se calcula automáticamente. |
| MinorUnit                  | number  | Valor de la unidad menor cuando `IsAutomaticMinorUnit` es `false`. |
| Title                      | object  | Configuración del título del eje (por ejemplo, `Text`, `Font`, `Visible`). |
| TickLabelPosition          | string  | Posición de las etiquetas de marca (por ejemplo, `Low`, `High`, `NextToAxis`). |
| ...                        | ...     | Propiedades adicionales del eje según se define en la especificación de la API. |

**Códigos de estado HTTP**

| Código | Significado                 | Descripción |
| ------ | --------------------------- | ----------- |
| 200    | OK                          | Filtro aplicado correctamente; la respuesta contiene los detalles de la operación. |
| 400    | Solicitud incorrecta        | Parámetros faltantes o no válidos (por ejemplo, tipo de archivo no admitido). |
| 401    | No autorizado               | Token JWT inválido o ausente. |
| 413    | Carga útil demasiado grande | El archivo cargado supera el límite de tamaño. |
| 500    | Error interno del servidor  | Error inesperado en el servidor. |

**Requisitos previos / Autenticación**

Para llamar a este punto de conexión, debe obtener un token de acceso JWT del servicio de autenticación de Aspose.Cells Cloud (`/connect/token`). Incluya el token en el encabezado `Authorization`, como se muestra en el siguiente ejemplo.

{{< tabs tabTotal="2" tabID="1" tabName1="Solicitud" tabName2="Respuesta" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/charts/{chartIndex}/categoryaxis?folder={folder}&storageName={storageName}" \
  -X POST \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>" \
  -d '{
        "axis": {
          "IsAutomaticMajorUnit": true,
          "IsAutomaticMinorUnit": true,
          "Title": {
            "Text": "Eje de categorías",
            "Visible": true
          }
        }
      }'
```

{{< /tab >}}

{{< tab tabNum="2" >}}

**Ejemplo de respuesta**

```json
{
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

La [Especificación de OpenAPI](https://apireference.aspose.cloud/cells/#/Charts/PostChartCategoryAxis) define una interfaz de programación accesible públicamente y le permite realizar interacciones REST directamente desde un navegador web.

### Notas

* El punto de conexión requiere HTTPS; usar HTTP puede generar advertencias de contenido mixto en los navegadores.
* Todos los valores de marcador de posición (`{name}`, `{sheetName}`, `{chartIndex}`, `{folder}`, `{storageName}`) deben reemplazarse con identificadores reales.
* Los tipos de gráficos admitidos para actualizaciones del eje de categorías se enumeran en la referencia de la API.

## Familia de SDK en la nube

Utilizar un SDK es la mejor manera de acelerar el desarrollo. Un SDK maneja los detalles de bajo nivel y le permite centrarse en las tareas de su proyecto. Consulte el [repositorio de GitHub](https://github.com/aspose-cells-cloud) para obtener una lista completa de los SDK de Aspose.Cells Cloud.

Los siguientes ejemplos de código muestran cómo realizar llamadas a los servicios web de Aspose.Cells mediante diversos SDK:

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example-Post-ChartCategoryAxis.js" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< /tab >}}

{{< /tabs >}}
---