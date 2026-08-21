---
title: "Aspose.Cells Cloud Web API: Extraer texto"
second_title: "Aspose.Cells Cloud – Código abreviado en línea"
linktitle: "Extraer texto"
type: docs
url: /es/extract-text/
keywords: "Aspose.Cells Cloud, extraer texto, API de Excel, extracción de texto de celdas, API REST"
description: "Extrae subcadenas, números o caracteres de celdas de Excel mediante la API de Aspose.Cells Cloud. Admite extracción basada en texto anterior/posterior, extracción basada en posición y salida directa en un nuevo rango."
weight: 100
ArticleTitle: "Documentación de la API de Aspose.Cells Cloud para extraer texto"
---

Extrae subcadenas, caracteres o números de una celda de hoja de cálculo hacia otra celda, eliminando la necesidad de fórmulas complejas como FIND, MIN, LEFT o RIGHT.

## **API ExtractText**

```http
PUT https://api.aspose.cloud/v4.0/cells/content/extract/text
```

### **Seguridad y autenticación**

Las API de Aspose.Cells Cloud son seguras y requieren <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">autenticación basada en token JWT</a>.

```bash
-H "Authorization: Bearer {access_token}"
```

### Parámetros de solicitud de la API **extractText**

| Nombre del parámetro | Tipo    | Ubicación           | Descripción                                                                                                                     |
|----------------------|---------|---------------------|---------------------------------------------------------------------------------------------------------------------------------|
| Spreadsheet          | File    | FormData            | Carga el archivo de hoja de cálculo.                                                                                            |
| extractTextType      | String  | Query               | Enum que indica el modo de extracción. Valores permitidos: `Before`, `After`, `BeforePosition`, `AfterPosition`.               |
| beforeText           | String  | Query               | Texto que debe aparecer **antes** de la subcadena extraída. Se utiliza cuando `extractTextType=Before`.                          |
| afterText            | String  | Query               | Texto que debe aparecer **después** de la subcadena extraída. Se utiliza cuando `extractTextType=After`.                         |
| beforePosition       | Integer | Query               | Número de caracteres a devolver desde el lado izquierdo de la celda. Se utiliza cuando `extractTextType=BeforePosition`.        |
| afterPosition        | Integer | Query               | Número de caracteres a devolver desde el lado derecho de la celda. Se utiliza cuando `extractTextType=AfterPosition`.           |
| outPositionRange     | String  | Query               | Rango de destino (por ejemplo, `Sheet1!A1`) donde se escribirá el texto extraído.                                               |
| worksheet            | String  | Query               | Nombre de la hoja de cálculo que contiene la celda de origen.                                                                   |
| range                | String  | Query               | Celda o rango de origen (por ejemplo, `A1`).                                                                                    |
| outPath              | String  | Query _(Opcional)_  | Ruta de carpeta en el almacenamiento donde se guardará el libro resultante. Si se omite, el resultado se devuelve en el cuerpo de la respuesta. |
| outStorageName       | String  | Query               | Nombre del almacenamiento que se utilizará para el archivo de salida.                                                           |
| region               | String  | Query               | Configuración regional de la hoja de cálculo (por ejemplo, `US`, `EU`).                                                          |
| password             | String  | Query               | Contraseña para abrir un libro protegido.                                                                                       |

**Solicitud cURL de ejemplo**

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/content/extract/text?extractTextType=Before&beforeText=Total&outPositionRange=Sheet1!B1&worksheet=Sheet1&range=A1" \
     -H "Authorization: Bearer {access_token}" \
     -F "Spreadsheet=@Sample.xlsx"
```

### **Respuesta**

Cuando la solicitud se completa correctamente, la API devuelve una carga útil JSON que contiene el texto extraído y la dirección de la celda donde se escribió:

```json
[
  {
    "Name": "ResponseFile",
    "DataType": {
      "Identifier": "File",
      "Reference": "Stream"
    }
  }
]
```

Si se proporciona el parámetro `outPath`, la respuesta contiene únicamente un mensaje de estado; el libro se escribe en la ubicación especificada.

**Respuesta de ejemplo cuando se omite `outPath`**

```json
{
  "Code": 200,
  "Status": "OK"
}
```

### Códigos de error

- **200 OK** – Extracción completada correctamente.  
- **202 Accepted** – Solicitud aceptada para procesamiento asíncrono.  
- **400 Bad Request** – URI de la API de Aspose.Cells Cloud no válido o parámetros obligatorios ausentes.  
- **401 Unauthorized** – Token de acceso, ID de cliente o secreto de cliente no válido.  
- **404 Not Found** – No se puede acceder al archivo de hoja de cálculo especificado.  
- **500 Server Error** – Se produjo un error inesperado al procesar el libro.

## Especificación OpenAPI

La [Especificación OpenAPI](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/TextProcessing/ExtractText) define una interfaz de programación accesible públicamente y permite realizar interacciones REST directamente desde un navegador web.

### Utilizar los SDK de Aspose.Cells Cloud

Utilizar el SDK es la mejor manera de acelerar el desarrollo. El SDK gestiona los detalles subyacentes, permitiéndole implementar simplemente la funcionalidad **Extraer texto** para celdas con un código mínimo. Consulte el [repositorio de GitHub](https://github.com/aspose-cells-cloud) para obtener una lista completa de los SDK de Aspose.Cells Cloud.

Los siguientes ejemplos de código muestran cómo realizar llamadas a los servicios web de Aspose.Cells mediante diversos SDK:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{<tab tabNum="1" >}}

```csharp
// Ejemplo en C# – extraer texto (código omitido para brevedad)
```

{{</tab>}}

{{<tab tabNum="2" >}}

```java
// Ejemplo en Java – extraer texto (código omitido para brevedad)
```

{{</tab>}}

{{<tab tabNum="3" >}}

```php
// Ejemplo en PHP – extraer texto (código omitido para brevedad)
```

{{</tab>}}

{{<tab tabNum="4" >}}

```ruby
# Ejemplo en Ruby – extraer texto (código omitido para brevedad)
```

{{</tab>}}

{{<tab tabNum="5" >}}

```javascript
// Ejemplo en Node.js – extraer texto (código omitido para brevedad)
```

{{</tab>}}

{{<tab tabNum="6" >}}

```python
# Ejemplo en Python – extraer texto (código omitido para brevedad)
```

{{</tab>}}

{{<tab tabNum="7" >}}

```perl
# Ejemplo en Perl – extraer texto (código omitido para brevedad)
```

{{</tab>}}

{{<tab tabNum="8" >}}

```go
// Ejemplo en Go – extraer texto (código omitido para brevedad)
```

{{</tab>}}

{{< /tabs >}}