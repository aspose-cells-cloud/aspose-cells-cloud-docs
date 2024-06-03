---
title: Verkohlen
second_title: Aspose.Cells Cloud Documen
type: docs
url: /de/specification/model/chart/
description: "Aspose.Cells Cloud-Modellspezifikation: Diagramm. Müheloses Bearbeiten von Excel und anderen Tabellenkalkulationsdokumenten mit Funktionen wie Öffnen, Generieren, Bearbeiten, Teilen, Zusammenführen, Vergleichen und Konvertieren"
kwords: Excel, Office, Tabellenkalkulation, Cloud REST API, Diagramm
weight: 50
---
## **Diagramm**

 Kapselt das Objekt, das ein einzelnes Excel-Diagramm darstellt.

| Name des Anwesens| Art der Immobilie| Nullwerte zulassen| Schreibgeschützt| Standardwert| Beschreibung|
|:- |:- |:- |:- |:- |:- |
| Automatische Skalierung| Boolescher Wert| WAHR| FALSCH|| True, wenn Microsoft Excel ein 3D-Diagramm so skaliert, dass es in der Größe näher an dem entsprechenden 2D-Diagramm liegt. Die RightAngleAxes-Eigenschaft muss True sein.|
| Rückwand| Klasse:Wände| WAHR| FALSCH|| Gibt ein Objekt zurück, das die Rückwand eines 3D-Diagramms darstellt.|
| KategorieAchse| Klasse:Achse| WAHR| FALSCH|| Ruft die X-Achse des Diagramms ab.|
| Diagrammbereich| Klasse:ChartArea| WAHR| FALSCH|| Ruft den Diagrammbereich im Arbeitsblatt ab.|
| DiagrammDatenTabelle| Klasse:ChartDataTable| WAHR| FALSCH|| Stellt die Diagrammdatentabelle dar.|
| Diagrammobjekt| Klasse:LinkElement| WAHR| FALSCH|| Stellt die Diagrammform dar;|
| TiefeProzent| Ganze Zahl| WAHR| FALSCH||Stellt die Tiefe eines 3D-Diagramms als Prozentsatz der Diagrammbreite dar (zwischen 20 und 2000 Prozent).|
| Elevation| Ganze Zahl| WAHR| FALSCH|| Stellt die Höhe der 3D-Kartenansicht in Grad dar.|
| ErsterScheibenwinkel| Ganze Zahl| WAHR| FALSCH|| Ruft den Winkel des ersten Kreis- oder Ringdiagrammsegments in Grad ab oder legt ihn fest (im Uhrzeigersinn von der Vertikalen). Gilt nur für Kreis-, 3D-Kreis- und Ringdiagramme, 0 bis 360.|
| Boden| Klasse:Boden| WAHR| FALSCH|| Gibt ein Objekt zurück, das die Wände eines 3D-Diagramms darstellt.|
| Lückentiefe| Ganze Zahl| WAHR| FALSCH|| Ruft den Abstand zwischen den Datenreihen in einem 3D-Diagramm als Prozentsatz der Markierungsbreite ab oder legt ihn fest. Der Wert dieser Eigenschaft muss zwischen 0 und 500 liegen.|
| Spaltbreite| Ganze Zahl| WAHR| FALSCH|| Gibt den Abstand zwischen Balken- oder Spaltenclustern als Prozentsatz der Balken- oder Spaltenbreite zurück oder legt ihn fest. Der Wert dieser Eigenschaft muss zwischen 0 und 500 liegen.|
| HöheProzent| Ganze Zahl| WAHR| FALSCH||Gibt die Höhe eines 3D-Diagramms als Prozentsatz der Diagrammbreite zurück oder legt sie fest (zwischen 5 und 500 Prozent).|
| PivotFieldButtons ausblenden| Boolescher Wert| WAHR| FALSCH|| Gibt an, ob die PivotChart-Feldschaltflächen nur ausgeblendet werden sollen, wenn es sich bei dem Diagramm um ein PivotChart handelt.|
| Is3D| Boolescher Wert| WAHR| FALSCH|| Gibt an, ob es sich bei dem Diagramm um ein 3D-Diagramm handelt.|
| IstRechteckigEckig| Boolescher Wert| WAHR| FALSCH|| Ruft einen Wert ab oder legt einen Wert fest, der angibt, ob der Diagrammbereich rechteckige Ecken hat. Der Standardwert ist „true“.|
| Legende| Klasse:Legende| WAHR| FALSCH|| Ruft die Diagrammlegende ab.|
| Name| Zeichenfolge| WAHR| FALSCH|| Stellt den Diagrammnamen dar.|
| NSerie| Klasse:Serienelemente| WAHR| FALSCH|| Ruft eine Sammlung ab, die die Datenreihe im Diagramm darstellt.|
| Seiteneinrichtung| Klasse:LinkElement| WAHR| FALSCH|| Stellt die Beschreibung der Seiteneinrichtung in diesem Diagramm dar.|
| Perspektive| Ganze Zahl| WAHR| FALSCH|| Gibt die Perspektive für die 3D-Diagrammansicht zurück oder legt sie fest. Muss zwischen 0 und 100 liegen. Diese Eigenschaft wird ignoriert, wenn die RightAngleAxes-Eigenschaft True ist.|
| PivotQuelle| Zeichenfolge| WAHR| FALSCH||Die Quelle sind die Daten der PivotTable. Wenn PivotSource nicht leer ist, ist das Diagramm ein PivotChart.|
| Platzierung| Zeichenfolge| WAHR| FALSCH|| Stellt die Art und Weise dar, wie das Diagramm mit den darunterliegenden Zellen verbunden ist.|
| Grundstücksfläche| Klasse:PlotArea| WAHR| FALSCH|| Ruft den Zeichnungsbereich des Diagramms ab, der die Beschriftungen der Achsenmarkierungen enthält.|
| PlotEmptyCellsTyp| Zeichenfolge| WAHR| FALSCH|| Ruft ab und legt fest, wie die leeren Zellen dargestellt werden.|
| Sichtbare Zellen zeichnen| Boolescher Wert| WAHR| FALSCH|| Gibt an, ob nur sichtbare Zellen dargestellt werden.|
| Druckgröße| Zeichenfolge| WAHR| FALSCH|| Ruft die Größe des gedruckten Diagramms ab und legt sie fest.|
| RechterWinkelAchsen| Boolescher Wert| WAHR| FALSCH|| Wahr, wenn die Diagrammachsen im rechten Winkel verlaufen. Gilt nur für 3D-Diagramme (außer Column3D und 3D-Kreisdiagramme).|
| Drehwinkel| Ganze Zahl| WAHR| FALSCH|| Stellt die Drehung der 3D-Diagrammansicht dar (die Drehung des Plotbereichs um die Z-Achse, in Grad).|
| ZweiteKategorieachse| Klasse:LinkElement| WAHR| FALSCH|| Ruft die zweite X-Achse des Diagramms ab.|
| ZweiteWertachse| Klasse:LinkElement| WAHR| FALSCH|| Ruft die zweite Y-Achse des Diagramms ab.|
| Serienachse| Klasse:LinkElement| WAHR| FALSCH|| Ruft die Serienachse des Diagramms ab.|
| Formen| Klasse:LinkElement| WAHR| FALSCH|| Gibt alle Zeichenformen in diesem Diagramm zurück.|
|Datentabelle anzeigen| Boolescher Wert| WAHR| FALSCH|| Ruft einen Wert ab oder legt einen Wert fest, der angibt, ob das Diagramm eine Datentabelle anzeigt.|
| Legende anzeigen| Boolescher Wert| WAHR| FALSCH|| Ruft einen Wert ab oder legt einen Wert fest, der angibt, ob die Diagrammlegende angezeigt wird. Der Standardwert ist „true“.|
| Seitenwand| Klasse:LinkElement| WAHR| FALSCH|| Gibt ein Objekt zurück, das die Seitenwand eines 3D-Diagramms darstellt.|
| GrößeMitFenster| Boolescher Wert| WAHR| FALSCH|| Wahr, wenn Microsoft Excel die Diagrammgröße so ändert, dass sie der Größe des Diagrammblattfensters entspricht.|
| Stil| Ganze Zahl| WAHR| FALSCH|| Ruft den integrierten Stil ab und legt ihn fest.|
| Titel| Klasse:LinkElement| WAHR| FALSCH|| Stellt den Diagrammtitel dar.|
| Typ| Zeichenfolge| WAHR| FALSCH|| Stellt den Diagrammtyp dar.|
| Werteachse| Klasse:Achse| WAHR| FALSCH|| Ruft die Y-Achse des Diagramms ab.|
| Wände| Klasse:LinkElement| WAHR| FALSCH|| Gibt ein Objekt zurück, das die Wände eines 3D-Diagramms darstellt.|
| WändeUndGitterlinien2D| Boolescher Wert| WAHR| FALSCH|| Wahr, wenn Gitternetzlinien in einem 3D-Diagramm zweidimensional gezeichnet werden.|
| Verknüpfung| Klasse:Link| WAHR| FALSCH|||

**Elternname** : [LinkElement](/specification/model/linkelement)

