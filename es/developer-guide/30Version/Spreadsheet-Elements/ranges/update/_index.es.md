---
title: "Cómo actualizar el contenido de un rango en una hoja de cálculo de Excel"
second_title: "Documento"
linktitle: "Actualizar"
type: docs
url: /ranges/update/
keywords: "Excel, actualización de rango, Aspose.Cells Cloud, API REST, hoja de cálculo, estilo de rango, valores de rango, altura de fila, ancho de columna"
description: "Actualice el contenido de un rango en una hoja de cálculo de Excel mediante la API REST de Aspose.Cells Cloud. Modifique estilos, valores, alturas de fila y anchos de columna mediante los SDK admitidos."
weight: 20
ArticleTitle: "Cómo actualizar el contenido de un rango en una hoja de cálculo de Excel – Documentación de Aspose.Cells Cloud"
---

## Trabajar con la actualización del contenido de un rango en una hoja de cálculo de Excel

Antes de utilizar las operaciones de actualización, asegúrese de tener un token válido de la API de Aspose.Cells Cloud y de que el libro de trabajo de destino esté almacenado en su almacenamiento en la nube. La API está disponible a través de SDK para Android, .NET, Go, Java, Node.js, Perl, PHP, Python, Ruby y Swift.

A continuación se presenta un resumen conciso de las cuatro acciones principales de actualización. Esta tabla proporciona a los desarrolladores una referencia rápida del método HTTP, el patrón de punto de conexión, los parámetros clave y la respuesta típica de éxito (200‑OK) para cada operación.

| Acción             | Método HTTP | Patrón de punto de conexión                                                                         | Parámetros clave              | Respuesta 200‑OK               |
|--------------------|-------------|-----------------------------------------------------------------------------------------------------|-------------------------------|--------------------------------|
| Establecer estilo  | PUT         | `/cells/{fileName}/worksheets/{sheetName}/ranges/{range}/style`                                    | Objeto `style`                | Estilo de rango actualizado    |
| Establecer valores | POST        | `/cells/{fileName}/worksheets/{sheetName}/ranges/{range}/values`                                  | Matriz `values`               | Valores de rango actualizados  |
| Altura de fila     | PUT         | `/cells/{fileName}/worksheets/{sheetName}/ranges/{range}/rowheight`                               | Número `height`               | Altura de fila actualizada     |
| Ancho de columna   | PUT         | `/cells/{fileName}/worksheets/{sheetName}/ranges/{range}/columnwidth`                             | Número `width`                | Ancho de columna actualizado   |

Esta página ofrece un acceso rápido a las cuatro acciones principales de actualización: establecer el estilo de un rango, establecer los valores de un rango, ajustar las alturas de fila y ajustar los anchos de columna.

- [Cómo establecer el estilo de un rango en una hoja de cálculo de Excel.](/cells/ranges/update/style/) 
- [Cómo establecer los valores de un rango en una hoja de cálculo de Excel.](/cells/ranges/update/values/) 
- [Cómo establecer las alturas de fila de un rango en una hoja de cálculo de Excel.](/cells/ranges/update/row-height/) 
- [Cómo establecer los anchos de columna de un rango en una hoja de cálculo de Excel.](/cells/ranges/update/column-width/)
---