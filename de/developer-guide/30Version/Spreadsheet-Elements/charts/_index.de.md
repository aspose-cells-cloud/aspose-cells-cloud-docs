---
title: "Arbeiten mit Excel-Diagrammen"
second_title: "Dokument"
linktitle: "Diagramme"
type: docs
url: /de/charts/
aliases: [  /de/working-with-charts/ ]
keywords: "Aspose, Cells, Excel, Diagramm, API, REST, Cloud, Tabellenkalkulation"
description: "Erfahren Sie, wie Sie Excel-Diagramme mit der Aspose.Cells Cloud API verwalten können. Schritt-für-Schritt-Anleitungen, Codebeispiele und Fehlerbehandlung zum Abrufen, Hinzufügen, Aktualisieren, Löschen und Konvertieren von Diagrammen in Bildformate."
weight: 100
ArticleTitle: "Arbeiten mit Excel-Diagrammen – Aspose.Cells Cloud-Dokumentation"
---

## Arbeiten mit Diagrammen in einer Excel-Datei

**Zuletzt aktualisiert:** Juli 2026  

Excel-Diagramme sind visuelle Darstellungen von Daten, die Benutzern helfen, Trends und Muster schnell zu verstehen.  
Die Aspose.Cells Cloud API ermöglicht Entwicklern, programmgesteuert mit diesen Diagrammen in Excel-Arbeitsmappen zu arbeiten, die in der Cloud gespeichert sind. Mit der API können Sie vorhandene Diagramme abrufen, neue hinzufügen, ihre Eigenschaften (wie Titel, Achsen und Legenden) ändern, unerwünschte Diagramme löschen und Diagramme in Bildformate konvertieren, um sie beispielsweise für Berichte oder nachgelagerte Verarbeitungsschritte zu nutzen. Die folgenden Links führen direkt zu den detaillierten Operationsseiten für jede unterstützte diagrammspezifische Aktion.

### Schnellübersicht

| Operation | HTTP-Methode | Endpunkt (Template) | Dokumentation |
|-----------|-------------|---------------------|---------------|
| Diagramm abrufen | GET | `/cells/{file}/worksheets/{sheet}/charts/{chartIndex}` | [Diagramm aus einem Arbeitsblatt abrufen](/cells/get-chart-from-a-worksheet/) |
| Diagramm hinzufügen | POST | `/cells/{file}/worksheets/{sheet}/charts` | [Diagramm in einem Arbeitsblatt hinzufügen](/cells/add-a-chart-in-a-worksheet/) |
| Alle Diagramme löschen | DELETE | `/cells/{file}/worksheets/{sheet}/charts` | [Alle Diagramme aus einem Arbeitsblatt löschen](/cells/delete-all-charts-from-a-worksheet/) |
| Diagramm löschen | DELETE | `/cells/{file}/worksheets/{sheet}/charts/{chartIndex}` | [Diagramm aus einem Arbeitsblatt löschen](/cells/delete-a-chart-from-a-worksheet/) |
| Diagramm in Bild konvertieren | GET | `/cells/{file}/worksheets/{sheet}/charts/{chartIndex}/image` | [Diagramm in Bild konvertieren](/cells/convert-chart-to-image/) |
| Diagrammbereich abrufen | GET | `/cells/{file}/worksheets/{sheet}/charts/{chartIndex}/area` | [Diagrammbereich aus einem Arbeitsblatt abrufen](/cells/get-chart-area-from-a-worksheet/) |
| Füllformat abrufen | GET | `/cells/{file}/worksheets/{sheet}/charts/{chartIndex}/area/fillformat` | [Füllformat eines Diagrammbereichs aus einem Arbeitsblatt abrufen](/cells/get-fill-format-of-a-chart-area-from-a-worksheet/) |
| Legende abrufen | GET | `/cells/{file}/worksheets/{sheet}/charts/{chartIndex}/legend` | [Diagrammlegende aus einem Arbeitsblatt abrufen](/cells/get-chart-legend-from-a-worksheet/) |
| Legende aktualisieren | POST | `/cells/{file}/worksheets/{sheet}/charts/{chartIndex}/legend` | [Diagrammlegende in einem Arbeitsblatt aktualisieren](/cells/update-chart-legend-in-a-worksheet/) |
| Legende anzeigen | POST | `/cells/{file}/worksheets/{sheet}/charts/{chartIndex}/legend/show` | [Diagrammlegende in einem Arbeitsblatt anzeigen](/cells/show-chart-legend-in-a-worksheet/) |
| Legende ausblenden | POST | `/cells/{file}/worksheets/{sheet}/charts/{chartIndex}/legend/hide` | [Diagrammlegende in einem Arbeitsblatt ausblenden](/cells/hide-chart-legend-in-a-worksheet/) |
| Titel abrufen | GET | `/cells/{file}/worksheets/{sheet}/charts/{chartIndex}/title` | [Diagrammtitel aus einem Arbeitsblatt abrufen](/cells/get-chart-title-from-a-worksheet/) |
| Titel festlegen | POST | `/cells/{file}/worksheets/{sheet}/charts/{chartIndex}/title` | [Diagrammtitel in Excel-Arbeitsblatt festlegen](/cells/set-chart-title-in-excel-worksheet/) |
| Titel aktualisieren | POST | `/cells/{file}/worksheets/{sheet}/charts/{chartIndex}/title` | [Diagrammtitel in Excel-Arbeitsblatt aktualisieren](/cells/update-chart-title-in-excel-worksheet/) |
| Titel löschen | DELETE | `/cells/{file}/worksheets/{sheet}/charts/{chartIndex}/title` | [Diagrammtitel in einem Arbeitsblatt löschen](/cells/delete-chart-title-in-a-worksheet/) |
| Diagrammeigenschaften aktualisieren | POST | `/cells/{file}/worksheets/{sheet}/charts/{chartIndex}` | [Diagrammeigenschaften aktualisieren](/cells/charts/properties/update/) |
| Kategorieachse abrufen | GET | `/cells/{file}/worksheets/{sheet}/charts/{chartIndex}/categoryaxis` | [Diagrammkategorieachse abrufen](/cells/charts/category-axis/get/) |
| Wertachse abrufen | GET | `/cells/{file}/worksheets/{sheet}/charts/{chartIndex}/valueaxis` | [Diagrammwertachse abrufen](/cells/charts/value-axis/get/) |
| Zweite Kategorieachse abrufen | GET | `/cells/{file}/worksheets/{sheet}/charts/{chartIndex}/secondcategoryaxis` | [Zweite Diagrammkategorieachse abrufen](/cells/charts/second-category-axis/get/) |
| Zweite Wertachse abrufen | GET | `/cells/{file}/worksheets/{sheet}/charts/{chartIndex}/secondvalueaxis` | [Zweite Diagrammwertachse abrufen](/cells/charts/second-value-axis/get/) |
| Kategorieachse aktualisieren | POST | `/cells/{file}/worksheets/{sheet}/charts/{chartIndex}/categoryaxis` | [Diagrammkategorieachse aktualisieren](/cells/charts/category-axis/update/) |
| Wertachse aktualisieren | POST | `/cells/{file}/worksheets/{sheet}/charts/{chartIndex}/valueaxis` | [Diagrammwertachse aktualisieren](/cells/charts/value-axis/update/) |
| Zweite Kategorieachse aktualisieren | POST | `/cells/{file}/worksheets/{sheet}/charts/{chartIndex}/secondcategoryaxis` | [Zweite Diagrammkategorieachse aktualisieren](/cells/charts/second-category-axis/update/) |
| Zweite Wertachse aktualisieren | POST | `/cells/{file}/worksheets/{sheet}/charts/{chartIndex}/secondvalueaxis` | [Zweite Diagrammwertachse aktualisieren](/cells/charts/second-value-axis/update/) |

- [Diagramm aus einem Arbeitsblatt abrufen](/cells/get-chart-from-a-worksheet/)
- [Diagramm in einem Arbeitsblatt hinzufügen](/cells/add-a-chart-in-a-worksheet/)
- [Alle Diagramme aus einem Arbeitsblatt löschen](/cells/delete-all-charts-from-a-worksheet/)
- [Diagramm aus einem Arbeitsblatt löschen](/cells/delete-a-chart-from-a-worksheet/)
- [Diagramm in Bild konvertieren](/cells/convert-chart-to-image/)
- [Diagrammbereich aus einem Arbeitsblatt abrufen](/cells/get-chart-area-from-a-worksheet/)
- [Füllformat eines Diagrammbereichs aus einem Arbeitsblatt abrufen](/cells/get-fill-format-of-a-chart-area-from-a-worksheet/)
- [Diagrammlegende aus einem Arbeitsblatt abrufen](/cells/get-chart-legend-from-a-worksheet/)
- [Diagrammlegende in einem Arbeitsblatt aktualisieren](/cells/update-chart-legend-in-a-worksheet/)
- [Diagrammlegende in einem Arbeitsblatt anzeigen](/cells/show-chart-legend-in-a-worksheet/)
- [Diagrammlegende in einem Arbeitsblatt ausblenden](/cells/hide-chart-legend-in-a-worksheet/)
- [Diagrammtitel aus einem Arbeitsblatt abrufen](/cells/get-chart-title-from-a-worksheet/)
- [Diagrammtitel in Excel-Arbeitsblatt festlegen](/cells/set-chart-title-in-excel-worksheet/)
- [Diagrammtitel in Excel-Arbeitsblatt aktualisieren](/cells/update-chart-title-in-excel-worksheet/)
- [Diagrammtitel in einem Arbeitsblatt löschen](/cells/delete-chart-title-in-a-worksheet/)
- [Diagrammeigenschaften aktualisieren](/cells/charts/properties/update/)
- [Diagrammkategorieachse abrufen](/cells/charts/category-axis/get/)
- [Diagrammwertachse abrufen](/cells/charts/value-axis/get/)
- [Zweite Diagrammkategorieachse abrufen](/cells/charts/second-category-axis/get/)
- [Zweite Diagrammwertachse abrufen](/cells/charts/second-value-axis/get/)
- [Diagrammkategorieachse aktualisieren](/cells/charts/category-axis/update/)
- [Diagrammwertachse aktualisieren](/cells/charts/value-axis/update/)
- [Zweite Diagrammkategorieachse aktualisieren](/cells/charts/second-category-axis/update/)
- [Zweite Diagrammwertachse aktualisieren](/cells/charts/second-value-axis/update/)