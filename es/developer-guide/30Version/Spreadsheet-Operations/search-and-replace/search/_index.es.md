---
title: "Buscar texto en archivos de Excel – API de Aspose.Cells Cloud"
description: "Busque texto específico en archivos de Excel (XLS, XLSX, XLSM, XLSB) y archivos ODS mediante la API de Aspose.Cells Cloud. Incluye detalles de la solicitud, ejemplos de cURL y SDK, y manejo de errores."
keywords: "Aspose.Cells, Excel, búsqueda, API, REST"
type: docs
url: /cells/search/
aliases:
  - /search/
  - /search-without-using-storage/
  - /search-without-storage/
weight: 50
---

# Buscar texto en archivos de Excel – API de Aspose.Cells Cloud

## Descripción general
Aspose.Cells Cloud proporciona un extremo **POST** que busca una cadena de texto específica dentro de libros de Excel (XLS, XLSX, XLSM, XLSB) y archivos de hojas de cálculo OpenDocument (ODS). La API devuelve cada celda que contiene el texto solicitado junto con un enlace a la hoja de cálculo donde se encontró la coincidencia.

> **Casos de uso**  
> - Validar que un valor específico existe en un informe antes de procesarlo adicionalmente.  
> - Crear una herramienta rápida de "buscar y reemplazar" que primero enumere todas las ocurrencias.  
> - Generar un índice de términos clave en un lote de hojas de cálculo.

---

## Requisitos previos
| Requisito | Detalles |
|-----------|----------|
| **Autenticación** | Token JWT obtenido mediante el flujo OAuth de Aspose Cloud. El token debe incluir el ámbito **Cells**. |
| **Formatos compatibles** | XLS, XLSX, XLSM, XLSB, ODS |
| **Tamaño máximo de archivo** | 150 MB (comprimido). Los archivos más grandes devuelven **413 Payload Too Large**. |
| **Encabezados necesarios** | `Authorization: Bearer <jwt-token>`  <br> `Accept: application/json` |
| **Permisos** | El token debe tener permiso de *lectura* en el almacenamiento destino (si se utiliza almacenamiento remoto); no es necesario cuando el archivo se carga como `multipart/form-data`. |

*Consejo:* Utilice el extremo **/connect/token** para generar un token JWT. Consulte la [Guía de autenticación](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/) para más detalles.

---

## Extremo

| Elemento | Valor |
|----------|-------|
| **Método HTTP** | `POST` |
| **URL** | `https://api.aspose.cloud/v3.0/cells/search` |
| **Propósito** | Buscar texto especificado dentro de un libro de Excel cargado. |
| **Seguridad** | Token JWT (Bearer) – consulte *Requisitos previos* anteriormente. |

---

### **Seguridad y autenticación**

Las API de Aspose.Cells Cloud son seguras y requieren <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">autenticación basada en token JWT</a>.

## Parámetros de la solicitud

| Nombre | Tipo | Ubicación | Obligatorio | Descripción |
|--------|------|-----------|-------------|-------------|
| `file` | **archivo** | `formData` (multipart) | **Sí** | El archivo de hoja de cálculo para cargar. |
| `text` | **cadena** | Cadena de consulta | **Sí** | La cadena de texto que se va a buscar. |
| `password` | **cadena** | Cadena de consulta | No | Contraseña para abrir un libro protegido, si es necesario. |
| `sheetname` | **cadena** | Cadena de consulta | No | Nombre de la hoja de cálculo en la que limitar la búsqueda. Si se omite, se buscan todas las hojas de cálculo. |
| `checkExcelRestriction` | **booleano** | Cadena de consulta | No (predeterminado: `true`) | Cuando es `true`, la API valida las restricciones específicas de Excel (por ejemplo, celdas de solo lectura) antes de realizar la búsqueda. |

---

## Ejemplo de solicitud (cURL)

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/search?text=Invoice&sheetname=Sheet1" \
  -X POST \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt-token>" \
  -F "file=@InvoiceReport.xlsx"
```

*Sustituya `<jwt-token>` por un token válido y ajuste los parámetros de consulta según sea necesario.*

---

## Respuesta correcta

**HTTP 200 – Búsqueda exitosa; la respuesta contiene los elementos de texto encontrados.**

```json
{
  "Status": "OK",
  "Code": 200,
  "TextItems": {
    "link": {
      "Href": "string",
      "Rel": "string",
      "Title": "string",
      "Type": "string"
    },
    "TextItemList": [
      {
        "Text": "Invoice #12345",
        "link": {
          "Href": "InvoiceReport.xlsx/worksheets/Sheet1",
          "Rel": "parent",
          "Title": "Sheet1",
          "Type": "string"
        }
      },
      {
        "Text": "Invoice #12346",
        "link": {
          "Href": "InvoiceReport.xlsx/worksheets/Sheet1",
          "Rel": "parent",
          "Title": "Sheet1",
          "Type": "string"
        }
      }
    ]
  }
}
```

### Campos de la respuesta

| Campo | Tipo | Descripción |
|-------|------|-------------|
| `Status` | cadena | Estado general de la solicitud (`OK` para éxito). |
| `Code` | entero | Código de estado HTTP (200). |
| `TextItems.link` | objeto | Enlace hipermédia al recurso de colección. |
| `TextItems.TextItemList` | matriz | Lista de coincidencias. Cada elemento contiene: |
| `Text` | cadena | El valor de la celda que coincidió con el texto buscado. |
| `link` | objeto | Enlace hipertexto a la hoja de cálculo donde se encontró la coincidencia (`Href` apunta a `Workbook/worksheets/SheetName`). |

---

## Respuestas de error

| Código HTTP | Significado | Causa típica | Cuerpo de ejemplo |
|-------------|-------------|--------------|-------------------|
| **400** | Solicitud incorrecta | Falta de parámetros obligatorios, tipo de archivo no admitido o valores de consulta inválidos. | `{ "Status":"Error","Code":400,"Message":"El parámetro de consulta 'text' es obligatorio." }` |
| **401** | No autorizado | Token JWT ausente o inválido. | `{ "Status":"Error","Code":401,"Message":"Token de acceso inválido o caducado." }` |
| **413** | Carga demasiado grande | El archivo cargado excede el límite de 150 MB. | `{ "Status":"Error","Code":413,"Message":"El tamaño del archivo supera el límite permitido." }` |
| **500** | Error interno del servidor | Problema inesperado del lado del servidor. | `{ "Status":"Error","Code":500,"Message":"Se produjo un error inesperado." }` |

---

## Ejemplos de SDK

A continuación se presentan fragmentos mínimos de código para la operación **PostSearch** utilizando los SDK oficiales de Aspose.Cells Cloud. Sustituya `YOUR_JWT_TOKEN` y la ruta del archivo por sus propios valores.

### C# (.NET)

```csharp
using Aspose.Cells.Cloud.SDK.Api;
using Aspose.Cells.Cloud.SDK.Model;
using System;
using System.IO;

class Program
{
    static void Main()
    {
        var config = new Configuration
        {
            AccessToken = "YOUR_JWT_TOKEN",
            BaseUrl = "https://api.aspose.cloud"
        };
        var cellsApi = new CellsApi(config);

        using var stream = File.OpenRead("InvoiceReport.xlsx");
        var result = cellsApi.PostSearch(
            file: stream,
            text: "Invoice",
            sheetname: "Sheet1",
            password: null,
            checkExcelRestriction: true
        );

        foreach (var item in result.TextItems.TextItemList)
        {
            Console.WriteLine($"{item.Text}  ->  {item.Link.Href}");
        }
    }
}
```

### Java

```java
import com.aspose.cells.cloud.sdk.api.CellsApi;
import com.aspose.cells.cloud.sdk.model.*;
import java.io.File;

public class PostSearchDemo {
    public static void main(String[] args) throws Exception {
        CellsApi api = new CellsApi("YOUR_JWT_TOKEN");
        File file = new File("InvoiceReport.xlsx");

        TextItemsResponse response = api.postSearch(
                file,
                "Invoice",
                null,          // password
                "Sheet1",      // sheetname
                true           // checkExcelRestriction
        );

        response.getTextItems().getTextItemList()
                .forEach(item -> System.out.println(item.getText() + " -> " + item.getLink().getHref()));
    }
}
```

### Python

```python
import asposecellscloudsdk
from asposecellscloudsdk import CellsApi, ApiException, Configuration
from asposecellscloudsdk.models import TextItemsResponse
import pathlib

config = Configuration()
config.access_token = "YOUR_JWT_TOKEN"
config.host = "https://api.aspose.cloud"

api_instance = CellsApi(configuration=config)

file_path = pathlib.Path("InvoiceReport.xlsx")
with open(file_path, "rb") as f:
    result: TextItemsResponse = api_instance.post_search(
        file=f,
        text="Invoice",
        password=None,
        sheetname="Sheet1",
        check_excel_restriction=True
    )

for item in result.text_items.text_item_list:
    print(f"{item.text} -> {item.link.href}")
```

### Node.js (TypeScript)

```typescript
import { CellsApi, Configuration } from "@asposecells-cloud/sdk";

const config = new Configuration({
    accessToken: "YOUR_JWT_TOKEN",
    basePath: "https://api.aspose.cloud"
});

const api = new CellsApi(config);

api.postSearch({
    file: fs.createReadStream("InvoiceReport.xlsx"),
    text: "Invoice",
    sheetname: "Sheet1",
    checkExcelRestriction: true
}).then(response => {
    response.textItems?.textItemList?.forEach(item => {
        console.log(`${item.text} -> ${item.link?.href}`);
    });
}).catch(err => console.error(err));
```

*(Los SDK para PHP, Ruby, Go y Perl están disponibles en el [repositorio de GitHub de Aspose.Cells Cloud](https://github.com/aspose-cells-cloud).)*

---

## Notas adicionales

- **`checkExcelRestriction`** tiene como valor predeterminado `true`. Establézcalo en `false` únicamente si está seguro de que el libro no contiene celdas protegidas que puedan interferir con la búsqueda.
- La API devuelve **enlaces hipermédia** (`Href`) que pueden utilizarse con otros extremos de Aspose.Cells (por ejemplo, para descargar la hoja de cálculo o recuperar el formato de celda).
- Al buscar en libros grandes, considere limitar el ámbito con el parámetro `sheetname` para mejorar el tiempo de respuesta.

---

## Enlaces relacionados

- **Guía de autenticación** – <https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/>
- **Especificación OpenAPI para PostSearch** – <https://apireference.aspose.cloud/cells/#/LightCells/PostSearch>
- **SDK de Aspose.Cells Cloud** – <https://github.com/aspose-cells-cloud>
- **Límites y cuotas** – <https://docs.aspose.cloud/total/getting-started/limits/>

---