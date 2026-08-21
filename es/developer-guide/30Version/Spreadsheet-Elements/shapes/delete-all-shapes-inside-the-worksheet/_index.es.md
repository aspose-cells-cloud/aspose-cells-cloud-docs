---
title: "Eliminar todas las formas en una hoja de cálculo de Excel"
ArticleTitle: "Eliminar todas las formas en una hoja de cálculo de Excel – Aspose.Cells Cloud API"
second_title: "Document"
linktitle: "Borrar"
type: docs
url: /es/shapes/clear/
aliases: [  /es/delete-all-shapes-inside-the-worksheet/ ]
keywords: "Aspose.Cells Cloud, Eliminar todas las formas, hoja de cálculo de Excel, REST API, SDK, cURL, .NET, Java, PHP, Ruby, Node.js, Python, Perl, Go, Android, Swift"
description: "Eliminar todas las formas de una hoja de cálculo de Excel utilizando la API REST de Aspose.Cells Cloud. La operación está disponible mediante cURL y una amplia gama de SDK (C#, Java, PHP, Ruby, Node.js, Python, Perl, Go, Android, Swift)."
weight: 40
---

Esta API REST elimina todas las formas de una hoja de cálculo de Excel.

**Requisitos previos:** Se requiere un token de acceso JWT válido. Obtenga uno a través del flujo OAuth2 de Aspose Cloud e inclúyalo en el encabezado `Authorization`, tal como se muestra en el ejemplo siguiente.

## API DeleteWorksheetShapes

```http
DELETE https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/shapes
```

### **Seguridad y autenticación**

Las API de Aspose.Cells Cloud son seguras y requieren <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">autenticación basada en token JWT</a>.

### **Parámetros de solicitud**

| Nombre del parámetro | Tipo   | Ubicación | Descripción                                   |
| -------------------- | ------ | --------- | --------------------------------------------- |
| name                 | string | path      | El nombre del documento de Excel.             |
| sheetName            | string | path      | El nombre de la hoja de cálculo.              |
| folder               | string | query     | La carpeta que contiene el documento.         |
| storageName          | string | query     | El nombre del almacenamiento donde reside el documento. |

La <a href="https://apireference.aspose.cloud/cells/#/Shapes/DeleteWorksheetShapes" rel="noopener noreferrer">Especificación OpenAPI</a> define una interfaz de programación públicamente accesible y le permite realizar interacciones REST directamente desde un navegador web.

Puede utilizar la herramienta de línea de comandos cURL para acceder fácilmente a los servicios web de Aspose.Cells. El siguiente ejemplo muestra cómo realizar una llamada a la API en la nube con cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Solicitud" tabName2="Respuesta" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/shapes" \
-X DELETE \
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

Utilizar un SDK es la mejor manera de acelerar el desarrollo. Un SDK maneja los detalles de bajo nivel, para que usted pueda centrarse en las tareas de su proyecto. Consulte el [repositorio de GitHub](https://github.com/aspose-cells-cloud) para obtener una lista completa de los SDK de Aspose.Cells Cloud.

Los siguientes ejemplos de código muestran cómo llamar a los servicios web de Aspose.Cells utilizando diversos SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleDeleteWorksheetShapes.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_DeleteWorksheetShapes.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_DeleteWorksheetShapes.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_DeleteWorksheetShapes.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_DeleteWorksheetShapes.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_DeleteWorksheetShapes.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_DeleteWorksheetShapes.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_DeleteWorksheetShapes.go" >}}

{{< /tab >}}

{{< /tabs >}}