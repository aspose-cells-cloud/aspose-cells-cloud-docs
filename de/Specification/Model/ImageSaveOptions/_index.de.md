---
title: BildSpeichernOption
second_title: Aspose.Cells Cloud Documen
type: docs
url: /de/specification/model/imagesaveoptions/
description: "Aspose.Cells Cloud-Modellspezifikation: ImageSaveOptions. Müheloses Bearbeiten von Excel und anderen Tabellenkalkulationsdokumenten mit Funktionen wie Öffnen, Generieren, Bearbeiten, Teilen, Zusammenführen, Vergleichen und Konvertieren"
kwords: Excel, Office, Tabellenkalkulation, Cloud REST API, ImageSaveOptions
weight: 50
---
## **BildSpeichernOptionen**

 Stellt Optionen zum Speichern der Bilddatei dar.

| Name des Anwesens| Art der Immobilie| Nullwerte zulassen| Schreibgeschützt| Standardwert| Beschreibung|
|:- |:- |:- |:- |:- |:- |
| ChartImageType| Zeichenfolge| WAHR| FALSCH|| Geben Sie beim Konvertieren den Diagrammbildtyp an.|
| EingebetteterBildnameInSvg| Zeichenfolge| WAHR| FALSCH|| Geben Sie den Dateinamen des eingebetteten Bildes in SVG an. Dies sollte der vollständige Pfad mit Verzeichnis sein, z. B. „c:\\xpsEmbeded“.|
| HorizontaleAuflösung| Ganze Zahl| WAHR| FALSCH|| Ruft die horizontale Auflösung für generierte Bilder in Punkten pro Zoll ab oder legt sie fest. Wendet die Methode zum Generieren von Bildern an, außer für Bilder im EMF-Format. Der Standardwert ist 96.|
| Bildformat| Zeichenfolge| WAHR| FALSCH|| Ruft das Format der generierten Bilder ab oder legt es fest. Wenden Sie nicht die Methode an, die ein Bitmap-Objekt zurückgibt. Der Standardwert ist ImageFormat.Bmp. Wenden Sie nicht die Methode an, die ein Bitmap-Objekt zurückgibt.|
| IsCellAutoFit| Boolescher Wert| WAHR| FALSCH|| Gibt an, ob die Breite und Höhe der Zellen automatisch anhand des Zellenwerts angepasst wird. Der Standardwert ist „false“.|
| EineSeiteProBlatt| Boolescher Wert| WAHR| FALSCH||Wenn OnePagePerSheet true ist, wird der gesamte Inhalt eines Blatts als Ergebnis nur auf einer Seite ausgegeben. Die Papiergröße von Seiteneinrichtung ist ungültig und die anderen Einstellungen von Seiteneinrichtung bleiben weiterhin wirksam.|
| NurBereich| Boolescher Wert| WAHR| FALSCH|| Wenn diese Eigenschaft wahr ist, wird nur die Fläche ausgegeben und es wird kein Maßstab wirksam.|
| Druckseite| Zeichenfolge| WAHR| FALSCH|| Gibt an, welche Seiten nicht gedruckt werden.|
| DruckenMitStatusDialog| Boolescher Wert| WAHR| FALSCH|| Wenn PrintWithStatusDialog = true ist, wird ein Dialogfeld angezeigt, das den aktuellen Druckstatus anzeigt. Andernfalls wird kein solches Dialogfeld angezeigt.|
| Qualität| Ganze Zahl| WAHR| FALSCH|| Ruft einen Wert ab oder legt ihn fest, der die Qualität der generierten Bilder bestimmt und nur beim Speichern von Seiten im JPEG-Format angewendet wird. Hat nur Auswirkungen beim Speichern in JPEG. Der Wert muss zwischen 0 und 100 liegen. Der Standardwert ist 100.|
| TiffKomprimierung| Zeichenfolge| WAHR| FALSCH|| Ruft den Komprimierungstyp ab oder legt ihn fest, der nur beim Speichern von Seiten im Tiff-Format angewendet werden soll. Hat nur Auswirkungen beim Speichern in TIFF. Der Standardwert ist Lzw.|
| Vertikale Auflösung| Ganze Zahl| WAHR| FALSCH||Ruft die vertikale Auflösung für generierte Bilder in Punkten pro Zoll ab oder legt sie fest. Wendet die Methode zur Bildgenerierung an, außer für Bilder im Emf-Format. Der Standardwert ist 96.|
| Format speichern| Zeichenfolge| WAHR| FALSCH|||
| ZwischengespeicherterDateiordner| Zeichenfolge| WAHR| FALSCH|||
| Daten löschen| Boolescher Wert| WAHR| FALSCH|||
| Verzeichnis erstellen| Boolescher Wert| WAHR| FALSCH|||
| HTTP-Komprimierung aktivieren| Boolescher Wert| WAHR| FALSCH|||
| ChartCache aktualisieren| Boolescher Wert| WAHR| FALSCH|||
| SortNames| Boolescher Wert| WAHR| FALSCH|||
| ValidateMergedAreas| Boolescher Wert| WAHR| FALSCH|||

**Elternname** : [Speicheroptionen](/specification/model/saveoptions)

