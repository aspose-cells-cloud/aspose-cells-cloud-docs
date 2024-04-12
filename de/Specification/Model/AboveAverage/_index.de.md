---
title: AboveAverag
second_title: Aspose.Cells Cloud Documen
type: docs
url: /de/specification/model/aboveaverage/
description: "Aspose.Cells Cloud-Modellspezifikation: AboveAverage. Bearbeiten Sie mühelos Excel und andere Tabellenkalkulationsdokumente mit Funktionen wie Öffnen, Generieren, Bearbeiten, Teilen, Zusammenführen, Vergleichen und Konvertieren"
weight: 50
---
## **überdurchschnittlich**

 Beschreiben Sie die bedingte Formatierungsregel AboveAverage. Diese bedingte Formatierungsregel hebt Zellen hervor, die über oder unter dem Durchschnitt aller Werte im Bereich liegen.

| Name des Anwesens| Art der Immobilie| Nullbar| Schreibgeschützt| Standardwert| Beschreibung|
|:- |:- |:- |:- |:- |:- |
| IsOverAverage| Boolescher Wert| WAHR| FALSCH||Rufen Sie das Flag ab, das angibt, ob die Regel eine „überdurchschnittliche“ Regel ist, oder legen Sie sie fest. „wahr“ bedeutet „überdurchschnittlich“. Der Standardwert ist wahr.|
| IsEqualAverage| Boolescher Wert| WAHR| FALSCH|| Rufen Sie das Flag ab, das angibt, ob die Kriterien „aboveAverage“ und „belowAverage“ den Durchschnitt selbst einschließen oder diesen Wert ausschließen, oder legen Sie es fest. „true“ gibt an, dass der Durchschnittswert in die Kriterien einbezogen wird. Der Standardwert ist falsch.|
| StdDev| Ganze Zahl| WAHR| FALSCH|| Rufen Sie die Anzahl der Standardabweichungen ab oder legen Sie sie fest, die über oder unter dem Durchschnitt in der Regel für bedingte Formatierung enthalten sein sollen. Der Eingabewert muss zwischen 0 und 3 liegen (einschließlich 0 und 3). Wenn Sie diesen Wert auf 0 setzen, bedeutet dies, dass stdDev nicht festgelegt ist. Der Standardwert ist 0.|

