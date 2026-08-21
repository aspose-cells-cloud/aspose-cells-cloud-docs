---
title: "Cómo fusionar celdas en una hoja de cálculo de Excel – API de Aspose.Cells Cloud (v3.0)"
type: docs
url: /es/merge-cells-in-excel-worksheet/
weight: 110
keywords: "fusionar celdas, Aspose.Cells, API en la nube, Excel"
description: "Guía para fusionar celdas en una hoja de cálculo de Excel mediante la API REST de Aspose.Cells Cloud con ejemplos en cURL y SDK."
ArticleTitle: "Cómo fusionar celdas en una hoja de cálculo de Excel – API de Aspose.Cells Cloud (v3.0)"
---

La API REST de Aspose.Cells Cloud fusiona un bloque rectangular de celdas en una única celda que abarca las filas y columnas especificadas.

**Requisitos previos**  
- Un token JWT válido para autenticación.  
- El libro ya debe existir en la carpeta de almacenamiento especificada.  
- La configuración del almacenamiento (nombre de carpeta y nombre de almacenamiento) debe estar configurada en su cuenta de Aspose.Cloud.

## API PostWorksheetMerge

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/merge
```

### **Seguridad y autenticación**

Las API de Aspose.Cells Cloud son seguras y requieren <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">autenticación basada en token JWT</a>.

### Parámetros de solicitud

| Nombre          | Tipo    | Ubicación | Descripción                                                   |
|-----------------|---------|-----------|---------------------------------------------------------------|
| name            | string  | path      | Nombre del libro.                                             |
| sheetName       | string  | path      | Nombre de la hoja de cálculo.                                 |
| startRow        | integer | query     | Índice de la primera fila (0 = primera fila).                 |
| startColumn     | integer | query     | Índice de la primera columna (0 = primera columna).           |
| totalRows       | integer | query     | Número de filas a fusionar.                                   |
| totalColumns    | integer | query     | Número de columnas a fusionar.                                |
| folder          | string  | query     | Carpeta que contiene el libro.                                |
| storageName     | string  | query     | Nombre del almacenamiento.                                    |

*Esta operación no requiere cuerpo de solicitud.*

## **Respuesta**

Devuelve un objeto `CellsCloudResponse`.

```json
{
  "Status": "OK",
  "Code": 200
}
```

**Códigos de estado HTTP**

| Código | Significado                 | Descripción                                                    |
|--------|-----------------------------|----------------------------------------------------------------|
| 200    | OK                          | Filtro aplicado correctamente; la respuesta contiene detalles de la operación. |
| 400    | Solicitud incorrecta        | Parámetros ausentes o inválidos (por ejemplo, tipo de archivo no admitido). |
| 401    | No autorizado               | Token JWT inválido o ausente.                                  |
| 413    | Payload demasiado grande    | El archivo cargado excede el límite de tamaño.                 |
| 500    | Error interno del servidor  | Error inesperado en el servidor.                               |

## Cómo usar la API PostWorksheetMerge con SDK

### Especificación de la API PostWorksheetMerge

La [Especificación OpenAPI](https://apireference.aspose.cloud/cells/#/Cells/PostWorksheetMerge) define una interfaz de programación accesible públicamente y le permite realizar interacciones REST directamente desde un navegador web.

Puede utilizar la herramienta de línea de comandos **cURL** para acceder fácilmente a los servicios web de Aspose.Cells. El siguiente ejemplo muestra cómo realizar llamadas a la API en la nube con cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Solicitud" tabName12="Respuesta" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/cells/merge?startRow=10&startColumn=10&totalRows=10&totalColumns=10" \
  -X POST \
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

Utilizar un SDK es la mejor manera de acelerar el desarrollo. Un SDK gestiona los detalles de bajo nivel para que pueda centrarse en las tareas de su proyecto. Consulte el [repositorio de GitHub](https://github.com/aspose-cells-cloud) para ver una lista completa de los SDK de Aspose.Cells Cloud.

Los siguientes ejemplos de código muestran cómo realizar llamadas a los servicios web de Aspose.Cells mediante distintos SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostWorksheetMerge.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostWorksheetMerge.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostWorksheetMerge.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostWorksheetMerge.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostWorksheetMerge.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostWorksheetMerge.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostWorksheetMerge.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostWorksheetMerge.go" >}}

{{< /tab >}}

{{< /tabs >}}
---