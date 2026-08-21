---
title: "Agregar un objeto OLE en una hoja de cálculo de Excel"
second_title: "Documento"
linktitle: "Agregar objeto OLE"
type: docs
url: /es/oleobjects/add/
aliases: [  /es/add-oleobject-to-excel-worksheet/ ]
keywords: "Agregar objeto OLE, Excel, Aspose.Cells Cloud, API REST, SDK"
description: "Use la API REST de Aspose.Cells Cloud para agregar objetos OLE a hojas de cálculo de Excel. La API puede llamarse directamente o a través de SDKs para C#, Java, PHP, Ruby, Node.js, Python, Perl y Go."
ArticleTitle: "Agregar objeto OLE a una hoja de cálculo de Excel con la API de Aspose.Cells Cloud"
weight: 20
---

La API de Aspose.Cells Cloud permite manipular programáticamente libros de Excel, incluida la capacidad de incrustar objetos OLE (por ejemplo, documentos de Word, PDF u otros archivos binarios) directamente en una hoja de cálculo.

Esta API REST agrega un **objeto OLE** a una hoja de cálculo de Excel.

**Prerrequisitos** – Debe tener un token de autenticación JWT válido, y cualquier archivo de origen referenciado por `oleFile` o `imageFile` debe cargarse previamente en la ubicación de almacenamiento especificada antes de invocar el punto de conexión.

## API PutWorksheetOleObject

```http
PUT https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/oleobjects
```

### **Seguridad y autenticación**

Las API de Aspose.Cells Cloud son seguras y requieren <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">autenticación basada en token JWT</a>.

### Parámetros de solicitud

| Nombre del parámetro | Tipo    | Ubicación | Descripción                                      |
|----------------------|---------|-----------|--------------------------------------------------|
| name                 | string  | path      | Nombre del archivo del libro.                    |
| sheetName            | string  | path      | Nombre de la hoja de cálculo.                    |
| oleObject            | object  | body      | Definición del objeto OLE.                       |
| upperLeftRow         | integer | query     | Índice de fila de la esquina superior izquierda (predeterminado: 0). |
| upperLeftColumn      | integer | query     | Índice de columna de la esquina superior izquierda (predeterminado: 0). |
| height               | integer | query     | Altura del objeto OLE (predeterminado: 0).       |
| width                | integer | query     | Ancho del objeto OLE (predeterminado: 0).        |
| oleFile              | string  | query     | Nombre del archivo fuente OLE.                   |
| imageFile            | string  | query     | Nombre del archivo de imagen de vista previa.   |
| folder               | string  | query     | Carpeta que contiene el libro.                   |
| storageName          | string  | query     | Nombre del almacenamiento a utilizar.            |

**Notas** – `upperLeftRow` y `upperLeftColumn` usan indexación basada en cero. El archivo `oleFile` (y opcionalmente `imageFile`) debe existir previamente en el almacenamiento de destino; de lo contrario, la solicitud devolverá un error.

La [Especificación OpenAPI](https://apireference.aspose.cloud/cells/#/OleObjects/PutWorksheetOleObject) define una interfaz de programación públicamente accesible y permite realizar interacciones REST directamente desde un navegador web.

Puede usar la herramienta de línea de comandos **cURL** para llamar a los servicios web de Aspose.Cells. El ejemplo siguiente muestra cómo agregar un objeto OLE con cURL. **Se requiere HTTPS para todas las llamadas en producción.**

{{< tabs tabTotal="2" tabID="1" tabName1="Solicitud" tabName2="Respuesta" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/oleobjects" \
  -X PUT \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>" \
  -d '{"ImageSourceFullName":"aspose-logo.png", "IsAutoSize":true, "SourceFullName":"Sample_Book2.xls", "UpperLeftRow":15, "Top":10, "UpperLeftColumn":5, "Left":10, "Width":400, "Height":400}'
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

![Captura de pantalla que muestra un objeto OLE incrustado en una hoja de cálculo de Excel](/cells/images/ole-object-example.png)

**Códigos de estado HTTP posibles**

| Código | Descripción                                       |
|--------|---------------------------------------------------|
| 200    | Objeto OLE agregado correctamente.               |
| 400    | Solicitud incorrecta: parámetros faltantes o no válidos. |
| 401    | No autorizado: token JWT inválido o faltante.    |
| 404    | No encontrado: el libro, la hoja de cálculo o el archivo de origen no existe. |
| 500    | Error interno del servidor: fallo inesperado.    |

Una respuesta correcta típica devuelve la siguiente carga JSON:

```json
{
  "Code": 200,
  "Status": "OK",
  "Data": {
    "OleObjectId": "12345",
    "UpperLeftRow": 15,
    "UpperLeftColumn": 5,
    "Width": 400,
    "Height": 400,
    "SourceFullName": "Sample_Book2.xls",
    "ImageSourceFullName": "aspose-logo.png"
  }
}
```

## Familia de SDK en la nube

Usar un SDK acelera el desarrollo. Un SDK abstracta los detalles de bajo nivel, permitiéndole centrarse en su lógica de negocio. Consulte el [repositorio de GitHub](https://github.com/aspose-cells-cloud) para obtener una lista completa de los SDK de Aspose.Cells Cloud.

Los siguientes ejemplos de código muestran cómo invocar los servicios web de Aspose.Cells mediante diversos SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePutWorksheetOleObject.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PutWorksheetOleObject.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PutWorksheetOleObject.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PutWorksheetOleObject.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PutWorksheetOleObject.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PutWorksheetOleObject.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PutWorksheetOleObject.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PutWorksheetOleObject.go" >}}

{{< /tab >}}

{{< /tabs >}}