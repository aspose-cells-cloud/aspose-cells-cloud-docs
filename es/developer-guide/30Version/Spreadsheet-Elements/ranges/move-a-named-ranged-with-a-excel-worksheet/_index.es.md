---
title: "Mover un rango con nombre en una hoja de cálculo de Excel"
second_title: "Documento"
linktitle: "Mover"
type: docs
url: /ranges/move/
aliases: [/move-a-named-range-with-an-excel-worksheet/]
keywords: "Aspose.Cells Cloud, mover rango con nombre, hoja de cálculo de Excel, API REST, mover rango, ejemplos de SDK"
description: "Aprenda a mover un rango con nombre dentro de una hoja de cálculo de Excel mediante la API REST de Aspose.Cells Cloud v3.0, incluyendo detalles del endpoint, autenticación, ejemplos y códigos de muestra en SDK."
weight: 20
ArticleTitle: "Mover un rango con nombre en una hoja de cálculo de Excel mediante la API de Aspose.Cells Cloud"
---

Mover un rango con nombre es una tarea común cuando necesita reorganizar datos programáticamente. Esta sección explica cómo reubicar un rango definido en una nueva posición dentro de la misma hoja de cálculo mediante la API REST de Aspose.Cells Cloud.

Esta API REST mueve un rango especificado a un rango de destino en una hoja de cálculo de Excel.

## API REST

```bash
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/ranges/moveto
```

### Autenticación
La API requiere un **token JWT Bearer** obtenido mediante el flujo OAuth de Aspose Cloud. Incluya el token en el encabezado `Authorization`:

```
Authorization: Bearer <token jwt>
```

El token debe tener el ámbito **Cells**.

### Requisitos previos
- El libro debe estar almacenado en el almacenamiento de Aspose Cloud.  
- Proporcione el nombre del almacenamiento (`storageName`) y la ruta de la carpeta (`folder`) si el archivo no se encuentra en el directorio raíz.  
- Utilice la versión más reciente del SDK de Aspose.Cells Cloud que admita la versión de la API **v3.0**.

### **Seguridad y autenticación**

Las API de Aspose.Cells Cloud son seguras y requieren <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">autenticación basada en token JWT</a>.

### Parámetros de solicitud

| Nombre           | Tipo   | Ubicación | Descripción |
|------------------|--------|-----------|-------------|
| **name**         | string | path      | Nombre del archivo del libro |
| **sheetName**    | string | path      | Nombre de la hoja de cálculo |
| **destRow**      | integer| query     | Índice de fila inicial del rango de destino (basado en 0) |
| **destColumn**   | integer| query     | Índice de columna inicial del rango de destino (basado en 0) |
| **range**        | object | body      | Definición del rango origen que se va a mover |
| **folder**       | string | query     | Ruta de la carpeta donde se almacena el libro |
| **storageName**  | string | query     | Nombre del almacenamiento de Aspose Cloud |

### Cuerpo de la solicitud

| Campo          | Tipo   | Obligatorio | Descripción |
|----------------|--------|-------------|-------------|
| **ColumnCount**| integer| No          | Número de columnas del rango origen |
| **ColumnWidth**| integer| No          | Anchura de cada columna (en puntos) |
| **FirstColumn**| integer| No          | Índice basado en 0 de la primera columna del rango origen |
| **FirstRow**   | integer| No          | Índice basado en 0 de la primera fila del rango origen |
| **Name**       | string | No          | Nombre del rango (si se trata de un rango con nombre) |
| **RefersTo**   | string | No          | Referencia en estilo A1 que define el rango |
| **RowCount**   | integer| No          | Número de filas del rango origen |
| **RowHeight**  | integer| No          | Altura de cada fila (en puntos) |
| **Worksheet**  | string | No          | Hoja de cálculo que contiene el rango origen |

### Flujo de trabajo

1. **Subir** el libro al almacenamiento de Aspose Cloud (si aún no existe).  
2. **Generar** un token JWT utilizando el endpoint OAuth.  
3. **Construir** la carga útil JSON que describe el rango origen.  
4. **Llamar** al endpoint `moveto` con los parámetros de ruta, query y cuerpo JSON requeridos.  
5. **Verificar** la respuesta; una llamada correcta devuelve el código de estado `200 OK`.

### Ejemplo de solicitud / respuesta

{{< tabs tabTotal="2" tabID="1" tabName1="Solicitud" tabName2="Respuesta" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/ranges/moveto?destRow=20&destColumn=20" \
-X POST \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <token jwt>" \
-d '{ 
  "ColumnCount": 7,
  "ColumnWidth": 19,
  "FirstColumn": 0,
  "FirstRow": 9,
  "Name": "MyRange",
  "RefersTo": "A10:G10",
  "RowCount": 1,
  "RowHeight": 15,
  "Worksheet": "Sheet1"
}'
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

Cuando se produce un error, la respuesta incluye un campo opcional `ErrorMessage` que proporciona detalles adicionales sobre la falla.

**Códigos de estado HTTP**

| Código | Significado                 | Descripción                                      |
|--------|-----------------------------|--------------------------------------------------|
| 200    | OK                          | Filtro aplicado correctamente; la respuesta contiene los detalles de la operación. |
| 400    | Solicitud incorrecta        | Parámetros faltantes o no válidos (por ejemplo, tipo de archivo no admitido). |
| 401    | No autorizado               | Token JWT no válido o faltante. |
| 413    | Payload demasiado grande    | El archivo subido excede el límite de tamaño. |
| 500    | Error interno del servidor  | Error inesperado en el servidor. |

**Esquema de respuesta**

| Campo | Tipo   | Descripción |
|-------|--------|-------------|
| **Code** | integer | Código de estado similar a HTTP devuelto por la API (por ejemplo, 200) |
| **Status** | string | Descripción textual del resultado (por ejemplo, "OK") |
| **ErrorMessage** | string (opcional) | Detalles del error legibles por humanos cuando la llamada falla |

## Familia de SDK en la nube

Utilizar un SDK es la mejor manera de acelerar el desarrollo. Un SDK gestiona los detalles de bajo nivel para que usted se enfoque en las tareas de su proyecto. Consulte el <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">repositorio de GitHub</a> para obtener una lista completa de los SDK de Aspose.Cells Cloud.

Los siguientes ejemplos de código muestran cómo realizar llamadas a los servicios web de Aspose.Cells mediante diversos SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostWorksheetCellsRangeMoveTo.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostWorksheetCellsRangeMoveTo.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostWorksheetCellsRangeMoveTo.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostWorksheetCellsRangeMoveTo.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostWorksheetCellsRangeMoveTo.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostWorksheetCellsRangeMoveTo.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostWorksheetCellsRangeMoveTo.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostWorksheetCellsRangeMoveTo.go" >}}

{{< /tab >}}

{{< /tabs >}}