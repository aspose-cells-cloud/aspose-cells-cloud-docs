---
title: "Aspose.Cells Cloud 3.0 Entwicklerhandbuch"
ArticleTitle: "Aspose.Cells Cloud 3.0 REST API Entwicklerhandbuch – Erstellung, Konvertierung und Gestaltung von Excel-Arbeitsmappen"
second_title: "Dokument"
type: docs
url: /de/developer-guide-3.0/
aliases: [/de/developer-guide/v3.0/,/de/developer-guide-v3.0/]
keywords: "Aspose.Cells Cloud, Excel REST API, Konvertierung von Arbeitsmappen, Chart API, Datenimport, Export, PDF, CSV, JSON, Entwicklerhandbuch"
description: "Erfahren Sie, wie Sie die REST APIs von Aspose.Cells Cloud 3.0 für die Erstellung, Konvertierung, Gestaltung, Diagrammerstellung, Tabellenbearbeitung und mehr von Excel-Arbeitsmappen verwenden. Enthält Codebeispiele und Best-Practice-Tipps."
weight: 150
---

## Arbeiten mit Aspose.Cells Cloud REST APIs

Das **Aspose.Cells Cloud 3.0 Entwicklerhandbuch** bietet eine prägnante, durchsuchbare Übersicht über die am häufigsten verwendeten REST API-Vorgänge für Excel-Arbeitsmappen und -Arbeitsblätter. Es richtet sich an Entwickler, die Excel-Dateien programmgesteuert erstellen, ändern, konvertieren und bearbeiten müssen. Nutzen Sie die nachfolgenden Abschnitte, um den gewünschten Vorgang zu finden; jeder Link führt zu einer detaillierten Seite mit Anforderungssyntax, Parametern und Beispielen. Diese Hub-Seite bündelt die Referenz zur **Aspose.Cells Cloud REST API**, sodass workbookbezogene Endpunkte, Diagrammfunktionen sowie Import- und Exportfunktionen leichter gefunden werden können.

**Voraussetzungen:** Bevor Sie die APIs nutzen, stellen Sie sicher, dass Sie über ein gültiges Aspose Cloud-Konto, einen API-Schlüssel und ein geheimes Schlüsselwort sowie die entsprechenden SDKs für Ihre Entwicklungsumgebung verfügen.

### Inhaltsverzeichnis
- [Dateivorgänge](#dateivorgänge)
- [Startseite (Zellformatierung & Zeilen-/Spaltenverwaltung)](#startseite-zellformatierung--zeilen--spaltenverwaltung)
- [Einfügen (Diagramme, Tabellen & OLE-Objekte)](#einfügen-diagramme-tabellen--ole-objekte)
- [Seitenlayout (Seitenumbrüche & Einrichtung)](#seitenlayout-seitenumbrüche--einrichtung)
- [Formeln (Berechnung & Namen)](#formeln-berechnung--namen)
- [Daten (Gliederung, Filter & Import)](#daten-gliederung-filter--import)
- [Überprüfen (Kommentare & Schutz)](#überprüfen-kommentare--schutz)
- [Ansicht (Fenster- & Zoomsteuerung)](#ansicht-fenster--zoomsteuerung)

### Kurze API-Übersicht

| API-Gruppe | Beispielendpunkt | Hauptaktion |
|-----------|----------------|----------------|
| **Arbeitsmappe erstellen** | `POST /cells/workbook` | Erstellt eine neue leere Excel-Arbeitsmappe |
| **Arbeitsmappe konvertieren** | `PUT /cells/workbook/convert` | Konvertiert eine Excel-Datei in PDF, CSV, JSON usw. |
| **Diagramm hinzufügen** | `POST /cells/worksheets/{sheetName}/charts` | Fügt ein neues Diagramm in ein Arbeitsblatt ein |
| **Tabellen verwalten** | `PUT /cells/worksheets/{sheetName}/tables/{tableName}` | Aktualisiert oder löscht ein Listenobjekt (Tabelle) |
| **Daten importieren** | `POST /cells/worksheets/{sheetName}/import` | Importiert CSV, JSON, Bilder oder Arrays in ein Arbeitsblatt |
| **Formeln berechnen** | `POST /cells/workbook/calculate` | Berechnet alle Formeln in einer Arbeitsmappe neu |
| **Filter anwenden** | `POST /cells/worksheets/{sheetName}/filters` | Fügt Filterkriterien hinzu oder entfernt sie |
| **Arbeitsmappe schützen** | `POST /cells/workbook/protect` | Wendet Passwortschutz auf eine Arbeitsmappe an |

Diese häufig genutzten Vorgänge decken die Kernfunktionalität der **Aspose.Cells Cloud Excel REST API** ab und verlinken direkt auf detaillierte Dokumentationsseiten.

Sie können eine PDF-Version der obigen Kurzübersicht für Offline-Nutzung herunterladen.

{{< tabs tabTotal="8" tabID="1" tabName1="Datei" tabName2="Startseite" tabName3="Einfügen" tabName4="Seitenlayout" tabName5="Formeln" tabName6="Daten" tabName7="Überprüfen" tabName8="Ansicht" >}}
{{< tab tabNum="1" >}}
<div class="row">
    <div class="col-md-6">
        <p>Arbeitsmappe: Neu, Konvertieren, Speichern unter</p>
        <ul>
            <li><a href="/de/cells/create-an-empty-excel-workbook/" title="Erstellt eine leere Excel-Arbeitsmappe per API" rel="noopener">Erstellen einer leeren Excel-Arbeitsmappe.</a></li>
            <li><a href="/de/cells/create-excel-workbook-from-a-template-file/" title="Erstellt eine Arbeitsmappe aus einer Vorlagendatei" rel="noopener">Erstellen einer Excel-Arbeitsmappe aus einer Vorlagendatei.</a></li>
            <li><a href="/de/cells/create-excel-workbook-from-a-smartmarker-template/" title="Erstellt eine Arbeitsmappe aus einer SmartMarker-Vorlage" rel="noopener">Erstellen einer Excel-Arbeitsmappe aus einer SmartMarker-Vorlage.</a></li>
            <li><a href="/de/cells/convert/" title="Konvertiert eine Excel-Arbeitsmappe in ein anderes Format" rel="noopener">Konvertieren einer Excel-Arbeitsmappe in verschiedene Dateiformate.</a></li>
            <li><a href="/de/cells/saveas-other-formats/" title="Speichert eine Excel-Arbeitsmappe in einem anderen Format" rel="noopener">Speichern einer Excel-Arbeitsmappe in verschiedenen Dateiformaten.</a></li>
        </ul>
        <p>Suchen, Ersetzen</p>
        <ul>
            <li><a href="/de/cells/search/" title="Sucht nach Text in Excel-Dateien" rel="noopener">Suchen von Text in Excel-Dateien.</a></li>
            <li><a href="/de/cells/replace/" title="Ersetzt Werte in Excel-Dateien" rel="noopener">Ersetzen alter Werte durch neue Werte in Excel-Dateien.</a></li>
        </ul>
        <p>Komprimieren</p>
        <ul>
            <li><a href="/de/cells/compress/" title="Komprimiert Excel-Dateien" rel="noopener">Komprimieren von Excel-Dateien.</a></li>
        </ul>
    </div>
    <div class="col-md-6">
        <p>Arbeitsmappe: Zusammenführen, Teilen</p>
        <ul>
            <li><a href="/de/cells/merge/" title="Fügt mehrere Excel-Arbeitsmappen zusammen" rel="noopener">Zusammenführen von Excel-Arbeitsmappen.</a></li>
            <li><a href="/de/cells/split/" title="Teilt eine Excel-Arbeitsmappe in einzelne Dateien" rel="noopener">Teilen von Excel-Arbeitsmappen.</a></li>
        </ul>
        <p=Wasserzeichen</p>
        <ul>
            <li><a href="/de/cells/add-background-in-workbook/" title="Fügt ein Hintergrundbild zu einer Arbeitsmappe hinzu" rel="noopener">Hinzufügen eines Hintergrundbilds zu einer Arbeitsmappe.</a></li>
            <li><a href="/de/cells/delete-background-in-workbook/" title="Löscht ein Hintergrundbild einer Arbeitsmappe" rel="noopener">Löschen eines Hintergrundbilds aus einer Arbeitsmappe.</a></li>
            <li><a href="/de/cells/set-background-or-watermark-for-excel-worksheet/" title="Setzt ein Hintergrundbild oder Wasserzeichen auf ein Arbeitsblatt" rel="noopener">Setzen eines Hintergrundbilds oder Wasserzeichens auf ein Excel-Arbeitsblatt.</a></li>
            <li><a href="/de/cells/delete-background-or-watermark-of-excel-worksheet/" title="Löscht ein Hintergrundbild oder Wasserzeichen eines Arbeitsblatts" rel="noopener">Löschen eines Hintergrundbilds oder Wasserzeichens von einem Excel-Arbeitsblatt.</a></li>
        </ul>
    </div>
</div>
{{< /tab >}}
{{< tab tabNum="2" >}}
<div class="row">
    <div class="col-md-6">
        <p>Zellenschriftarten, -stile, bedingte Formatierung und Werte</p>
        <ul>
            <li><a href="/de/cells/get-cell-style-from-a-worksheet/" title="Ruft einen Zellstil aus einem Arbeitsblatt ab" rel="noopener">Abrufen eines Zellstils aus einem Excel-Arbeitsblatt.</a></li>
            <li><a href="/de/cells/update-multiple-cells-style/" title="Aktualisiert Stile mehrerer Zellen" rel="noopener">Aktualisieren des Stils mehrerer Zellen auf einem Excel-Arbeitsblatt.</a></li>
            <li><a href="/de/cells/change-cell-style-in-excel-worksheet/" title="Ändert den Stil einer einzelnen Zelle" rel="noopener">Aktualisieren des Zellstils auf einem Excel-Arbeitsblatt.</a></li>
            <li><a href="/de/cells/apply-rich-text-formatting-to-a-cell/" title="Wendet Rich-Text-Formatierung auf eine Zelle an" rel="noopener">Anwenden von Rich-Text-Formatierung für eine Zelle auf einem Excel-Arbeitsblatt.</a></li>
            <li><a href="/de/cells/clear-contents-and-styles-of-cells-in-excel-worksheet/" title="Löscht Zellinhalte und -stile" rel="noopener">Löschen von Inhalten und Stilen von Zellen auf einem Excel-Arbeitsblatt.</a></li>
            <li><a href="/de/cells/working-with-conditional-formatting/" title="Verwaltet bedingte Formatierungsregeln" rel="noopener">Hinzufügen, Löschen und Aktualisieren bedingter Formatierungen auf einem Excel-Arbeitsblatt.</a></li>
            <li><a href="/de/cells/set-value-of-a-cell-in-a-worksheet/" title="Legt den Wert einer Zelle fest" rel="noopener">Festlegen des Werts einer Zelle auf einem Excel-Arbeitsblatt.</a></li>
        </ul>
    </div>
    <div class="col-md-6">
        <p>Zeile/Spalte: Einfügen, Löschen, Kopieren, Ausblenden und automatische Anpassung</p>
        <ul>
            <li><a href="/de/cells/add-an-empty-row-in-a-worksheet/" title="Fügt eine leere Zeile in ein Arbeitsblatt ein" rel="noopener">Hinzufügen einer leeren Zeile auf einem Excel-Arbeitsblatt.</a></li>
            <li><a href="/de/cells/delete-row-from-a-worksheet/" title="Löscht eine Zeile aus einem Arbeitsblatt" rel="noopener">Löschen einer Zeile aus einem Excel-Arbeitsblatt.</a></li>
            <li><a href="/de/cells/copy-rows-in-excel-worksheet/" title="Kopiert Zeilen innerhalb eines Arbeitsblatts" rel="noopener">Kopieren von Zeilen auf einem Excel-Arbeitsblatt.</a></li>
            <li><a href="/de/cells/hide-rows-in-excel-worksheet/" title="Blendet Zeilen in einem Arbeitsblatt aus" rel="noopener">Ausblenden von Zeilen auf einem Excel-Arbeitsblatt.</a></li>
            <li><a href="/de/cells/auto-fit-rows-in-excel-workbooks/" title="Passt Zeilen in einer Arbeitsmappe automatisch an" rel="noopener">Automatisches Anpassen von Zeilen auf einer Excel-Arbeitsmappe.</a></li>
            <li><a href="/de/cells/columns/add/" title="Fügt eine leere Spalte in ein Arbeitsblatt ein" rel="noopener">Hinzufügen einer leeren Spalte auf einem Excel-Arbeitsblatt.</a></li>
            <li><a href="/de/cells/columns/delete/" title="Löscht eine Spalte aus einem Arbeitsblatt" rel="noopener">Löschen einer Spalte aus einem Excel-Arbeitsblatt.</a></li>
            <li><a href="/de/cells/columns/copy/" title="Kopiert Spalten innerhalb eines Arbeitsblatts" rel="noopener">Kopieren von Spalten auf einem Excel-Arbeitsblatt.</a></li>
            <li><a href="/de/cells/columns/hide/" title="Blendet Spalten in einem Arbeitsblatt aus" rel="noopener">Ausblenden von Spalten auf einem Excel-Arbeitsblatt.</a></li>
            <li><a href="/de/cells/columns/autofit/" title="Passt Spalten in einer Arbeitsmappe automatisch an" rel="noopener">Automatisches Anpassen von Spalten auf einer Excel-Arbeitsmappe.</a></li>
        </ul>
    </div>
</div>
{{< /tab >}}
{{< tab tabNum="3" >}}
<div class="row">
    <div class="col-md-6">
        <p>Diagramm</p>
        <ul>
            <li><a href="/de/cells/add-a-chart-in-a-worksheet/" title="Fügt ein Diagramm zu einem Arbeitsblatt hinzu" rel="noopener">Hinzufügen eines Diagramms auf einem Excel-Arbeitsblatt.</a></li>
            <li><a href="/de/cells/delete-a-chart-from-a-worksheet/" title="Löscht ein Diagramm aus einem Arbeitsblatt" rel="noopener">Löschen eines Diagramms auf einem Excel-Arbeitsblatt.</a></li>
            <li><a href="/de/cells/delete-all-charts-from-a-worksheet/" title="Löscht alle Diagramme aus einem Arbeitsblatt" rel="noopener">Löschen aller Diagramme auf einem Excel-Arbeitsblatt.</a></li>
            <li><a href="/de/cells/convert-chart-to-image/" title="Konvertiert ein Diagramm in eine Bilddatei" rel="noopener">Konvertieren eines Diagramms in ein Bild.</a></li>
            <li><a href="/de/cells/hide-chart-legend-in-a-worksheet/" title="Blendet ein Diagramm-Legende aus" rel="noopener">Ausblenden der Diagramm-Legende auf einem Excel-Arbeitsblatt.</a></li>
            <li><a href="/de/cells/update-chart-title-in-excel-worksheet/" title="Aktualisiert einen Diagrammtitel" rel="noopener">Aktualisieren des Diagrammtitels auf einem Excel-Arbeitsblatt.</a></li>
            <li><a href="/de/cells/delete-chart-title-in-a-worksheet/" title="Löscht einen Diagrammtitel" rel="noopener">Löschen des Diagrammtitels auf einem Excel-Arbeitsblatt.</a></li>
        </ul>
        <p>Tabelle</p>
        <ul>
            <li><a href="/de/cells/add-a-list-object-or-table-inside-the-worksheet/" title="Fügt eine Tabelle (Listenobjekt) zu einem Arbeitsblatt hinzu" rel="noopener">Hinzufügen eines Listenobjekts auf einem Excel-Arbeitsblatt.</a></li>
            <li><a href="/de/cells/update-a-list-object-or-table-inside-the-worksheet/" title="Aktualisiert eine Tabelle in einem Arbeitsblatt" rel="noopener">Aktualisieren eines Listenobjekts auf einem Excel-Arbeitsblatt.</a></li>
            <li><a href="/de/cells/convert-list-object-or-table-to-range/" title="Konvertiert eine Tabelle in einen Bereich" rel="noopener">Konvertieren eines Listenobjekts in einen Bereich.</a></li>
            <li><a href="/de/cells/sort-table-data/" title="Sortiert Daten innerhalb einer Tabelle" rel="noopener">Sortieren von Tabellendaten.</a></li>
        </ul>
        <p>OLE-Objekt</p>
        <ul>
            <li><a href="/de/cells/add-oleobject-to-excel-worksheet/" title="Fügt ein OLE-Objekt zu einem Arbeitsblatt hinzu" rel="noopener">Hinzufügen eines OLE-Objekts auf einem Excel-Arbeitsblatt.</a></li>
            <li><a href="/de/cells/update-a-specific-oleobject-from-excel-worksheet/" title="Aktualisiert ein bestimmtes OLE-Objekt" rel="noopener">Aktualisieren eines bestimmten OLE-Objekts auf einem Excel-Arbeitsblatt.</a></li>
            <li><a href="/de/cells/convert-oleobject-to-image/" title="Konvertiert ein OLE-Objekt in ein Bild" rel="noopener">Konvertieren eines OLE-Objekts in ein Bild.</a></li>
            <li><a href="/de/cells/delete-all-oleobjects-from-excel-worksheet/" title="Löscht alle OLE-Objekte aus einem Arbeitsblatt" rel="noopener">Löschen aller OLE-Objekte auf einem Excel-Arbeitsblatt.</a></li>
            <li><a href="/de/cells/delete-a-specific-oleobject-from-excel-worksheet/" title="Löscht ein bestimmtes OLE-Objekt" rel="noopener">Löschen eines bestimmten OLE-Objekts auf einem Excel-Arbeitsblatt.</a></li>
        </ul>
    </div>
    <div class="col-md-6">
        <p>Form</p>
        <ul>
            <li><a href="/de/cells/add-a-shape-inside-the-worksheet/" title="Fügt eine Form zu einem Arbeitsblatt hinzu" rel="noopener">Hinzufügen einer Form auf einem Excel-Arbeitsblatt.</a></li>
            <li><a href="/de/cells/delete-all-shapes-inside-the-worksheet/" title="Löscht alle Formen aus einem Arbeitsblatt" rel="noopener">Löschen aller Formen auf einem Excel-Arbeitsblatt.</a></li>
            <li><a href="/de/cells/delete-a-shape-by-index-inside-the-worksheet/" title="Löscht eine Form anhand ihres Index" rel="noopener">Löschen einer Form anhand ihres Index auf einem Excel-Arbeitsblatt.</a></li>
        </ul>
        <p>Pivot-Tabelle</p>
        <ul>
            <li><a href="/de/cells/add-a-pivot-table-in-a-worksheet/" title="Fügt eine Pivot-Tabelle zu einem Arbeitsblatt hinzu" rel="noopener">Hinzufügen einer Pivot-Tabelle auf einem Excel-Arbeitsblatt.</a></li>
            <li><a href="/de/cells/delete-worksheet-pivot-tables/" title="Löscht alle Pivot-Tabellen aus einem Arbeitsblatt" rel="noopener">Löschen aller Pivot-Tabellen auf einem Excel-Arbeitsblatt.</a></li>
            <li><a href="/de/cells/delete-worksheet-pivot-table-by-index/" title="Löscht eine Pivot-Tabelle anhand ihres Index" rel="noopener">Löschen einer Pivot-Tabelle anhand ihres Index auf einem Excel-Arbeitsblatt.</a></li>
            <li><a href="/de/cells/update-cell-style-for-pivot-table/" title="Aktualisiert den Zellstil in einer Pivot-Tabelle" rel="noopener">Aktualisieren des Zellstils einer Pivot-Tabelle auf einem Excel-Arbeitsblatt.</a></li>
            <li><a href="/de/cells/update-style-for-pivot-table/" title="Aktualisiert den Gesamtstil einer Pivot-Tabelle" rel="noopener">Aktualisieren des Stils einer Pivot-Tabelle auf einem Excel-Arbeitsblatt.</a></li>
            <li><a href="/de/cells/working-with-pivot-filters/" title="Arbeitet mit Pivot-Tabellenfiltern" rel="noopener">Arbeiten mit Pivot-Filtern auf einem Excel-Arbeitsblatt.</a></li>
            <li><a href="/de/cells/hide-pivot-field-item/" title="Blendet ein Pivot-Feld-Element aus" rel="noopener">Ausblenden von Pivot-Feld-Elementen auf einem Excel-Arbeitsblatt.</a></li>
            <li><a href="/de/cells/move-pivot-table/" title="Verschiebt eine Pivot-Tabelle innerhalb eines Arbeitsblatts" rel="noopener">Verschieben einer Pivot-Tabelle auf einem Excel-Arbeitsblatt.</a></li>
        </ul>
    </div>
</div>
{{< /tab >}}
{{< tab tabNum="4" >}}
<div class="row">
    <div class="col-md-6">
        <p>Seitenumbruch</p>
        <ul>
            <li><a href="/de/cells/insert-horizontal-page-break-inside-worksheet/" title="Fügt einen horizontalen Seitenumbruch ein" rel="noopener">Einfügen eines horizontalen Seitenumbruchs auf einem Excel-Arbeitsblatt.</a></li>
            <li><a href="/de/cells/insert-vertical-page-break-inside-worksheet/" title="Fügt einen vertikalen Seitenumbruch ein" rel="noopener">Einfügen eines vertikalen Seitenumbruchs auf einem Excel-Arbeitsblatt.</a></li>
            <li><a href="/de/cells/delete-horizontal-page-break-inside-worksheet/" title="Löscht einen horizontalen Seitenumbruch" rel="noopener">Löschen eines horizontalen Seitenumbruchs auf einem Excel-Arbeitsblatt.</a></li>
            <li><a href="/de/cells/delete-vertical-page-break-inside-worksheet/" title="Löscht einen vertikalen Seitenumbruch" rel="noopener">Löschen eines vertikalen Seitenumbruchs auf einem Excel-Arbeitsblatt.</a></li>
        </ul>
    </div>
    <div class="col-md-6">
        <p>Seiteneinrichtung</p>
        <ul>
        </ul>
    </div>
</div>
{{< /tab >}}
{{< tab tabNum="5" >}}
<div class="row">
    <div class="col-md-6">
        <p>Berechnung</p>
        <ul>
            <li><a href="/de/cells/calculate-all-formulas-in-a-workbook/" title="Berechnet alle Formeln in einer Arbeitsmappe" rel="noopener">Berechnen aller Formeln auf einer Excel-Arbeitsmappe.</a></li>
            <li><a href="/de/cells/calculate-cells-formula/" title="Berechnet die Formel einer bestimmten Zelle" rel="noopener">Berechnen von Zellformeln auf einer Excel-Arbeitsmappe.</a></li>
            <li><a href="/de/cells/calculate-formula-in-a-worksheet/" title="Berechnet eine Formel in einem Arbeitsblatt" rel="noopener">Berechnen einer Formel auf einem Excel-Arbeitsblatt.</a></li>
        </ul>
    </div>
    <div class="col-md-6">
        <p>Name</p>
        <ul>
        </ul>
    </div>
</div>
{{< /tab >}}
{{< tab tabNum="6" >}}
<div class="row">
    <div class="col-md-6">
        <p>Gliederung</p>
        <ul>
            <li><a href="/de/cells/group-rows-in-excel-worksheet/" title="Gruppiert Zeilen in einem Arbeitsblatt" rel="noopener">Gruppieren von Zeilen auf einem Excel-Arbeitsblatt.</a></li>
            <li><a href="/de/cells/ungroup-rows-in-excel-worksheet/" title="Hebt die Gruppierung von Zeilen in einem Arbeitsblatt auf" rel="noopener">Aufheben der Gruppierung von Zeilen auf einem Excel-Arbeitsblatt.</a></li>
        </ul>
        <p>Filter</p>
        <ul>
            <li><a href="/de/cells/add-a-filter-for-a-filter-column/" title="Fügt einem Spaltenfilter hinzu" rel="noopener">Hinzufügen eines Filters für eine Spalte auf einem Excel-Arbeitsblatt.</a></li>
            <li><a href="/de/cells/delete-a-filter-for-a-filter-column/" title="Löscht einen Spaltenfilter" rel="noopener">Löschen eines Filters für eine Spalte auf einem Excel-Arbeitsblatt.</a></li>
            <li><a href="/de/cells/remove-a-date-filter/" title="Entfernt einen Datumsfilter" rel="noopener">Entfernen eines Datumsfilters auf einem Excel-Arbeitsblatt.</a></li>
            <li><a href="/de/cells/add-an-icon-filter/" title="Fügt einen Symbolfilter hinzu" rel="noopener">Hinzufügen eines Symbolfilters auf einem Excel-Arbeitsblatt.</a></li>
            <li><a href="/de/cells/add-date-filter-in-a-worksheet/" title="Fügt einen Datumsfilter hinzu" rel="noopener">Hinzufügen eines Datumsfilters auf einem Excel-Arbeitsblatt.</a></li>
            <li><a href="/de/cells/filter-data-by-using-an-autofilter/" title="Filtert Daten mithilfe von AutoFilter" rel="noopener">Filtern von Daten mithilfe eines AutoFilters auf einem Excel-Arbeitsblatt.</a></li>
            <li><a href="/de/cells/filter-the-top-10-items-in-the-list/" title="Filtert die Top-10-Elemente" rel="noopener">Filtern der Top-10-Elemente in der Liste auf einem Excel-Arbeitsblatt.</a></li>
            <li><a href="/de/cells/match-all-blank-cells-in-the-list/" title="Findet alle leeren Zellen" rel="noopener">Finden aller leeren Zellen in der Liste auf einem Excel-Arbeitsblatt.</a></li>
        </ul>
        <p>Sortierung</p>
        <ul>
            <li><a href="/de/cells/sort-worksheet-data/" title="Sortiert Arbeitsblattdaten" rel="noopener">Sortieren von Daten auf einem Excel-Arbeitsblatt.</a></li>
        </ul>
    </div>
    <div class="col-md-6">
        <p>Datenimport</p>
        <ul>
            <li><a href="/de/cells/import/" title="Importiert Daten in Excel-Dateien" rel="noopener">Importieren von Daten in Excel-Dateien.</a></li>
            <li><a href="/de/cells/import-CSV-data-into-worksheet/" title="Importiert CSV-Daten in ein Arbeitsblatt" rel="noopener">Importieren von CSV-Daten in ein Excel-Arbeitsblatt.</a></li>
            <li><a href="/de/cells/import/picture/" title="Importiert ein Bild in ein Arbeitsblatt" rel="noopener">Importieren eines Bildes in ein Excel-Arbeitsblatt.</a></li>
            <li><a href="/de/cells/import/double-array/" title="Importiert ein Double-Array in ein Arbeitsblatt" rel="noopener">Importieren eines Double-Arrays in ein Excel-Arbeitsblatt.</a></li>
            <li><a href="/de/cells/import/integer-array/" title="Importiert ein Integer-Array in ein Arbeitsblatt" rel="noopener">Importieren eines Integer-Arrays in ein Excel-Arbeitsblatt.</a></li>
            <li><a href="/de/cells/import/string-array/" title="Importiert ein String-Array in ein Arbeitsblatt" rel="noopener">Importieren eines String-Arrays in ein Excel-Arbeitsblatt.</a></li>
            <li><a href="/de/cells/import/with-using-storage/" title="Importiert Daten unter Verwendung des Speichers" rel="noopener">Importieren von Daten in ein Excel-Arbeitsblatt unter Verwendung des Speichers.</a></li>
            <li><a href="/de/cells/import/without-using-storage/" title="Importiert Daten ohne Verwendung des Speichers" rel="noopener">Importieren von Daten in ein Excel-Arbeitsblatt ohne Verwendung des Speichers.</a></li>
        </ul>
        <p>Assembly</p>
        <ul>
            <li><a href="/de/cells/assembly/" title="Fügt Daten in Excel-Dateien zusammen" rel="noopener">Zusammenführen von Daten in Excel-Dateien.</a></li>
        </ul>
    </div>
</div>
{{< /tab >}}
{{< tab tabNum="7" >}}
<div class="row">
    <div class="col-md-6">
        <p>Kommentare</p>
        <ul>
            <li><a href="/de/cells/add-a-comment-to-a-cell-in-a-worksheet/" title="Fügt einer Zelle einen Kommentar hinzu" rel="noopener">Hinzufügen eines Kommentars zu einer Zelle auf einem Excel-Arbeitsblatt.</a></li>
            <li><a href="/de/cells/update-a-comment-in-excel-workbook/" title="Aktualisiert einen Zellkommentar" rel="noopener">Aktualisieren eines Kommentars auf einem Excel-Arbeitsblatt.</a></li>
            <li><a href="/de/cells/delete-all-comments-in-a-worksheet/" title="Löscht alle Kommentare in einem Arbeitsblatt" rel="noopener">Löschen aller Kommentare auf einem Excel-Arbeitsblatt.</a></li>
        </ul>
    </div>
    <div class="col-md-6">
        <p>Änderungen</p>
        <ul>
            <li><a href="/de/cells/protect-excel-workbooks/" title="Schützt eine Excel-Arbeitsmappe" rel="noopener">Schützen einer Excel-Arbeitsmappe.</a></li>
            <li><a href="/de/cells/unprotect-excel-workbooks/" title="Hebt den Schutz einer Excel-Arbeitsmappe auf" rel="noopener">Aufheben des Schutzes einer Excel-Arbeitsmappe.</a></li>
        </ul>
    </div>
</div>
{{< /tab >}}
{{< tab tabNum="8" >}}
<div class="row">
    <div class="col-md-6">
        <p>Fenster</p>
        <ul>
            <li><a href="/de/cells/freeze-panes-in-excel-worksheet/" title="Friert Bereiche in einem Arbeitsblatt ein" rel="noopener">Einfrieren von Bereichen auf einem Excel-Arbeitsblatt.</a></li>
            <li><a href="/de/cells/unfreeze-panes-in-excel-worksheet/" title="Gefriert Bereiche in einem Arbeitsblatt wieder auf" rel="noopener">Aufheben des Einfrierens von Bereichen auf einem Excel-Arbeitsblatt.</a></li>
            <li><a href="/de/cells/hide-excel-worksheets/" title="Blendet ein Arbeitsblatt aus" rel="noopener">Ausblenden eines Excel-Arbeitsblatts.</a></li>
            <li><a href="/de/cells/unhide-excel-worksheets/" title="Blendet ein Arbeitsblatt wieder ein" rel="noopener">Einsblenden eines Excel-Arbeitsblatts.</a></li>
        </ul>
    </div>
    <div class="col-md-6">
        <p>Zoom</p>
        <ul>
            <li><a href="/de/cells/set-zoom-in-excel-worksheet/" title="Legt den Zoom-Faktor eines Arbeitsblatts fest" rel="noopener">Festlegen des Zoom-Faktors auf einem Excel-Arbeitsblatt.</a></li>
        </ul>
    </div>
</div>
{{< /tab >}}

{{< /tabs >}}
---