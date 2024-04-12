---
title: ImageSaveOption
second_title: Aspose.Cells Cloud Documen
type: docs
url: /de/specification/model/imagesaveoptions/
description: "Aspose.Cells Cloud-Modellspezifikation: ImageSaveOptions. Bearbeiten Sie mühelos Excel und andere Tabellenkalkulationsdokumente mit Funktionen wie Öffnen, Generieren, Bearbeiten, Teilen, Zusammenführen, Vergleichen und Konvertieren"
weight: 50
---
## **imageSaveOptions**

 Stellt Optionen zum Speichern einer Bilddatei dar.

| Name des Anwesens| Art der Immobilie| Nullbar| Schreibgeschützt| Standardwert| Beschreibung|
|:- |:- |:- |:- |:- |:- |
| ChartImageType| Zeichenfolge| WAHR| FALSCH|| Geben Sie beim Konvertieren den Bildtyp des Diagramms an.|
| EmbededImageNameInSvg| Zeichenfolge| WAHR| FALSCH|| Geben Sie den Dateinamen des eingebetteten Bildes im SVG-Format an. Dies sollte ein vollständiger Pfad mit einem Verzeichnis wie „c:\\xpsEmbeded“ sein.|
| Horizontale Auflösung| Ganze Zahl| WAHR| FALSCH|| Ruft die horizontale Auflösung für generierte Bilder in Punkten pro Zoll ab oder legt diese fest. Wendet die Methode zur Bildgenerierung an, mit Ausnahme von Bildern im Emf-Format. Der Standardwert ist 96.|
| Bildformat| Zeichenfolge| WAHR| FALSCH||Ruft das Format der generierten Bilder ab oder legt es fest. Wenden Sie nicht die Methode an, die ein Bitmap-Objekt zurückgibt. Der Standardwert ist ImageFormat.Bmp. Wenden Sie nicht die Methode an, die ein Bitmap-Objekt zurückgibt.|
| IsCellAutoFit| Boolescher Wert| WAHR| FALSCH|| Gibt an, ob die Breite und Höhe der Zellen automatisch an den Zellenwert angepasst wird. Der Standardwert ist false.|
| Eine Seite pro Blatt| Boolescher Wert| WAHR| FALSCH|| Wenn OnePagePerSheet true ist, wird der gesamte Inhalt eines Blattes im Ergebnis nur auf einer Seite ausgegeben. Das Papierformat von „pagesetup“ ist ungültig und die anderen Einstellungen von „pagesetup“ bleiben weiterhin wirksam.|
| OnlyArea| Boolescher Wert| WAHR| FALSCH|| Wenn diese Eigenschaft true ist, wird nur die Fläche ausgegeben und es wird keine Skalierung wirksam.|
| Druckseite| Zeichenfolge| WAHR| FALSCH|| Gibt an, welche Seiten nicht gedruckt werden.|
| PrintWithStatusDialog| Boolescher Wert| WAHR| FALSCH|| Wenn PrintWithStatusDialog = true ist, wird ein Dialog angezeigt, der den aktuellen Druckstatus anzeigt. Andernfalls wird kein solcher Dialog angezeigt.|
|Qualität| Ganze Zahl| WAHR| FALSCH||Ruft einen Wert ab oder legt ihn fest, der die Qualität der generierten Bilder bestimmt und nur beim Speichern von Seiten im JPEG-Format angewendet wird. Wirkt nur beim Speichern unter JPEG. Der Wert muss zwischen 0 und 100 liegen. Der Standardwert ist 100.|
| TiffCompression| Zeichenfolge| WAHR| FALSCH|| Ruft den Komprimierungstyp ab, der nur beim Speichern von Seiten im TIFF-Format angewendet werden soll, oder legt diesen fest. Wirkt nur beim Speichern auf TIFF. Der Standardwert ist Lzw.|
| Vertikale Auflösung| Ganze Zahl| WAHR| FALSCH|| Ruft die vertikale Auflösung für generierte Bilder in Punkten pro Zoll ab oder legt diese fest. Wendet die Methode zur Bildgenerierung an, mit Ausnahme von Bildern im EMF-Format. Der Standardwert ist 96.|
| SaveFormat| Zeichenfolge| WAHR| FALSCH|||
| CachedFileFolder| Zeichenfolge| WAHR| FALSCH|||
| Daten löschen| Boolescher Wert| WAHR| FALSCH|||
| Verzeichnis erstellen| Boolescher Wert| WAHR| FALSCH|||
| Aktivieren Sie HTTP-Komprimierung| Boolescher Wert| WAHR| FALSCH|||
| ChartCache aktualisieren| Boolescher Wert| WAHR| FALSCH|||
|Sortiernamen| Boolescher Wert| WAHR| FALSCH|||
| ValidateMergedAreas| Boolescher Wert| WAHR| FALSCH|||

**Elternname** : (Speicheroptionen)[Speicheroptionen]