---
title: Cel
second_title: Aspose.Cells Cloud Documen
type: docs
url: /de/specification/model/cell/
description: "Aspose.Cells Cloud-Modellspezifikation: Zelle. Müheloses Bearbeiten von Excel und anderen Tabellenkalkulationsdokumenten mit Funktionen wie Öffnen, Generieren, Bearbeiten, Teilen, Zusammenführen, Vergleichen und Konvertieren"
kwords: Excel, Office, Tabellenkalkulation, Cloud REST API, Zelle
weight: 50
---
## **Zelle**

 Kapselt das Objekt, das eine einzelne Arbeitsmappenzelle darstellt.

| Name des Anwesens| Art der Immobilie| Nullwerte zulassen| Schreibgeschützt| Standardwert| Beschreibung|
|:- |:- |:- |:- |:- |:- |
| Name| Zeichenfolge| WAHR| FALSCH|| Ruft den Namen der Zelle ab.|
| Reihe| Ganze Zahl| WAHR| FALSCH|| Ruft die Zeilennummer (basierend auf Null) der Zelle ab.|
| Spalte| Ganze Zahl| WAHR| FALSCH|| Ruft die Spaltennummer (basierend auf Null) der Zelle ab.|
| Wert| Zeichenfolge| WAHR| FALSCH|| Ruft den in dieser Zelle enthaltenen Wert ab.|
| Typ| Zeichenfolge| WAHR| FALSCH|| Stellt den Zellenwerttyp dar.|
| Formel| Zeichenfolge| WAHR| FALSCH||Ruft eine Formel von ab oder legt sie fest.|
| IstFormel| Boolescher Wert| WAHR| FALSCH|| Gibt an, ob die angegebene Zelle eine Formel enthält.|
| IstZusammengeführt| Boolescher Wert| WAHR| FALSCH|| Überprüft, ob eine Zelle Teil eines zusammengeführten Bereichs ist oder nicht.|
| IsArrayHeader| Boolescher Wert| WAHR| FALSCH|| Gibt an, dass es sich bei der Formel der Zelle um eine Array-Formel handelt und dass es sich um die erste Zelle des Arrays handelt.|
| IstInArray| Boolescher Wert| WAHR| FALSCH|| Gibt an, ob die Zellformel eine Arrayformel ist.|
| IstFehlerwert| Boolescher Wert| WAHR| FALSCH|| Überprüft, ob der Wert dieser Zelle ein Fehler ist.|
| IstInTabelle| Boolescher Wert| WAHR| FALSCH|| Gibt an, ob diese Zelle Teil einer Tabellenformel ist.|
| IstStyleSet| Boolescher Wert| WAHR| FALSCH|| Gibt an, ob der Stil der Zelle festgelegt ist. Wenn false zurückgegeben wird, bedeutet dies, dass diese Zelle ein Standardzellenformat hat.|
| HTMLString| Zeichenfolge| WAHR| FALSCH|| Ruft die HTML-Zeichenfolge ab und legt sie fest, die Daten und einige Formate in dieser Zelle enthält.|
| Stil| Klasse:LinkElement| WAHR| FALSCH|||
| Arbeitsblatt| Zeichenfolge| WAHR| FALSCH|| Ruft das übergeordnete Arbeitsblatt ab.|
| Verknüpfung| Klasse:Link| WAHR| FALSCH|||

**Elternname** : [LinkElement](/specification/model/linkelement)

