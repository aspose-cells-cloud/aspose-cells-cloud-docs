---
title: AbstraktBerechnungEngineer
second_title: Aspose.Cells Cloud Documen
type: docs
url: /de/specification/model/abstractcalculationengine/
description: "Aspose.Cells Cloud-Modellspezifikation: AbstractCalculationEngine. Müheloses Bearbeiten von Excel und anderen Tabellenkalkulationsdokumenten mit Funktionen wie Öffnen, Generieren, Bearbeiten, Teilen, Zusammenführen, Vergleichen und Konvertieren"
kwords: Excel, Office, Tabellenkalkulation, Cloud REST API, AbstractCalculationEngine
weight: 50
---
## **abstrakteBerechnungsmaschine**

Stellt die benutzerdefinierte Berechnungs-Engine des Benutzers dar, um die Standardberechnungs-Engine Aspose.Cells zu erweitern.

| Name des Anwesens| Art der Immobilie| Nullwerte zulassen| Schreibgeschützt| Standardwert| Beschreibung|
|:- |:- |:- |:- |:- |:- |
| IstParamLiteralErforderlich| Boolescher Wert| WAHR| FALSCH|| Gibt an, ob diese Engine bei der Berechnung den wörtlichen Text des Parameters benötigt. Der Standardwert ist „false“.|
| IstParamArrayModeRequired| Boolescher Wert| WAHR| FALSCH|| Gibt an, ob diese Engine den Parameter im Array-Modus berechnen muss. Der Standardwert ist „false“. Wenn dies bei der Berechnung benutzerdefinierter Funktionen erforderlich ist, muss diese Eigenschaft auf „true“ gesetzt werden.|
| Integrierte Prozessfunktionen| Boolescher Wert| WAHR| FALSCH|| Ob integrierte Funktionen, die von der integrierten Engine unterstützt werden, von dieser Implementierung überprüft und verarbeitet werden sollen. Der Standardwert ist „false“. Wenn der Benutzer die Berechnungslogik einiger integrierter Funktionen ändern muss, sollte diese Eigenschaft auf „true“ gesetzt werden. Andernfalls belassen Sie diese Eigenschaft aus Leistungsgründen auf „false“.|

