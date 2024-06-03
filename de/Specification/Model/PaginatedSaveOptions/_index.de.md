---
title: PaginatedSaveOption
second_title: Aspose.Cells Cloud Documen
type: docs
url: /de/specification/model/paginatedsaveoptions/
description: "Aspose.Cells Cloud-Modellspezifikation: PaginatedSaveOptions. Müheloses Bearbeiten von Excel und anderen Tabellenkalkulationsdokumenten mit Funktionen wie Öffnen, Generieren, Bearbeiten, Teilen, Zusammenführen, Vergleichen und Konvertieren"
kwords: Excel, Office, Tabellenkalkulation, Cloud REST API, PaginatedSaveOptions
weight: 50
---
## **paginierteSpeicheroptionen**

 Stellt die Optionen für die Seitennummerierung dar.

| Name des Anwesens| Art der Immobilie| Nullwerte zulassen| Schreibgeschützt| Standardwert| Beschreibung|
|:- |:- |:- |:- |:- |:- |
| Standardschriftart| Zeichenfolge| WAHR| FALSCH|| Wenn Zeichen in Excel Unicode sind und nicht mit der richtigen Schriftart im Zellenstil festgelegt sind, werden sie möglicherweise als Block in PDFs und Bildern angezeigt. Legen Sie die Standardschriftart wie MingLiu oder MS Gothic fest, um diese Zeichen anzuzeigen. Wenn diese Eigenschaft nicht festgelegt ist, verwendet Aspose.Cells die Standardschriftart des Systems, um diese Unicode-Zeichen anzuzeigen.|
| Überprüfen Sie die Arbeitsmappen-Standardschriftart| Boolescher Wert| WAHR| FALSCH|| Wenn die Zeichen in Excel Unicode sind und im Zellenstil nicht mit der richtigen Schriftart festgelegt sind, werden sie im PDF-Bild möglicherweise als Block angezeigt. Setzen Sie dies auf „True“, um zu versuchen, die Standardschriftart der Arbeitsmappe zu verwenden, um diese Zeichen zuerst anzuzeigen.|
| Schriftartenkompatibilität prüfen| Boolescher Wert| WAHR| FALSCH|| Gibt an, ob die Schriftartkompatibilität für jedes Zeichen im Text überprüft werden soll.|
| IsFontSubstitutionCharGranularity| Boolescher Wert| WAHR| FALSCH||Gibt an, ob die Schriftart des Zeichens nur ersetzt werden soll, wenn die Zellenschriftart damit nicht kompatibel ist.|
| EineSeiteProBlatt| Boolescher Wert| WAHR| FALSCH|| Wenn „OnePagePerSheet“ wahr ist, wird der gesamte Inhalt eines Blattes im Ergebnis nur auf einer Seite ausgegeben. Die Papiergröße von „pagesetup“ ist ungültig und die anderen Einstellungen von „pagesetup“ bleiben weiterhin wirksam.|
| AlleSpaltenAufEinerSeiteProBlatt| Boolescher Wert| WAHR| FALSCH|| Wenn „AllColumnsInOnePagePerSheet“ „true“ ist, wird der gesamte Spalteninhalt eines Blattes im Ergebnis nur auf einer Seite ausgegeben. Die Papierbreite des Seiten-Setups wird ignoriert und die anderen Einstellungen des Seiten-Setups bleiben weiterhin wirksam.|
| Fehler ignorieren| Boolescher Wert| WAHR| FALSCH|| Gibt an, ob Sie den Fehler beim Rendern ausblenden müssen. Der Fehler kann ein Fehler beim Rendern einer Form, eines Bilds, eines Diagramms usw. sein.|
| Ausgabe einer leeren Seite, wenn nichts zu drucken ist| Boolescher Wert| WAHR| FALSCH|| Gibt an, ob eine leere Seite ausgegeben werden soll, wenn nichts zu drucken ist.|
| Seitenindex| Ganze Zahl| WAHR| FALSCH|| Ruft den 0-basierten Index der ersten zu speichernden Seite ab oder legt ihn fest.|
| Seitenzahl| Ganze Zahl| WAHR| FALSCH|| Ruft die Anzahl der zu speichernden Seiten ab oder legt sie fest.|
| Druckseitentyp| Zeichenfolge| WAHR| FALSCH|| Gibt an, welche Seiten nicht gedruckt werden.|
| Gitternetzlinientyp| Zeichenfolge| WAHR| FALSCH|| Ruft den Gitternetzlinientyp ab oder legt ihn fest.|
| TextCrossType| Zeichenfolge| WAHR| FALSCH|| Ruft den anzuzeigenden Texttyp ab oder legt ihn fest, wenn die Textbreite größer als die Zellenbreite ist.|
| Standardsprache bearbeiten| Zeichenfolge| WAHR| FALSCH|| Ruft die Standardbearbeitungssprache ab oder legt sie fest.|
| EmfRenderEinstellung| Zeichenfolge| WAHR| FALSCH|||
| Bereiche zusammenführen| Boolescher Wert| WAHR| FALSCH|||
| SortExternalNames| Boolescher Wert| WAHR| FALSCH|||
| AktualisierenSmartArt| Boolescher Wert| WAHR| FALSCH|||
| Format speichern| Zeichenfolge| WAHR| FALSCH|||
| ZwischengespeicherterDateiordner| Zeichenfolge| WAHR| FALSCH|||
| Daten löschen| Boolescher Wert| WAHR| FALSCH|||
| Verzeichnis erstellen| Boolescher Wert| WAHR| FALSCH|||
| HTTP-Komprimierung aktivieren| Boolescher Wert| WAHR| FALSCH|||
| ChartCache aktualisieren| Boolescher Wert| WAHR| FALSCH|||
| SortNames| Boolescher Wert| WAHR| FALSCH|||
| ValidateMergedAreas| Boolescher Wert| WAHR| FALSCH|||

**Elternname** : [Speicheroptionen](/specification/model/saveoptions)

**Name des Kindes** : 
	-  [DocxSaveOptions](docxsaveoptions) 
	-  [PptxSpeichernOptionen](pptxsaveoptions) 
	-  [XpsSaveOptions](xpssaveoptions) 
