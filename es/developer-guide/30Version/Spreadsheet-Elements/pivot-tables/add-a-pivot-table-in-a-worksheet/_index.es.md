---
title: "Agregar una tabla dinámica en una hoja de cálculo de Excel"
second_title: "Documento"
linktitle: Agregar
type: docs
url: /es/pivot-tables/add/
aliases: [  /es/add-a-pivot-table-in-a-worksheet/ ]
keywords: "Agregar tabla dinámica, hoja de cálculo de Excel, Aspose.Cells Cloud, API REST, SDK, tabla dinámica de Excel"
description: "Utilice la API REST de Aspose.Cells Cloud para agregar una tabla dinámica en una hoja de cálculo de Excel. Disponible mediante SDK para C#, Java, PHP, Python, Node.js, Android, Swift, Perl y Go."
weight: 30
ArticleTitle: "Cómo agregar una tabla dinámica en una hoja de cálculo de Excel mediante Aspose.Cells Cloud"
---

Esta API REST agrega una tabla dinámica en una hoja de cálculo.

**Prerrequisitos:**
- Una cuenta de Aspose.Cells Cloud con un token de acceso JWT válido.
- El libro objetivo debe estar almacenado en una ubicación de almacenamiento compatible (almacenamiento predeterminado o un almacenamiento especificado por el usuario).
- La hoja de cálculo especificada mediante `sheetName` debe existir en el libro.

## API PutWorksheetPivotTable

```http
PUT https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/pivottables
```

### **Seguridad y autenticación**

Las API de Aspose.Cells Cloud son seguras y requieren <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">autenticación basada en token JWT</a>.

### **Parámetros de solicitud**

| Nombre del parámetro | Tipo    | Ubicación | Descripción                                                                                                                         |
| --------------------- | ------- | --------- | ----------------------------------------------------------------------------------------------------------------------------------- |
| name                  | string  | path      | El nombre del documento de Excel.                                                                                                  |
| sheetName             | string  | path      | El nombre de la hoja de cálculo donde se creará la tabla dinámica.                                                                |
| request               | object  | body      | DTO `CreatePivotTableRequest` que contiene la definición de la tabla dinámica.                                                    |
| folder                | string  | query     | La carpeta que contiene el documento.                                                                                              |
| storageName           | string  | query     | El nombre del almacenamiento donde se encuentra el documento.                                                                     |
| sourceData            | string  | query     | El rango que proporciona los datos de origen para la nueva memoria caché de la tabla dinámica (por ejemplo, `A5:E10`).             |
| destCellName          | string  | query     | La dirección de la celda superior izquierda del rango de destino del informe de la tabla dinámica.                                |
| tableName             | string  | query     | El nombre asignado a la nueva tabla dinámica.                                                                                      |
| useSameSource         | boolean | query     | Cuando es `true`, la nueva tabla dinámica reutiliza una fuente de datos existente, ahorrando memoria si otra tabla dinámica ya ha usado esta fuente. |

La [Especificación de OpenAPI](https://apireference.aspose.cloud/cells/#/PivotTables/PutWorksheetPivotTable) define una interfaz de programación públicamente accesible y permite realizar interacciones REST directamente desde un navegador web.

Puede utilizar la herramienta de línea de comandos **cURL** para acceder fácilmente a los servicios web de Aspose.Cells. El siguiente ejemplo muestra cómo invocar la API en la nube mediante cURL.

**Nota de seguridad:** Utilice siempre `https://` al invocar la API y mantenga su token JWT confidencial; transmitirlo mediante HTTP sin cifrar puede exponerlo a interceptaciones.

{{< tabs tabTotal="2" tabID="1" tabName1="Solicitud" tabName2="Respuesta" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Sample_Test_Book.xls/worksheets/Sheet1/pivottables" \
-X PUT \
-d '{"Name":"MyPivot","SourceData":"A5:E10","DestCellName":"H20","UseSameSource":true,"PivotFieldRows":[1],"PivotFieldColumns":[1],"PivotFieldData":[1]}' \
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

| Código | Significado                 | Descripción                                             |
| ------ | --------------------------- | ------------------------------------------------------- |
| 200    | Correcto                    | Filtro aplicado correctamente; la respuesta contiene detalles de la operación. |
| 400    | Solicitud incorrecta        | Parámetros ausentes o no válidos (por ejemplo, tipo de archivo no admitido). |
| 401    | No autorizado               | Token JWT inválido o ausente.                           |
| 413    | Payload demasiado grande    | El archivo cargado excede el límite de tamaño.         |
| 500    | Error interno del servidor  | Error inesperado en el servidor.                        |

## Familia de SDK en la nube

Utilizar un SDK es la mejor manera de acelerar el desarrollo. Un SDK maneja los detalles de bajo nivel y le permite centrarse en las tareas de su proyecto. Consulte el [repositorio de GitHub](https://github.com/aspose-cells-cloud) para ver una lista completa de los SDK de Aspose.Cells Cloud.

Los siguientes ejemplos de código muestran cómo invocar los servicios web de Aspose.Cells mediante diversos SDK:

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNET-CSharp-PivotTables-AddPivottableWorksheet-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-pivottables-AddPivottableWorksheet-add-pivot-table-worksheet.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "AddPivotTableInw" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-PivotTables-AddPivottableWorksheet-1.js" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "9d725d4678edaac53f95c5208e17783c" "Examples-Android-pivottables-AddPivottableWorksheet-add-pivot-table-worksheet.java" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-PivotTables-AddPivottableWorksheet-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< gist "aspose-cells-cloud-gists" "980246b631d7816f257f2ad4664788ea" >}}

{{< /tab >}}

{{< /tabs >}}

Para obtener más operaciones, consulte las páginas de API relacionadas: **[Obtener una tabla dinámica](https://docs.aspose.cloud/cells/pivot-tables/get/)**, **[Eliminar una tabla dinámica](https://docs.aspose.cloud/cells/pivot-tables/delete/)** y **[Actualizar una tabla dinámica](https://docs.aspose.cloud/cells/pivot-tables/update/)**.