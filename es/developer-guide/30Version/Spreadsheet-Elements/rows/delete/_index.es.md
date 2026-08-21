---
title: "Trabajar con la eliminación de filas en una hoja de cálculo de Excel"
second_title: "Document"
linktype: "Delete"
type: docs
url: /rows/delete/
keywords: "Aspose.Cells, eliminar fila, API de Excel, REST, nube, hoja de cálculo, Excel, SDK"
description: "Aprenda cómo eliminar una sola fila o varias filas en una hoja de cálculo de Excel utilizando la API REST de Aspose.Cells Cloud. Incluye ejemplos de código para Android, C#, Go, Java, Node.js, Perl, PHP, Python, Ruby y Swift."
weight: 20
ArticleTitle: "Trabajar con la eliminación de filas en una hoja de cálculo de Excel – Guía de la API de Aspose.Cells Cloud"
---

## Operaciones de eliminación disponibles

Los siguientes ejemplos muestran cómo eliminar una única fila vacía o varias filas de una hoja de cálculo de Excel utilizando la API REST de Aspose.Cells Cloud.

- [Cómo eliminar una fila vacía en una hoja de cálculo de Excel](/cells/rows/delete/row/)
- [Cómo eliminar varias filas en una hoja de cálculo de Excel](/cells/rows/delete/rows/)

**Referencia de la API**

| Elemento              | Detalles |
|----------------------|---------------------------------------------------------------|
| **Método HTTP**      | DELETE |
| **Punto de conexión**| `/cells/{fileName}/worksheets/{sheetName}/rows` |
| **Parámetros de ruta**| `fileName` – nombre del archivo de Excel (obligatorio)<br>`sheetName` – nombre de la hoja de cálculo (obligatorio) |
| **Parámetros de consulta**| `startrow` – índice de la primera fila a eliminar (obligatorio)<br>`totalRows` – número de filas a eliminar (obligatorio)<br>`storage` – nombre del almacenamiento en la nube (opcional)<br>`folder` – ruta de la carpeta en el almacenamiento (opcional) |
| **Cuerpo de la solicitud** | *Ninguno* |
| **Ejemplo de respuesta**| ```json<br>{<br>  "Code": 200,<br>  "Status": "OK",<br>  "RowsDeleted": 1<br>}<br>``` |
| **Códigos de estado posibles**| 200 OK – filas eliminadas correctamente<br>400 Bad Request – parámetros no válidos<br>401 Unauthorized – error de autenticación<br>404 Not Found – archivo o hoja de cálculo no encontrados<br>500 Internal Server Error – error del lado del servidor |

**Consulte también**

- [Agregar fila](/cells/rows/add/)
- [Obtener fila](/cells/rows/get/)
- [Copiar fila](/cells/rows/copy/)
- [Ocultar fila](/cells/rows/hide/)
- [Información general sobre filas](/cells/rows/)
---