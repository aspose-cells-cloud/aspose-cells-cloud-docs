---
title: "Convertir objeto de lista a rango: API de Aspose.Cells Cloud"
ArticleTitle: "Convertir objeto de lista a rango usando la API de Aspose.Cells Cloud"
second_title: "Documento"
linktype: "Conversión"
type: docs
url: /es/list-objects/to-range/
aliases:
  - /convert-list-object-or-table-to-range/
  - /tables/to-range/
keywords: "API de Aspose Cells, convertir objeto de lista a rango, API REST de Excel"
description: "Aprenda cómo convertir un ListObject (tabla) de Excel en un rango utilizando la API REST de Aspose.Cells Cloud. Incluye sintaxis de solicitud, parámetros, ejemplo de cURL, esquema de respuesta, detalles de autenticación, códigos de error y ejemplos de SDK."
weight: 30
---

Esta API REST convierte un **ListObject (tabla)** en un **rango** dentro de una hoja de cálculo de Excel.

**Requisitos previos:**  
Antes de llamar al endpoint, asegúrese de que el libro esté cargado en su almacenamiento de Aspose Cloud, la hoja de cálculo contenga el ListObject objetivo y esté utilizando un formato de archivo compatible (por ejemplo, .xlsx, .xlsm).

## API REST

**Autenticación**  
Para llamar a esta operación, debe incluir un token JWT válido en el encabezado `Authorization`. Obtenga el token enviando una solicitud POST al endpoint de token OAuth 2.0 con su ID de cliente y secreto de cliente. El token debe incluir el ámbito `Cells.ReadWrite` y será válido durante el período indicado por el servicio de tokens.

```bash
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/listobjects/{listObjectIndex}/ConvertToRange
```

### **Seguridad y autenticación**

Las API de Aspose.Cells Cloud son seguras y requieren <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">autenticación mediante token JWT</a>.

### Parámetros de solicitud

| Nombre              | Tipo    | Ubicación | Obligatorio | Valor por defecto | Descripción                                               |
| ------------------- | ------- | --------- | ----------- | ----------------- | --------------------------------------------------------- |
| **name**            | string  | ruta      | Sí          | –                 | Nombre del archivo de Excel.                              |
| **sheetName**       | string  | ruta      | Sí          | –                 | Nombre de la hoja de cálculo que contiene el ListObject. |
| **listObjectIndex** | integer | ruta      | Sí          | –                 | Índice de base cero del ListObject (tabla) que se convertirá. |
| **folder**          | string  | consulta  | No          | –                 | Ruta de la carpeta donde se guarda el archivo.            |
| **storageName**     | string  | consulta  | No          | –                 | Nombre del servicio de almacenamiento.                    |

> **Nota:** Esta operación solo funciona con formatos modernos de Excel como **.xlsx** y **.xlsm**. El ListObject no debe estar protegido. Para obtener más información sobre ListObjects, consulte la [descripción general de ListObjects](/list-objects/). Para obtener detalles sobre el trabajo con rangos, consulte la [documentación sobre rangos](/ranges/).

### Ejemplo de cURL (solicitud)

{{< tabs tabTotal="2" tabID="11" tabName11="Solicitud" tabName12="Respuesta" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/listobjects/0/ConvertToRange" \
  -X POST \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <su-token-jwt>"
```

{{< /tab >}}

#### Esquema de respuesta

La API devuelve una respuesta **200 OK** con los detalles del rango recién creado.

```json
{
  "Code": 200,
  "Status": "OK",
  "RangeName": "A1:C10",
  "Address": "Sheet1!A1:C10",
  "FirstRow": 0,
  "FirstColumn": 0,
  "RowCount": 10,
  "ColumnCount": 3
}
```

| Campo           | Tipo    | Descripción                                        |
| --------------- | ------- | -------------------------------------------------- |
| **Code**        | integer | Código de estado tipo HTTP (200 indica éxito).     |
| **Status**      | string  | Mensaje de estado en texto.                        |
| **RangeName**   | string  | Nombre asignado al rango creado.                   |
| **Address**     | string  | Dirección completa del rango, incluyendo el nombre de la hoja. |
| **FirstRow**    | integer | Índice de base cero de la primera fila del rango.  |
| **FirstColumn** | integer | Índice de base cero de la primera columna del rango. |
| **RowCount**    | integer | Número de filas del rango.                         |
| **ColumnCount** | integer | Número de columnas del rango.                      |

**Códigos de estado HTTP**

| Código | Significado                 | Descripción                                             |
|--------|-----------------------------|---------------------------------------------------------|
| 200  | OK                          | Filtro aplicado correctamente; la respuesta contiene los detalles de la operación. |
| 400  | Solicitud incorrecta        | Parámetros faltantes o no válidos (por ejemplo, tipo de archivo no admitido). |
| 401  | No autorizado               | Token JWT inválido o ausente. |
| 413  | Carga demasiado grande       | El archivo cargado excede el límite de tamaño. |
| 500  | Error interno del servidor  | Error inesperado del servidor. |

**Esquema de respuesta de error (ejemplo):**

```json
{
  "Code": 400,
  "Message": "listObjectIndex no válido. El índice debe estar entre 0 y 5."
}
```

{{< tab tabNum="12" >}}

```json
{
  "Code": 200,
  "Status": "OK",
  "RangeName": "A1:C10",
  "Address": "Sheet1!A1:C10",
  "FirstRow": 0,
  "FirstColumn": 0,
  "RowCount": 10,
  "ColumnCount": 3
}
```

{{< /tab >}}

{{< /tabs >}}

## Familia de SDK en la nube

Utilizar un SDK es la mejor forma de acelerar el desarrollo. Un SDK maneja los detalles de bajo nivel para que usted pueda centrarse en las tareas de su proyecto. Consulte el [repositorio de GitHub](https://github.com/aspose-cells-cloud) para ver una lista completa de los SDK de Aspose.Cells Cloud.

Los siguientes ejemplos de código muestran cómo realizar llamadas a los servicios web de Aspose.Cells utilizando varios SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostWorksheetListObjectConvertToRange.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostWorksheetListObjectConvertToRange.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostWorksheetListObjectConvertToRange.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostWorksheetListObjectConvertToRange.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostWorksheetListObjectConvertToRange.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostWorksheetListObjectConvertToRange.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostWorksheetListObjectConvertToRange.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostWorksheetListObjectConvertToRange.go" >}}

{{< /tab >}}

{{< /tabs >}}