---
title: AbstractCalculationEngine
second_title: Aspose.Cells Cloud Documen
type: docs
url: /de/specification/model/abstractcalculationengine/
description: "Aspose.Cells Cloud-Modellspezifikation: AbstractCalculationEngine. Bearbeiten Sie mühelos Excel und andere Tabellenkalkulationsdokumente mit Funktionen wie Öffnen, Generieren, Bearbeiten, Teilen, Zusammenführen, Vergleichen und Konvertieren"
weight: 50
---
## **abstractCalculationEngine**

 Stellt die benutzerdefinierte Berechnungs-Engine des Benutzers dar, um die Standard-Berechnungs-Engine von Aspose.Cells zu erweitern.

| Name des Anwesens| Art der Immobilie| Nullbar| Schreibgeschützt| Standardwert| Beschreibung|
|:- |:- |:- |:- |:- |:- |
| IsParamLiteralRequired| Boolescher Wert| WAHR| FALSCH|| Gibt an, ob diese Engine während der Berechnung den Literaltext des Parameters benötigt. Der Standardwert ist falsch.|
| IsParamArrayModeRequired| Boolescher Wert| WAHR| FALSCH|| Gibt an, ob diese Engine die Berechnung des Parameters im Array-Modus benötigt. Der Standardwert ist falsch. Wenn dies bei der Berechnung benutzerdefinierter Funktionen erforderlich ist, muss diese Eigenschaft auf „true“ festgelegt werden.|
| ProcessBuiltInFunctions| Boolescher Wert| WAHR| FALSCH||Ob integrierte Funktionen, die von der integrierten Engine unterstützt wurden, von dieser Implementierung überprüft und verarbeitet werden sollen. Der Standardwert ist falsch. Wenn der Benutzer die Berechnungslogik einiger integrierter Funktionen ändern muss, sollte diese Eigenschaft auf „true“ festgelegt werden. Andernfalls belassen Sie diese Eigenschaft aus Leistungsgründen bitte auf „false“.|

