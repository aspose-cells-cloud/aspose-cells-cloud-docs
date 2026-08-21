---
---
title: Agregar Condición al Formato Condicional
description: Aprenda cómo agregar una condición al formato condicional de una hoja de cálculo mediante la API REST de Aspose.Cells Cloud (v3.0). Incluye endpoint, parámetros, autenticación, ejemplo en cURL, fragmentos de SDK y manejo de errores.
keywords: "Aspose.Cells Cloud, Formato Condicional, Agregar Condición, API REST, Excel, Hoja de Cálculo"
type: docs
url: /es/conditional-formattings/add-a-condition/
aliases:
  - /es/add-a-condition-for-format-condition/
weight: 40
---

# Agregar Condición al Formato Condicional

Agregue una condición a una regla existente de formato condicional en una hoja de cálculo mediante la API REST de Aspose.Cells Cloud (v3.0).

---

## Requisitos Previos

| Requisito | Detalles |
|-----------|----------|
| **Autenticación** | Un token de acceso JWT válido (Bearer) obtenido mediante el flujo OAuth 2.0. |
| **Versión de la API** | v3.0 – la URL del endpoint contiene `/v3.0/`. |
| **Almacenamiento** | El libro debe encontrarse en una ubicación de almacenamiento accesible para Aspose.Cells Cloud (el valor predeterminado es `Default`). |
| **Permisos** | Permiso de lectura/escritura sobre el libro de destino. |
| **Formatos admitidos** | Cualquier formato de libro admitido por Aspose.Cells (por ejemplo, `.xlsx`, `.xls`, `.xlsm`). |

---

## Endpoint

**Método HTTP:** `PUT`  
**URL:**  

```
https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/conditionalFormattings/{index}/condition
```

| Parámetro | Ubicación | Tipo | Obligatorio | Descripción |
|-----------|-----------|------|-------------|-------------|
| `name` | Ruta | string | **Sí** | Nombre del archivo del libro (incluyendo la extensión). |
| `sheetName` | Ruta | string | **Sí** | Nombre de la hoja de cálculo que contiene el formato condicional. |
| `index` | Ruta | integer | **Sí** | Índice de base cero de la colección de formato condicional que se va a modificar. |
| `type` | Consulta | string | **Sí** | Tipo de condición. Valores permitidos: `CellValue`, `Expression`, `ColorScale`, `DataBar`, `IconSet`, `Top10`, `UniqueValues`, `DuplicateValues`, `ContainsText`, `NotContainsText`, `BeginsWith`, `EndsWith`, `ContainsBlanks`, `NotContainsBlanks`, `ContainsErrors`, `NotContainsErrors`, `TimePeriod`, `AboveAverage`. |
| `operatorType` | Consulta | string | **Sí** | Operador para la condición. Valores permitidos: `Between`, `Equal`, `GreaterThan`, `GreaterOrEqual`, `LessThan`, `None`, `NotBetween`, `NotEqual`. |
| `formula1` | Consulta | string | **Sí** | Primera fórmula/valor asociado con la condición. |
| `formula2` | Consulta | string | No | Segunda fórmula/valor (requerido únicamente para operadores que necesitan dos valores, por ejemplo, `Between`). |
| `folder` | Consulta | string | No | Carpeta en el almacenamiento donde se encuentra el libro. |
| `storageName` | Consulta | string | No | Nombre del servicio de almacenamiento. |

> **Nota:** Todos los parámetros de ruta (`name`, `sheetName`, `index`) y los parámetros de consulta `type`, `operatorType`, `formula1` son obligatorios. `formula2`, `folder` y `storageName` son opcionales.

---

## Ejemplo de Solicitud (cURL)

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/conditionalFormattings/0/condition?type=CellValue&operatorType=Equal&formula1=v1&formula2=v2" \
 -X PUT \
 -H "Content-Type: application/json" \
 -H "Accept: application/json" \
 -H "Authorization: Bearer <jwt_token>"
```

*Reemplace `<jwt_token>` con un token de acceso válido y ajuste `name`, `sheetName`, `index` y los valores de consulta según sea necesario.*

---

## Respuesta Exitosa

```json
{
  "Code": "200",
  "Status": "OK"
}
```

La respuesta indica que la condición se agregó correctamente. La operación devuelve un objeto genérico `CellsCloudResponse` que contiene el código de estado HTTP y un mensaje breve de estado.

---

## Respuestas de Error

| Código HTTP | Razón | Cuerpo de Ejemplo |
|-------------|-------|-------------------|
| **400** | Solicitud Incorrecta – parámetros faltantes o inválidos. | `{ "Code":"400", "Message":"Invalid parameter value." }` |
| **401** | No Autorizado – token JWT faltante o inválido. | `{ "Code":"401", "Message":"Access token is missing or invalid." }` |
| **404** | No Encontrado – el libro, la hoja de cálculo o el índice de formato condicional no existe. | `{ "Code":"404", "Message":"File not found." }` |
| **500** | Error Interno del Servidor – fallo inesperado del servidor. | `{ "Code":"500", "Message":"An unexpected error occurred." }` |

---

## Notas y Errores Comunes

* **Codificación de Parámetros** – Codifique los caracteres especiales en `formula1`/`formula2` según URL (por ejemplo, los espacios → `%20`).  
* **Compatibilidad de Operadores** – Algunos operadores (por ejemplo, `Between`) requieren tanto `formula1` como `formula2`. Omita `formula2` para operadores que solo necesitan un único valor.  
* **Índice de Formato Condicional** – El índice es de base cero. Utilice el endpoint **Obtener Formatos Condicionales** para recuperar el índice correcto si no está seguro.  
* **Carpeta de Almacenamiento** – Si el libro se encuentra en una carpeta distinta a la predeterminada, proporcione el parámetro de consulta `folder`; de lo contrario, la API asume la carpeta raíz.  
* **Limitación de Tasa** – Aspose.Cells Cloud impone límites por cuenta para las solicitudes. Si recibe una respuesta 429, espere un breve intervalo antes de reintentar.

---

## Ejemplos de SDK

A continuación se presentan fragmentos listos para ejecutar para los SDK más populares. Reemplace los valores de marcador de posición (`YOUR_FILE`, `YOUR_SHEET`, etc.) con sus propios datos.

### C# (.NET)

```csharp
using Aspose.Cells.Cloud.SDK.Api;
using Aspose.Cells.Cloud.SDK.Model;
using System;

class Program
{
    static void Main()
    {
        var apiInstance = new ConditionalFormattingsApi();
        string name = "Book1.xlsx";
        string sheetName = "Sheet1";
        int index = 0;
        string type = "CellValue";
        string operatorType = "Equal";
        string formula1 = "v1";
        string formula2 = "v2";
        string folder = null;          // opcional
        string storageName = null;     // opcional

        try
        {
            var response = apiInstance.PutWorksheetFormatConditionCondition(
                name, sheetName, index, type, operatorType, formula1, formula2, folder, storageName);
            Console.WriteLine($"Status: {response.Status}");
        }
        catch (Exception e)
        {
            Console.WriteLine("Exception when calling ConditionalFormattingsApi.PutWorksheetFormatConditionCondition: " + e.Message);
        }
    }
}
```

### Java

```java
import com.aspose.cloud.cells.api.ConditionalFormattingsApi;
import com.aspose.cloud.cells.model.CellsCloudResponse;

public class AddConditionExample {
    public static void main(String[] args) {
        ConditionalFormattingsApi api = new ConditionalFormattingsApi();

        String name = "Book1.xlsx";
        String sheetName = "Sheet1";
        int index = 0;
        String type = "CellValue";
        String operatorType = "Equal";
        String formula1 = "v1";
        String formula2 = "v2";

        try {
            CellsCloudResponse resp = api.putWorksheetFormatConditionCondition(
                    name, sheetName, index, type, operatorType, formula1, formula2, null, null);
            System.out.println("Response: " + resp.getStatus());
        } catch (Exception e) {
            e.printStackTrace();
        }
    }
}
```

### Node.js

```javascript
const { ConditionalFormattingsApi, ApiClient } = require('asposecellscloud');
const api = new ConditionalFormattingsApi();

const name = "Book1.xlsx";
const sheetName = "Sheet1";
const index = 0;
const type = "CellValue";
const operatorType = "Equal";
const formula1 = "v1";
const formula2 = "v2";

api.putWorksheetFormatConditionCondition(
    name,
    sheetName,
    index,
    type,
    operatorType,
    formula1,
    formula2,
    null,
    null
).then((response) => {
    console.log('Status:', response.body.Status);
}).catch((err) => {
    console.error(err);
});
```

### Ruby

```ruby
require 'aspose_cells_cloud'

api_instance = AsposeCellsCloud::ConditionalFormattingsApi.new
name = 'Book1.xlsx'
sheet_name = 'Sheet1'
index = 0
type = 'CellValue'
operator_type = 'Equal'
formula1 = 'v1'
formula2 = 'v2'

begin
  result = api_instance.put_worksheet_format_condition_condition(
    name, sheet_name, index, type, operator_type, formula1, formula2, nil, nil
  )
  puts "Status: #{result.status}"
rescue AsposeCellsCloud::ApiError => e
  puts "Exception when calling ConditionalFormattingsApi->put_worksheet_format_condition_condition: #{e}"
end
```

### Perl

```perl
use AsposeCellsCloud::ConditionalFormattingsApi;

my $api_instance = AsposeCellsCloud::ConditionalFormattingsApi->new();

my $name         = 'Book1.xlsx';
my $sheet_name   = 'Sheet1';
my $index        = 0;
my $type         = 'CellValue';
my $operatorType = 'Equal';
my $formula1     = 'v1';
my $formula2     = 'v2';

eval {
    my $result = $api_instance->put_worksheet_format_condition_condition(
        name => $name,
        sheet_name => $sheet_name,
        index => $index,
        type => $type,
        operator_type => $operatorType,
        formula1 => $formula1,
        formula2 => $formula2,
        folder => undef,
        storage_name => undef
    );
    print "Status: " . $result->{status} . "\n";
};
if ($@) {
    warn "Exception when calling ConditionalFormattingsApi->put_worksheet_format_condition_condition: $@\n";
}
```

### Go

```go
package main

import (
    "fmt"
    "github.com/asposecellscloud/aspose-cells-cloud-go/v3/sdk"
)

func main() {
    cfg := sdk.NewConfiguration()
    cfg.AccessToken = "YOUR_JWT_TOKEN"
    api := sdk.NewConditionalFormattingsApi(cfg)

    name := "Book1.xlsx"
    sheetName := "Sheet1"
    index := int32(0)
    condType := "CellValue"
    operatorType := "Equal"
    formula1 := "v1"
    formula2 := "v2"

    resp, _, err := api.PutWorksheetFormatConditionCondition(
        name, sheetName, index, condType, operatorType, formula1, formula2, nil, nil,
    )
    if err != nil {
        fmt.Printf("Error: %v\n", err)
        return
    }
    fmt.Printf("Status: %s\n", resp.Status)
}
```

> **SDK no disponibles** – Si necesita un lenguaje que no aparece listado aquí, consulte la **Referencia de la API** genérica y construya manualmente la solicitud HTTP.

---

## Consulte También

- **[Obtener Formatos Condicionales](https://docs.aspose.cloud/cells/conditional-formattings/get-conditional-formattings/)** – Recupera la lista de reglas de formato condicional para una hoja de cálculo.  
- **[Eliminar Formato Condicional](https://docs.aspose.cloud/cells/conditional-formattings/delete-a-conditional-formatting/)** – Elimina una regla de formato condicional existente.  
- **[Especificación OpenAPI](https://apireference.aspose.cloud/cells/#/ConditionalFormattings/PutWorksheetFormatConditionCondition)** – Definición completa legible por máquinas para esta operación.  

---