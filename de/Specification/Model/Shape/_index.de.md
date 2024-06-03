---
title: Form
second_title: Aspose.Cells Cloud Documen
type: docs
url: /de/specification/model/shape/
description: "Aspose.Cells Cloud-Modellspezifikation: Shape. Müheloses Bearbeiten von Excel und anderen Tabellenkalkulationsdokumenten mit Funktionen wie Öffnen, Generieren, Bearbeiten, Teilen, Zusammenführen, Vergleichen und Konvertieren"
kwords: Excel, Office, Tabellenkalkulation, Cloud REST API, Form
weight: 50
---
## **Form**

 Stellt das MSOdrawing-Objekt dar.

| Name des Anwesens| Art der Immobilie| Nullwerte zulassen| Schreibgeschützt| Standardwert| Beschreibung|
|:- |:- |:- |:- |:- |:- |
| Name| Zeichenfolge| WAHR| FALSCH|| Ruft den Namen der Form ab und legt ihn fest.|
| MsoDrawingType| Zeichenfolge| WAHR| FALSCH|| Ruft den MSO-Zeichnungstyp ab.|
| AutoFormTyp| Zeichenfolge| WAHR| FALSCH|| Ruft den automatischen Formtyp ab und legt ihn fest.|
| Platzierung| Zeichenfolge| WAHR| FALSCH|| Stellt die Art und Weise dar, wie das Zeichenobjekt mit den darunterliegenden Zellen verbunden ist. Die Eigenschaft steuert die Platzierung eines Objekts auf einem Arbeitsblatt.|
| Obere Linke Zeile| Ganze Zahl| WAHR| FALSCH|| Stellt den Zeilenindex in der oberen linken Ecke dar.|
| Spitze| Ganze Zahl| WAHR| FALSCH|| Stellt den vertikalen Versatz der Form von ihrer obersten Reihe in Pixeln dar.|
| Obere Linke Spalte| Ganze Zahl| WAHR| FALSCH|| Stellt den Spaltenindex in der oberen linken Ecke dar.|
| Links| Ganze Zahl| WAHR| FALSCH|| Stellt den horizontalen Versatz der Form von ihrer linken Spalte in Pixeln dar.|
| UntereRechteReihe| Ganze Zahl| WAHR| FALSCH|| Stellt den Zeilenindex in der unteren rechten Ecke dar.|
| Unten| Ganze Zahl| WAHR| FALSCH||Stellt die Breite des vertikalen Versatzes der Form von ihrer unteren Eckreihe in Pixeln dar.|
| Untere Rechte Spalte| Ganze Zahl| WAHR| FALSCH|| Stellt den Spaltenindex in der unteren rechten Ecke dar.|
| Rechts| Ganze Zahl| WAHR| FALSCH|| Stellt die Breite des horizontalen Versatzes der Form von ihrer unteren rechten Eckspalte in Pixeln dar.|
| Breite| Ganze Zahl| WAHR| FALSCH|| Stellt die Breite der Form in Pixeln dar.|
| Höhe| Ganze Zahl| WAHR| FALSCH|| Stellt die Höhe der Form in Pixeln dar.|
| X| Ganze Zahl| WAHR| FALSCH|| Ruft den horizontalen Versatz der Form vom linken Arbeitsblattrand in Pixeln ab und legt ihn fest.|
| Y| Ganze Zahl| WAHR| FALSCH|| Ruft den vertikalen Versatz der Form vom oberen Arbeitsblattrand in Pixeln ab und legt ihn fest.|
| Drehwinkel| Schwimmend| WAHR| FALSCH|| Ruft die Drehung der Form ab und legt sie fest.|
|HTMLText| Zeichenfolge| WAHR| FALSCH|| Ruft die HTML-Zeichenfolge ab und legt sie fest, die Daten und einige Formate in diesem Textfeld enthält.|
| Text| Zeichenfolge| WAHR| FALSCH|| Stellt die Zeichenfolge in diesem TextBox-Objekt dar.|
| Alternativer Text| Zeichenfolge| WAHR| FALSCH|| Gibt die beschreibende (alternative) Textzeichenfolge des Objekts zurück oder legt sie fest.|
| TextHorizontalAlignment| Zeichenfolge| WAHR| FALSCH|| Ruft den horizontalen Textausrichtungstyp der Form ab und legt ihn fest.|
| TextHorizontalOverflow| Zeichenfolge| WAHR| FALSCH|| Ruft den horizontalen Textüberlauftyp der Form ab, die Text enthält, und legt ihn fest.|
| TextOrientationType| Zeichenfolge| WAHR| FALSCH||Ruft den Textausrichtungstyp der Form ab und legt ihn fest.|
| TextVerticalAlignment| Zeichenfolge| WAHR| FALSCH|| Ruft den Typ der vertikalen Textausrichtung der Form ab und legt ihn fest.|
| TextVerticalOverflow| Zeichenfolge| WAHR| FALSCH|| Ruft den vertikalen Textüberlauftyp der Form ab, die Text enthält, und legt ihn fest.|
| IstGruppe| Boolescher Wert| WAHR| FALSCH|| Gibt an, ob die Form eine Gruppe ist.|
| Ist versteckt| Boolescher Wert| WAHR| FALSCH|| Gibt an, ob das Objekt sichtbar ist.|
| IsLockAspectRatio| Boolescher Wert| WAHR| FALSCH|| „True“ bedeutet, dass keine Änderungen des Seitenverhältnisses zulässig sind.|
| Ist gesperrt| Boolescher Wert| WAHR| FALSCH|| „True“, wenn das Objekt gesperrt ist, „False“, wenn das Objekt geändert werden kann, während das Blatt geschützt ist.|
| IstDruckbar| Boolescher Wert| WAHR| FALSCH|| Wahr, wenn das Objekt druckbar ist|
| IstTextWrapped| Boolescher Wert| WAHR| FALSCH|| Ruft den Textumbruchtyp der Form ab, die Text enthält, und legt ihn fest.|
| IstWordArt| Boolescher Wert| WAHR| FALSCH|| Gibt an, ob es sich bei dieser Form um eine WordArt handelt.|
| LinkedCell| Zeichenfolge| WAHR| FALSCH|| Ruft den mit dem Wert des Steuerelements verknüpften Arbeitsblattbereich ab oder legt ihn fest.|
| ZOrderPosition| Ganze Zahl| WAHR| FALSCH|| Gibt die Position einer Form in der Z-Reihenfolge zurück.|
| Schriftart| Klasse:Schriftart| WAHR| FALSCH|| Stellt die Schriftart der Form dar.|
| Hyperlink| Zeichenfolge| WAHR| FALSCH|| Ruft den Hyperlink der Form ab.|
| Verknüpfung| Klasse:Link| WAHR| FALSCH|||

**Elternname** : [LinkElement](/specification/model/linkelement)

**Name des Kindes** : 
	-  [Bogenform](arcshape) 
	-  [AutoForm](autoshape) 
	-  [Taste](button) 
	-  [ZellenZeichnung](cellsdrawing) 
	-  [Kontrollkästchen](checkbox) 
	-  [Kombinationsfeld](combobox) 
	-  [Kommentarform](commentshape) 
	-  [Bilden](form) 
	-  [Gruppenfeld](groupbox) 
	-  [Gruppenform](groupshape) 
	-  [Etikett](label) 
	-  [Linienform](lineshape) 
	-  [Listenfeld](listbox) 
	-  [OLE-Objekt](oleobject) 
	-  [Oval](oval) 
	-  [Bild](picture) 
	-  [Radio knopf](radiobutton) 
	-  [Rechteckform](rectangleshape) 
	-  [Scrollleiste](scrollbar) 
	-  [Spinner](spinner) 
	-  [Textfeld](textbox) 
	-  [Diagrammform](chartshape) 
