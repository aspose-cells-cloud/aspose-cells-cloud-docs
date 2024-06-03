---
title: Trendlin
second_title: Aspose.Cells Cloud Documen
type: docs
url: /de/specification/model/trendline/
description: "Aspose.Cells Cloud-Modellspezifikation: Trendline. Müheloses Bearbeiten von Excel und anderen Tabellenkalkulationsdokumenten mit Funktionen wie Öffnen, Generieren, Bearbeiten, Teilen, Zusammenführen, Vergleichen und Konvertieren"
kwords: Excel, Office, Tabellenkalkulation, Cloud REST API, Trendline
weight: 50
---
## **Trendlinie**

 Stellt eine Trendlinie in einem Diagramm dar.

| Name des Anwesens| Art der Immobilie| Nullwerte zulassen| Schreibgeschützt| Standardwert| Beschreibung|
|:- |:- |:- |:- |:- |:- |
| Verknüpfung| Klasse:Link| WAHR| FALSCH|||
| Rückwärts| Schwimmend| WAHR| FALSCH|| Gibt die Anzahl der Perioden (oder Einheiten in einem Streudiagramm) zurück oder legt sie fest, um die sich die Trendlinie nach hinten erstreckt. Die Anzahl der Perioden muss größer oder gleich Null sein. Wenn der Diagrammtyp ein Spaltendiagramm ist, muss die Anzahl der Perioden zwischen 0 und 0,5 liegen.|
| Datenaufkleber| Klasse:Datenbeschriftungen| WAHR| FALSCH|| Stellt das DataLabels-Objekt für die angegebene Reihe dar.|
| Gleichung anzeigen| Boolescher Wert| WAHR| FALSCH|| Gibt an, ob die Gleichung für die Trendlinie im Diagramm angezeigt wird (in derselben Datenbeschriftung wie der R-Quadrat-Wert). Wenn Sie diese Eigenschaft auf True setzen, werden Datenbeschriftungen automatisch aktiviert.|
| AnzeigeRSquared| Boolescher Wert| WAHR| FALSCH||Gibt an, ob der R-Quadrat-Wert der Trendlinie im Diagramm angezeigt wird (in derselben Datenbeschriftung wie die Gleichung). Wenn Sie diese Eigenschaft auf True setzen, werden Datenbeschriftungen automatisch aktiviert.|
| Nach vorne| Schwimmend| WAHR| FALSCH|| Gibt die Anzahl der Perioden (oder Einheiten in einem Streudiagramm) zurück oder legt sie fest, um die sich die Trendlinie nach vorne erstreckt. Die Anzahl der Perioden muss größer oder gleich Null sein.|
| Abfangen| Schwimmend| WAHR| FALSCH|| Gibt den Punkt zurück oder legt ihn fest, an dem die Trendlinie die Werteachse kreuzt.|
| IstNameAuto| Boolescher Wert| WAHR| FALSCH|| Gibt zurück, wenn Microsoft Excel automatisch den Namen der Trendlinie bestimmt.|
| Legendeneintrag| Klasse:LegendEntry| WAHR| FALSCH|| Ruft den Legendeneintrag gemäß dieser Trendlinie ab|
| Name| Zeichenfolge| WAHR| FALSCH|| Gibt den Namen der Trendlinie zurück.|
| Befehl| Ganze Zahl| WAHR| FALSCH|| Gibt die Trendlinienreihenfolge (eine Ganzzahl größer als 1) zurück oder legt sie fest, wenn der Trendlinientyp Polynom ist. Die Reihenfolge muss zwischen 2 und 6 liegen.|
| Zeitraum| Ganze Zahl| WAHR| FALSCH|| Gibt den Zeitraum für die gleitende Durchschnittstrendlinie zurück oder legt ihn fest.|
| Typ| Zeichenfolge| WAHR| FALSCH|| Gibt den Trendlinientyp zurück.|
| Pfeillänge beginnen| Zeichenfolge| WAHR| FALSCH|||
| Pfeilbreite beginnen| Zeichenfolge| WAHR| FALSCH|||
| Anfangstyp| Zeichenfolge| WAHR| FALSCH|||
| Kappentyp| Zeichenfolge| WAHR| FALSCH|||
| Farbe| Klasse:Farbe| WAHR| FALSCH|||
| Verbundtyp| Zeichenfolge| WAHR| FALSCH|||
| Strichtyp| Zeichenfolge| WAHR| FALSCH|||
| EndPfeilLänge| Zeichenfolge| WAHR| FALSCH|||
| EndPfeilBreite| Zeichenfolge| WAHR| FALSCH|||
| Endtyp| Zeichenfolge| WAHR| FALSCH|||
| Farbverlaufsfüllung| Klasse:GradientFill| WAHR| FALSCH|||
| IsAuto| Boolescher Wert| WAHR| FALSCH|||
| IstAutomatischeFarbe| Boolescher Wert| WAHR| FALSCH|||
| Ist sichtbar| Boolescher Wert| WAHR| FALSCH|||
| Verbindungstyp| Zeichenfolge| WAHR| FALSCH|||
| Stil| Zeichenfolge| WAHR| FALSCH|||
| Transparenz| Schwimmend| WAHR| FALSCH|||
| Gewicht| Zeichenfolge| WAHR| FALSCH|||
| GewichtPt| Schwimmend| WAHR| FALSCH|||

**Elternname** : [Linie](/specification/model/line)

