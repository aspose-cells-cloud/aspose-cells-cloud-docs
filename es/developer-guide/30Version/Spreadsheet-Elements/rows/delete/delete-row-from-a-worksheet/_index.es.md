---
title: "Eliminar una fila en una hoja de cálculo de Excel"
second_title: "Documento"
linktitle: "Fila"
type: docs
url: /rows/delete/row/
aliases: [/delete-row-from-a-worksheet/]
description: "Utilice el punto de conexión DELETE /worksheets/{sheetName}/cells/rows/{rowIndex} para eliminar una fila específica de una hoja de cálculo de Excel mediante la API REST de Aspose.Cells Cloud. Incluye comando cURL, ejemplos de SDK y referencia completa de parámetros."
keywords: "Aspose.Cells, eliminar fila, Excel, API, REST, Cloud, SDK"
weight: 80
ArticleTitle: "Eliminar una fila en una hoja de cálculo de Excel – Guía de la API de Aspose.Cells Cloud"
---

Esta API REST elimina una fila de una hoja de cálculo de Excel.

**Prerrequisitos**  
- Un token JWT válido de **autorización**.  
- El libro debe estar almacenado en un repositorio compatible de Aspose Cloud (predeterminado o personalizado).  
- La carpeta objetivo (si se especifica) debe existir en el repositorio elegido.

## API REST

```bash
DELETE https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/rows/{rowIndex}
```

### **Parámetros de la solicitud**

| Nombre del parámetro | Tipo    | Ruta / Consulta | Obligatorio | Descripción                                                                                         |
| ------------------- | ------- | --------------- | ----------- | --------------------------------------------------------------------------------------------------- |
| **name**            | string  | ruta            | Sí          | Nombre del libro.                                                                                   |
| **sheetName**       | string  | ruta            | Sí          | Nombre de la hoja de cálculo.                                                                       |
| **rowIndex**        | integer | ruta            | Sí          | Índice de base cero de la fila que se va a eliminar.                                                |
| **startrow**        | integer | consulta        | No          | Índice de la primera fila que se va a eliminar (normalmente el mismo que `rowIndex`).               |
| **totalRows**       | integer | consulta        | No          | Número de filas consecutivas que se van a eliminar.                                                 |
| **updateReference** | boolean | consulta        | No          | Cuando es `true` (valor predeterminado), se actualizan las fórmulas, los intervalos con nombre y otras referencias tras la eliminación. |
| **folder**          | string  | consulta        | No          | Carpeta que contiene el libro.                                                                      |
| **storageName**     | string  | consulta        | No          | Nombre del servicio de almacenamiento.                                                              |

La [Especificación de OpenAPI](https://apireference.aspose.cloud/cells/#/Cells/DeleteWorksheetRow) define una interfaz de programación públicamente accesible y le permite realizar interacciones REST directamente desde un navegador web.

Puede utilizar la herramienta de línea de comandos cURL para acceder fácilmente a los servicios web de Aspose.Cells. El siguiente ejemplo muestra una llamada completa y ejecutable.

{{< tabs tabTotal="2" tabID="1" tabName1="Solicitud" tabName2="Respuesta" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/cells/rows?startrow=1&totalRows=1&updateReference=true" \
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

**Códigos de respuesta HTTP posibles**

| Código | Significado                            | Descripción                                                                 |
|--------|----------------------------------------|-----------------------------------------------------------------------------|
| 200    | OK                                     | La fila se eliminó correctamente.                                          |
| 400    | Solicitud incorrecta                   | Parámetros faltantes o no válidos (por ejemplo, `rowIndex` no numérico).   |
| 401    | No autorizado                          | Token JWT no válido o faltante.                                             |
| 404    | No encontrado                          | El libro, la hoja de cálculo o la fila especificados no existen.           |
| 500    | Error interno del servidor             | Error inesperado del servidor; consulte la respuesta de error para detalles. |

**Ejemplo de respuesta de error**

```json
{
  "Code": 400,
  "Message": "Índice de fila no válido proporcionado."
}
```

## Familia de SDK en la nube

Utilizar un SDK es la mejor forma de acelerar el desarrollo. Un SDK abstracta los detalles de bajo nivel para que pueda centrarse en las tareas de su proyecto. Consulte el [repositorio de GitHub](https://github.com/aspose-cells-cloud) para obtener una lista completa de los SDK de Aspose.Cells Cloud.

Los siguientes ejemplos de código demuestran cómo realizar llamadas a los servicios web de Aspose.Cells mediante diversos SDK:

{{< tabs tabTotal="2" tabID="1" tabName1="Solicitud" tabName2="Respuesta" >}}

{{< tab tabNum="1" >}}

```bash
curl -X DELETE "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/cells/rows?startrow=1&totalRows=1&updateReference=true" \
  -H "accept: application/json" \
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

**Operaciones relacionadas**  
- [Agregar una fila](/cells/rows/add/row/)  
- [Eliminar varias filas](/cells/rows/delete/rows/)  
- [Obtener detalles de la fila](/cells/rows/get/row/)  
---