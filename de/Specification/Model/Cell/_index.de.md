---
title: Cel
second_title: Aspose.Cells Cloud Documen
type: docs
url: /de/specification/model/cell/
description: "Aspose.Cells Cloud-Modellspezifikation: Zelle. Bearbeiten Sie mühelos Excel und andere Tabellenkalkulationsdokumente mit Funktionen wie Öffnen, Generieren, Bearbeiten, Teilen, Zusammenführen, Vergleichen und Konvertieren"
weight: 50
---
## **Zelle**

 

| Name des Anwesens| Art der Immobilie| Nullbar| Schreibgeschützt| Standardwert| Beschreibung|
|:- |:- |:- |:- |:- |:- |
| Name| Zeichenfolge| WAHR| FALSCH|| Ruft den Namen der Zelle ab.|
| Reihe| Ganze Zahl| WAHR| FALSCH|| Ruft die Zeilennummer (nullbasiert) der Zelle ab.|
| Spalte| Ganze Zahl| WAHR| FALSCH|| Ruft die Spaltennummer (nullbasiert) der Zelle ab.|
| Wert| Zeichenfolge| WAHR| FALSCH|| Ruft den in dieser Zelle enthaltenen Wert ab.|
| Typ| Zeichenfolge| WAHR| FALSCH|| Stellt den Zellwerttyp dar.|
|Formel| Zeichenfolge| WAHR| FALSCH|| Ruft eine Formel ab oder legt diese fest.|
| IsFormula| Boolescher Wert| WAHR| FALSCH|| Stellt dar, ob die angegebene Zelle eine Formel enthält.|
| IsMerged| Boolescher Wert| WAHR| FALSCH|| Überprüft, ob eine Zelle Teil eines zusammengeführten Bereichs ist oder nicht.|
| IsArrayHeader| Boolescher Wert| WAHR| FALSCH|| Gibt an, dass die Formel der Zelle eine Array-Formel ist und es sich um die erste Zelle des Arrays handelt.|
| IsInArray| Boolescher Wert| WAHR| FALSCH|| Gibt an, ob die Zellformel eine Arrayformel ist.|
| IsErrorValue| Boolescher Wert| WAHR| FALSCH|| Überprüft, ob der Wert dieser Zelle ein Fehler ist.|
| IsInTable| Boolescher Wert| WAHR| FALSCH|| Gibt an, ob diese Zelle Teil einer Tabellenformel ist.|
| IsStyleSet| Boolescher Wert| WAHR| FALSCH|| Gibt an, ob der Stil der Zelle festgelegt ist. Wenn „false“ zurückgegeben wird, bedeutet dies, dass diese Zelle ein Standardzellenformat hat.|
| HtmlString| Zeichenfolge| WAHR| FALSCH|| Ruft die HTML-Zeichenfolge ab, die Daten und einige Formate in dieser Zelle enthält, und legt sie fest.|
| Stil| Klasse:LinkElement| WAHR| FALSCH|||
| Arbeitsblatt| Zeichenfolge| WAHR| FALSCH|| Ruft das übergeordnete Arbeitsblatt ab.|
| Verknüpfung| Klasse:Link| WAHR| FALSCH|||

**Elternname** : (LinkElement)[Linkelement]