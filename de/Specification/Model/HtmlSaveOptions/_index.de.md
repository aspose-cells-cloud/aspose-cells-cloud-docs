---
title: HtmlSaveOption
second_title: Aspose.Cells Cloud Documen
type: docs
url: /de/specification/model/htmlsaveoptions/
description: "Aspose.Cells Cloud-Modellspezifikation: HtmlSaveOptions. Müheloses Bearbeiten von Excel und anderen Tabellenkalkulationsdokumenten mit Funktionen wie Öffnen, Generieren, Bearbeiten, Teilen, Zusammenführen, Vergleichen und Konvertieren"
kwords: Excel, Office, Tabellenkalkulation, Cloud REST API, HtmlSaveOptions
weight: 50
---
## **htmlSaveOptions**

 Stellt Optionen zum Speichern der HTML-Datei dar.

| Name des Anwesens| Art der Immobilie| Nullwerte zulassen| Schreibgeschützt| Standardwert| Beschreibung|
|:- |:- |:- |:- |:- |:- |
| Seitenkopfzeilen exportieren| Boolescher Wert| WAHR| FALSCH|||
| Seitenfußzeilen exportieren| Boolescher Wert| WAHR| FALSCH|||
| Zeilen- und Spaltenüberschriften exportieren| Boolescher Wert| WAHR| FALSCH|||
| AlleBlätter anzeigen| Boolescher Wert| WAHR| FALSCH|||
| Bildoptionen| Klasse:Bild-oder-Druckoptionen| WAHR| FALSCH|||
| AlsEinzeldatei Speichern| Boolescher Wert| WAHR| FALSCH|| Gibt an, ob das HTML als einzelne Datei gespeichert werden soll. Der Standardwert ist „false“.|
| ExportHiddenWorksheet| Boolescher Wert| WAHR| FALSCH|| Gibt an, ob das HTML als einzelne Datei gespeichert werden soll. Der Standardwert ist „false“.|
| GitternetzlinienExportieren| Boolescher Wert| WAHR| FALSCH|| Gibt an, ob die Gitternetzlinien exportiert werden. Der Standardwert ist „false“.|
| Präsentationspräferenz| Boolescher Wert| WAHR| FALSCH|| Gibt an, ob die Präsentation bevorzugt als HTML- oder MHT-Datei erfolgt. Der Standardwert ist „false“. Wenn Sie eine schönere Präsentation wünschen, setzen Sie den Wert bitte auf „true“.|
| CellCssPrefix| Zeichenfolge| WAHR| FALSCH||Ruft das Präfix des CSS-Namens ab und legt es fest. Der Standardwert ist "".|
| Tabellen-CssId| Zeichenfolge| WAHR| FALSCH|| Ruft das Präfix des Typ-CSS-Namens wie tr, col, td usw. ab und legt es fest. Sie sind im Tabellenelement enthalten, das das spezifische TableCssId-Attribut hat. Der Standardwert ist "".|
| IstVollständigerPfadLink| Boolescher Wert| WAHR| FALSCH|| Gibt an, ob der vollständige Pfadlink in sheet00x.htm, filelist.xml und tabstrip.htm verwendet wird. Der Standardwert ist „false“.|
| ExportArbeitsblattCSSSeparat| Boolescher Wert| WAHR| FALSCH|| Gibt an, ob das Arbeitsblatt-CSS separat exportiert wird. Der Standardwert ist „false“.|
| ExportSimilarBorderStyle| Boolescher Wert| WAHR| FALSCH|||
| ZusammenführenLeerenTdForcely| Boolescher Wert| WAHR| FALSCH||Gibt an, ob leere TD-Elemente beim Exportieren der Datei in HTML zwangsweise zusammengeführt werden sollen. Die Größe der HTML-Datei wird erheblich reduziert, wenn der Wert auf „true“ gesetzt wird. Der Standardwert ist „false“. Wenn Sie die HTML-Datei in Excel importieren oder beim Speichern der Datei in HTML perfekte Gitternetzlinien exportieren möchten, behalten Sie bitte den Standardwert bei.|
| Zellenkoordinate exportieren| Boolescher Wert| WAHR| FALSCH|| Gibt an, ob beim Speichern der Datei in HTML die Excel-Koordinaten nicht leerer Zellen exportiert werden. Der Standardwert ist „false“. Wenn Sie die HTML-Ausgabe in Excel importieren möchten, behalten Sie bitte den Standardwert bei.|
| ExportierenZusätzlicheÜberschriften| Boolescher Wert| WAHR| FALSCH|| Gibt an, ob zusätzliche Überschriften exportiert werden, wenn die Textlänge die maximale Anzahl an Anzeigespalten überschreitet. Der Standardwert ist „false“. Wenn Sie die HTML-Datei in Excel importieren möchten, behalten Sie bitte den Standardwert bei.|
| Überschriften exportieren| Boolescher Wert| WAHR| FALSCH||Gibt an, ob Überschriften exportiert werden, wenn die Datei als HTML gespeichert wird. Der Standardwert ist „false“. Wenn Sie die HTML-Datei in Excel importieren möchten, behalten Sie bitte den Standardwert bei.|
| ExportFormel| Boolescher Wert| WAHR| FALSCH|| Gibt an, ob die Formel exportiert wird, wenn die Datei als HTML gespeichert wird. Der Standardwert ist „true“. Wenn Sie die HTML-Ausgabe in Excel importieren möchten, behalten Sie bitte den Standardwert bei.|
| TooltipText hinzufügen| Boolescher Wert| WAHR| FALSCH|| Gibt an, ob Tooltip-Text hinzugefügt werden soll, wenn die Daten nicht vollständig angezeigt werden können.|
| ExportBogusRowData| Boolescher Wert| WAHR| FALSCH|| Gibt an, ob falsche Daten der unteren Zeile exportiert werden. Der Standardwert ist „true“. Wenn Sie die HTML- oder MHT-Datei in Excel importieren möchten, behalten Sie bitte den Standardwert bei.|
| Nicht verwendete Stile ausschließen| Boolescher Wert| WAHR| FALSCH|| Gibt an, ob nicht verwendete Stile ausgeschlossen werden sollen. Der Standardwert ist „false“. Wenn Sie die HTML- oder MHT-Datei in Excel importieren möchten, behalten Sie bitte den Standardwert bei.|
| Dokumenteigenschaften exportieren| Boolescher Wert| WAHR| FALSCH||Gibt an, ob Dokumenteigenschaften exportiert werden. Der Standardwert ist „true“. Wenn Sie die HTML- oder MHT-Datei in Excel importieren möchten, behalten Sie bitte den Standardwert bei.|
| Arbeitsblatteigenschaften exportieren| Boolescher Wert| WAHR| FALSCH|| Gibt an, ob Arbeitsblatteigenschaften exportiert werden. Der Standardwert ist „true“. Wenn Sie die HTML- oder MHT-Datei in Excel importieren möchten, behalten Sie bitte den Standardwert bei.|
| ExportWorkbookProperties| Boolescher Wert| WAHR| FALSCH|| Gibt an, ob Arbeitsmappeneigenschaften exportiert werden. Der Standardwert ist „true“. Wenn Sie die HTML- oder MHT-Datei in Excel importieren möchten, behalten Sie bitte den Standardwert bei.|
| ExportFrameScriptsAndProperties| Boolescher Wert| WAHR| FALSCH|| Gibt an, ob Frame-Skripte und Dokumenteigenschaften exportiert werden. Der Standardwert ist „true“. Wenn Sie die HTML- oder MHT-Datei in Excel importieren möchten, behalten Sie bitte den Standardwert bei.|
| Verzeichnis für angehängte Dateien| Zeichenfolge| WAHR| FALSCH|| Das Verzeichnis, in dem die angehängten Dateien gespeichert werden. Nur zum Speichern im HTML-Stream.|
| URL-Präfix für angehängte Dateien| Zeichenfolge| WAHR| FALSCH||Geben Sie das URL-Präfix angehängter Dateien wie Bilder in der HTML-Datei an. Nur zum Speichern im HTML-Stream.|
| Codierung| Zeichenfolge| WAHR| FALSCH|||
| NurAktivArbeitsblattExportieren| Boolescher Wert| WAHR| FALSCH|| Gibt an, ob die gesamte Arbeitsmappe in eine HTML-Datei exportiert wird.|
| ExportChartImageFormat| Zeichenfolge| WAHR| FALSCH|| Abrufen oder Festlegen des Formats des Diagrammbilds vor dem Exportieren|
| ExportImagesAsBase64| Boolescher Wert| WAHR| FALSCH|||
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

