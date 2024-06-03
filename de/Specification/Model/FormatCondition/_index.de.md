---
title: FormatConditio
second_title: Aspose.Cells Cloud Documen
type: docs
url: /de/specification/model/formatcondition/
description: "Aspose.Cells Cloud-Modellspezifikation: FormatCondition. Müheloses Bearbeiten von Excel und anderen Tabellenkalkulationsdokumenten mit Funktionen wie Öffnen, Generieren, Bearbeiten, Teilen, Zusammenführen, Vergleichen und Konvertieren"
kwords: Excel, Office, Tabellenkalkulation, Cloud REST API, FormatCondition
weight: 50
---
## **formatCondition**

 Stellt eine bedingte Formatierungsbedingung dar.

| Name des Anwesens| Art der Immobilie| Nullwerte zulassen| Schreibgeschützt| Standardwert| Beschreibung|
|:- |:- |:- |:- |:- |:- |
| Priorität| Ganze Zahl| WAHR| FALSCH||Die Priorität dieser Regel für bedingte Formatierung. Dieser Wert wird verwendet, um zu bestimmen, welches Format ausgewertet und gerendert werden soll. Niedrigere numerische Werte haben eine höhere Priorität als höhere numerische Werte, wobei „1“ die höchste Priorität ist.|
| Typ| Zeichenfolge| WAHR| FALSCH|| Ruft den Typ des bedingten Formats ab und legt ihn fest.|
| StoppenWennWahr| Boolescher Wert| WAHR| FALSCH|| True: Wenn diese Regel als True ausgewertet wird, dürfen keine Regeln mit niedrigerer Priorität auf diese Regel angewendet werden. Gilt nur für Excel 2007;|
| Überdurchschnittlich| Klasse:Überdurchschnittlich| WAHR| FALSCH|| Holen Sie sich die Instanz „ÜberDurchschnitt“ der bedingten Formatierung. Die Regel der Standardinstanz hebt Zellen hervor, die über dem Durchschnitt für alle Werte im Bereich liegen. Nur gültig für Typ = ÜberDurchschnitt.|
| Farbskala| Klasse:Farbskala| WAHR| FALSCH||Holen Sie sich die „ColorScale“-Instanz der bedingten Formatierung. Die Standardinstanz ist eine „grün-gelb-rote“ 3ColorScale. Nur gültig für Typ = ColorScale.|
| Datenleiste| Klasse:DataBar| WAHR| FALSCH|| Ruft die Instanz „DataBar“ der bedingten Formatierung ab. Die Standardfarbe der Instanz ist blau. Nur gültig für den Typ „DataBar“.|
| Formel 1| Zeichenfolge| WAHR| FALSCH|| Ruft den mit der bedingten Formatierung verknüpften Wert oder Ausdruck ab und legt ihn fest.|
| Formel2| Zeichenfolge| WAHR| FALSCH|| Ruft den mit der bedingten Formatierung verknüpften Wert oder Ausdruck ab und legt ihn fest.|
| Symbolsatz| Klasse:IconSet| WAHR| FALSCH|| Holen Sie sich die „IconSet“-Instanz der bedingten Formatierung. Der IconSetType der Standardinstanz ist TrafficLights31. Nur gültig für Typ = IconSet.|
| Operator| Zeichenfolge| WAHR| FALSCH|| Ruft den Operatortyp für das bedingte Format ab und legt ihn fest.|
| Stil| Klasse:Stil| WAHR| FALSCH|| Ruft den Stil bedingt formatierter Zellbereiche ab oder legt ihn fest.|
| Text| Zeichenfolge| WAHR| FALSCH||Der Textwert in einer bedingten Formatierungsregel vom Typ „Text enthält“. Nur gültig für Typ = containsText, notContainsText, beginWith und endsWith. Der Standardwert ist null.|
| Zeitraum| Zeichenfolge| WAHR| FALSCH|| Der anwendbare Zeitraum in einer bedingten Formatierungsregel vom Typ „Datum, an dem …“ gilt. Nur gültig für Typ = Zeitraum. Der Standardwert ist TimePeriodType.Today.|
| Top 10| Klasse:Top10| WAHR| FALSCH|| Holen Sie sich die „Top10“-Instanz der bedingten Formatierung. Die Regel der Standardinstanz hebt Zellen hervor, deren Werte in die Top 10-Klammer fallen. Nur gültig für den Typ „Top10“.|
| Verknüpfung| Klasse:Link| WAHR| FALSCH|||

**Elternname** : [LinkElement](/specification/model/linkelement)

**Name des Kindes** : 
	-  [StilFormatBedingung](styleformatcondition) 
