---
title: MHtmlSaveOption
second_title: Aspose.Cells Cloud Documen
type: docs
url: /de/specification/model/mhtmlsaveoptions/
description: "Aspose.Cells Cloud-Modellspezifikation: MHtmlSaveOptions. Bearbeiten Sie mühelos Excel und andere Tabellenkalkulationsdokumente mit Funktionen wie Öffnen, Generieren, Bearbeiten, Teilen, Zusammenführen, Vergleichen und Konvertieren"
weight: 50
---
## **mHtmlSaveOptions**

 Stellt Optionen zum Speichern einer .mhtml-Datei dar.

| Name des Anwesens| Art der Immobilie| Nullbar| Schreibgeschützt| Standardwert| Beschreibung|
|:- |:- |:- |:- |:- |:- |
| AttachedFilesDirectory| Zeichenfolge| WAHR| FALSCH|| Das Verzeichnis, in dem die angehängten Dateien gespeichert werden. Nur zum Speichern im HTML-Stream.|
| AttachedFilesUrlPrefix| Zeichenfolge| WAHR| FALSCH||Geben Sie das URL-Präfix angehängter Dateien wie z. B. Bilder in der HTML-Datei an. Nur zum Speichern im HTML-Stream.|
| Codierung| Zeichenfolge| WAHR| FALSCH|| Wenn nicht festgelegt, verwenden Sie Encoding.UTF8 als Standardcodierungstyp.|
| ExportActiveWorksheetOnly| Boolescher Wert| WAHR| FALSCH|| Gibt an, ob die gesamte Arbeitsmappe in eine HTML-Datei exportiert wird.|
| ExportChartImageFormat| Zeichenfolge| WAHR| FALSCH|| Rufen Sie vor dem Exportieren das Format des Diagrammbilds ab oder legen Sie es fest|
| ExportImagesAsBase64| Boolescher Wert| WAHR| FALSCH|| Gibt an, ob Bilder im Base64-Format unter HTML, MHTML oder EPUB gespeichert werden.|
| HiddenColDisplayType| Zeichenfolge| WAHR| FALSCH|| Versteckte Spalte (die Breite dieser Spalte ist 0) in Excel, bevor Sie dies im HTML-Format speichern. Wenn HtmlHiddenColDisplayType „Entfernen“ ist, wird die ausgeblendete Spalte nicht ausgegeben. Wenn der Wert „Ausgeblendet“ ist, wird die Spalte ausgegeben. war aber ausgeblendet, der Standardwert ist „Ausgeblendet“|
| HiddenRowDisplayType| Zeichenfolge| WAHR| FALSCH||Versteckte Zeile (die Höhe dieser Zeile ist 0) in Excel, bevor Sie dies im HTML-Format speichern. Wenn HtmlHiddenRowDisplayType „Entfernen“ ist, wird die ausgeblendete Zeile nicht ausgegeben. Wenn der Wert „Ausgeblendet“ ist, wird die Zeile ausgegeben. war aber ausgeblendet, der Standardwert ist „Ausgeblendet“|
| HtmlCrossStringType| Zeichenfolge| WAHR| FALSCH|| Gibt an, ob eine zellenübergreifende Zeichenfolge auf die gleiche Weise wie MS Excel angezeigt wird, wenn eine Excel-Datei im HTML-Format gespeichert wird. Standardmäßig ist der Wert „Default“, sodass es bei zellenübergreifenden Zeichenfolgen kaum einen Unterschied zwischen den von Aspose.Cells und MS Excel erstellten HTML-Dateien gibt. Die Leistung beim Erstellen großer HTML-Dateien wäre jedoch um ein Vielfaches höher, wenn der Wert auf „Cross“ gesetzt wäre Setzen Sie es auf „Standard“ oder „Fit2Cell“.|
| IsExpImageToTempDir| Boolescher Wert| WAHR| FALSCH|| Gibt an, ob Bilddateien in das temporäre Verzeichnis exportiert werden. Nur zum Speichern im HTML-Stream.|
| Seitentitel| Zeichenfolge| WAHR| FALSCH||Der Titel der HTML-Seite. Nur zum Speichern im HTML-Stream.|
| ParseHtmlTagInCell| Boolescher Wert| WAHR| FALSCH|| Analysieren Sie das HTML-Tag in der Zelle, z. B. als Zellenwert oder als HTML-Tag. Die Standardeinstellung ist „true“.|
| SaveFormat| Zeichenfolge| WAHR| FALSCH|||
| CachedFileFolder| Zeichenfolge| WAHR| FALSCH|||
| Daten löschen| Boolescher Wert| WAHR| FALSCH|||
| Verzeichnis erstellen| Boolescher Wert| WAHR| FALSCH|||
| Aktivieren Sie HTTP-Komprimierung| Boolescher Wert| WAHR| FALSCH|||
| ChartCache aktualisieren| Boolescher Wert| WAHR| FALSCH|||
|Sortiernamen| Boolescher Wert| WAHR| FALSCH|||
| ValidateMergedAreas| Boolescher Wert| WAHR| FALSCH|||

**Elternname** : (Speicheroptionen)[Speicheroptionen]