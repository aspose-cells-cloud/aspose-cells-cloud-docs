---
title: HtmlSaveOption
second_title: Aspose.Cells Cloud Documen
type: docs
url: /de/specification/model/htmlsaveoptions/
description: "Aspose.Cells Cloud-Modellspezifikation: HtmlSaveOptions. Bearbeiten Sie mühelos Excel und andere Tabellenkalkulationsdokumente mit Funktionen wie Öffnen, Generieren, Bearbeiten, Teilen, Zusammenführen, Vergleichen und Konvertieren"
weight: 50
---
## **htmlSaveOptions**

 Stellt Optionen zum Speichern einer HTML-Datei dar.

| Name des Anwesens| Art der Immobilie| Nullbar| Schreibgeschützt| Standardwert| Beschreibung|
|:- |:- |:- |:- |:- |:- |
| ExportPageHeaders| Boolescher Wert| WAHR| FALSCH|||
| Seitenfußzeilen exportieren| Boolescher Wert| WAHR| FALSCH|||
| ExportRowColumnHeadings| Boolescher Wert| WAHR| FALSCH|||
| ShowAllSheets| Boolescher Wert| WAHR| FALSCH|||
| Bildoptionen| Klasse:ImageOrPrintOptions| WAHR| FALSCH|||
| Als einzelne Datei speichern| Boolescher Wert| WAHR| FALSCH|| Gibt an, ob der HTML-Code als einzelne Datei gespeichert wird. Der Standardwert ist false.|
| ExportHiddenWorksheet| Boolescher Wert| WAHR| FALSCH|| Gibt an, ob der HTML-Code als einzelne Datei gespeichert wird. Der Standardwert ist false.|
| Gitterlinien exportieren| Boolescher Wert| WAHR| FALSCH||Gibt an, ob die Gitternetzlinien exportiert werden. Der Standardwert ist „false“.|
| Präsentationspräferenz| Boolescher Wert| WAHR| FALSCH|| Gibt an, ob eine HTML- oder MHT-Datei die bevorzugte Präsentation ist. Der Standardwert ist „false“. Wenn Sie eine schönere Präsentation wünschen, setzen Sie den Wert bitte auf „true“.|
| CellCssPrefix| Zeichenfolge| WAHR| FALSCH|| Ruft das Präfix des CSS-Namens ab und legt es fest. Der Standardwert ist „“.|
| TableCssId| Zeichenfolge| WAHR| FALSCH|| Ruft das Präfix des Typ-CSS-Namens wie tr,col,td usw. ab und legt es fest. Sie sind im Tabellenelement enthalten, das über das spezifische TableCssId-Attribut verfügt. Der Standardwert ist „“.|
| IsFullPathLink| Boolescher Wert| WAHR| FALSCH|| Gibt an, ob der vollständige Pfadlink in sheet00x.htm, filelist.xml und tabstrip.htm verwendet wird. Der Standardwert ist false.|
| Arbeitsblatt CSS separat exportieren| Boolescher Wert| WAHR| FALSCH|| Gibt an, ob das Arbeitsblatt-CSS separat exportiert werden soll. Der Standardwert ist „false“.|
| ExportSimilarBorderStyle| Boolescher Wert| WAHR| FALSCH|||
| MergeEmptyTdForcely| Boolescher Wert| WAHR| FALSCH||Gibt an, ob das Zusammenführen leerer TD-Elemente beim Exportieren der Datei in HTML erzwungen wird. Die Größe der HTML-Datei wird erheblich reduziert, nachdem der Wert auf „true“ gesetzt wurde. Der Standardwert ist false. Wenn Sie die HTML-Datei in Excel importieren oder beim Speichern der Datei im HTML-Format perfekte Gitterlinien exportieren möchten, behalten Sie bitte den Standardwert bei.|
| ExportCellCoordinate| Boolescher Wert| WAHR| FALSCH|| Gibt an, ob Excel-Koordinaten nicht leerer Zellen exportiert werden, wenn die Datei im HTML-Format gespeichert wird. Der Standardwert ist false. Wenn Sie die HTML-Ausgabe in Excel importieren möchten, behalten Sie bitte den Standardwert bei.|
| ExportExtraHeadings| Boolescher Wert| WAHR| FALSCH|| Gibt an, ob zusätzliche Überschriften exportiert werden, wenn die Textlänge länger als die maximale Anzeigespalte ist. Der Standardwert ist false. Wenn Sie die HTML-Datei in Excel importieren möchten, behalten Sie bitte den Standardwert bei.|
| Überschriften exportieren| Boolescher Wert| WAHR| FALSCH||Gibt an, ob beim Speichern der Datei im HTML-Format Überschriften exportiert werden. Der Standardwert ist „false“. Wenn Sie die HTML-Datei in Excel importieren möchten, behalten Sie bitte den Standardwert bei.|
| Formel exportieren| Boolescher Wert| WAHR| FALSCH|| Gibt an, ob die Formel beim Speichern der Datei im HTML-Format exportiert wird. Der Standardwert ist wahr. Wenn Sie die HTML-Ausgabe in Excel importieren möchten, behalten Sie bitte den Standardwert bei|
| AddTooltipText| Boolescher Wert| WAHR| FALSCH|| Gibt an, ob QuickInfo-Text hinzugefügt wird, wenn die Daten nicht vollständig angezeigt werden können.|
| ExportBogusRowData| Boolescher Wert| WAHR| FALSCH|| Gibt an, ob falsche Daten in der unteren Zeile exportiert werden. Der Standardwert ist true. Wenn Sie die HTML- oder MHT-Datei in Excel importieren möchten, behalten Sie bitte den Standardwert bei.|
| UnusedStyles ausschließen| Boolescher Wert| WAHR| FALSCH|| Gibt an, ob nicht verwendete Stile ausgeschlossen werden. Der Standardwert ist „false“. Wenn Sie die HTML- oder MHT-Datei in Excel importieren möchten, behalten Sie bitte den Standardwert bei.|
| ExportDocumentProperties| Boolescher Wert| WAHR| FALSCH||Gibt an, ob Dokumenteigenschaften exportiert werden. Der Standardwert ist „true“. Wenn Sie die HTML- oder MHT-Datei in Excel importieren möchten, behalten Sie bitte den Standardwert bei.|
| ExportWorksheetProperties| Boolescher Wert| WAHR| FALSCH|| Gibt an, ob Arbeitsblatteigenschaften exportiert werden. Der Standardwert ist „true“. Wenn Sie die HTML- oder MHT-Datei in Excel importieren möchten, behalten Sie bitte den Standardwert bei.|
| ExportWorkbookProperties| Boolescher Wert| WAHR| FALSCH|| Gibt an, ob Arbeitsmappeneigenschaften exportiert werden. Der Standardwert ist „true“. Wenn Sie die HTML- oder MHT-Datei in Excel importieren möchten, behalten Sie bitte den Standardwert bei.|
| ExportFrameScriptsAndProperties| Boolescher Wert| WAHR| FALSCH|| Gibt an, ob Rahmenskripte und Dokumenteigenschaften exportiert werden. Der Standardwert ist true. Wenn Sie die HTML- oder MHT-Datei in Excel importieren möchten, behalten Sie bitte den Standardwert bei.|
| AttachedFilesDirectory| Zeichenfolge| WAHR| FALSCH|| Das Verzeichnis, in dem die angehängten Dateien gespeichert werden. Nur zum Speichern im HTML-Stream.|
| AttachedFilesUrlPrefix| Zeichenfolge| WAHR| FALSCH||Geben Sie das URL-Präfix angehängter Dateien wie z. B. Bilder in der HTML-Datei an. Nur zum Speichern im HTML-Stream.|
| Codierung| Zeichenfolge| WAHR| FALSCH|||
| ExportActiveWorksheetOnly| Boolescher Wert| WAHR| FALSCH|| Gibt an, ob die gesamte Arbeitsmappe in eine HTML-Datei exportiert wird.|
| ExportChartImageFormat| Zeichenfolge| WAHR| FALSCH|| Rufen Sie vor dem Exportieren das Format des Diagrammbilds ab oder legen Sie es fest|
| ExportImagesAsBase64| Boolescher Wert| WAHR| FALSCH|||
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