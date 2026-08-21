---
title: "Agrupar Columnas – Documentación de la API en la Nube Aspise.Cells"
description: "Agrupar columnas de hoja de cálculo en una hoja de cálculo de Excel usando la API REST de Aspose.Cells Cloud (v3.0). Incluye sintaxis de solicitud, parámetros, ejemplos en cURL y SDK, y detalles de respuesta."
keywords: "Aspose.Cells, agrupar columnas, API de Excel, REST, SDK en la nube"
weight: 60
type: docs
aliases:
  - /group-columns-in-an-excel-worksheet/
  - /group-columns-in-excel-worksheet/
---

# Agrupar Columnas en una Hoja de Cálculo de Excel

**Versión de la API:** v3.0  
**Operación:** `PostGroupWorksheetColumns` – Agrupa columnas de la hoja de cálculo en la hoja de cálculo.

---

## Descripción General

Esta API REST le permite agrupar un rango de columnas en una hoja de cálculo. Las columnas agrupadas pueden mostrarse u ocultarse, lo que le permite crear secciones plegables similares a las de Microsoft Excel.

---

## Requisitos Previos

- Un **token de acceso JWT** válido obtenido desde el servicio de autenticación de Aspose Cloud.  
- El libro debe estar almacenado en una ubicación accesible para Aspose.Cells Cloud (almacén predeterminado o un nombre de almacenamiento personalizado).  
- Versión necesaria del SDK (si se utiliza un SDK): la última versión que soporte la API versión **v3.0**.  

---

## Autenticación

Todas las solicitudes requieren autenticación mediante **token Bearer**.

```http
Authorization: Bearer <access_token>
```

Para más detalles sobre cómo obtener un token, consulte la [guía de autenticación JWT](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/).

---

## Solicitud HTTP

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/columns/group
```

| Parámetro | Ubicación | Obligatorio | Descripción |
|-----------|-----------|-------------|-------------|
| `name` | Ruta | Sí | Nombre del archivo del libro (por ejemplo, `test.xlsx`). |
| `sheetName` | Ruta | Sí | Hoja de cálculo que contiene las columnas que se van a agrupar. |
| `firstIndex` | Consulta | Sí | Índice de base cero de la primera columna que se incluirá en el grupo. |
| `lastIndex` | Consulta | Sí | Índice de base cero de la última columna que se incluirá en el grupo. |
| `hide` | Consulta | No | Si es `true`, las columnas agrupadas se ocultan; de lo contrario, permanecen visibles. |
| `folder` | Consulta | No | Ruta de la carpeta que contiene el libro. |
| `storageName` | Consulta | No | Nombre del servicio de almacenamiento donde se encuentra el archivo. |

---

## Ejemplo de Solicitud (cURL)

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/cells/columns/group?firstIndex=1&lastIndex=2&hide=true" \
     -H "accept: application/json" \
     -H "Authorization: Bearer <access_token>"
```

> **Nota:** La solicitud utiliza **HTTPS** para garantizar una comunicación cifrada.

---

## Respuesta

### Éxito (200)

| Campo | Tipo | Descripción |
|-------|------|-------------|
| `Code` | entero | Código de estado HTTP (`200`). |
| `Status` | cadena | Estado textual de la operación (`OK`). |

**Ejemplo**

```json
{
  "Code": 200,
  "Status": "OK"
}
```

### Error (por ejemplo, 400 Solicitud Incorrecta)

| Campo | Tipo | Descripción |
|-------|------|-------------|
| `Code` | entero | Código de estado HTTP (`400`, `401`, `404`, `500`, …). |
| `Status` | cadena | Estado textual (`Error`). |
| `ErrorMessage` | cadena | Descripción legible por humanos del problema. |
| `ErrorCode` | cadena | Identificador programático del error. |

**Ejemplo – Solicitud Incorrecta**

```json
{
  "Code": 400,
  "Status": "Error",
  "ErrorMessage": "Índice de columna no válido.",
  "ErrorCode": "InvalidParameter"
}
```

---

## Ejemplos de SDK

Los fragmentos siguientes muestran cómo llamar a la operación **Agrupar Columnas de la Hoja de Cálculo** utilizando los SDK admitidos.

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostGroupWorksheetColumns.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostGroupWorksheetColumns.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostGroupWorksheetColumns.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostGroupWorksheetColumns.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostGroupWorksheetColumns.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostGroupWorksheetColumns.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostGroupWorksheetColumns.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostGroupWorksheetColumns.go" >}}

{{< /tab >}}

{{< /tabs >}}

---

## Observaciones

- **Comportamiento de agrupación:** La API crea un grupo de columnas que puede expandirse o contraerse en Excel. Configurar `hide=true` contrae inmediatamente el grupo.  
- **Indexación base cero:** Tanto `firstIndex` como `lastIndex` comienzan en **0**; la primera columna de una hoja de cálculo tiene el índice 0.  
- **Consideraciones sobre almacenamiento:** Si el libro reside en un almacenamiento no predeterminado, proporcione ambos parámetros de consulta `folder` y `storageName`.  

---

## Consulte también

- [Autenticación – Token JWT](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/)  
- [Especificación OpenAPI para Agrupar Columnas de la Hoja de Cálculo](https://apireference.aspose.cloud/cells/#/Cells/PostGroupWorksheetColumns)  
- [SDK de Aspose.Cells Cloud (GitHub)](https://github.com/aspose-cells-cloud)  
- [Agrupar Filas en una Hoja de Cálculo de Excel](/rows/group/)  

---

> *Ilustración:* ![Captura de pantalla que muestra columnas agrupadas en una hoja de cálculo de Excel](./images/group-columns.png){: .img-fluid alt="Captura de pantalla que muestra columnas agrupadas en una hoja de cálculo de Excel" }

*La imagen de marcador de posición anterior debe reemplazarse por una captura de pantalla real que muestre el resultado visual de agrupar columnas.*
---