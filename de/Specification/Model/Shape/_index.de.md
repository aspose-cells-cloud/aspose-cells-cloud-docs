---
title: Form
second_title: Aspose.Cells Cloud Documen
type: docs
url: /de/specification/model/shape/
description: "Aspose.Cells Wolkenmodellspezifikation: Form. Bearbeiten Sie mühelos Excel und andere Tabellenkalkulationsdokumente mit Funktionen wie Öffnen, Generieren, Bearbeiten, Teilen, Zusammenführen, Vergleichen und Konvertieren"
weight: 50
---
## **Form**

 

| Name des Anwesens| Art der Immobilie| Nullbar| Schreibgeschützt| Standardwert| Beschreibung|
|:- |:- |:- |:- |:- |:- |
| Name| Zeichenfolge| WAHR| FALSCH|| Ruft den Namen der Form ab und legt ihn fest.|
| MsoDrawingType| Zeichenfolge| WAHR| FALSCH|| Ruft den MSO-Zeichnungstyp ab.|
| AutoShapeType| Zeichenfolge| WAHR| FALSCH|| Ruft den automatischen Formtyp ab und legt ihn fest.|
| Platzierung| Zeichenfolge| WAHR| FALSCH|| Stellt die Art und Weise dar, wie das Zeichenobjekt an die darunter liegenden Zellen angehängt wird. Die Eigenschaft steuert die Platzierung eines Objekts auf einem Arbeitsblatt.|
| UpperLeftRow| Ganze Zahl| WAHR| FALSCH|| Stellt den Zeilenindex der oberen linken Ecke dar.|
| Spitze| Ganze Zahl| WAHR| FALSCH||Stellt den vertikalen Versatz der Form von ihrer oberen Reihe in Pixeleinheiten dar.|
| UpperLeftColumn| Ganze Zahl| WAHR| FALSCH|| Stellt den Spaltenindex in der oberen linken Ecke dar.|
| Links| Ganze Zahl| WAHR| FALSCH|| Stellt den horizontalen Versatz der Form von ihrer linken Spalte in Pixeleinheiten dar.|
| LowerRightRow| Ganze Zahl| WAHR| FALSCH|| Stellt den Zeilenindex in der unteren rechten Ecke dar.|
| Unten| Ganze Zahl| WAHR| FALSCH|| Stellt die Breite des vertikalen Versatzes der Form von ihrer unteren unteren Eckreihe in Pixeleinheiten dar.|
| LowerRightColumn| Ganze Zahl| WAHR| FALSCH|| Stellt den Spaltenindex in der unteren rechten Ecke dar.|
| Rechts| Ganze Zahl| WAHR| FALSCH|| Stellt die Breite des horizontalen Versatzes der Form von ihrer unteren rechten Eckspalte in der Einheit Pixel dar.|
| Breite| Ganze Zahl| WAHR| FALSCH|| Stellt die Breite der Form in der Einheit Pixel dar.|
| Höhe| Ganze Zahl| WAHR| FALSCH|| Stellt die Höhe der Form in der Einheit Pixel dar.|
| X| Ganze Zahl| WAHR| FALSCH|| Ruft den horizontalen Versatz der Form vom linken Rand des Arbeitsblatts in Pixeleinheiten ab und legt diesen fest.|
| Y| Ganze Zahl| WAHR| FALSCH|| Ruft den vertikalen Versatz der Form vom oberen Rand des Arbeitsblatts in Pixeleinheiten ab und legt diesen fest.|
| Drehwinkel| Schwebend| WAHR| FALSCH|| Ruft die Drehung der Form ab und legt sie fest.|
| HTMLText| Zeichenfolge| WAHR| FALSCH|| Ruft die HTML-Zeichenfolge ab, die Daten und einige Formate in diesem Textfeld enthält, und legt diese fest.|
| Text| Zeichenfolge| WAHR| FALSCH||Stellt die Zeichenfolge in diesem TextBox-Objekt dar.|
| Alternativer Text| Zeichenfolge| WAHR| FALSCH|| Gibt die beschreibende (alternative) Textzeichenfolge des Objekts zurück oder legt sie fest.|
| TextHorizontalAlignment| Zeichenfolge| WAHR| FALSCH|| Ruft den horizontalen Textausrichtungstyp der Form ab und legt diesen fest.|
| TextHorizontalOverflow| Zeichenfolge| WAHR| FALSCH|| Ruft den horizontalen Textüberlauftyp der Form ab, die Text enthält, und legt diesen fest.|
| TextOrientationType| Zeichenfolge| WAHR| FALSCH|| Ruft den Textausrichtungstyp der Form ab und legt ihn fest.|
| TextVerticalAlignment| Zeichenfolge| WAHR| FALSCH|| Ruft den vertikalen Textausrichtungstyp der Form ab und legt diesen fest.|
| TextVerticalOverflow| Zeichenfolge| WAHR| FALSCH|| Ruft den vertikalen Textüberlauftyp der Form ab, die Text enthält, und legt diesen fest.|
| IsGroup| Boolescher Wert| WAHR| FALSCH|| Gibt an, ob es sich bei der Form um eine Gruppe handelt.|
| Ist versteckt| Boolescher Wert| WAHR| FALSCH|| Gibt an, ob das Objekt sichtbar ist.|
| IsLockAspectRatio| Boolescher Wert| WAHR| FALSCH|| „True“ bedeutet, dass keine Änderungen im Seitenverhältnis zulässig sind.|
| Ist gesperrt| Boolescher Wert| WAHR| FALSCH|| True, wenn das Objekt gesperrt ist, False, wenn das Objekt geändert werden kann, während das Blatt geschützt ist.|
| IsPrintable| Boolescher Wert| WAHR| FALSCH|| True, wenn das Objekt druckbar ist|
| IsTextWrapped| Boolescher Wert| WAHR| FALSCH|| Ruft den Textumbruchtyp der Form ab, die Text enthält, und legt diesen fest.|
| Ist WordArt| Boolescher Wert| WAHR| FALSCH|| Gibt an, ob es sich bei dieser Form um eine Wortkunst handelt.|
| LinkedCell| Zeichenfolge| WAHR| FALSCH|| Ruft den mit dem Wert des Steuerelements verknüpften Arbeitsblattbereich ab oder legt diesen fest.|
| ZOrderPosition| Ganze Zahl| WAHR| FALSCH||Gibt die Position einer Form in der Z-Reihenfolge zurück.|
| Schriftart| Klasse:Schriftart| WAHR| FALSCH|| Stellt die Schriftart der Form dar.|
| Hyperlink| Zeichenfolge| WAHR| FALSCH|| Ruft den Hyperlink der Form ab.|
| Verknüpfung| Klasse:Link| WAHR| FALSCH|||

**Elternname** : (LinkElement)[Linkelement]**Kindername** : 
	-  [ArcShape](arcshape) 
	-  [AutoForm](autoshape) 
	-  [Taste](button) 
	-  [ZellenZeichnung](cellsdrawing) 
	-  [CheckBox](checkbox) 
	-  [Kombinationsfeld](combobox) 
	-  [KommentarForm](commentshape) 
	-  [Bilden](form) 
	-  [GroupBox](groupbox) 
	-  [GroupShape](groupshape) 
	-  [Etikett](label) 
	-  [Linienform](lineshape) 
	-  [ListBox](listbox) 
	-  [OLE-Objekt](oleobject) 
	-  [Oval](oval) 
	-  [Bild](picture) 
	-  [Radio knopf](radiobutton) 
	-  [Rechteckform](rectangleshape) 
	-  [Scrollleiste](scrollbar) 
	-  [Spinner](spinner) 
	-  [Textfeld](textbox) 
	-  [ChartShape](chartshape) 
