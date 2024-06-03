---
title: PdfSaveOption
second_title: Aspose.Cells Cloud Documen
type: docs
url: /de/specification/model/pdfsaveoptions/
description: "Aspose.Cells Cloud-Modellspezifikation: PdfSaveOptions. Müheloses Bearbeiten von Excel und anderen Tabellenkalkulationsdokumenten mit Funktionen wie Öffnen, Generieren, Bearbeiten, Teilen, Zusammenführen, Vergleichen und Konvertieren"
kwords: Excel, Office, Tabellenkalkulation, Cloud REST API, PdfSaveOptions
weight: 50
---
## **pdfSpeicheroptionen**

 Stellt Optionen zum Speichern der PDF-Datei dar.

| Name des Anwesens| Art der Immobilie| Nullwerte zulassen| Schreibgeschützt| Standardwert| Beschreibung|
|:- |:- |:- |:- |:- |:- |
| Dokumenttitel anzeigen| Boolescher Wert| WAHR| FALSCH|| Gibt an, ob in der Titelleiste des Fensters der Dokumenttitel angezeigt werden soll.|
| Dokumentstruktur exportieren| Boolescher Wert| WAHR| FALSCH|| Gibt an, ob die Dokumentstruktur exportiert werden soll.|
| EmfRenderEinstellung| Zeichenfolge| WAHR| FALSCH|| Einstellung zum Rendern der EMF-Metadatei.|
| BenutzerdefinierteEigenschaftenExport| Zeichenfolge| WAHR| FALSCH|| Gibt an, wie CustomDocumentPropertyCollection in die Datei PDF exportiert werden.|
| Optimierungstyp| Zeichenfolge| WAHR| FALSCH|| Ruft den PDF-Optimierungstyp ab und legt ihn fest.|
| Hersteller| Zeichenfolge| WAHR| FALSCH|| Ruft den Produzenten des generierten PDF-Dokuments ab und legt ihn fest.|
| PDF-Komprimierung| Zeichenfolge| WAHR| FALSCH|| Geben Sie den Komprimierungsalgorithmus an.|
| Schriftkodierung| Zeichenfolge| WAHR| FALSCH|| Ruft die eingebettete Schriftkodierung im PDF ab oder legt sie fest.|
| Wasserzeichen|Klasse:RenderingWatermark| WAHR| FALSCH|| Ruft das Wasserzeichen für die Ausgabe ab oder legt es fest.|
| Formel berechnen| Boolescher Wert| WAHR| FALSCH|| Gibt an, ob Formeln vor dem Speichern der PDF-Datei berechnet werden. Der Standardwert ist „false“.|
| Schriftartenkompatibilität prüfen| Boolescher Wert| WAHR| FALSCH|| Gibt an, ob die Schriftartkompatibilität für jedes Zeichen im Text überprüft wird. Der Standardwert ist „true“. Das Deaktivieren dieser Eigenschaft kann zu einer besseren Leistung führen. Wenn jedoch die Standardschriftart oder die angegebene Schriftart des Textes/Zeichens nicht zum Rendern verwendet werden kann, können im generierten PDF unlesbare Zeichen (z. B. Block) auftreten. In solchen Fällen sollte der Benutzer diese Eigenschaft auf „true“ belassen, damit eine alternative Schriftart gesucht und stattdessen zum Rendern des Textes verwendet werden kann.|
| Einhaltung| Zeichenfolge| WAHR| FALSCH|| Die Arbeitsmappe wird gemäß PdfCompliance in dieser Eigenschaft ins PDF konvertiert.|
| Standardschriftart| Zeichenfolge| WAHR| FALSCH||Wenn Zeichen in Excel Unicode sind und nicht mit der richtigen Schriftart im Zellenstil festgelegt sind, können sie in PDFs und Bildern als Block angezeigt werden. Legen Sie die Standardschriftart wie MingLiu oder MS Gothic fest, um diese Zeichen anzuzeigen. Wenn diese Eigenschaft nicht festgelegt ist, verwendet Aspose.Cells die Standardschriftart des Systems, um diese Unicode-Zeichen anzuzeigen.|
| EineSeiteProBlatt| Boolescher Wert| WAHR| FALSCH|| Wenn OnePagePerSheet true ist, wird der gesamte Inhalt eines Blatts als Ergebnis nur auf einer Seite ausgegeben. Die Papiergröße von Seiteneinrichtung ist ungültig und die anderen Einstellungen von Seiteneinrichtung bleiben weiterhin wirksam.|
| Druckseitentyp| Zeichenfolge| WAHR| FALSCH|| Gibt an, welche Seiten nicht gedruckt werden.|
| Sicherheitsoptionen| Klasse:PdfSecurityOptions| WAHR| FALSCH|| Legen Sie diese Optionen fest, wenn Sicherheit im XLS2PDF-Ergebnis erforderlich ist.|
| gewünschterPPI| Ganze Zahl| WAHR| FALSCH||Legen Sie die gewünschte PPI (Pixel pro Zoll) für die Neuabtastung von Bildern und die JPEG-Qualität fest. Alle Bilder werden mit der angegebenen Qualitätseinstellung in JPEG konvertiert und Bilder, die größer als die angegebene PPI (Pixel pro Zoll) sind, werden neu abgetastet. Gewünschte Pixel pro Zoll: 220 hohe Qualität. 150 Bildschirmqualität. 96 E-Mail-Qualität.|
| jpegQualität| Ganze Zahl| WAHR| FALSCH|| Stellen Sie die gewünschte PPI (Pixel pro Zoll) der Neuabtastung von Bildern und die JPEG-Qualität ein. Alle Bilder werden mit der angegebenen Qualitätseinstellung in JPEG konvertiert und Bilder, die größer als die angegebene PPI (Pixel pro Zoll) sind, werden neu abgetastet. 0 - 100 % JPEG Qualität.|
| Bildtyp| Zeichenfolge| WAHR| FALSCH|| Stellt den Bildtyp beim Konvertieren des Diagramms und der Form dar.|
| Format speichern| Zeichenfolge| WAHR| FALSCH|||
| ZwischengespeicherterDateiordner| Zeichenfolge| WAHR| FALSCH|||
| Daten löschen| Boolescher Wert| WAHR| FALSCH|||
| Verzeichnis erstellen| Boolescher Wert| WAHR| FALSCH|||
| HTTP-Komprimierung aktivieren| Boolescher Wert| WAHR| FALSCH|||
| ChartCache aktualisieren| Boolescher Wert| WAHR| FALSCH|||
| SortNames| Boolescher Wert| WAHR| FALSCH|||
| ValidateMergedAreas| Boolescher Wert| WAHR| FALSCH|||

**Elternname** : [Speicheroptionen](/specification/model/saveoptions)

