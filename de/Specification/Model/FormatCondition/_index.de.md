---
title: FormatConditio
second_title: Aspose.Cells Cloud Documen
type: docs
url: /de/specification/model/formatcondition/
description: "Aspose.Cells Cloud-Modellspezifikation: FormatCondition. Bearbeiten Sie mühelos Excel und andere Tabellenkalkulationsdokumente mit Funktionen wie Öffnen, Generieren, Bearbeiten, Teilen, Zusammenführen, Vergleichen und Konvertieren"
weight: 50
---
## **formatCondition**

 

| Name des Anwesens| Art der Immobilie| Nullbar| Schreibgeschützt| Standardwert| Beschreibung|
|:- |:- |:- |:- |:- |:- |
| Priorität| Ganze Zahl| WAHR| FALSCH|| Die Priorität dieser bedingten Formatierungsregel. Dieser Wert wird verwendet, um zu bestimmen, welches Format ausgewertet und gerendert werden soll. Niedrigere numerische Werte haben eine höhere Priorität als höhere numerische Werte, wobei „1“ die höchste Priorität darstellt.|
| Typ| Zeichenfolge| WAHR| FALSCH|| Ruft den Typ des bedingten Formats ab und legt diesen fest.|
| StopIfTrue| Boolescher Wert| WAHR| FALSCH|| True, es dürfen keine Regeln mit niedrigerer Priorität gegenüber dieser Regel angewendet werden, wenn diese Regel als „true“ ausgewertet wird. Gilt nur für Excel 2007;|
| Überdurchschnittlich| Klasse:Überdurchschnittlich| WAHR| FALSCH||Rufen Sie die „AboveAverage“-Instanz der bedingten Formatierung ab. Die Regel der Standardinstanz hebt Zellen hervor, die über dem Durchschnitt aller Werte im Bereich liegen. Nur gültig für Typ = AboveAverage.|
| Farbskala| Klasse:ColorScale| WAHR| FALSCH|| Rufen Sie die „ColorScale“-Instanz der bedingten Formatierung ab. Die Standardinstanz ist eine „grün-gelb-rote“ 3ColorScale . Nur gültig für Typ = ColorScale.|
| DataBar| Klasse:DataBar| WAHR| FALSCH|| Rufen Sie die „DataBar“-Instanz der bedingten Formatierung ab. Die Farbe der Standardinstanz ist blau. Nur gültig für den Typ „DataBar“.|
| Formel 1| Zeichenfolge| WAHR| FALSCH|| Ruft den Wert oder Ausdruck ab, der der bedingten Formatierung zugeordnet ist, und legt diesen fest.|
| Formel2| Zeichenfolge| WAHR| FALSCH|| Ruft den Wert oder Ausdruck ab, der der bedingten Formatierung zugeordnet ist, und legt diesen fest.|
| IconSet| Klasse:IconSet| WAHR| FALSCH||Rufen Sie die „IconSet“-Instanz der bedingten Formatierung ab. Der IconSetType der Standardinstanz ist TrafficLights31. Nur gültig für Typ = IconSet.|
| Operator| Zeichenfolge| WAHR| FALSCH|| Ruft den Operatortyp für das bedingte Format ab und legt ihn fest.|
| Stil| Klasse:Stil| WAHR| FALSCH|| Ruft den Stil bedingt formatierter Zellbereiche ab oder legt diesen fest.|
| Text| Zeichenfolge| WAHR| FALSCH|| Der Textwert in einer bedingten Formatierungsregel „Text enthält“. Nur gültig für Typ = enthältText, notContainsText, beginntmit und endetmit. Der Standardwert ist null.|
| Zeitraum| Zeichenfolge| WAHR| FALSCH|| Der anwendbare Zeitraum in einer bedingten Formatierungsregel „Datum des Auftretens…“. Nur gültig für Typ = timePeriod. Der Standardwert ist TimePeriodType.Today.|
| Top 10| Klasse:Top10| WAHR| FALSCH||Rufen Sie die „Top10“-Instanz der bedingten Formatierung ab. Die Regel der Standardinstanz hebt Zellen hervor, deren Werte in der oberen 10-Klammer liegen. Gilt nur für den Typ „Top10“.|
| Verknüpfung| Klasse:Link| WAHR| FALSCH|||

**Elternname** : (LinkElement)[Linkelement]**Kindername** : 
	-  [StyleFormatCondition](styleformatcondition) 
