---
title: Berechnungsoption
second_title: Aspose.Cells Cloud Documen
type: docs
url: /de/specification/model/calculationoptions/
description: "Aspose.Cells Cloud-Modellspezifikation: CalculationOptions. Müheloses Bearbeiten von Excel und anderen Tabellenkalkulationsdokumenten mit Funktionen wie Öffnen, Generieren, Bearbeiten, Teilen, Zusammenführen, Vergleichen und Konvertieren"
kwords: Excel, Office, Tabellenkalkulation, Cloud REST API, Berechnungsoptionen
weight: 50
---
## **Berechnungsoptionen**

 Stellt Optionen zur Berechnung dar.

| Name des Anwesens| Art der Immobilie| Nullwerte zulassen| Schreibgeschützt| Standardwert| Beschreibung|
|:- |:- |:- |:- |:- |:- |
| Stapelgröße berechnen| Ganze Zahl| WAHR| FALSCH|| Gibt die Stapelgröße für die rekursive Berechnung von Zellen an.|
| Fehler ignorieren| Boolescher Wert| WAHR| FALSCH|| Gibt an, ob beim Berechnen von Formeln aufgetretene Fehler ignoriert werden sollen. Der Fehler kann auf eine nicht unterstützte Funktion, externe Links usw. zurückzuführen sein. Der Standardwert ist „true“.|
| Präzisionsstrategie| Zeichenfolge| WAHR| FALSCH|| Gibt die Strategie zur Verarbeitung der Berechnungsgenauigkeit an.|
| Rekursiv| Boolescher Wert| WAHR| FALSCH|| Gibt an, ob die abhängigen Zellen rekursiv berechnet werden, wenn eine Zelle berechnet wird und diese von anderen Zellen abhängt. Der Standardwert ist „true“.|
| KundenspezifischeEngine|Klasse:AbstractCalculationEngine| WAHR| FALSCH|| Der benutzerdefinierte Formelberechnungs-Engine zur Erweiterung des Standardberechnungs-Engines Aspose.Cells.|
| BerechnungsMonitor| Klasse:AbstractCalculationMonitor| WAHR| FALSCH|| Der Monitor ermöglicht dem Benutzer, den Fortschritt der Formelberechnung zu verfolgen.|
| Verknüpfte Datenquellen|Anordnung<Class:Workbook> | WAHR| FALSCH|| Gibt die Datenquellen für in Formeln verwendete externe Links an.|

