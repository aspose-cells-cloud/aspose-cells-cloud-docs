---
title: MHtmlSaveOption
second_title: Aspose.Cells Cloud Documen
type: docs
url: /de/specification/model/mhtmlsaveoptions/
description: "Aspose.Cells Cloud-Modellspezifikation: MHtmlSaveOptions. Müheloses Bearbeiten von Excel und anderen Tabellenkalkulationsdokumenten mit Funktionen wie Öffnen, Generieren, Bearbeiten, Teilen, Zusammenführen, Vergleichen und Konvertieren"
kwords: Excel, Office, Tabellenkalkulation, Cloud REST API, MHtmlSaveOptions
weight: 50
---
## **mHtmlSaveOptions**

 Stellt Optionen zum Speichern der MHTML-Datei dar.

| Name des Anwesens| Art der Immobilie| Nullwerte zulassen| Schreibgeschützt| Standardwert| Beschreibung|
|:- |:- |:- |:- |:- |:- |
| Verzeichnis für angehängte Dateien| Zeichenfolge| WAHR| FALSCH|| Das Verzeichnis, in dem die angehängten Dateien gespeichert werden. Nur zum Speichern im HTML-Stream.|
| URL-Präfix für angehängte Dateien| Zeichenfolge| WAHR| FALSCH||Geben Sie das URL-Präfix angehängter Dateien wie Bilder in der HTML-Datei an. Nur zum Speichern im HTML-Stream.|
| Codierung| Zeichenfolge| WAHR| FALSCH|| Wenn nicht festgelegt, verwenden Sie Encoding.UTF8 als Standardkodierungstyp.|
| NurAktivArbeitsblattExportieren| Boolescher Wert| WAHR| FALSCH|| Gibt an, ob die gesamte Arbeitsmappe in eine HTML-Datei exportiert wird.|
| ExportChartImageFormat| Zeichenfolge| WAHR| FALSCH|| Abrufen oder Festlegen des Formats des Diagrammbilds vor dem Exportieren|
| ExportImagesAsBase64| Boolescher Wert| WAHR| FALSCH|| Gibt an, ob Bilder im Base64-Format HTML, MHTML oder EPUB gespeichert werden.|
| HiddenColDisplayType| Zeichenfolge| WAHR| FALSCH|| Versteckte Spalte (die Breite dieser Spalte beträgt 0) in Excel. Vor dem Speichern im HTML-Format wird die versteckte Spalte nicht ausgegeben, wenn HtmlHiddenColDisplayType „Remove“ ist. Wenn der Wert „Hidden“ ist, wird die Spalte ausgegeben, aber versteckt. Der Standardwert ist „Hidden“.|
| Anzeigetyp für versteckte Zeilen| Zeichenfolge| WAHR| FALSCH||Versteckte Zeile (die Höhe dieser Zeile ist 0) in Excel. Vor dem Speichern im HTML-Format wird die versteckte Zeile nicht ausgegeben, wenn HtmlHiddenRowDisplayType „Remove“ ist. Wenn der Wert „Hidden“ ist, wird die Zeile ausgegeben, aber versteckt. Der Standardwert ist „Hidden“.|
| HtmlCrossStringType| Zeichenfolge| WAHR| FALSCH|| Gibt an, ob eine zellenübergreifende Zeichenfolge auf dieselbe Weise wie MS Excel angezeigt wird, wenn eine Excel-Datei im HTML-Format gespeichert wird. Standardmäßig ist der Wert Default, sodass es bei zellenübergreifenden Zeichenfolgen kaum einen Unterschied zwischen den von Aspose.Cells und MS Excel erstellten HTML-Dateien gibt. Die Leistung beim Erstellen großer HTML-Dateien ist jedoch um ein Vielfaches höher, wenn der Wert auf Cross gesetzt wird, als wenn er auf Default oder Fit2Cell gesetzt wird.|
| IsExpImageToTempDir| Boolescher Wert| WAHR| FALSCH|| Gibt an, ob Bilddateien in ein temporäres Verzeichnis exportiert werden. Nur zum Speichern im HTML-Stream.|
| Seitentitel| Zeichenfolge| WAHR| FALSCH||Der Titel der HTML-Seite. Nur zum Speichern im HTML-Stream.|
| ParseHtmlTagInCell| Boolescher Wert| WAHR| FALSCH|| HTML-Tag in Zelle analysieren, z. B. als Zellenwert oder als HTML-Tag, Standard ist „true“|
| Format speichern| Zeichenfolge| WAHR| FALSCH|||
| ZwischengespeicherterDateiordner| Zeichenfolge| WAHR| FALSCH|||
| Daten löschen| Boolescher Wert| WAHR| FALSCH|||
| Verzeichnis erstellen| Boolescher Wert| WAHR| FALSCH|||
| HTTP-Komprimierung aktivieren| Boolescher Wert| WAHR| FALSCH|||
| ChartCache aktualisieren| Boolescher Wert| WAHR| FALSCH|||
| SortNames| Boolescher Wert| WAHR| FALSCH|||
| ValidateMergedAreas| Boolescher Wert| WAHR| FALSCH|||

**Elternname** : [Speicheroptionen](/specification/model/saveoptions)

