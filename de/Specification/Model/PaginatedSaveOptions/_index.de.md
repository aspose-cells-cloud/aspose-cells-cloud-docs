---
title: PaginatedSaveOption
second_title: Aspose.Cells Cloud Documen
type: docs
url: /de/specification/model/paginatedsaveoptions/
description: "Aspose.Cells Cloud-Modellspezifikation: PaginatedSaveOptions. Bearbeiten Sie mühelos Excel und andere Tabellenkalkulationsdokumente mit Funktionen wie Öffnen, Generieren, Bearbeiten, Teilen, Zusammenführen, Vergleichen und Konvertieren"
weight: 50
---
## **paginatedSaveOptions**

 Stellt die Optionen für die Paginierung dar.

| Name des Anwesens| Art der Immobilie| Nullbar| Schreibgeschützt| Standardwert| Beschreibung|
|:- |:- |:- |:- |:- |:- |
| Standardschriftart| Zeichenfolge| WAHR| FALSCH||Wenn Zeichen in Excel Unicode sind und nicht mit der richtigen Schriftart im Zellenstil festgelegt sind, werden sie möglicherweise als Block im PDF-Bild angezeigt. Legen Sie die Standardschriftart wie MingLiu oder MS Gothic fest, um diese Zeichen anzuzeigen. Wenn diese Eigenschaft nicht festgelegt ist, verwendet Aspose.Cells die Standardschriftart des Systems, um diese Unicode-Zeichen anzuzeigen.|
| CheckWorkbookDefaultFont| Boolescher Wert| WAHR| FALSCH|| Wenn Zeichen in Excel Unicode sind und nicht mit der richtigen Schriftart im Zellenstil festgelegt sind, werden sie möglicherweise als Block im PDF-Bild angezeigt. Setzen Sie dies auf „true“, um zu versuchen, die Standardschriftart der Arbeitsmappe zu verwenden, um diese Zeichen zuerst anzuzeigen.|
| CheckFontCompatibility| Boolescher Wert| WAHR| FALSCH|| Gibt an, ob die Schriftartkompatibilität für jedes Zeichen im Text überprüft werden soll.|
| IsFontSubstitutionCharGranularity| Boolescher Wert| WAHR| FALSCH|| Gibt an, ob die Schriftart des Zeichens nur dann ersetzt werden soll, wenn die Zellenschriftart nicht damit kompatibel ist.|
| Eine Seite pro Blatt| Boolescher Wert| WAHR| FALSCH|| Wenn OnePagePerSheet true ist, wird der gesamte Inhalt eines Blattes im Ergebnis nur auf einer Seite ausgegeben. Das Papierformat von pagesetup ist ungültig und die anderen Einstellungen von pagesetup bleiben weiterhin wirksam.|
| AllColumnsInOnePagePerSheet| Boolescher Wert| WAHR| FALSCH||Wenn AllColumnsInOnePagePerSheet true ist, wird der gesamte Spalteninhalt eines Blattes im Ergebnis nur auf einer Seite ausgegeben. Die Breite des Papierformats von pagesetup wird ignoriert und die anderen Einstellungen von pagesetup bleiben weiterhin wirksam.|
| Fehler ignorieren| Boolescher Wert| WAHR| FALSCH|| Gibt an, ob Sie den Fehler beim Rendern ausblenden müssen. Der Fehler kann ein Fehler in Form, Bild, Diagrammwiedergabe usw. sein.|
| OutputBlankPageWhenNothingToPrint| Boolescher Wert| WAHR| FALSCH|| Gibt an, ob eine leere Seite ausgegeben werden soll, wenn nichts zu drucken ist.|
| SeitenIndex| Ganze Zahl| WAHR| FALSCH|| Ruft den 0-basierten Index der ersten zu speichernden Seite ab oder legt diesen fest.|
| Seitenzahl| Ganze Zahl| WAHR| FALSCH|| Ruft die Anzahl der zu speichernden Seiten ab oder legt diese fest.|
| PrintingPageType| Zeichenfolge| WAHR| FALSCH|| Gibt an, welche Seiten nicht gedruckt werden.|
| GridlineType| Zeichenfolge| WAHR| FALSCH|| Ruft den Rasterlinientyp ab oder legt diesen fest.|
| TextCrossType| Zeichenfolge| WAHR| FALSCH|| Ruft den Anzeigetexttyp ab oder legt diesen fest, wenn die Textbreite größer als die Zellenbreite ist.|
| DefaultEditLanguage| Zeichenfolge| WAHR| FALSCH|| Ruft die Standardbearbeitungssprache ab oder legt diese fest.|
| EmfRenderSetting| Zeichenfolge| WAHR| FALSCH|||
| MergeAreas| Boolescher Wert| WAHR| FALSCH|||
|SortExternalNames| Boolescher Wert| WAHR| FALSCH|||
| UpdateSmartArt| Boolescher Wert| WAHR| FALSCH|||
| SaveFormat| Zeichenfolge| WAHR| FALSCH|||
| CachedFileFolder| Zeichenfolge| WAHR| FALSCH|||
| Daten löschen| Boolescher Wert| WAHR| FALSCH|||
| Verzeichnis erstellen| Boolescher Wert| WAHR| FALSCH|||
| Aktivieren Sie HTTP-Komprimierung| Boolescher Wert| WAHR| FALSCH|||
| ChartCache aktualisieren| Boolescher Wert| WAHR| FALSCH|||
|Sortiernamen| Boolescher Wert| WAHR| FALSCH|||
| ValidateMergedAreas| Boolescher Wert| WAHR| FALSCH|||

**Elternname** : (Speicheroptionen)[Speicheroptionen]**Kindername** : 
	-  [DocxSaveOptions](docxsaveoptions) 
	-  [PptxSaveOptions](pptxsaveoptions) 
	-  [XpsSaveOptions](xpssaveoptions) 
