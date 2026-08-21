---
title: "Trabajo con filtros de tabla dinámica"
second_title: "Documento"
linktitle: Filtros
type: docs
url: /es/pivot-tables/add-filters/
aliases: [  /es/working-with-pivot-filters/ ]
keywords: "Aspose.Cells, Tabla dinámica, Filtro, API REST, Nube"
description: "Aprenda cómo agregar, recuperar y eliminar filtros de tabla dinámica mediante la API REST de Aspose.Cells Cloud. Incluye sintaxis de solicitud, parámetros necesarios, ejemplo de cURL y fragmentos de código para C# y Go."
weight: 50
ArticleTitle: "Trabajo con filtros de tabla dinámica – Documentación de Aspose.Cells Cloud"
---

Esta API REST agrega un **filtro de tabla dinámica** a la tabla dinámica ubicada en el índice especificado.

**Requisitos previos**  
Antes de llamar a este punto de conexión, debe:

- Generar un token de acceso OAuth/JWT válido e incluirlo en el encabezado `Authorization`.
- Asegurarse de que el libro de trabajo objetivo esté almacenado en una carpeta en la nube a la que tenga acceso (especifique `folder` y opcionalmente `storageName`).
- Utilizar la versión 3.0 o posterior de la API de Aspose.Cells Cloud.

## API PutWorksheetPivotTableFilter

```http
PUT https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/pivottables/{pivotTableIndex}/PivotFilters
```

### **Seguridad y autenticación**

Las API de Aspose.Cells Cloud son seguras y requieren <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">autenticación basada en token JWT</a>.

### Parámetros de solicitud

| Nombre del parámetro  | Tipo    | Ubicación | Descripción                                                                                     |
| --------------------- | ------- | --------- | ----------------------------------------------------------------------------------------------- |
| **name**              | string  | path      | Nombre del archivo Excel.                                                                       |
| **sheetName**         | string  | path      | Hoja de cálculo que contiene la tabla dinámica.                                                 |
| **pivotTableIndex**   | integer | path      | Índice de base cero de la tabla dinámica a la que se aplicará el filtro.                        |
| **filter**            | object  | body      | Objeto JSON que define la configuración del filtro. Consulte la tabla **esquema de filtro** a continuación. |
| **needReCalculate**   | boolean | query     | Si es **true**, fuerza la recalculación del libro de trabajo tras agregar el filtro. Valor predeterminado: **false**. |
| **folder**            | string  | query     | Carpeta en el almacenamiento en la nube donde se encuentra el archivo.                         |
| **storageName**       | string  | query     | Nombre del almacenamiento en la nube.                                                           |

**Esquema de filtro**

| Propiedad                    | Tipo    | Descripción                                                                                 |
| ---------------------------- | ------- | ------------------------------------------------------------------------------------------- |
| **AutoFilter**               | object  | Configuración para un filtro automático; puede omitirse si no se utiliza.                    |
| **EvaluationOrder**          | integer | Orden en el que se evalúa el filtro.                                                        |
| **FieldIndex**               | integer | Índice de base cero del campo al que se aplica el filtro.                                   |
| **FilterType**               | string  | Tipo de filtro (por ejemplo, `Value`, `Count`, `Label`).                                    |
| **MeasureFldIndex**          | integer | Índice del campo de medida, si corresponde.                                                 |
| **MemberPropertyFieldIndex** | integer | Índice del campo de propiedad de miembro, si corresponde.                                   |
| **Name**                     | string  | Nombre opcional para el filtro.                                                             |
| **Value1**                   | string  | Primer valor utilizado por el filtro (por ejemplo, límite inferior para un rango).          |
| **Value2**                   | string  | Segundo valor utilizado por el filtro (por ejemplo, límite superior para un rango).         |
| **CustomFilters**            | array   | Colección de objetos de filtro personalizado (cada uno con `FilterOperatorType`, `Value1`, `Value2`). |
| **DynamicFilter**            | object  | Configuración para un filtro dinámico (por ejemplo, Top10, Bottom10).                       |
| **IconFilter**               | object  | Configuración para un filtro basado en iconos.                                              |
| **Top10Filter**              | object  | Configuración para un filtro Top10/Bottom10.                                                |
| **ColorFilter**              | object  | Configuración para un filtro basado en color.                                               |
| **Visibledropdown**          | boolean | Indica si el menú desplegable del filtro es visible.                                        |

> **Nota:** Todos los parámetros enumerados anteriormente son obligatorios a menos que se indique explícitamente como opcionales en la referencia de la API.

### Códigos de respuesta

| Código | Significado                                     |
| ------ | ----------------------------------------------- |
| 200    | Filtro agregado correctamente.                  |
| 400    | Solicitud incorrecta: parámetros no válidos.    |
| 401    | No autorizado: token ausente o no válido.       |
| 404    | No encontrado: libro de trabajo o tabla dinámica no encontrados. |
| 500    | Error interno del servidor.                     |

**Prácticas recomendadas**  
- Mantenga los objetos de filtro tan pequeños como sea posible; definiciones de filtro grandes pueden aumentar la latencia de la solicitud.  
- Las llamadas son idempotentes: agregar el mismo filtro dos veces no creará duplicados.  
- Respete el límite de velocidad de la API: 100 solicitudes por minuto por cuenta.  

*Notas adicionales:*  
- El tamaño máximo de una definición de filtro es de 1 MB; las cargas útiles más grandes se rechazarán con un error 400.  
- Al utilizar `needReCalculate=true`, la recalculación puede aumentar el tiempo de respuesta para libros de trabajo grandes.  

Puede explorar la definición completa de OpenAPI aquí:  
[Especificación OpenAPI](https://apireference.aspose.cloud/cells/#/PivotTables/PutWorksheetPivotTableFilter)

### Ejemplo de solicitud con cURL

{{< tabs tabTotal="2" tabID="1" tabName1="Solicitud" tabName2="Respuesta" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/pivottables/0/PivotFilters?needReCalculate=true" \
  -X PUT \
  -d '{
        "AutoFilter": {
          "link": { "Href": "https://example.com", "Rel": "self", "Title": "Enlace de filtro automático", "Type": "application/json" },
          "FilterColumns": [
            {
              "FieldIndex": 0,
              "FilterType": "Value",
              "MultipleFilters": {
                "MatchBlank": true,
                "MultipleFilterList": [ { "Value": "ejemplo" } ]
              },
              "ColorFilter": {
                "FilterByFillColor": "FF0000",
                "Pattern": "Solid",
                "Color": {
                  "Color": { "A": 255, "R": 255, "G": 0, "B": 0 },
                  "ColorIndex": 3,
                  "IsShapeColor": false,
                  "ThemeColor": { "ColorType": "Accent1", "Tint": 0 },
                  "Type": "Rgb"
                },
                "ForegroundColorColor": null,
                "BackgroundColor": null
              },
              "CustomFilters": [ { "FilterOperatorType": "Equals", "Value1": "Ejemplo" } ],
              "DynamicFilter": { "DynamicFilterType": "Top10" },
              "IconFilter": { "IconId": 1, "IconSetType": "3Arrows" },
              "Top10Filter": { "Criteria": "Top", "IsPercent": true, "IsTop": true, "Items": 10 },
              "Visibledropdown": "true"
            }
          ],
          "Range": "A1:D100",
          "Sorter": {
            "CaseSensitive": false,
            "HasHeaders": true,
            "KeyList": [ { "Key": 0, "SortOrder": "Ascending", "CustomList": null } ],
            "SortLeftToRight": false
          }
        },
        "EvaluationOrder": 0,
        "FieldIndex": 0,
        "FilterType": "Value",
        "MeasureFldIndex": 0,
        "MemberPropertyFieldIndex": 0,
        "Name": "MiFiltro",
        "Value1": "10",
        "Value2": "20"
      }' \
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

## Familia de SDK en la nube

Utilizar un SDK es la forma más rápida de desarrollar contra Aspose.Cells Cloud. Los SDK manejan los detalles de bajo nivel, permitiéndole centrarse en su lógica de negocio. Consulte el [repositorio de GitHub](https://github.com/aspose-cells-cloud) para obtener una lista completa de los SDK de Aspose.Cells Cloud.

Los siguientes ejemplos de código muestran cómo realizar llamadas a los servicios web de Aspose.Cells mediante varios SDK.

{{< tabs tabTotal="2" tabID="4" tabName1="C#" tabName2="Go" >}}

{{< tab tabNum="1" >}}

```csharp
using System;
using System.Threading.Tasks;
using Aspose.Cells.Cloud.Sdk.Api;
using Aspose.Cells.Cloud.Sdk.Model;

public class PivotFilterExample
{
    public static async Task AddPivotFilterAsync()
    {
        // Inicializar el cliente de la API (reemplace con sus credenciales)
        var config = new Configuration
        {
            ClientId = "SU_ID_CLIENTE",
            ClientSecret = "SU_CLAVE_SECRETA"
        };
        var apiInstance = new CellsApi(config);

        // Construir el objeto filtro
        var filter = new PivotFilter
        {
            AutoFilter = null,
            EvaluationOrder = 0,
            FieldIndex = 1,
            FilterType = "Count"
        };

        // Preparar la solicitud
        var request = new PutWorksheetPivotTableFilterRequest(
            name: "Book1.xlsx",
            sheetName: "HojaTablaDinamica",
            pivotTableIndex: 0,
            filter: filter,
            needReCalculate: true,
            folder: "Temp",
            storageName: null);

        // Ejecutar la solicitud
        var response = await apiInstance.PutWorksheetPivotTableFilterAsync(request);
        Console.WriteLine($"Estado: {response.Status}");
    }
}
```

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "2a2aa16c2d9fd7e46b1b19f5fea5842b" >}}

{{< /tab >}}

{{< /tabs >}}

Para operaciones adicionales relacionadas con tablas dinámicas, consulte la documentación sobre **agregar**, **eliminar** y **limpiar** filtros.