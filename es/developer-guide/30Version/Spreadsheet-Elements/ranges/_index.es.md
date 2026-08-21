---
title: "Trabajar con rangos de Excel"
second_title: "Documentos"
linktype: "Rango"
type: docs
url: /ranges/
aliases: [/working-with-ranges/]
keywords: "Aspose.Cells, rango de Excel, API REST, SDK, .NET, Java, Python, fusionar celdas, copiar rango, establecer valor de rango"
description: "Aprenda cómo recuperar, modificar, aplicar estilo, fusionar, mover y copiar rangos de Excel mediante la API REST de Aspose.Cells Cloud. Incluye ejemplos de código SDK para .NET, Java, Python y más."
weight: 100
ArticleTitle: "Trabajar con rangos de Excel – Documentación de Aspose.Cells Cloud"
---

Un **rango** representa una única celda, una fila completa, una columna entera, un bloque contiguo de celdas o un rango tridimensional (3‑D) que abarca varias hojas de cálculo.

## Trabajar con rangos en un archivo de Excel

La API REST de Aspose.Cells Cloud proporciona puntos de conexión dedicados para cada operación de rango. La siguiente lista enlaza a ejemplos detallados de uso e incluye el método HTTP y el punto de conexión correspondientes para referencia rápida.

- [Obtener rangos con nombre dentro del libro de trabajo](/cells/get-named-ranges-inside-the-workbook/) – Recupera todos los rangos con nombre definidos en un libro de trabajo, devolviendo sus direcciones y ámbito. **API**: `GET /cells/{fileName}/worksheets/{sheetName}/namedranges`.
- [Obtener datos de celdas basados en un rango con nombre](/cells/get-cells-data-based-on-named-range/) – Devuelve los valores de las celdas que pertenecen a un rango con nombre especificado. **API**: `GET /cells/{fileName}/worksheets/{sheetName}/namedranges/{rangeName}/cells`.
- [Cambiar alturas de filas dentro del rango](/cells/cells/change-heights-of-rows-inside-the-range/) – Ajusta la altura de cada fila que se encuentra dentro del rango dado. **API**: `PUT /cells/{fileName}/worksheets/{sheetName}/ranges/{rangeName}/rows/height`.
- [Cambiar anchos de columnas dentro del rango](/cells/cells/change-widths-of-columns-inside-the-range/) – Modifica el ancho de columna para todas las columnas que intersectan el rango. **API**: `PUT /cells/{fileName}/worksheets/{sheetName}/ranges/{rangeName}/columns/width`.
- [Fusionar un rango de celdas en una sola celda](/cells/combines-a-range-of-cells-into-a-single-cell/) – Fusiona las celdas seleccionadas en una única celda, preservando el valor de la celda superior izquierda. **API**: `POST /cells/{fileName}/worksheets/{sheetName}/ranges/{rangeName}/merge`.
- [Copiar rango en una hoja de cálculo con opciones de pegado](/cells/copy-range-in-a-worksheet-with-paste-options/) – Copia un rango de origen a un rango de destino con tipos de pegado opcionales (valores, formatos, fórmulas, etc.). **API**: `POST /cells/{fileName}/worksheets/{sheetName}/ranges/{sourceRange}/copy?destCell={destRange}&pasteType={type}`.
- [Establecer el estilo del rango](/cells/set-the-style-of-the-range/) – Aplica estilos de fuente, relleno, borde y alineación a todas las celdas del rango. **API**: `PUT /cells/{fileName}/worksheets/{sheetName}/ranges/{rangeName}/style`.
- [Desfusionar celdas fusionadas del rango](/cells/unmerge-merged-cells-of-the-range/) – Invierte una operación de fusión previa, restaurando las celdas individuales originales. **API**: `POST /cells/{fileName}/worksheets/{sheetName}/ranges/{rangeName}/unmerge`.
- [Mover un rango con nombre con una hoja de cálculo de Excel](/cells/move-a-named-ranged-with-a-excel-worksheet/) – Reubica un rango con nombre a una nueva dirección dentro de la misma hoja de cálculo o en otra hoja de cálculo. **API**: `PUT /cells/{fileName}/worksheets/{sheetName}/namedranges/{rangeName}/move`.
- [Establecer valor de rango en una hoja de cálculo de Excel](/cells/ranges/set-value/) – Escribe un único valor o un array de valores en el rango especificado. **API**: `PUT /cells/{fileName}/worksheets/{sheetName}/ranges/{rangeName}/value`.

Todas las peticiones y respuestas están en formato JSON. Incluya el encabezado `Authorization` con su token de acceso para la autenticación.