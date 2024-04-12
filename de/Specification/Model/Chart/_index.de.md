---
title: Verkohlen
second_title: Aspose.Cells Cloud Documen
type: docs
url: /de/specification/model/chart/
description: "Aspose.Cells Wolkenmodellspezifikation: Diagramm. Bearbeiten Sie mühelos Excel und andere Tabellenkalkulationsdokumente mit Funktionen wie Öffnen, Generieren, Bearbeiten, Teilen, Zusammenführen, Vergleichen und Konvertieren"
weight: 50
---
## **Diagramm**

 

| Name des Anwesens| Art der Immobilie| Nullbar| Schreibgeschützt| Standardwert| Beschreibung|
|:- |:- |:- |:- |:- |:- |
| AutoScaling| Boolescher Wert| WAHR| FALSCH|| True, wenn Microsoft Excel ein 3D-Diagramm so skaliert, dass es näher an der Größe des entsprechenden 2D-Diagramms liegt. Die RightAngleAxes-Eigenschaft muss True sein.|
| Rückwand| Klasse:LinkElement| WAHR| FALSCH||Gibt ein Objekt zurück, das die Rückwand eines 3D-Diagramms darstellt.|
| KategorieAchse| Klasse:LinkElement| WAHR| FALSCH|| Ruft die X-Achse des Diagramms ab.|
| ChartArea| Klasse:LinkElement| WAHR| FALSCH|| Ruft den Diagrammbereich im Arbeitsblatt ab.|
| ChartDataTable| Klasse:LinkElement| WAHR| FALSCH|| Stellt die Diagrammdatentabelle dar.|
| ChartObject| Klasse:LinkElement| WAHR| FALSCH|| Stellt die chartShape dar;|
| DepthPercent| Ganze Zahl| WAHR| FALSCH|| Stellt die Tiefe eines 3D-Diagramms als Prozentsatz der Diagrammbreite dar (zwischen 20 und 2000 Prozent).|
| Elevation| Ganze Zahl| WAHR| FALSCH|| Stellt die Höhe der 3D-Kartenansicht in Grad dar.|
| FirstSliceAngle| Ganze Zahl| WAHR| FALSCH|| Ruft den Winkel des ersten Kreisdiagramm- oder Ringdiagrammabschnitts in Grad ab (im Uhrzeigersinn von der Vertikalen) oder legt diesen fest. Gilt nur für Kreis-, 3D-Kreis- und Ringdiagramme, 0 bis 360.|
| Boden| Klasse:LinkElement| WAHR| FALSCH|| Gibt ein Objekt zurück, das die Wände eines 3D-Diagramms darstellt.|
| Lückentiefe| Ganze Zahl| WAHR| FALSCH|| Ruft den Abstand zwischen den Datenreihen in einem 3D-Diagramm als Prozentsatz der Markierungsbreite ab oder legt diesen fest. Der Wert dieser Eigenschaft muss zwischen 0 und 500 liegen.|
|Spaltbreite| Ganze Zahl| WAHR| FALSCH|| Gibt den Abstand zwischen Balken- oder Säulenclustern als Prozentsatz der Balken- oder Säulenbreite zurück oder legt diesen fest. Der Wert dieser Eigenschaft muss zwischen 0 und 500 liegen.|
| HöheProzent| Ganze Zahl| WAHR| FALSCH|| Gibt die Höhe eines 3D-Diagramms als Prozentsatz der Diagrammbreite zurück oder legt sie fest (zwischen 5 und 500 Prozent).|
| PivotFieldButtons ausblenden| Boolescher Wert| WAHR| FALSCH|| Gibt an, ob die Feldschaltflächen des Pivot-Diagramms nur ausgeblendet werden, wenn es sich bei dem Diagramm um ein PivotChart handelt.|
| Is3D| Boolescher Wert| WAHR| FALSCH|| Gibt an, ob es sich bei dem Diagramm um ein 3D-Diagramm handelt.|
| IsRectangularCornered| Boolescher Wert| WAHR| FALSCH|| Ruft einen Wert ab, der angibt, ob der Diagrammbereich rechteckige Ecken hat, oder legt diesen fest. Der Standardwert ist wahr.|
| Legende| Klasse:LinkElement| WAHR| FALSCH|| Ruft die Diagrammlegende ab.|
| Name| Zeichenfolge| WAHR| FALSCH|||
| NSerie| Klasse:LinkElement| WAHR| FALSCH|| Ruft eine Sammlung ab, die die Datenreihe im Diagramm darstellt.|
| Seiteneinrichtung| Klasse:LinkElement| WAHR| FALSCH|| Stellt die Beschreibung der Seiteneinrichtung in diesem Diagramm dar.|
| Perspektive| Ganze Zahl| WAHR| FALSCH||Gibt die Perspektive für die 3D-Diagrammansicht zurück oder legt sie fest. Muss zwischen 0 und 100 liegen. Diese Eigenschaft wird ignoriert, wenn die RightAngleAxes-Eigenschaft True ist.|
| PivotSource| Zeichenfolge| WAHR| FALSCH|| Die Quelle sind die Daten der PivotTable. Wenn PivotSource nicht leer ist, ist das Diagramm ein PivotChart.|
| Platzierung| Zeichenfolge| WAHR| FALSCH|| Stellt die Art und Weise dar, wie das Diagramm an die darunter liegenden Zellen angehängt wird.|
| Grundstücksfläche| Klasse:LinkElement| WAHR| FALSCH|| Ruft den Plotbereich des Diagramms ab, der Achsenteilstrichbeschriftungen enthält.|
| PlotEmptyCellsType| Zeichenfolge| WAHR| FALSCH|| Ruft ab und legt fest, wie die leeren Zellen dargestellt werden.|
| PlotVisibleCells| Boolescher Wert| WAHR| FALSCH|| Gibt an, ob nur sichtbare Zellen dargestellt werden sollen.|
| Druckgröße| Zeichenfolge| WAHR| FALSCH|| Ruft die Größe des gedruckten Diagramms ab und legt diese fest.|
| Rechte Winkelachsen| Boolescher Wert| WAHR| FALSCH|| True, wenn die Diagrammachsen im rechten Winkel stehen. Gilt nur für 3D-Diagramme (außer Column3D und 3D-Kreisdiagramme).|
| Drehwinkel| Ganze Zahl| WAHR| FALSCH|| Stellt die Drehung der 3D-Diagrammansicht dar (die Drehung des Diagrammbereichs um die Z-Achse in Grad).|
| SecondCategoryAxis| Klasse:LinkElement| WAHR| FALSCH|| Ruft die zweite X-Achse des Diagramms ab.|
|SecondValueAxis| Klasse:LinkElement| WAHR| FALSCH|| Ruft die zweite Y-Achse des Diagramms ab.|
| SeriesAxis| Klasse:LinkElement| WAHR| FALSCH|| Ruft die Reihenachse des Diagramms ab.|
| Formen| Klasse:LinkElement| WAHR| FALSCH|| Gibt alle Zeichnungsformen in diesem Diagramm zurück.|
| ShowDataTable| Boolescher Wert| WAHR| FALSCH|| Ruft einen Wert ab, der angibt, ob das Diagramm eine Datentabelle anzeigt, oder legt diesen fest.|
| ShowLegend| Boolescher Wert| WAHR| FALSCH|| Ruft einen Wert ab, der angibt, ob die Diagrammlegende angezeigt wird, oder legt diesen fest. Der Standardwert ist wahr.|
| Seitenwand| Klasse:LinkElement| WAHR| FALSCH|| Gibt ein Objekt zurück, das die Seitenwand eines 3D-Diagramms darstellt.|
| SizeWithWindow| Boolescher Wert| WAHR| FALSCH|| True, wenn Microsoft Excel die Größe des Diagramms an die Größe des Diagrammblattfensters anpasst.|
| Stil| Ganze Zahl| WAHR| FALSCH|| Ruft den integrierten Stil ab und legt ihn fest.|
| Titel| Klasse:LinkElement| WAHR| FALSCH|||
| Typ| Zeichenfolge| WAHR| FALSCH|||
| Wertachse| Klasse:LinkElement| WAHR| FALSCH|| Ruft die Y-Achse des Diagramms ab.|
| Wände| Klasse:LinkElement| WAHR| FALSCH|| Gibt ein Objekt zurück, das die Wände eines 3D-Diagramms darstellt.|
| WallsAndGridlines2D| Boolescher Wert| WAHR| FALSCH|| True, wenn Gitterlinien zweidimensional in einem 3D-Diagramm gezeichnet werden.|
| Verknüpfung| Klasse:Link| WAHR| FALSCH|||

**Elternname** : (LinkElement)[Linkelement]