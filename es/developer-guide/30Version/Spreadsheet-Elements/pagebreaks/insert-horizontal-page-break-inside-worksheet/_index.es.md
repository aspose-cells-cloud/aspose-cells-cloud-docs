---
title: "Agregar un salto de página horizontal"
second_title: "Documento"
linktitle: "Agregar un salto de página horizontal"
type: docs
url: /page-breaks/add-horizontal-page-break/
aliases: [/insert-horizontal-page-break-inside-worksheet/]
keywords: "salto de página horizontal, Aspose.Cells Cloud, API de Excel, REST, SDK, hoja de cálculo, cURL"
description: "Aprenda cómo agregar un salto de página horizontal a una hoja de cálculo de Excel mediante la API REST de Aspose.Cells Cloud. Incluye detalles de la solicitud, un ejemplo con cURL y fragmentos de código del SDK para múltiples lenguajes de programación."
weight: 30
ArticleTitle: "Agregar un salto de página horizontal – API de Aspose.Cells Cloud"
---

La API **Agregar un salto de página horizontal** inserta un salto de página horizontal en una hoja de cálculo de Excel.

**Requisitos previos y autenticación**  
Se requiere un token JWT válido para todas las llamadas a la API de Aspose.Cells Cloud. Obtenga el token mediante el flujo OAuth 2.0 descrito en la guía de autenticación e inclúyalo en la cabecera de la solicitud como `Authorization: Bearer <jwt token>`. El libro de trabajo objetivo debe encontrarse en una ubicación de almacenamiento accesible para la API (almacenamiento predeterminado o un `storageName` personalizado que especifique).

## API PutHorizontalPageBreak

```http
PUT https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/horizontalpagebreaks
```

### **Seguridad y autenticación**

Las API de Aspose.Cells Cloud son seguras y requieren <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">autenticación basada en token JWT</a>.

### Parámetros de solicitud

| Nombre del parámetro | Tipo    | Ubicación | Descripción                                                                 |
|----------------------|---------|-----------|-----------------------------------------------------------------------------|
| name                 | string  | path      | Nombre del archivo de Excel.                                                |
| sheetName            | string  | path      | Nombre de la hoja de cálculo donde se agregará el salto de página.         |
| cellname             | string  | query     | Referencia de celda (por ejemplo, **A1**) que marca el inicio del salto de página. |
| row                  | integer | query     | Índice de fila (base cero) del salto de página.                             |
| column               | integer | query     | Índice de columna (base cero) del salto de página.                          |
| startColumn          | integer | query     | Columna inicial de un rango al insertar un salto de página.                 |
| endColumn            | integer | query     | Columna final de un rango al insertar un salto de página.                   |
| folder               | string  | query     | Ruta de la carpeta que contiene el archivo de Excel.                        |
| storageName          | string  | query     | Nombre del almacenamiento de Aspose Cloud.                                  |

La <a href="https://apireference.aspose.cloud/cells/#/PageBreaks/PutHorizontalPageBreak" target="_blank" rel="noopener noreferrer">Especificación OpenAPI</a> define una interfaz accesible públicamente que permite realizar interacciones REST directamente desde un navegador web.

Puede utilizar la herramienta de línea de comandos **cURL** para acceder fácilmente a los servicios web de Aspose.Cells. El siguiente ejemplo muestra cómo llamar a la API con cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Solicitud" tabName2="Respuesta" >}}

{{< tab tabNum="1" >}}

```bash
# Utilice HTTPS para garantizar la comunicación cifrada
curl -v "https://api.aspose.cloud/v3.0/cells/sampleExcelPageBreaks.xlsx/worksheets/Sheet1/horizontalpagebreaks?row=18" \
  -X PUT \
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

Ejemplo de una respuesta de error cuando el token JWT no está presente o no es válido:

```json
{
  "Code": 401,
  "Status": "Unauthorized",
  "Message": "Token JWT inválido o faltante."
}
```

**Códigos de estado HTTP**

| Código | Significado                 | Descripción                                                  |
|--------|-----------------------------|--------------------------------------------------------------|
| 200    | OK                          | Filtro aplicado correctamente; la respuesta contiene detalles de la operación. |
| 400    | Solicitud incorrecta        | Parámetros faltantes o no válidos (por ejemplo, tipo de archivo no admitido). |
| 401    | No autorizado               | Token JWT inválido o faltante.                               |
| 413    | Carga útil demasiado grande | El archivo cargado excede el límite de tamaño.               |
| 500    | Error interno del servidor  | Error inesperado del servidor.                               |

Para obtener más detalles sobre operaciones relacionadas, consulte las páginas de la API para **[Obtener saltos de página horizontales](../get-horizontal-page-breaks/)** y **[Eliminar salto de página horizontal](../delete-horizontal-page-break/)**.

## Familia de SDKs en la nube

Utilizar un SDK es la forma más rápida de desarrollar. Un SDK abstracta los detalles de bajo nivel para que pueda centrarse en su proyecto. Consulte el <a href="https://github.com/aspose-cells-cloud" target="_blank" rel="noopener noreferrer">repositorio de GitHub</a> para obtener una lista completa de los SDKs de Aspose.Cells Cloud.

Los siguientes ejemplos de código muestran cómo llamar a los servicios web de Aspose.Cells mediante diversos SDKs:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePutHorizontalPageBreak.cs" >}}
{{< /tab >}}

{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PutHorizontalPageBreak.java" >}}
{{< /tab >}}

{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PutHorizontalPageBreak.php" >}}
{{< /tab >}}

{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PutHorizontalPageBreak.rb" >}}
{{< /tab >}}

{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PutHorizontalPageBreak.ts" >}}
{{< /tab >}}

{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PutHorizontalPageBreak.py" >}}
{{< /tab >}}

{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PutHorizontalPageBreak.pl" >}}
{{< /tab >}}

{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PutHorizontalPageBreak.go" >}}
{{< /tab >}}

{{< /tabs >}}