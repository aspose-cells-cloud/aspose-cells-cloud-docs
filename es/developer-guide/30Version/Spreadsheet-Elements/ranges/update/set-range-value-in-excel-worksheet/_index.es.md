---
title: "Establecer valor de rango en una hoja de cálculo de Excel"
second_title: "Documento"
linktitle: "Establecer valores"
type: docs
url: /es/ranges/update/values/
aliases: [  /es/set-range-value-in-excel-worksheet/ ]
keywords: "Aspose.Cells, API de Excel, establecer valor de rango, API REST, SDK en la nube, actualización de hoja de cálculo"
description: "Aprenda cómo establecer el valor de una celda o rango en un libro de Excel utilizando la API REST de Aspose.Cells Cloud (v3.0). Incluye el punto de conexión, los parámetros, un ejemplo con cURL, ejemplos de código con SDK y manejo de errores."
weight: 72
ArticleTitle: "Establecer valor de rango en una hoja de cálculo de Excel – API de Aspose.Cells Cloud"
---

Utilice esta API REST para establecer un valor en el rango especificado. Cuando corresponda, el valor se convierte a otro tipo de datos y se restablece el formato numérico de la celda.

**Requisitos previos**  
- Una cuenta válida de Aspose Cloud.  
- Un token JWT que incluya el ámbito `Cells.ReadWrite`.  
- El libro ya debe haberse cargado en la ubicación de almacenamiento de destino.

## API PostWorksheetCellsRangeValue

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/ranges/value
```

Los parámetros de solicitud son:

| Nombre del parámetro | Tipo    | Ubicación | Descripción                                                |
|----------------------|---------|-----------|------------------------------------------------------------|
| name                 | string  | path      | Nombre del libro                                           |
| sheetName            | string  | path      | Nombre de la hoja de cálculo                               |
| value                | string  | query     | Valor de entrada                                           |
| range                | object  | body      | Objeto de rango en la hoja de cálculo                      |
| isConverted          | boolean | query     | Indica si el valor de entrada debe convertirse             |
| setStyle             | boolean | query     | Indica si se debe aplicar estilo a las celdas de destino   |
| folder               | string  | query     | Carpeta del libro                                          |
| storageName          | string  | query     | Nombre del almacenamiento                                  |

**Ejemplo del objeto `range`** que puede enviarse en el cuerpo de la solicitud:

```json
{
  "range": {
    "FirstRow": 0,
    "FirstColumn": 0,
    "RowCount": 1,
    "ColumnCount": 1
  }
}
```

La [Especificación OpenAPI](https://apireference.aspose.cloud/cells/#/Ranges/PostWorksheetCellsRangeValue) define una interfaz de programación accesible públicamente y le permite realizar interacciones REST directamente desde un navegador web.

Puede utilizar la herramienta de línea de comandos cURL para acceder fácilmente a los servicios web de Aspose.Cells. El siguiente ejemplo muestra cómo llamar a la API en la nube con cURL. **Incluya un token JWT válido en el encabezado `Authorization`.**

{{< tabs tabTotal="2" tabID="1" tabName1="Solicitud" tabName2="Respuesta" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/ranges/value?value=25&isConverted=false&setStyle=false" \
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

**Esquema de respuesta**

| Campo   | Tipo    | Descripción                                              |
|---------|---------|----------------------------------------------------------|
| Code    | integer | Código de estado HTTP de la operación.                  |
| Status  | string  | Descripción breve del resultado (por ejemplo, "OK").    |
| Message | string  | Mensaje detallado de error cuando la solicitud falla (opcional). |
| Result  | object  | Datos adicionales devueltos en llamadas exitosas (opcional). |

**Códigos de estado HTTP posibles**

- **200 OK** – El valor del rango se estableció correctamente.  
- **400 Bad Request** – Parámetros no válidos o cuerpo de solicitud mal formado.  
- **401 Unauthorized** – Token JWT faltante o no válido.  
- **403 Forbidden** – Permisos insuficientes para la operación solicitada.  
- **404 Not Found** – El libro, la hoja de cálculo o el rango especificados no existen.  
- **500 Internal Server Error** – Error inesperado del servidor.

*Ejemplo de respuesta de error para un 400 Bad Request:*

```json
{
  "Code": 400,
  "Status": "Bad Request",
  "Message": "Faltan campos obligatorios en el objeto 'range'."
}
```

## Familia de SDK en la nube

Utilizar un SDK es la mejor forma de acelerar el desarrollo. Un SDK maneja los detalles de bajo nivel, lo que le permite centrarse en las tareas de su proyecto. Consulte el [repositorio de GitHub](https://github.com/aspose-cells-cloud) para ver una lista completa de los SDK de Aspose.Cells Cloud.

Los siguientes ejemplos de código muestran cómo realizar llamadas a los servicios web de Aspose.Cells utilizando diversos SDK:

{{< tabs tabTotal="9" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Swift" tabName8="Perl" tabName9="Go" >}}

{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNET-CSharp-Cells-SetRangeValueWorksheet-1.cs" >}}
{{< /tab >}}

{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-cells-SetRangeValueWorksheet-1.java" >}}
{{< /tab >}}

{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Cells-PostSetCellRangeValue-.php" >}}
{{< /tab >}}

{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Cells-set_cell_range_value-.rb" >}}
{{< /tab >}}

{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-Cells-SetRangeValueWorksheet-1.js" >}}
{{< /tab >}}

{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "SetRangeValueInExcelWorksheet.py" >}}
{{< /tab >}}

{{< tab tabNum="7" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-Cells-SetRangeValueWorksheet-1.pl" >}}
{{< /tab >}}

{{< tab tabNum="9" >}}
{{< gist "aspose-cells-cloud-gists" "7dc9243752ac8a0e5d9c0f211a029cd9" >}}
{{< /tab >}}

{{< /tabs >}}