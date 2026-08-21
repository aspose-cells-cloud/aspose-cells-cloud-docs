---
title: "Cómo trabajar con la visibilidad en una hoja de cálculo de Excel"
second_title: "Documento"
linktitle: "Visibilidad"
type: docs
url: /worksheets/panes/
keywords: "Aspose.Cells Cloud, API para ocultar hoja de cálculo, API para mostrar hoja de cálculo, visibilidad de hojas de cálculo de Excel, API REST de Excel, Aspose.Cells v3.0"
description: "Aprenda a ocultar o mostrar programáticamente hojas de cálculo de Excel mediante la API REST de Aspose.Cells Cloud. Incluye URLs de solicitud, ejemplos de cURL y .NET SDK, manejo de errores y notas específicas por versión."
weight: 20
---

## Trabajo con visibilidad en una hoja de cálculo de Excel

La *visibilidad de hoja de cálculo* define si una hoja se muestra al usuario final. Con Aspose.Cells Cloud puede ocultar o mostrar una hoja de cálculo mediante una llamada REST sencilla. Los puntos de conexión de la API utilizados son:

* **Ocultar una hoja de cálculo**: `PUT /cells/{fileName}/worksheets/{sheetName}/visibility`  
* **Mostrar una hoja de cálculo**: `PUT /cells/{fileName}/worksheets/{sheetName}/visibility`

> **Versión de API admitida**: **v3.0** (a partir de marzo de 2026)

### Requisitos previos
1. Una cuenta activa de **Aspose.Cells Cloud**.  
2. Un **ID de cliente** y un **secreto de cliente** válidos (o un token de acceso OAuth 2.0).  
3. El libro (`{fileName}`) ya debe estar cargado en el almacenamiento en la nube de Aspose.  

---

## Ocultar una hoja de cálculo

### Solicitud
```http
PUT https://api.aspose.cloud/v3.0/cells/{fileName}/worksheets/{sheetName}/visibility
Authorization: Bearer {access_token}
Content-Type: application/json

{
  "Visible": false
}
```

### Respuesta
```json
{
  "Code": 200,
  "Status": "OK",
  "Worksheet": {
    "Name": "{sheetName}",
    "Index": 2,
    "Visible": false
  }
}
```

### Ejemplo de cURL
```bash
curl -X PUT "https://api.aspose.cloud/v3.0/cells/MyWorkbook.xlsx/worksheets/Sheet2/visibility" \
     -H "Authorization: Bearer YOUR_ACCESS_TOKEN" \
     -H "Content-Type: application/json" \
     -d '{ "Visible": false }'
```

### Ejemplo de .NET SDK
```csharp
var api = new CellsApi("client_id", "client_secret");
var request = new Visibility { Visible = false };
var response = api.PutWorksheetVisibility("MyWorkbook.xlsx", "Sheet2", request);
Console.WriteLine($"Hoja de cálculo oculta: {response.Worksheet.Visible}");
```

### Errores comunes
| Código HTTP | Descripción                              | Solución                                               |
|-------------|------------------------------------------|--------------------------------------------------------|
| 400         | Cuerpo JSON no válido o falta `Visible` | Asegúrese de que el cuerpo de la solicitud sea JSON válido y contenga la clave. |
| 401         | No autorizado – token ausente o caducado | Actualice el token OAuth y inclúyalo en la cabecera. |
| 404         | Hoja de cálculo o archivo no encontrado | Verifique que `{fileName}` y `{sheetName}` sean correctos. |
| 409         | Hoja de cálculo ya oculta                | Compruebe la visibilidad actual antes de enviar la solicitud. |

---

## Mostrar una hoja de cálculo

### Solicitud
```http
PUT https://api.aspose.cloud/v3.0/cells/{fileName}/worksheets/{sheetName}/visibility
Authorization: Bearer {access_token}
Content-Type: application/json

{
  "Visible": true
}
```

### Respuesta
```json
{
  "Code": 200,
  "Status": "OK",
  "Worksheet": {
    "Name": "{sheetName}",
    "Index": 2,
    "Visible": true
  }
}
```

### Ejemplo de cURL
```bash
curl -X PUT "https://api.aspose.cloud/v3.0/cells/MyWorkbook.xlsx/worksheets/Sheet2/visibility" \
     -H "Authorization: Bearer YOUR_ACCESS_TOKEN" \
     -H "Content-Type: application/json" \
     -d '{ "Visible": true }'
```

### Ejemplo de .NET SDK
```csharp
var api = new CellsApi("client_id", "client_secret");
var request = new Visibility { Visible = true };
var response = api.PutWorksheetVisibility("MyWorkbook.xlsx", "Sheet2", request);
Console.WriteLine($"Hoja de cálculo visible: {response.Worksheet.Visible}");
```

### Errores comunes
| Código HTTP | Descripción                              | Solución                                               |
|-------------|------------------------------------------|--------------------------------------------------------|
| 400         | Cuerpo JSON no válido o falta `Visible` | Proporcione una carga JSON correcta con `"Visible": true`. |
| 401         | No autorizado – token ausente o caducado | Regenere el token de acceso e inténtelo de nuevo.     |
| 404         | Hoja de cálculo o archivo no encontrado | Confirme que el nombre del archivo y de la hoja existen en el almacenamiento. |
| 409         | Hoja de cálculo ya visible               | No se requiere ninguna acción; la hoja ya está mostrada. |

---

## Operaciones relacionadas
> *Fijar paneles* | *Dividir paneles* | *Zoom* – consulte las páginas correspondientes para obtener controles adicionales de diseño de hoja de cálculo.

---

## Preguntas frecuentes

<dl>
  <dt>¿Cómo oculto una hoja de cálculo mediante la API de Aspose.Cells Cloud?</dt>
  <dd>Envíe una solicitud `PUT` a `/cells/{fileName}/worksheets/{sheetName}/visibility` con el cuerpo JSON `{ "Visible": false }`. Incluya un token portador OAuth 2.0 válido. Una respuesta `200 OK` devuelve el objeto de hoja de cálculo actualizado.</dd>

  <dt>¿Qué respuesta recibo tras mostrar una hoja de cálculo?</dt>
  <dd>La API devuelve `200 OK` con una carga que contiene el objeto de hoja de cálculo donde `"Visible": true`. La respuesta incluye las propiedades `Name`, `Index` y `Visible` de la hoja de cálculo.</dd>

  <dt>¿Puedo ocultar varias hojas de cálculo en una única llamada?</dt>
  <dd>No. El punto de conexión de visibilidad opera sobre una única hoja de cálculo identificada por `{sheetName}`. Para ocultar varias hojas, recorra cada nombre en su código cliente.</dd>
</dl>

---

*Escrito por el equipo de documentación de Aspose – más de 15 años de experiencia automatizando flujos de trabajo de Excel.*