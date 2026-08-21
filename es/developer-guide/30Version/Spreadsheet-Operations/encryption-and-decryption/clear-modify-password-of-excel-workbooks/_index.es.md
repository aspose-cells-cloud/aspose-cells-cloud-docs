---
title: "Quitar la protección de escritura (contraseña) de un libro de Excel"
second_title: "Documento"
linktitle: "Eliminar la contraseña de archivos de Excel"
type: docs
url: /clear-excel-files-password/
aliases:
  [
    /clear-modify-password-of-excel-workbooks/,
    /workbook/clear-modify-password/，/workbook/password/clear/,
  ]
keywords: "Aspose.Cells, Excel, eliminación de contraseña, protección de escritura, API REST, ejemplos de SDK"
description: "Aprenda cómo eliminar la protección de escritura (contraseña) de un libro de Excel mediante la API REST de Aspose.Cells Cloud. Incluye un ejemplo con cURL, pasos de autenticación y ejemplos de código SDK."
weight: 110
ArticleTitle: "Quitar la protección de escritura (contraseña) de un libro de Excel"
---

Esta API REST elimina la **protección de escritura (contraseña)** de un libro de Excel, lo que le permite **quitar la protección por contraseña de Excel** mediante programación.

**Requisitos previos:** Obtenga un token JWT válido, asegúrese de que el libro esté almacenado en una ubicación compatible con el almacenamiento y utilice la versión de la API v3.0.

Para agregar protección, consulte la guía [Proteger Excel](/cells/protect/).

## API DeleteDocumentUnprotectFromChanges

```http
DELETE https://api.aspose.cloud/v3.0/cells/{name}/writeProtection
```

### **Seguridad y autenticación**

Las API de Aspose.Cells Cloud son seguras y requieren <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">autenticación basada en token JWT</a>.

### **Parámetros de la solicitud**

| Nombre del parámetro | Tipo   | Ubicación | Descripción                                         |
| --------------------- | ------ | --------- | --------------------------------------------------- |
| `name`               | string | path      | El nombre del libro de Excel.                       |
| `folder`             | string | query     | La carpeta que contiene el libro (opcional).        |
| `storageName`        | string | query     | El nombre del servicio de almacenamiento (opcional).|


### Respuesta

```json
{
  "Status":"OK",
  "Code":200
}
```

**Códigos de estado HTTP**

| Código | Significado                 | Descripción                                             |
|--------|-----------------------------|---------------------------------------------------------|
| 200    | OK                          | Filtro aplicado correctamente; la respuesta contiene los detalles de la operación. |
| 400    | Solicitud incorrecta        | Parámetros faltantes o no válidos (por ejemplo, tipo de archivo no admitido). |
| 401    | No autorizado               | Token JWT no válido o faltante.                         |
| 413    | Payload demasiado grande     | El archivo cargado excede el límite de tamaño.          |
| 500    | Error interno del servidor  | Error inesperado en el servidor.                        |

## Cómo usar la API DeleteDocumentUnprotectFromChanges con SDK

### Especificación de la API DeleteDocumentUnprotectFromChanges

La [Especificación OpenAPI](https://apireference.aspose.cloud/cells/#/Workbook/DeleteDocumentUnprotectFromChanges) define una interfaz de programación accesible públicamente y permite realizar interacciones REST directamente desde un navegador web.

Puede utilizar la herramienta de línea de comandos cURL para acceder fácilmente a los servicios de Aspose.Cells. El siguiente ejemplo muestra cómo realizar una llamada a la API REST con cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Solicitud" tabName2="Respuesta" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Sample_Test_Book.xlsx/writeProtection" \
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


### Utilizar los SDK de Aspose.Cells Cloud

Utilizar un SDK es la mejor forma de acelerar el desarrollo. Un SDK maneja los detalles de bajo nivel, por lo que usted puede centrarse en las tareas de su proyecto. Consulte el [repositorio de GitHub](https://github.com/aspose-cells-cloud) para obtener una lista completa de los SDK de Aspose.Cells Cloud.

Los siguientes ejemplos de código muestran cómo llamar a los servicios web de Aspose.Cells mediante diversos SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleDeleteDocumentUnprotectFromChanges.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_DeleteDocumentUnprotectFromChanges.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_DeleteDocumentUnprotectFromChanges.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_DeleteDocumentUnprotectFromChanges.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2b4189bc27ae92abf73c36b4df0" "Example_DeleteDocumentUnprotectFromChanges.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_DeleteDocumentUnprotectFromChanges.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_DeleteDocumentUnprotectFromChanges.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_DeleteDocumentUnprotectFromChanges.go" >}}

{{< /tab >}}

{{< /tabs >}}