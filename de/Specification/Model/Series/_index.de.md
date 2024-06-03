---
title: Serie
second_title: Aspose.Cells Cloud Documen
type: docs
url: /de/specification/model/series/
description: "Aspose.Cells Cloud-Modellspezifikation: Serie. Müheloses Bearbeiten von Excel und anderen Tabellenkalkulationsdokumenten mit Funktionen wie Öffnen, Generieren, Bearbeiten, Teilen, Zusammenführen, Vergleichen und Konvertieren"
kwords: Excel, Office, Tabellenkalkulation, Cloud REST API, Serie
weight: 50
---
## **Serie**

 Kapselt das Objekt, das eine einzelne Datenreihe in einem Diagramm darstellt.

| Name des Anwesens| Art der Immobilie| Nullwerte zulassen| Schreibgeschützt| Standardwert| Beschreibung|
|:- |:- |:- |:- |:- |:- |
| Bereich| Klasse:Bereich| WAHR| FALSCH|| Stellt den Hintergrundbereich des Serienobjekts dar.|
| Balken3DFormTyp| Zeichenfolge| WAHR| FALSCH|| Ruft den 3D-Formtyp ab oder legt ihn fest, der mit dem 3D-Balken- oder Säulendiagramm verwendet wird.|
| Grenze| Klasse:Linie| WAHR| FALSCH|| Stellt den Rand eines Serienobjekts dar.|
| Blasenwaage| Ganze Zahl| WAHR| FALSCH||Ruft den Skalierungsfaktor für Blasen in der angegebenen Diagrammgruppe ab oder legt ihn fest. Dies kann ein ganzzahliger Wert zwischen 0 (null) und 300 sein, der einem Prozentsatz der Standardgröße entspricht. Gilt nur für Blasendiagramme.|
| Blasengrößen| Zeichenfolge| WAHR| FALSCH|| Ruft die Blasengrößenwerte der Diagrammreihe ab oder legt sie fest.|
| AnzahlDerDatenwerte| Ganze Zahl| WAHR| FALSCH|| Ruft die Anzahl der Datenwerte ab.|
| Datenaufkleber| Klasse:Datenbeschriftungen| WAHR| FALSCH|| Stellt das DataLabels-Objekt für die angegebene ASeries dar.|
| Anzeigename| Zeichenfolge| WAHR| FALSCH|| Ruft den Namen der Serie ab, der im Diagramm angezeigt wird.|
| DonutLochGröße| Ganze Zahl| WAHR| FALSCH|| Gibt die Größe des Lochs in einer Ringdiagrammgruppe zurück oder legt sie fest. Die Lochgröße wird als Prozentsatz der Diagrammgröße zwischen 10 und 90 Prozent ausgedrückt.|
| Abwärtsbalken| Klasse:DropBars| WAHR| FALSCH|| Gibt ein Objekt zurück, das die Abwärtsbalken in einem Liniendiagramm darstellt. Gilt nur für Liniendiagramme.|
| DropLines| Klasse:Linie| WAHR| FALSCH||Gibt ein Objekt zurück, das die Bezugslinien für eine Reihe im Linien- oder Flächendiagramm darstellt. Gilt nur für Linien- oder Flächendiagramme.|
| Explosion| Ganze Zahl| WAHR| FALSCH|| Der Abstand eines offenen Kreisstücks von der Mitte des Kreisdiagramms wird als Prozentsatz des Kreisdurchmessers ausgedrückt.|
| ErsterScheibenwinkel| Ganze Zahl| WAHR| FALSCH|| Ruft den Winkel des ersten Kreis- oder Ringdiagrammsegments in Grad ab oder legt ihn fest (im Uhrzeigersinn von der Vertikalen). Gilt nur für Kreis-, 3D-Kreis- und Ringdiagramme, 0 bis 360.|
| Spaltbreite| Ganze Zahl| WAHR| FALSCH|| Gibt den Abstand zwischen Balken- oder Spaltenclustern als Prozentsatz der Balken- oder Spaltenbreite zurück oder legt ihn fest. Der Wert dieser Eigenschaft muss zwischen 0 und 500 liegen.|
| Has3DEffect| Boolescher Wert| WAHR| FALSCH|| Wahr, wenn die Reihe dreidimensional aussieht. Gilt nur für Blasendiagramme.|
| HatDropLines| Boolescher Wert| WAHR| FALSCH|| Wahr, wenn das Diagramm Bezugslinien hat. Gilt nur für Linien- oder Flächendiagramme.|
| HasHiLoLines| Boolescher Wert| WAHR| FALSCH|| Wahr, wenn das Liniendiagramm Hoch-Tief-Linien hat. Gilt nur für Liniendiagramme.|
| HatFührungslinien| Boolescher Wert| WAHR| FALSCH|| Wahr, wenn die Reihe Führungslinien hat.|
| HatRadarAxisLabels| Boolescher Wert| WAHR| FALSCH|| Wahr, wenn ein Radardiagramm Kategorieachsenbeschriftungen hat. Gilt nur für Radardiagramme.|
| HatSeriesLines| Boolescher Wert| WAHR| FALSCH||Wahr, wenn ein gestapeltes Säulen- oder Balkendiagramm Serienlinien hat oder wenn ein Kreis-aus-Kreis-Diagramm oder ein Balken-aus-Kreis-Diagramm Verbindungslinien zwischen den beiden Abschnitten hat. Gilt nur für gestapelte Säulen-, Balken-, Kreis-aus-Kreis-Diagramme oder Balken-aus-Kreis-Diagramme.|
| HatUpDownBars| Boolescher Wert| WAHR| FALSCH|| Wahr, wenn ein Liniendiagramm Aufwärts- und Abwärtsbalken hat. Gilt nur für Liniendiagramme.|
| HiLoLines| Klasse:Linie| WAHR| FALSCH|| Gibt ein HiLoLines-Objekt zurück, das die Hoch-Tief-Linien für eine Reihe in einem Liniendiagramm darstellt. Gilt nur für Liniendiagramme.|
| IstAutoSplit| Boolescher Wert| WAHR| FALSCH|| Gibt an, ob der Schwellenwert automatisch ist.|
| IstFarbeVariiert| Boolescher Wert| WAHR| FALSCH|| Gibt an, ob die Farbe der Punkte variiert. Das Diagramm darf nur eine Reihe enthalten.|
| Führungslinien| Klasse:Linie| WAHR| FALSCH||Stellt Führungslinien in einem Diagramm dar. Führungslinien verbinden Datenbeschriftungen mit Datenpunkten. Dieses Objekt ist keine Sammlung; es gibt kein Objekt, das eine einzelne Führungslinie darstellt.|
| Legendeneintrag| Klasse:LegendEntry| WAHR| FALSCH|| Ruft den Legendeneintrag gemäß dieser Serie ab.|
| Marker| Klasse:Marker| WAHR| FALSCH|| Ruft den Marker ab.|
| Name| Zeichenfolge| WAHR| FALSCH|| Ruft den Namen der Datenreihe ab oder legt ihn fest.|
| Überlappung| Ganze Zahl| WAHR| FALSCH|| Gibt an, wie Balken und Säulen positioniert werden. Kann ein Wert zwischen –100 und 100 sein. Gilt nur für 2D-Balken- und 2D-Säulendiagramme.|
| PlotOnSecondAxis| Boolescher Wert| WAHR| FALSCH|| Gibt an, ob diese Reihe auf der zweiten Werteachse dargestellt wird.|
| Punkte| Klasse:LinkElement| WAHR| FALSCH|| Ruft die Sammlung von Punkten in einer Reihe in einem Diagramm ab.|
| ZweitePlotGröße| Ganze Zahl| WAHR| FALSCH|| Gibt die Größe des sekundären Abschnitts eines Kreis- oder Balkendiagramms als Prozentsatz der Größe des primären Kreises zurück oder legt sie fest. Kann ein Wert zwischen 5 und 200 sein.|
| SerienLinien| Klasse:Linie| WAHR| FALSCH||Gibt ein SeriesLines-Objekt zurück, das die Serienlinien für ein gestapeltes Balkendiagramm oder ein gestapeltes Säulendiagramm darstellt. Gilt nur für gestapelte Balken- und Säulendiagramme.|
| Schatten| Boolescher Wert| WAHR| FALSCH|| Wahr, wenn die Serie einen Schatten hat.|
| NegativeBlasen anzeigen| Boolescher Wert| WAHR| FALSCH|| Wahr, wenn für die Diagrammgruppe negative Blasen angezeigt werden. Nur gültig für Blasendiagramme.|
| GrößeRepräsentiert| Zeichenfolge| WAHR| FALSCH|| Ruft ab oder legt fest, was die Blasengröße in einem Blasendiagramm darstellt.|
| Glatt| Boolescher Wert| WAHR| FALSCH|| Stellt die Kurvenglättung dar. Wahr, wenn die Kurvenglättung für das Liniendiagramm oder das Streudiagramm aktiviert ist. Gilt nur für durch Linien verbundene Linien- und Streudiagramme.|
| TeilenTyp| Zeichenfolge| WAHR| FALSCH|| Gibt einen Wert zurück oder legt ihn fest, der bestimmt, welche Datenpunkte sich im zweiten Kreis- oder Balkendiagramm eines Kreis- oder Kreis-Balkendiagramms befinden.|
| Wert teilen| Schwimmend| WAHR| FALSCH||Gibt einen Wert zurück oder legt einen Wert fest, der verwendet werden soll, um zu bestimmen, welche Datenpunkte sich im zweiten Kreis- oder Balkendiagramm eines Kreis-aus-Kreis- oder Kreis-aus-Balken-Diagramms befinden.|
| Trendlinien| Klasse:Trendlinien| WAHR| FALSCH|| Gibt ein Objekt zurück, das eine Sammlung aller Trendlinien für die Reihe darstellt.|
| Typ| Zeichenfolge| WAHR| FALSCH|| Ruft den Typ einer Datenreihe ab oder legt ihn fest.|
| UpBars| Klasse:DropBars| WAHR| FALSCH|| Gibt ein DropBars-Objekt zurück, das die Aufwärtsbalken in einem Liniendiagramm darstellt. Gilt nur für Liniendiagramme.|
| Werte| Zeichenfolge| WAHR| FALSCH|| Stellt die Daten der Diagrammreihe dar.|
| XErrorBar| Klasse:ErrorBar| WAHR| FALSCH|| Stellt den Fehlerbalken der Reihe in X-Richtung dar.|
| XWerte| Zeichenfolge| WAHR| FALSCH|| Stellt die x-Werte der Diagrammreihe dar.|
| YErrorBar| Klasse:ErrorBar| WAHR| FALSCH|| Stellt den Fehlerbalken der Reihe in Y-Richtung dar.|
| Verknüpfung| Klasse:Link| WAHR| FALSCH|||

**Elternname** : [LinkElement](/specification/model/linkelement)

