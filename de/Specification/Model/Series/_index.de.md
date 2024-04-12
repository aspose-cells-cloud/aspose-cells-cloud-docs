---
title: Serie
second_title: Aspose.Cells Cloud Documen
type: docs
url: /de/specification/model/series/
description: "Aspose.Cells Cloud-Modellspezifikation: Serie. Bearbeiten Sie mühelos Excel und andere Tabellenkalkulationsdokumente mit Funktionen wie Öffnen, Generieren, Bearbeiten, Teilen, Zusammenführen, Vergleichen und Konvertieren"
weight: 50
---
## **Serie**

 

| Name des Anwesens| Art der Immobilie| Nullbar| Schreibgeschützt| Standardwert| Beschreibung|
|:- |:- |:- |:- |:- |:- |
| Bereich| Klasse:Bereich| WAHR| FALSCH|| Stellt den Hintergrundbereich des Series-Objekts dar.|
| Bar3DShapeType| Zeichenfolge| WAHR| FALSCH|| Ruft den 3D-Formtyp ab, der mit dem 3D-Balken- oder Säulendiagramm verwendet wird, oder legt diesen fest.|
| Grenze| Klasse:Linie| WAHR| FALSCH|| Stellt den Rand des Series-Objekts dar.|
| BubbleScale| Ganze Zahl| WAHR| FALSCH||Ruft den Skalierungsfaktor für Blasen in der angegebenen Diagrammgruppe ab oder legt diesen fest. Es kann ein ganzzahliger Wert von 0 (Null) bis 300 sein, der einem Prozentsatz der Standardgröße entspricht. Gilt nur für Blasendiagramme.|
| Blasengrößen| Zeichenfolge| WAHR| FALSCH|| Ruft die Blasengrößenwerte der Diagrammreihe ab oder legt diese fest.|
| CountOfDataValues| Ganze Zahl| WAHR| FALSCH|| Ruft die Anzahl der Datenwerte ab.|
| Datenaufkleber| Klasse:LinkElement| WAHR| FALSCH|| Stellt das DataLabels-Objekt für die angegebene ASeries dar.|
| Anzeigename| Zeichenfolge| WAHR| FALSCH|| Ruft den Namen der Reihe ab, der im Diagrammdiagramm angezeigt wird.|
| DonutHoleSize| Ganze Zahl| WAHR| FALSCH|| Gibt die Größe des Lochs in einer Ringdiagrammgruppe zurück oder legt sie fest. Die Lochgröße wird als Prozentsatz der Diagrammgröße ausgedrückt und liegt zwischen 10 und 90 Prozent.|
| DownBars| Klasse:LinkElement| WAHR| FALSCH|| Gibt ein Objekt zurück, das die unteren Balken in einem Liniendiagramm darstellt. Gilt nur für Liniendiagramme.|
| DropLines| Klasse:Linie| WAHR| FALSCH||Gibt ein Objekt zurück, das die Falllinien für eine Reihe im Liniendiagramm oder Flächendiagramm darstellt. Gilt nur für Liniendiagramme oder Flächendiagramme.|
| Explosion| Ganze Zahl| WAHR| FALSCH|| Der Abstand eines offenen Tortenstücks von der Mitte des Tortendiagramms wird als Prozentsatz des Tortendurchmessers ausgedrückt.|
| FirstSliceAngle| Ganze Zahl| WAHR| FALSCH|| Ruft den Winkel des ersten Kreisdiagramm- oder Ringdiagrammabschnitts in Grad ab (im Uhrzeigersinn von der Vertikalen) oder legt diesen fest. Gilt nur für Kreis-, 3D-Kreis- und Ringdiagramme, 0 bis 360.|
|Spaltbreite| Ganze Zahl| WAHR| FALSCH|| Gibt den Abstand zwischen Balken- oder Säulenclustern als Prozentsatz der Balken- oder Säulenbreite zurück oder legt diesen fest. Der Wert dieser Eigenschaft muss zwischen 0 und 500 liegen.|
| Has3DEffect| Boolescher Wert| WAHR| FALSCH|| True, wenn die Serie ein dreidimensionales Erscheinungsbild hat. Gilt nur für Blasendiagramme.|
| HasDropLines| Boolescher Wert| WAHR| FALSCH|| True, wenn das Diagramm Falllinien hat. Gilt nur für Liniendiagramme oder Flächendiagramme.|
| HasHiLoLines| Boolescher Wert| WAHR| FALSCH|| True, wenn das Liniendiagramm Hoch-Tief-Linien aufweist. Gilt nur für Liniendiagramme.|
| HasLeaderLines| Boolescher Wert| WAHR| FALSCH|| True, wenn die Serie Führungslinien hat.|
| HasRadarAxisLabels| Boolescher Wert| WAHR| FALSCH|| True, wenn ein Netzdiagramm Kategorieachsenbeschriftungen hat. Gilt nur für Radarkarten.|
| HasSeriesLines| Boolescher Wert| WAHR| FALSCH||True, wenn ein gestapeltes Säulendiagramm oder Balkendiagramm Reihenlinien aufweist oder wenn ein Kreisdiagramm oder Balkendiagramm Verbindungslinien zwischen den beiden Abschnitten aufweist. Gilt nur für gestapelte Säulendiagramme, Balkendiagramme, Kreisdiagramme oder Balkendiagramme.|
| HasUpDownBars| Boolescher Wert| WAHR| FALSCH|| True, wenn ein Liniendiagramm über Aufwärts- und Abwärtsbalken verfügt. Gilt nur für Liniendiagramme.|
| HiLoLines| Klasse:Linie| WAHR| FALSCH|| Gibt ein HiLoLines-Objekt zurück, das die Hoch-Tief-Linien für eine Reihe in einem Liniendiagramm darstellt. Gilt nur für Liniendiagramme.|
| IsAutoSplit| Boolescher Wert| WAHR| FALSCH|| Gibt an, ob der Schwellenwert automatisch ist.|
| IsColorVaried| Boolescher Wert| WAHR| FALSCH|| Stellt dar, ob die Farbe der Punkte variiert wird. Das Diagramm darf nur eine Serie enthalten.|
| Führungslinien| Klasse:Linie| WAHR| FALSCH||Stellt Führungslinien in einem Diagramm dar. Führungslinien verbinden Datenbeschriftungen mit Datenpunkten. Dieses Objekt ist keine Sammlung; Es gibt kein Objekt, das eine einzelne Führungslinie darstellt.|
| Legendeneintrag| Klasse:LinkElement| WAHR| FALSCH|| Ruft den Legendeneintrag gemäß dieser Serie ab.|
| Linie| Klasse:Linie| WAHR| FALSCH|||
| Marker| Klasse:Marker| WAHR| FALSCH|| Ruft die Markierung ab.|
| Name| Zeichenfolge| WAHR| FALSCH|| Ruft den Namen der Datenreihe ab oder legt diesen fest.|
| Überlappung| Ganze Zahl| WAHR| FALSCH|| Gibt an, wie Balken und Säulen positioniert werden. Kann ein Wert zwischen – 100 und 100 sein. Gilt nur für 2D-Balken- und 2D-Säulendiagramme.|
| PlotOnSecondAxis| Boolescher Wert| WAHR| FALSCH|| Gibt an, ob diese Reihe auf der zweiten Werteachse dargestellt wird.|
| Punkte| Klasse:LinkElement| WAHR| FALSCH|| Ruft die Sammlung von Punkten in einer Reihe in einem Diagramm ab.|
| SecondPlotSize| Ganze Zahl| WAHR| FALSCH|| Gibt die Größe des sekundären Abschnitts eines Kreis- oder Kreisdiagramms oder eines Balken-Kreisdiagramms als Prozentsatz der Größe des primären Kreisdiagramms zurück oder legt sie fest. Kann ein Wert zwischen 5 und 200 sein.|
| SeriesLines| Klasse:Linie| WAHR| FALSCH||Gibt ein SeriesLines-Objekt zurück, das die Reihenlinien für ein gestapeltes Balkendiagramm oder ein gestapeltes Säulendiagramm darstellt. Gilt nur für gestapelte Balken- und gestapelte Säulendiagramme.|
| Schatten| Boolescher Wert| WAHR| FALSCH|| True, wenn die Serie einen Schatten hat.|
| ShapeProperties| Klasse:LinkElement| WAHR| FALSCH|| Ruft das Objekt ab, das die visuellen Formeigenschaften der Serie enthält.|
| NegativeBlasen anzeigen| Boolescher Wert| WAHR| FALSCH|| True, wenn für die Diagrammgruppe negative Blasen angezeigt werden. Gilt nur für Blasendiagramme.|
| GrößeRepräsentiert| Zeichenfolge| WAHR| FALSCH|| Ruft ab oder legt fest, was die Blasengröße in einem Blasendiagramm darstellt.|
| Glatt| Boolescher Wert| WAHR| FALSCH|| Stellt eine Kurvenglättung dar. True, wenn die Kurvenglättung für das Liniendiagramm oder Streudiagramm aktiviert ist. Gilt nur für durch Linien verbundene Linien- und Streudiagramme.|
| SplitType| Zeichenfolge| WAHR| FALSCH|| Gibt einen Wert zurück oder legt ihn fest, um zu bestimmen, welche Datenpunkte sich im zweiten Kreis oder Balken eines Kreisdiagramms oder Balkendiagramms befinden.|
| SplitValue| Schwebend| WAHR| FALSCH||Gibt einen Wert zurück oder legt ihn fest, der verwendet werden soll, um zu bestimmen, welche Datenpunkte sich im zweiten Kreis oder Balken eines Kreisdiagramms oder Balkendiagramms befinden.|
| TrendLines| Klasse:LinkElement| WAHR| FALSCH|| Gibt ein Objekt zurück, das eine Sammlung aller Trendlinien für die Serie darstellt.|
| Typ| Zeichenfolge| WAHR| FALSCH|| Ruft den Typ einer Datenreihe ab oder legt diesen fest.|
| UpBars| Klasse:LinkElement| WAHR| FALSCH|| Gibt ein DropBars-Objekt zurück, das die oberen Balken in einem Liniendiagramm darstellt. Gilt nur für Liniendiagramme.|
| Werte| Zeichenfolge| WAHR| FALSCH|| Stellt die Daten der Diagrammreihe dar.|
| XErrorBar| Klasse:LinkElement| WAHR| FALSCH|| Stellt den X-Richtungsfehlerbalken der Reihe dar.|
| XWerte| Zeichenfolge| WAHR| FALSCH|| Stellt die x-Werte der Diagrammreihe dar.|
| YErrorBar| Klasse:LinkElement| WAHR| FALSCH|| Stellt den Y-Richtungsfehlerbalken der Reihe dar.|
| Verknüpfung| Klasse:Link| WAHR| FALSCH|||

**Elternname** : (LinkElement)[Linkelement]