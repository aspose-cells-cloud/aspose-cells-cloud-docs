---
title: PDFSaveOption
second_title: Aspose.Cells Cloud Documen
type: docs
url: /de/specification/model/pdfsaveoptions/
description: "Aspose.Cells Cloud-Modellspezifikation: PdfSaveOptions. Bearbeiten Sie mühelos Excel und andere Tabellenkalkulationsdokumente mit Funktionen wie Öffnen, Generieren, Bearbeiten, Teilen, Zusammenführen, Vergleichen und Konvertieren"
weight: 50
---
## **pdfSaveOptions**

 Stellt Optionen zum Speichern einer PDF-Datei dar.

| Name des Anwesens| Art der Immobilie| Nullbar| Schreibgeschützt| Standardwert| Beschreibung|
|:- |:- |:- |:- |:- |:- |
| DisplayDocTitle| Boolescher Wert| WAHR| FALSCH|| Gibt an, ob in der Titelleiste des Fensters der Dokumenttitel angezeigt werden soll.|
| ExportDocumentStructure| Boolescher Wert| WAHR| FALSCH|| Gibt an, ob die Dokumentstruktur exportiert werden soll.|
| EmfRenderSetting| Zeichenfolge| WAHR| FALSCH|| Einstellung zum Rendern der EMF-Metadatei.|
| CustomPropertiesExport| Zeichenfolge| WAHR| FALSCH|| Gibt die Art und Weise an, wie CustomDocumentPropertyCollection in die Datei PDF exportiert wird.|
| Optimierungstyp| Zeichenfolge| WAHR| FALSCH|| Ruft den PDF-Optimierungstyp ab und legt ihn fest.|
| Hersteller| Zeichenfolge| WAHR| FALSCH|| Ruft den Produzenten des generierten PDF-Dokuments ab und legt diesen fest.|
| PDFKomprimierung| Zeichenfolge| WAHR| FALSCH||Geben Sie den Komprimierungsalgorithmus an.|
| FontEncoding| Zeichenfolge| WAHR| FALSCH|| Ruft die eingebettete Schriftartenkodierung im PDF ab oder legt diese fest.|
| Wasserzeichen| Klasse:RenderingWatermark| WAHR| FALSCH|| Ruft das Wasserzeichen für die Ausgabe ab oder legt es fest.|
| BerechnenFormel| Boolescher Wert| WAHR| FALSCH|| Gibt an, ob Formeln berechnet werden sollen, bevor die PDF-Datei gespeichert wird. Der Standardwert ist „false“.|
| CheckFontCompatibility| Boolescher Wert| WAHR| FALSCH|| Gibt an, ob die Schriftartkompatibilität für jedes Zeichen im Text überprüft werden soll. Der Standardwert ist wahr. Durch Deaktivieren dieser Eigenschaft kann die Leistung verbessert werden. Wenn jedoch die Standardschriftart oder die angegebene Schriftart für Text/Zeichen nicht zum Rendern verwendet werden kann, können im generierten PDF unlesbare Zeichen (z. B. Blöcke) auftreten. In einer solchen Situation sollte der Benutzer diese Eigenschaft auf „true“ belassen, damit alternative Schriftarten gesucht und stattdessen zum Rendern des Texts verwendet werden können.|
| Einhaltung| Zeichenfolge| WAHR| FALSCH|| Die Konvertierung der Arbeitsmappe in PDF erfolgt gemäß PdfCompliance in dieser Eigenschaft.|
| Standardschriftart| Zeichenfolge| WAHR| FALSCH||Wenn Zeichen in Excel Unicode sind und nicht mit der richtigen Schriftart im Zellenstil festgelegt sind, werden sie möglicherweise als Block im PDF-Bild angezeigt. Legen Sie die Standardschriftart wie MingLiu oder MS Gothic fest, um diese Zeichen anzuzeigen. Wenn diese Eigenschaft nicht festgelegt ist, verwendet Aspose.Cells die Standardschriftart des Systems, um diese Unicode-Zeichen anzuzeigen.|
| Eine Seite pro Blatt| Boolescher Wert| WAHR| FALSCH|| Wenn OnePagePerSheet true ist, wird der gesamte Inhalt eines Blattes im Ergebnis nur auf einer Seite ausgegeben. Das Papierformat von „pagesetup“ ist ungültig und die anderen Einstellungen von „pagesetup“ bleiben weiterhin wirksam.|
| PrintingPageType| Zeichenfolge| WAHR| FALSCH|| Gibt an, welche Seiten nicht gedruckt werden.|
| Sicherheitsoptionen| Klasse:PdfSecurityOptions| WAHR| FALSCH|| Legen Sie diese Optionen fest, wenn Sicherheit im xls2pdf-Ergebnis erforderlich ist.|
| gewünschtePPI| Ganze Zahl| WAHR| FALSCH||Legen Sie den gewünschten PPI (Pixel pro Zoll) für die Neuabtastung von Bildern und die JPEG-Qualität fest. Alle Bilder werden mit der angegebenen Qualitätseinstellung in JPEG konvertiert, und Bilder, die größer als der angegebene PPI (Pixel pro Zoll) sind, werden neu abgetastet. Gewünschte Pixel pro Zoll. 220 hohe Qualität. 150 Bildschirmqualität. 96 E-Mail-Qualität.|
| jpegQuality| Ganze Zahl| WAHR| FALSCH|| Legen Sie den gewünschten PPI (Pixel pro Zoll) für die Neuabtastung von Bildern und die JPEG-Qualität fest. Alle Bilder werden mit der angegebenen Qualitätseinstellung in JPEG konvertiert, und Bilder, die größer als der angegebene PPI (Pixel pro Zoll) sind, werden neu abgetastet. 0 - 100 % JPEG Qualität.|
| Bildtyp| Zeichenfolge| WAHR| FALSCH|| Stellt den Bildtyp beim Konvertieren des Diagramms und der Form dar.|
| SaveFormat| Zeichenfolge| WAHR| FALSCH|||
| CachedFileFolder| Zeichenfolge| WAHR| FALSCH|||
| Daten löschen| Boolescher Wert| WAHR| FALSCH|||
| Verzeichnis erstellen| Boolescher Wert| WAHR| FALSCH|||
| Aktivieren Sie HTTP-Komprimierung| Boolescher Wert| WAHR| FALSCH|||
| ChartCache aktualisieren| Boolescher Wert| WAHR| FALSCH|||
|Sortiernamen| Boolescher Wert| WAHR| FALSCH|||
| ValidateMergedAreas| Boolescher Wert| WAHR| FALSCH|||

**Elternname** : (Speicheroptionen)[Speicheroptionen]