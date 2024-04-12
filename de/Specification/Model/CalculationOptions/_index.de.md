---
title: Berechnungsoption
second_title: Aspose.Cells Cloud Documen
type: docs
url: /de/specification/model/calculationoptions/
description: "Aspose.Cells Cloud-Modellspezifikation: CalculationOptions. Bearbeiten Sie mühelos Excel und andere Tabellenkalkulationsdokumente mit Funktionen wie Öffnen, Generieren, Bearbeiten, Teilen, Zusammenführen, Vergleichen und Konvertieren"
weight: 50
---
## **Berechnungsoptionen**

 

| Name des Anwesens| Art der Immobilie| Nullbar| Schreibgeschützt| Standardwert| Beschreibung|
|:- |:- |:- |:- |:- |:- |
| CalcStackSize| Ganze Zahl| WAHR| FALSCH|| Gibt die Stapelgröße für die rekursive Berechnung von Zellen an.|
| Fehler ignorieren| Boolescher Wert| WAHR| FALSCH|| Gibt an, ob beim Berechnen von Formeln aufgetretene Fehler ignoriert werden sollen. Der Fehler kann auf nicht unterstützte Funktionen, externe Links usw. zurückzuführen sein. Der Standardwert ist „true“.|
| Präzisionsstrategie| Zeichenfolge| WAHR| FALSCH|| Gibt die Strategie zur Verarbeitung der Berechnungsgenauigkeit an.|
| Rekursiv| Boolescher Wert| WAHR| FALSCH||Gibt an, ob die abhängigen Zellen rekursiv berechnet werden, wenn eine Zelle berechnet wird und sie von anderen Zellen abhängt. Der Standardwert ist wahr.|
| CustomEngine| Klasse:AbstractCalculationEngine| WAHR| FALSCH|| Die benutzerdefinierte Formelberechnungs-Engine zur Erweiterung der Standardberechnungs-Engine von Aspose.Cells.|
| Berechnungsmonitor| Klasse:AbstractCalculationMonitor| WAHR| FALSCH|| Der Monitor, mit dem der Benutzer den Fortschritt der Formelberechnung verfolgen kann.|
| LinkedDataSources|Array<Class:Workbook> | WAHR| FALSCH|| Gibt die Datenquellen für externe Links an, die in Formeln verwendet werden.|

