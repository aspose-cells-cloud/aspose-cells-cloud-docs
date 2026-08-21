---
title: "Agrupar filas en una hoja de cálculo de Excel"
second_title: "Documento"
linktitle: "Agrupar"
type: docs
url: /rows/group/
aliases: [/group-rows-in-excel-worksheet/]
keywords: "agrupar filas, Excel, Aspose.Cells Cloud, API REST, SDK, hoja de cálculo, API de Excel"
description: "Agrupar filas en una hoja de cálculo de Excel utilizando la API REST de Aspose.Cells Cloud. Compatible con múltiples SDK (C#, Java, PHP, Ruby, Node.js, Python, Perl, Go) para una integración sencilla."
weight: 60
ArticleTitle: "Agrupar filas en una hoja de cálculo de Excel mediante la API de Aspose.Cells Cloud"
---

Esta API REST agrupa filas en una hoja de cálculo de Excel.

**Prerrequisitos:**
- Debe suministrarse un token de acceso OAuth 2.0 válido (Bearer JWT) en el encabezado `Authorization`.
- El libro debe existir previamente en la carpeta `folder` especificada del `storageName` elegido (o del almacenamiento predeterminado) antes de realizar la solicitud.

## API PostGroupWorksheetRows

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/rows/group
```

### **Seguridad y autenticación**

Las API de Aspose.Cells Cloud son seguras y requieren <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">autenticación basada en token JWT</a>.

### **Parámetros de solicitud**

| Nombre del parámetro | Tipo    | Ubicación | Descripción                                                                 |
|----------------------|---------|-----------|-----------------------------------------------------------------------------|
| name                 | string  | path      | Nombre del archivo del libro.                                               |
| sheetName            | string  | path      | Nombre de la hoja de cálculo.                                               |
| firstIndex           | integer | query     | Índice de base cero de la primera fila que se va a agrupar.                |
| lastIndex            | integer | query     | Índice de base cero de la última fila que se va a agrupar.                 |
| hide                 | boolean | query     | Indica si las filas agrupadas deben ocultarse (`true` o `false`).          |
| folder               | string  | query     | Ruta a la carpeta que contiene el libro.                                    |
| storageName          | string  | query     | Nombre del almacenamiento donde se encuentra el libro.                     |

La [Especificación OpenAPI](https://apireference.aspose.cloud/cells/#/Cells/PostGroupWorksheetRows) define una interfaz de programación accesible públicamente y permite realizar interacciones REST directamente desde un navegador web.

Puede utilizar la herramienta de línea de comandos cURL para acceder fácilmente a los servicios web de Aspose.Cells. El siguiente ejemplo muestra cómo realizar llamadas a la API en la nube con cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Solicitud" tabName2="Respuesta" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/cells/rows/group?firstIndex=1&lastIndex=2&hide=true" \
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

**Códigos de estado HTTP**

| Código | Significado                 | Descripción                                                                 |
|--------|-----------------------------|-----------------------------------------------------------------------------|
| 200    | OK                          | Filtro aplicado correctamente; la respuesta contiene detalles de la operación. |
| 400    | Solicitud incorrecta        | Parámetros faltantes o no válidos (por ejemplo, tipo de archivo no admitido). |
| 401    | No autorizado               | Token JWT no válido o faltante.                                             |
| 413    | Carga útil demasiado grande | El archivo subido excede el límite de tamaño.                              |
| 500    | Error interno del servidor  | Error inesperado en el servidor.                                            |

Respuestas de error típicas:

- **400 Solicitud incorrecta** – compruebe que `firstIndex` y `lastIndex` sean enteros válidos y que `firstIndex` ≤ `lastIndex`.  
- **401 No autorizado** – verifique que el encabezado `Authorization` contenga un token JWT válido y actualizado.  
- **404 No encontrado** – asegúrese de que el libro (`name`) y la hoja de cálculo (`sheetName`) existan en la carpeta (`folder`) y el almacenamiento (`storageName`) especificados.

{{< /tab >}}

{{< /tabs >}}

**Consulte también:** [Desagrupar filas en una hoja de cálculo de Excel](../rows/ungroup/ "Desagrupar filas en una hoja de cálculo de Excel"), [Ocultar filas en una hoja de cálculo de Excel](../rows/hide/ "Ocultar filas en una hoja de cálculo de Excel"), [Mostrar filas en una hoja de cálculo de Excel](../rows/unhide/ "Mostrar filas en una hoja de cálculo de Excel").

## Familia de SDK en la nube

Utilizar un SDK es la mejor forma de acelerar el desarrollo. Un SDK gestiona los detalles de bajo nivel para que usted pueda centrarse en las tareas de su proyecto. Consulte el [repositorio de GitHub](https://github.com/aspose-cells-cloud) para ver una lista completa de los SDK de Aspose.Cells Cloud.

Los siguientes ejemplos de código muestran cómo llamar a los servicios web de Aspose.Cells mediante diversos SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostGroupWorksheetRows.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostGroupWorksheetRows.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostGroupWorksheetRows.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostGroupWorksheetRows.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostGroupWorksheetRows.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostGroupWorksheetRows.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostGroupWorksheetRows.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostGroupWorksheetRows.go" >}}

{{< /tab >}}

{{< /tabs >}}