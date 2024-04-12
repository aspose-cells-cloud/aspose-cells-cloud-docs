---
title: CopyOption
second_title: Aspose.Cells Cloud Documen
type: docs
url: /de/specification/model/copyoptions/
description: "Aspose.Cells Cloud-Modellspezifikation: CopyOptions. Bearbeiten Sie mühelos Excel und andere Tabellenkalkulationsdokumente mit Funktionen wie Öffnen, Generieren, Bearbeiten, Teilen, Zusammenführen, Vergleichen und Konvertieren"
weight: 50
---
## **copyOptions**

 Stellt die Kopieroptionen dar.

| Name des Anwesens| Art der Immobilie| Nullbar| Schreibgeschützt| Standardwert| Beschreibung|
|:- |:- |:- |:- |:- |:- |
| ColumnCharacterWidth| Boolescher Wert| WAHR| FALSCH||Gibt an, ob die Spaltenbreite in Zeicheneinheiten kopiert wird.|
| CopyInvalidFormulasAsValues| Boolescher Wert| WAHR| FALSCH|| Wenn die Formel für das Ziel nicht gültig ist, kopieren Sie nur Werte.|
| CopyNames| Boolescher Wert| WAHR| FALSCH|| Gibt an, ob die Namen kopiert werden.|
| ExtendToAdjacentRange| Boolescher Wert| WAHR| FALSCH|| Gibt an, ob Bereiche erweitert werden, wenn der Bereich in einen angrenzenden Bereich kopiert wird.|
| ReferToDestinationSheet| Boolescher Wert| WAHR| FALSCH|| Wenn der Bereich in dieselbe Datei kopiert wird und das Diagramm auf das Quellblatt verweist, bedeutet „False“, dass die Datenquelle des kopierten Diagramms nicht geändert wird. „True“ bedeutet, dass die Datenquelle des kopierten Diagramms auf das Zielblatt verweist.|
| ReferToSheetWithSameName| Boolescher Wert| WAHR| FALSCH||Wenn Sie in MS Excel Formeln kopieren, die auf andere Arbeitsblätter verweisen, während Sie ein Arbeitsblatt in ein anderes kopieren, sollten sich die kopierten Formeln auf die Quellarbeitsmappe beziehen. In manchen Situationen kann es jedoch sein, dass der Benutzer die kopierten Formeln auf Arbeitsblätter mit demselben Namen in derselben Arbeitsmappe verweisen muss, beispielsweise wenn diese Arbeitsblätter vor diesem Kopiervorgang kopiert wurden. Dann sollte diese Eigenschaft auf „true“ belassen werden.|

