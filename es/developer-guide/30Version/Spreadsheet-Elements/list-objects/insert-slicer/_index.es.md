---
title: "Insertar un filtro de segmentación en un ListObject de Excel – API de Aspose.Cells Cloud"
second_title: "Documento"
linktitle: "Insertar filtro de segmentación"
type: docs
keywords: "Aspose.Cells, filtro de segmentación de Excel, ListObject, API REST, SDK en la nube"
description: "Aprenda cómo agregar un filtro de segmentación a un ListObject de Excel utilizando la API REST de Aspose.Cells Cloud (v3.0). Incluye el punto de conexión, parámetros, autenticación, solicitud de ejemplo con cURL y respuesta JSON."
weight: 20
ArticleTitle: "Insertar un filtro de segmentación en un ListObject de Excel – API de Aspose.Cells Cloud"
---

Esta API REST inserta un filtro de segmentación para un objeto de lista en una hoja de cálculo de Excel.

## API REST

```bash
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/listobjects/{listObjectIndex}/InsertSlicer
```

### Parámetros de solicitud

| Nombre del parámetro | Tipo    | Ubicación | Descripción                                                                 |
|----------------------|---------|-----------|-----------------------------------------------------------------------------|
| name                 | String  | Path      | El nombre del archivo de Excel.                                            |
| sheetName            | String  | Path      | El nombre de la hoja de cálculo que contiene el objeto de lista.           |
| listObjectIndex      | Integer | Path      | El índice basado en cero del objeto de lista al que se agregará el filtro. |
| columnIndex          | Integer | Query     | El índice basado en cero de la columna sobre la cual se basa el filtro.    |
| destCellName         | String  | Query     | La referencia de celda (por ejemplo, **A1**) donde se colocará el filtro. |
| folder               | String  | Query     | La carpeta en el almacenamiento que contiene el archivo de Excel.          |
| storageName          | String  | Query     | El nombre del servicio de almacenamiento en la nube de Aspose Cloud.       |

Puede utilizar la herramienta de línea de comandos cURL para llamar a la API:

{{< tabs tabTotal="2" tabID="1" tabName1="Solicitud" tabName2="Respuesta" >}}
{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/listobjects/{listObjectIndex}/InsertSlicer" \
  -X POST \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

> **Nota:** La solicitud requiere un token JWT portador válido obtenido del servicio de autenticación de Aspose Cloud. Este punto de conexión no requiere un cuerpo de solicitud; envíe un objeto JSON vacío `{}` si su biblioteca cliente exige un payload.

{{< /tab >}}
{{< tab tabNum="2" >}}

```json
{
  "Code": 200,
  "Status": "OK",
  "Slicer": {
    "Name": "Slicer1",
    "ColumnIndex": 2,
    "Position": "A1"
  }
}
```

> **Encabezado de respuesta:** `Content-Type: application/json`

{{< /tab >}}
{{< /tabs >}}

**Códigos de estado HTTP**

| Código | Significado                  | Descripción                                                  |
|--------|------------------------------|--------------------------------------------------------------|
| 200    | OK                           | Filtro aplicado correctamente; la respuesta contiene detalles de la operación. |
| 400    | Solicitud incorrecta         | Parámetros faltantes o inválidos (por ejemplo, tipo de archivo no admitido). |
| 401    | No autorizado                | Token JWT inválido o faltante.                               |
| 413    | Payload demasiado grande     | El archivo subido excede el límite de tamaño.                |
| 500    | Error interno del servidor   | Error inesperado en el servidor.                             |

### Manejo de errores

Cuando ocurre un error, la API devuelve un objeto JSON con un campo `ErrorMessage` que describe el problema. Inspeccione el código de estado HTTP y el `ErrorMessage` para determinar la acción correctiva.

## Familia de SDK en la nube

Utilizar un SDK es la mejor forma de acelerar el desarrollo. Un SDK se encarga de los detalles de bajo nivel y le permite centrarse en las tareas de su proyecto. Consulte el repositorio de GitHub para obtener una lista completa de los SDK de Aspose.Cells Cloud.

Los siguientes ejemplos de código muestran cómo realizar llamadas a los servicios web de Aspose.Cells mediante diversos SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostWorksheetListObjectInsertSlicer.cs" >}}
{{< /tab >}}

{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostWorksheetListObjectInsertSlicer.java" >}}
{{< /tab >}}

{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostWorksheetListObjectInsertSlicer.php" >}}
{{< /tab >}}

{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostWorksheetListObjectInsertSlicer.rb" >}}
{{< /tab >}}

{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostWorksheetListObjectInsertSlicer.ts" >}}
{{< /tab >}}

{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostWorksheetListObjectInsertSlicer.py" >}}
{{< /tab >}}

{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostWorksheetListObjectInsertSlicer.pl" >}}
{{< /tab >}}

{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostWorksheetListObjectInsertSlicer.go" >}}
{{< /tab >}}

{{< /tabs >}}