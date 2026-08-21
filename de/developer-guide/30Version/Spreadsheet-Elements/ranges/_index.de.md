---
title: "Arbeiten mit Excel-Bereichen"
second_title: "Dokument"
linktitle: "Bereich"
type: docs
url: /de/ranges/
aliases: [  /de/working-with-ranges/ ]
keywords: "Aspose.Cells, Excel-Bereich, REST-API, SDK, .NET, Java, Python, Zellen zusammenführen, Bereich kopieren, Bereichswert festlegen"
description: "Erfahren Sie, wie Sie Excel-Bereiche mithilfe der Aspose.Cells Cloud REST API abrufen, ändern, gestalten, zusammenführen, verschieben und kopieren. Enthält SDK-Codebeispiele für .NET, Java, Python und weitere."
weight: 100
ArticleTitle: "Arbeiten mit Excel-Bereichen – Aspose.Cells Cloud-Dokumentation"
---

Ein **Bereich** stellt eine einzelne Zelle, eine ganze Zeile, eine gesamte Spalte, einen zusammenhängenden Zellblock oder einen dreidimensionalen (3D-)Bereich dar, der sich über mehrere Arbeitsblätter erstreckt.

## Arbeiten mit Bereichen in einer Excel-Datei

Die Aspose.Cells Cloud REST-API bietet spezielle Endpunkte für jede Bereichsoperation. Die folgende Liste verweist auf detaillierte Nutzungshinweise und enthält die jeweilige HTTP-Methode und den Endpunkt zur schnellen Orientierung.

- [Benannte Bereiche innerhalb der Arbeitsmappe abrufen](/cells/get-named-ranges-inside-the-workbook/) – Ruft alle in einer Arbeitsmappe definierten benannten Bereiche ab und gibt deren Adressen sowie Gültigkeitsbereich zurück. **API**: `GET /cells/{fileName}/worksheets/{sheetName}/namedranges`.
- [Zellendaten basierend auf benanntem Bereich abrufen](/cells/get-cells-data-based-on-named-range/) – Gibt die Werte der Zellen zurück, die zum angegebenen benannten Bereich gehören. **API**: `GET /cells/{fileName}/worksheets/{sheetName}/namedranges/{rangeName}/cells`.
- [Zeilenhöhen innerhalb des Bereichs ändern](/cells/cells/change-heights-of-rows-inside-the-range/) – Passt die Höhe jeder Zeile an, die sich innerhalb des angegebenen Bereichs befindet. **API**: `PUT /cells/{fileName}/worksheets/{sheetName}/ranges/{rangeName}/rows/height`.
- [Spaltenbreiten innerhalb des Bereichs ändern](/cells/cells/change-widths-of-columns-inside-the-range/) – Ändert die Spaltenbreite für alle Spalten, die den Bereich schneiden. **API**: `PUT /cells/{fileName}/worksheets/{sheetName}/ranges/{rangeName}/columns/width`.
- [Zellbereich zu einer einzelnen Zelle zusammenführen](/cells/combines-a-range-of-cells-into-a-single-cell/) – Führt die ausgewählten Zellen zu einer einzigen Zelle zusammen und bewahrt dabei den Wert der oberen linken Zelle. **API**: `POST /cells/{fileName}/worksheets/{sheetName}/ranges/{rangeName}/merge`.
- [Bereich in einem Arbeitsblatt mit Paste-Optionen kopieren](/cells/copy-range-in-a-worksheet-with-paste-options/) – Kopiert einen Quellbereich in einen Zielbereich mit optionalen Paste-Typen (Werte, Formatierungen, Formeln usw.). **API**: `POST /cells/{fileName}/worksheets/{sheetName}/ranges/{sourceRange}/copy?destCell={destRange}&pasteType={type}`.
- [Stil des Bereichs festlegen](/cells/set-the-style-of-the-range/) – Wendet Schriftart-, Füll-, Rahmen- und Ausrichtungsstile auf alle Zellen im Bereich an. **API**: `PUT /cells/{fileName}/worksheets/{sheetName}/ranges/{rangeName}/style`.
- [Zusammengeführte Zellen des Bereichs trennen](/cells/unmerge-merged-cells-of-the-range/) – Kehrt eine zuvor durchgeführte Zusammenführung um und stellt die ursprünglichen einzelnen Zellen wieder her. **API**: `POST /cells/{fileName}/worksheets/{sheetName}/ranges/{rangeName}/unmerge`.
- [Benannter Bereich mit Excel-Arbeitsblatt verschieben](/cells/move-a-named-ranged-with-a-excel-worksheet/) – Verschiebt einen benannten Bereich auf eine neue Adresse innerhalb desselben Arbeitsblatts oder auf ein anderes Arbeitsblatt. **API**: `PUT /cells/{fileName}/worksheets/{sheetName}/namedranges/{rangeName}/move`.
- [Bereichswert in Excel-Arbeitsblatt festlegen](/cells/ranges/set-value/) – Schreibt einen einzelnen Wert oder ein Array von Werten in den angegebenen Bereich. **API**: `PUT /cells/{fileName}/worksheets/{sheetName}/ranges/{rangeName}/value`.

Alle Anfragen und Antworten erfolgen im JSON-Format. Fügen Sie den Header `Authorization` mit Ihrem Zugriffstoken für die Authentifizierung hinzu.