---
title: "Arbeitsmappenkonvertierungsoptionen"
second_title: "Dokument"
linktitle: "Arbeitsmappenkonvertierungsoptionen"
type: docs
url: /convert-workbook-options/
keywords: "Aspose.Cells, ConvertWorkbookOptions, Excel-Konvertierung, PDF, CSV, API"
description: "Arbeitsmappenkonvertierungsoptionen – Konfigurieren Sie die Excel-Arbeitsmappenkonvertierung in PDF, CSV, HTML und weitere Formate mit der Aspose.Cells Cloud API."
weight: 79
ArticleTitle: "Arbeitsmappenkonvertierungsoptionen – Aspose.Cells Cloud API"
---

# ConvertWorkbookOptions-Eigenschaften

**API-Version:** 23.12 (2024‑03)

`ConvertWorkbookOptions` ist das Anforderungsmodell, das von der Aspose.Cells Cloud-Konvertierungs-API verwendet wird, um festzulegen, wie eine Excel-Arbeitsmappe in ein anderes Format (PDF, CSV, HTML usw.) transformiert werden soll. Es fasst die Quelldateiinformationen, das Zielformat, die Seiteneinrichtungseinstellungen und formatspezifische Speicheroptionen zusammen.

| Name                                | Typ         | Beschreibung                                                                                                   | Hinweise |
| ----------------------------------- | ----------- | ------------------------------------------------------------------------------------------------------------- | ------- |
| **DataSource**                      | **Objekt**  | Quelldateiquelle: `CloudFileSystem`, `RequestFiles` oder `HttpUri`.                                            |         |
| **[FileInfo](/cells/file-info/)**   | **Objekt**  | Gibt Dateinamen, Größe und base64-codierten Inhalt an.                                                   |         |
| **[PageSetup](/cells/page-setup/)** | **Objekt**  | Seiteneinrichtungseigenschaften wie Ränder, Ausrichtung und Skalierung.                                              |         |
| **SaveOptions**                     | **Objekt**  | Container für formatspezifische Speicheroptionen (z. B. `PdfSaveOptions`, `HtmlSaveOptions`).                |         |
| **ConvertFormat**                   | **Zeichenfolge**  | Zieldateiformat (z. B. **PDF**, **CSV**, **HTML**, **XLSX**, **TIFF**, usw.).                              |         |
| **CheckExcelRestriction**           | **Boolean** | Gibt an, ob Excel-spezifische Einschränkungen (maximale Zeilen, Spalten, Blattname-Länge usw.) erzwungen werden sollen. |         |

**Voraussetzungen**

- Holen Sie sich ein gültiges OAuth 2.0-Zugriffstoken für Aspose.Cells Cloud.  
- Stellen Sie sicher, dass die Quelldatei über einen der unterstützten `DataSource`-Typen erreichbar ist.

**Kurzes Beispiel**

```json
{
  "DataSource": {
    "FileInfo": {
      "FileName": "Beispiel.xlsx",
      "FileContent": "<base64-codierter-Inhalt>"
    }
  },
  "ConvertFormat": "pdf",
  "SaveOptions": {
    "PdfSaveOptions": {
      "CompressImages": true,
      "ImageQuality": 90
    }
  }
}
```

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/convert" \
     -H "Authorization: Bearer {access_token}" \
     -H "Content-Type: application/json" \
     -d @request.json \
     -o Beispiel.pdf
```

**API-Anforderungsdetails**

Die Konvertierungsoperation erfolgt mit einer **POST**-Anforderung an den Endpunkt:

```
https://api.aspose.cloud/v3.0/cells/convert
```

Erforderliche Header:

| Header                | Wert                               |
|-----------------------|------------------------------------|
| `Authorization`       | `Bearer {access_token}`            |
| `Content-Type`        | `application/json`                |

Der Anforderungstext muss eine JSON-Repräsentation von `ConvertWorkbookOptions` sein (siehe obiges Beispiel). Alle Eigenschaften sind optional, es sei denn, sie werden vom gewählten `ConvertFormat` benötigt.

**API-Antwort**

Eine erfolgreiche Konvertierung gibt **HTTP 200 OK** (oder **202 Accepted** bei asynchroner Verarbeitung) zurück und liefert die konvertierte Datei im Antworttext. Bei gestreamter Antwort enthält der `Content-Disposition`-Header den vorgeschlagenen Dateinamen.

Beispiel einer JSON-Antwort für eine asynchrone Anforderung:

```json
{
  "JobId": "a1b2c3d4e5",
  "Status": "InProgress",
  "ResultUrl": "https://api.aspose.cloud/v3.0/cells/jobs/a1b2c3d4e5/result"
}
```

**Statuscodes**

| Code | Bedeutung                                 |
|------|------------------------------------------|
| 200  | Konvertierung abgeschlossen; Datei zurückgegeben.     |
| 202  | Konvertierung akzeptiert; Ergebnis später verfügbar. |
| 400  | Ungültige Anforderung – fehlende oder ungültige Parameter. |
| 401  | Nicht autorisiert – ungültiges oder fehlendes Token. |
| 403  | Verboten – unzureichende Berechtigungen.   |
| 500  | Interner Serverfehler.                   |

**Hinweise / Einschränkungen**

- Die `CheckExcelRestriction`-Flag erzwingt Excel-Grenzwerte wie maximale Zeilen (1.048.576) und Spalten (16.384).  
- Nicht alle Zielformate unterstützen alle `SaveOptions`-Eigenschaften; nicht unterstützte Optionen werden ignoriert.  
- Wenn `HttpUri` als Datenquelle verwendet wird, muss die URL öffentlich erreichbar sein und keine Authentifizierung erfordern.  
- Die API-Methode und der Endpunkt wurden hinzugefügt, um die Klarheit für Entwickler zu verbessern und Integrationsfehler zu reduzieren.  

## FileSource-Eigenschaften

| Eigenschaftsname  | Eigenschaftstyp | Nullable | ReadOnly | Standardwert | Beschreibung                                                               |
| ----------------- | --------------- | -------- | -------- | ------------ | -------------------------------------------------------------------------- |
| FileSourceType    | Zeichenfolge    | true     | false    |              | Gibt den Quelltyp an (`CloudFileSystem`, `RequestFiles`, `HttpUri`). |
| FilePath          | Zeichenfolge    | true     | false    |              | Dateipfadposition.                                                       |

## DbfSaveOptions-Eigenschaften

| Eigenschaftsname          | Eigenschaftstyp | Nullable | ReadOnly | Standardwert | Beschreibung                                        |
| ------------------------- | --------------- | -------- | -------- | ------------ | --------------------------------------------------- |
| ExportAsString            | Boolean         | true     | false    |              | Wenn **true**, werden numerische Werte als Zeichenfolgen exportiert. |
| SaveFormat                | Zeichenfolge    | true     | false    |              | Bezeichner des DBF-Dateiformats.                    |
| CachedFileFolder          | Zeichenfolge    | true     | false    |              | Ordner für temporäre Zwischengespeicherte Dateien.  |
| ClearData                 | Boolean         | true     | false    |              | Löscht vorhandene Daten vor dem Speichern.          |
| CreateDirectory           | Boolean         | true     | false    |              | Erstellt das Zielverzeichnis, falls es nicht existiert. |
| EnableHttpCompression     | Boolean         | true     | false    |              | Aktiviert HTTP-Komprimierung für die Antwort.       |
| RefreshChartCache         | Boolean         | true     | false    |              | Aktualisiert zwischengespeicherte Diagrammdaten vor dem Speichern. |
| SortNames                 | Boolean         | true     | false    |              | Sortiert benannte Bereiche alphabetisch.            |
| ValidateMergedAreas       | Boolean         | true     | false    |              | Überprüft verbundene Zellen auf Konsistenz.         |
| MergeAreas                | Boolean         | true     | false    |              | Vereint benachbarte Zellen, wo möglich.             |
| SortExternalNames         | Boolean         | true     | false    |              | Sortiert externe benannte Verweise.                 |
| CheckExcelRestriction     | Boolean         | true     | false    |              | Erzwingt Excel-spezifische Grenzwerte während der Konvertierung. |
| UpdateSmartArt            | Boolean         | true     | false    |              | Aktualisiert SmartArt-Objekte auf die neueste Version. |
| EncryptDocumentProperties | Boolean         | true     | false    |              | Verschlüsselt Dokumenteigenschaften in der Ausgabedatei. |

## DifSaveOptions-Eigenschaften

| Eigenschaftsname          | Eigenschaftstyp | Nullable | ReadOnly | Standardwert | Beschreibung                                        |
| ------------------------- | --------------- | -------- | -------- | ------------ | --------------------------------------------------- |
| SaveFormat                | Zeichenfolge    | true     | false    |              | Bezeichner des DIF-Dateiformats.                    |
| CachedFileFolder          | Zeichenfolge    | true     | false    |              | Ordner für temporäre Zwischengespeicherte Dateien.  |
| ClearData                 | Boolean         | true     | false    |              | Löscht vorhandene Daten vor dem Speichern.          |
| CreateDirectory           | Boolean         | true     | false    |              | Erstellt das Zielverzeichnis, falls es nicht existiert. |
| EnableHttpCompression     | Boolean         | true     | false    |              | Aktiviert HTTP-Komprimierung für die Antwort.       |
| RefreshChartCache         | Boolean         | true     | false    |              | Aktualisiert zwischengespeicherte Diagrammdaten vor dem Speichern. |
| SortNames                 | Boolean         | true     | false    |              | Sortiert benannte Bereiche alphabetisch.            |
| ValidateMergedAreas       | Boolean         | true     | false    |              | Überprüft verbundene Zellen auf Konsistenz.         |
| MergeAreas                | Boolean         | true     | false    |              | Vereint benachbarte Zellen, wo möglich.             |
| SortExternalNames         | Boolean         | true     | false    |              | Sortiert externe benannte Verweise.                 |
| CheckExcelRestriction     | Boolean         | true     | false    |              | Erzwingt Excel-spezifische Grenzwerte während der Konvertierung. |
| UpdateSmartArt            | Boolean         | true     | false    |              | Aktualisiert SmartArt-Objekte auf die neueste Version. |
| EncryptDocumentProperties | Boolean         | true     | false    |              | Verschlüsselt Dokumenteigenschaften in der Ausgabedatei. |

## DocxSaveOptions-Eigenschaften

| Eigenschaftsname                  | Eigenschaftstyp | Nullable | ReadOnly | Standardwert | Beschreibung                                           |
| --------------------------------- | --------------- | -------- | -------- | ------------ | ------------------------------------------------------ |
| DefaultFont                       | Zeichenfolge    | true     | false    |              | Schriftart, die verwendet wird, wenn eine Quellschriftart nicht verfügbar ist. |
| CheckWorkbookDefaultFont          | Boolean         | true     | false    |              | Überprüft, ob die Standardarbeitsmappenschriftart angewendet wird. |
| CheckFontCompatibility            | Boolean         | true     | false    |              | Überprüft Schriftartkompatibilität für das Zielformat. |
| IsFontSubstitutionCharGranularity | Boolean         | true     | false    |              | Steuert zeichenbasierte Schriftartersatzfunktion.     |
| OnePagePerSheet                   | Boolean         | true     | false    |              | Erzwingt, dass jedes Blatt auf einer separaten Seite erscheint. |
| AllColumnsInOnePagePerSheet       | Boolean         | true     | false    |              | Passt alle Spalten eines Blattes auf eine Seite.     |
| IgnoreError                       | Boolean         | true     | false    |              | Ignoriert nicht-kritische Fehler während der Konvertierung. |
| OutputBlankPageWhenNothingToPrint | Boolean         | true     | false    |              | Erzeugt eine leere Seite, wenn nichts gerendert werden soll. |
| PageIndex                         | Integer         | true     | false    |              | Index der ersten zu exportierenden Seite.            |
| PageCount                         | Integer         | true     | false    |              | Anzahl der zu exportierenden Seiten.                  |
| PrintingPageType                  | Zeichenfolge    | true     | false    |              | Gibt den Seitentyp für das Drucken an.                |
| GridlineType                      | Zeichenfolge    | true     | false    |              | Bestimmt, wie Gitterlinien gerendert werden.          |
| TextCrossType                     | Zeichenfolge    | true     | false    |              | Definiert den Kreuztyp für die Textwiedergabe.        |
| DefaultEditLanguage               | Zeichenfolge    | true     | false    |              | Standardsprache für die Textbearbeitung.             |
| EmfRenderSetting                  | Zeichenfolge    | true     | false    |              | Einstellungen für die EMF-Wiedergabe.                 |
| MergeAreas                        | Boolean         | true     | false    |              | Vereint benachbarte Zellen, wo möglich.               |
| SortExternalNames                 | Boolean         | true     | false    |              | Sortiert externe benannte Verweise.                   |
| UpdateSmartArt                    | Boolean         | true     | false    |              | Aktualisiert SmartArt-Objekte auf die neueste Version. |
| SaveFormat                        | Zeichenfolge    | true     | false    |              | Bezeichner des DOCX-Dateiformats.                     |
| CachedFileFolder                  | Zeichenfolge    | true     | false    |              | Ordner für temporäre Zwischengespeicherte Dateien.    |
| ClearData                         | Boolean         | true     | false    |              | Löscht vorhandene Daten vor dem Speichern.            |
| CreateDirectory                   | Boolean         | true     | false    |              | Erstellt das Zielverzeichnis, falls es nicht existiert. |
| EnableHttpCompression             | Boolean         | true     | false    |              | Aktiviert HTTP-Komprimierung für die Antwort.         |
| RefreshChartCache                 | Boolean         | true     | false    |              | Aktualisiert zwischengespeicherte Diagrammdaten vor dem Speichern. |
| SortNames                         | Boolean         | true     | false    |              | Sortiert benannte Bereiche alphabetisch.              |
| ValidateMergedAreas               | Boolean         | true     | false    |              | Überprüft verbundene Zellen auf Konsistenz.           |
| CheckExcelRestriction             | Boolean         | true     | false    |              | Erzwingt Excel-spezifische Grenzwerte während der Konvertierung. |
| EncryptDocumentProperties         | Boolean         | true     | false    |              | Verschlüsselt Dokumenteigenschaften in der Ausgabedatei. |

## HtmlSaveOptions-Eigenschaften

| Eigenschaftsname                | Eigenschaftstyp | Nullable | ReadOnly | Standardwert | Beschreibung                                          |
| ------------------------------- | --------------- | -------- | -------- | ------------ | ----------------------------------------------------- |
| ExportPageHeaders               | Boolean         | true     | false    |              | Schließt Seitenheader in die HTML-Ausgabe ein.       |
| ExportPageFooters               | Boolean         | true     | false    |              | Schließt Seitenfußzeilen in die HTML-Ausgabe ein.    |
| ExportRowColumnHeadings         | Boolean         | true     | false    |              | Exportiert Zeilen- und Spaltenüberschriften.         |
| ShowAllSheets                   | Boolean         | true     | false    |              | Zeigt alle Arbeitsblätter in einer einzigen HTML-Datei. |
| ImageOptions                    | Klasse          | true     | false    |              | Einstellungen zur Steuerung der Bildwiedergabe.      |
| SaveAsSingleFile                | Boolean         | true     | false    |              | Speichert die gesamte Arbeitsmappe als eine HTML-Datei. |
| ExportHiddenWorksheet           | Boolean         | true     | false    |              | Schließt ausgeblendete Arbeitsblätter in den Export ein. |
| ExportGridLines                 | Boolean         | true     | false    |              | Rendert Gitterlinien in der HTML-Ausgabe.             |
| PresentationPreference          | Boolean         | true     | false    |              | Optimiert HTML für den Präsentationsmodus.           |
| CellCssPrefix                   | Zeichenfolge    | true     | false    |              | Präfix, das generierten CSS-Klassennamen für Zellen hinzugefügt wird. |
| TableCssId                      | Zeichenfolge    | true     | false    |              | ID-Attribut für die generierte HTML-Tabelle.          |
| IsFullPathLink                  | Boolean         | true     | false    |              | Erzeugt vollständige Pfad-Hyperlinks für Ressourcen. |
| ExportWorksheetCSSSeparately    | Boolean         | true     | false    |              | Platziert das CSS jedes Arbeitsblatts in einer separaten Datei. |
| ExportSimilarBorderStyle        | Boolean         | true     | false    |              | Vereint ähnliche Randstile, um die CSS-Größe zu reduzieren. |
| MergeEmptyTdForcely             | Boolean         | true     | false    |              | Erzwingt das Zusammenführen leerer `<td>`-Elemente.  |
| ExportCellCoordinate            | Boolean         | true     | false    |              | Schließt Zellkoordinaten (z. B. A1) in die HTML-Ausgabe ein. |
| ExportExtraHeadings             | Boolean         | true     | false    |              | Fügt zusätzliche Überschriftenzeilen/-spalten hinzu, falls erforderlich. |
| ExportHeadings                  | Boolean         | true     | false    |              | Exportiert Zeilen- und Spaltenüberschriften.         |
| ExportFormula                   | Boolean         | true     | false    |              | Zeigt Formeln anstelle berechneter Werte an.          |
| AddTooltipText                  | Boolean         | true     | false    |              | Fügt Tooltips mit Zellkommentaren hinzu.              |
| ExportBogusRowData              | Boolean         | true     | false    |              | Schließt Platzhalterzeilen für leere Daten ein.       |
| ExcludeUnusedStyles             | Boolean         | true     | false    |              | Entfernt nicht verwendete CSS-Stile.                  |
| ExportDocumentProperties        | Boolean         | true     | false    |              | Schreibt dokumentübergreifende Eigenschaften in HTML-Meta-Tags. |
| ExportWorksheetProperties       | Boolean         | true     | false    |              | Schreibt arbeitsblattübergreifende Eigenschaften in HTML. |
| ExportWorkbookProperties        | Boolean         | true     | false    |              | Schreibt arbeitsmappenübergreifende Eigenschaften in HTML. |
| ExportFrameScriptsAndProperties | Boolean         | true     | false    |              | Schließt Skripte und Eigenschaften für Frames ein.    |
| AttachedFilesDirectory          | Zeichenfolge    | true     | false    |              | Verzeichnispfad für angehängte Dateien.               |
| AttachedFilesUrlPrefix          | Zeichenfolge    | true     | false    |              | URL-Präfix für angehängte Dateien.                    |
| Encoding                        | Zeichenfolge    | true     | false    |              | Zeichenkodierung für die HTML-Datei.                  |
| ExportActiveWorksheetOnly       | Boolean         | true     | false    |              | Exportiert nur das aktive Arbeitsblatt.               |
| ExportChartImageFormat          | Zeichenfolge    | true     | false    |              | Bildformat für eingebettete Diagramme.                |
| ExportImagesAsBase64            | Boolean         | true     | false    |              | Kodiert Bilder als Base64-Zeichenfolgen.              |
| HiddenColDisplayType            | Zeichenfolge    | true     | false    |              | Gibt an, wie ausgeblendete Spalten angezeigt werden.  |
| HiddenRowDisplayType            | Zeichenfolge    | true     | false    |              | Gibt an, wie ausgeblendete Zeilen angezeigt werden.   |
| HtmlCrossStringType             | Zeichenfolge    | true     | false    |              | Bestimmt, wie Kreuzzeichenfolgen-Daten gerendert werden. |
| IsExpImageToTempDir             | Boolean         | true     | false    |              | Exportiert Bilder in ein temporäres Verzeichnis.      |
| PageTitle                       | Zeichenfolge    | true     | false    |              | Titel für die generierte HTML-Seite.                  |
| ParseHtmlTagInCell              | Boolean         | true     | false    |              | Analysiert HTML-Tags in Zellwerten.                   |
| CellNameAttribute               | Zeichenfolge    | true     | false    |              | Attributname, der den Zellverweis enthält.            |
| SaveFormat                      | Zeichenfolge    | true     | false    |              | Bezeichner des HTML-Dateiformats.                     |
| CachedFileFolder                | Zeichenfolge    | true     | false    |              | Ordner für temporäre Zwischengespeicherte Dateien.    |
| ClearData                       | Boolean         | true     | false    |              | Löscht vorhandene Daten vor dem Speichern.            |
| CreateDirectory                 | Boolean         | true     | false    |              | Erstellt das Zielverzeichnis, falls es nicht existiert. |
| EnableHttpCompression           | Boolean         | true     | false    |              | Aktiviert HTTP-Komprimierung für die Antwort.         |
| RefreshChartCache               | Boolean         | true     | false    |              | Aktualisiert zwischengespeicherte Diagrammdaten vor dem Speichern. |
| SortNames                       | Boolean         | true     | false    |              | Sortiert benannte Bereiche alphabetisch.              |
| ValidateMergedAreas             | Boolean         | true     | false    |              | Überprüft verbundene Zellen auf Konsistenz.           |
| MergeAreas                      | Boolean         | true     | false    |              | Vereint benachbarte Zellen, wo möglich.               |
| SortExternalNames               | Boolean         | true     | false    |              | Sortiert externe benannte Verweise.                   |
| CheckExcelRestriction           | Boolean         | true     | false    |              | Erzwingt Excel-spezifische Grenzwerte während der Konvertierung. |
| UpdateSmartArt                  | Boolean         | true     | false    |              | Aktualisiert SmartArt-Objekte auf die neueste Version. |
| EncryptDocumentProperties       | Boolean         | true     | false    |              | Verschlüsselt Dokumenteigenschaften in der Ausgabedatei. |

## ImageSaveOptions-Eigenschaften

| Eigenschaftsname          | Eigenschaftstyp | Nullable | ReadOnly | Standardwert | Beschreibung                                        |
| ------------------------- | --------------- | -------- | -------- | ------------ | --------------------------------------------------- |
| ChartImageType            | Zeichenfolge    | true     | false    |              | Bildformat für die Diagrammwiedergabe.              |
| EmbeddedImageNameInSvg    | Zeichenfolge    | true     | false    |              | Name für eingebettete Bilder in SVG-Ausgaben.       |
| HorizontalResolution      | Integer         | true     | false    |              | Horizontale DPI der exportierten Bilddatei.         |
| ImageFormat               | Zeichenfolge    | true     | false    |              | Zielbildformat (PNG, JPG usw.).                     |
| IsCellAutoFit             | Boolean         | true     | false    |              | Passt Zellinhalte automatisch an die Bildgröße an.  |
| OnePagePerSheet           | Boolean         | true     | false    |              | Rendert jedes Arbeitsblatt auf einer separaten Seite. |
| OnlyArea                  | Boolean         | true     | false    |              | Exportiert nur den definierten Bereich des Arbeitsblattes. |
| PrintingPage              | Zeichenfolge    | true     | false    |              | Seitenaufbau für das Drucken.                       |
| PrintWithStatusDialog     | Boolean         | true     | false    |              | Zeigt einen Statusdialog während des Druckvorgangs an. |
| Quality                   | Integer         | true     | false    |              | Komprimierungsqualität für JPEG-Bilder (0–100).     |
| TiffCompression           | Zeichenfolge    | true     | false    |              | Komprimierungstyp für TIFF-Bilder.                  |
| VerticalResolution        | Integer         | true     | false    |              | Vertikale DPI der exportierten Bilddatei.           |
| SaveFormat                | Zeichenfolge    | true     | false    |              | Bezeichner des Bilddateiformats.                    |
| CachedFileFolder          | Zeichenfolge    | true     | false    |              | Ordner für temporäre Zwischengespeicherte Dateien.  |
| ClearData                 | Boolean         | true     | false    |              | Löscht vorhandene Daten vor dem Speichern.          |
| CreateDirectory           | Boolean         | true     | false    |              | Erstellt das Zielverzeichnis, falls es nicht existiert. |
| EnableHttpCompression     | Boolean         | true     | false    |              | Aktiviert HTTP-Komprimierung für die Antwort.       |
| RefreshChartCache         | Boolean         | true     | false    |              | Aktualisiert zwischengespeicherte Diagrammdaten vor dem Speichern. |
| SortNames                 | Boolean         | true     | false    |              | Sortiert benannte Bereiche alphabetisch.            |
| ValidateMergedAreas       | Boolean         | true     | false    |              | Überprüft verbundene Zellen auf Konsistenz.         |
| MergeAreas                | Boolean         | true     | false    |              | Vereint benachbarte Zellen, wo möglich.             |
| SortExternalNames         | Boolean         | true     | false    |              | Sortiert externe benannte Verweise.                 |
| CheckExcelRestriction     | Boolean         | true     | false    |              | Erzwingt Excel-spezifische Grenzwerte während der Konvertierung. |
| UpdateSmartArt            | Boolean         | true     | false    |              | Aktualisiert SmartArt-Objekte auf die neueste Version. |
| EncryptDocumentProperties | Boolean         | true     | false    |              | Verschlüsselt Dokumenteigenschaften in der Ausgabedatei. |

## JsonSaveOptions-Eigenschaften

| Eigenschaftsname          | Eigenschaftstyp | Nullable | ReadOnly | Standardwert | Beschreibung                                              |
| ------------------------- | --------------- | -------- | -------- | ------------ | --------------------------------------------------------- |
| ExportArea                | Klasse          | true     | false    |              | Definiert den zu exportierenden Arbeitsblattbereich.      |
| HasHeaderRow              | Boolean         | true     | false    |              | Gibt an, ob die erste Zeile Spaltenüberschriften enthält. |
| ExportAsString            | Boolean         | true     | false    |              | Exportiert alle Werte als Zeichenfolgen.                  |
| Indent                    | Zeichenfolge    | true     | false    |              | Zeichenfolge für Einzüge (z. B. zwei Leerzeichen).        |
| SaveFormat                | Zeichenfolge    | true     | false    |              | Bezeichner des JSON-Dateiformats.                         |
| CachedFileFolder          | Zeichenfolge    | true     | false    |              | Ordner für temporäre Zwischengespeicherte Dateien.        |
| ClearData                 | Boolean         | true     | false    |              | Löscht vorhandene Daten vor dem Speichern.                |
| CreateDirectory           | Boolean         | true     | false    |              | Erstellt das Zielverzeichnis, falls es nicht existiert.   |
| EnableHttpCompression     | Boolean         | true     | false    |              | Aktiviert HTTP-Komprimierung für die Antwort.             |
| RefreshChartCache         | Boolean         | true     | false    |              | Aktualisiert zwischengespeicherte Diagrammdaten vor dem Speichern. |
| SortNames                 | Boolean         | true     | false    |              | Sortiert benannte Bereiche alphabetisch.                  |
| ValidateMergedAreas       | Boolean         | true     | false    |              | Überprüft verbundene Zellen auf Konsistenz.               |
| MergeAreas                | Boolean         | true     | false    |              | Vereint benachbarte Zellen, wo möglich.                   |
| SortExternalNames         | Boolean         | true     | false    |              | Sortiert externe benannte Verweise.                       |
| CheckExcelRestriction     | Boolean         | true     | false    |              | Erzwingt Excel-spezifische Grenzwerte während der Konvertierung. |
| UpdateSmartArt            | Boolean         | true     | false    |              | Aktualisiert SmartArt-Objekte auf die neueste Version.    |
| EncryptDocumentProperties | Boolean         | true     | false    |              | Verschlüsselt Dokumenteigenschaften in der Ausgabedatei.  |

## MarkdownSaveOptions-Eigenschaften

| Eigenschaftsname          | Eigenschaftstyp | Nullable | ReadOnly | Standardwert | Beschreibung                                                  |
| ------------------------- | --------------- | -------- | -------- | ------------ | ------------------------------------------------------------- |
| Encoding                  | Zeichenfolge    | true     | false    |              | Zeichenkodierung für die Markdown-Datei.                      |
| FormatStrategy            | Zeichenfolge    | true     | false    |              | Strategie zur Formatierung von Markdown (z. B. GitHub, CommonMark). |
| LineSeparator             | Zeichenfolge    | true     | false    |              | Zeilenumbruchzeichen (mehrere Zeichen möglich).                |
| SaveFormat                | Zeichenfolge    | true     | false    |              | Bezeichner des Markdown-Dateiformats.                         |
| CachedFileFolder          | Zeichenfolge    | true     | false    |              | Ordner für temporäre Zwischengespeicherte Dateien.            |
| ClearData                 | Boolean         | true     | false    |              | Löscht vorhandene Daten vor dem Speichern.                    |
| CreateDirectory           | Boolean         | true     | false    |              | Erstellt das Zielverzeichnis, falls es nicht existiert.       |
| EnableHttpCompression     | Boolean         | true     | false    |              | Aktiviert HTTP-Komprimierung für die Antwort.                 |
| RefreshChartCache         | Boolean         | true     | false    |              | Aktualisiert zwischengespeicherte Diagrammdaten vor dem Speichern. |
| SortNames                 | Boolean         | true     | false    |              | Sortiert benannte Bereiche alphabetisch.                      |
| ValidateMergedAreas       | Boolean         | true     | false    |              | Überprüft verbundene Zellen auf Konsistenz.                   |
| MergeAreas                | Boolean         | true     | false    |              | Vereint benachbarte Zellen, wo möglich.                       |
| SortExternalNames         | Boolean         | true     | false    |              | Sortiert externe benannte Verweise.                           |
| CheckExcelRestriction     | Boolean         | true     | false    |              | Erzwingt Excel-spezifische Grenzwerte während der Konvertierung. |
| UpdateSmartArt            | Boolean         | true     | false    |              | Aktualisiert SmartArt-Objekte auf die neueste Version.        |
| EncryptDocumentProperties | Boolean         | true     | false    |              | Verschlüsselt Dokumenteigenschaften in der Ausgabedatei.      |

## OoxmlSaveOptions-Eigenschaften

| Eigenschaftsname          | Eigenschaftstyp | Nullable | ReadOnly | Standardwert | Beschreibung                                          |
| ------------------------- | --------------- | -------- | -------- | ------------ | ----------------------------------------------------- |
| ExportCellName            | Boolean         | true     | false    |              | Schließt Zellennamen in die exportierte Datei ein.    |
| UpdateZoom                | Boolean         | true     | false    |              | Aktualisiert den Zoomfaktor im Ausgabedokument.       |
| EnableZip64               | Boolean         | true     | false    |              | Aktiviert ZIP64-Erweiterungen für große Dateien.      |
| EmbedOoxmlAsOleObject     | Boolean         | true     | false    |              | Integriert OOXML als OLE-Objekt.                      |
| CompressionType           | Zeichenfolge    | true     | false    |              | Art der angewendeten Komprimierung (z. B. Normal, Maximum). |
| SaveFormat                | Zeichenfolge    | true     | false    |              | Bezeichner des OOXML-Dateiformats.                    |
| CachedFileFolder          | Zeichenfolge    | true     | false    |              | Ordner für temporäre Zwischengespeicherte Dateien.    |
| ClearData                 | Boolean         | true     | false    |              | Löscht vorhandene Daten vor dem Speichern.            |
| CreateDirectory           | Boolean         | true     | false    |              | Erstellt das Zielverzeichnis, falls es nicht existiert. |
| EnableHttpCompression     | Boolean         | true     | false    |              | Aktiviert HTTP-Komprimierung für die Antwort.         |
| RefreshChartCache         | Boolean         | true     | false    |              | Aktualisiert zwischengespeicherte Diagrammdaten vor dem Speichern. |
| SortNames                 | Boolean         | true     | false    |              | Sortiert benannte Bereiche alphabetisch.              |
| ValidateMergedAreas       | Boolean         | true     | false    |              | Überprüft verbundene Zellen auf Konsistenz.           |
| MergeAreas                | Boolean         | true     | false    |              | Vereint benachbarte Zellen, wo möglich.               |
| SortExternalNames         | Boolean         | true     | false    |              | Sortiert externe benannte Verweise.                   |
| CheckExcelRestriction     | Boolean         | true     | false    |              | Erzwingt Excel-spezifische Grenzwerte während der Konvertierung. |
| UpdateSmartArt            | Boolean         | true     | false    |              | Aktualisiert SmartArt-Objekte auf die neueste Version. |
| EncryptDocumentProperties | Boolean         | true     | false    |              | Verschlüsselt Dokumenteigenschaften in der Ausgabedatei. |

## PclSaveOptions-Eigenschaften

| Eigenschaftsname          | Eigenschaftstyp | Nullable | ReadOnly | Standardwert | Beschreibung                                        |
| ------------------------- | --------------- | -------- | -------- | ------------ | --------------------------------------------------- |
| fontFullName              | Zeichenfolge    | true     | false    |              | Vollständiger Name der zu verwendenden Schriftart.  |
| fontPclName               | Zeichenfolge    | true     | false    |              | PCL-spezifischer Schriftartname.                    |
| SaveFormat                | Zeichenfolge    | true     | false    |              | Bezeichner des PCL-Dateiformats.                    |
| CachedFileFolder          | Zeichenfolge    | true     | false    |              | Ordner für temporäre Zwischengespeicherte Dateien.  |
| ClearData                 | Boolean         | true     | false    |              | Löscht vorhandene Daten vor dem Speichern.          |
| CreateDirectory           | Boolean         | true     | false    |              | Erstellt das Zielverzeichnis, falls es nicht existiert. |
| EnableHttpCompression     | Boolean         | true     | false    |              | Aktiviert HTTP-Komprimierung für die Antwort.       |
| RefreshChartCache         | Boolean         | true     | false    |              | Aktualisiert zwischengespeicherte Diagrammdaten vor dem Speichern. |
| SortNames                 | Boolean         | true     | false    |              | Sortiert benannte Bereiche alphabetisch.            |
| ValidateMergedAreas       | Boolean         | true     | false    |              | Überprüft verbundene Zellen auf Konsistenz.         |
| MergeAreas                | Boolean         | true     | false    |              | Vereint benachbarte Zellen, wo möglich.             |
| SortExternalNames         | Boolean         | true     | false    |              | Sortiert externe benannte Verweise.                 |
| CheckExcelRestriction     | Boolean         | true     | false    |              | Erzwingt Excel-spezifische Grenzwerte während der Konvertierung. |
| UpdateSmartArt            | Boolean         | true     | false    |              | Aktualisiert SmartArt-Objekte auf die neueste Version. |
| EncryptDocumentProperties | Boolean         | true     | false    |              | Verschlüsselt Dokumenteigenschaften in der Ausgabedatei. |

## PDFSaveOptions-Eigenschaften

| Eigenschaftsname          | Eigenschaftstyp | Nullable | ReadOnly | Standardwert | Beschreibung                                          |
| ------------------------- | --------------- | -------- | -------- | ------------ | ----------------------------------------------------- |
| DisplayDocTitle           | Boolean         | true     | false    |              | Verwendet den Dokumenttitel als PDF-Titel.           |
| ExportDocumentStructure   | Boolean         | true     | false    |              | Behält die logische Dokumentstruktur bei.            |
| EmfRenderSetting          | Zeichenfolge    | true     | false    |              | Einstellungen für die EMF-Bildwiedergabe.            |
| CustomPropertiesExport    | Zeichenfolge    | true     | false    |              | Steuert den Export benutzerdefinierter Dokumenteigenschaften. |
| OptimizationType          | Zeichenfolge    | true     | false    |              | Art der PDF-Optimierung (z. B. Größe, Geschwindigkeit). |
| Producer                  | Zeichenfolge    | true     | false    |              | Name der PDF-Erstellungsanwendung.                   |
| PDFCompression            | Zeichenfolge    | true     | false    |              | Komprimierungsalgorithmus für PDF-Streams.           |
| FontEncoding              | Zeichenfolge    | true     | false    |              | Kodierung für eingebettete Schriftarten.             |
| Watermark                 | Klasse          | true     | false    |              | Wasserzeichen-Einstellungen für das PDF.             |
| CalculateFormula          | Boolean         | true     | false    |              | Berechnet Formeln vor dem Export.                    |
| CheckFontCompatibility    | Boolean         | true     | false    |              | Überprüft Schriftartkompatibilität für PDF-Wiedergabe. |
| Compliance                | Zeichenfolge    | true     | false    |              | PDF/A- oder PDF/X-Konformitätsstufe.                  |
| DefaultFont               | Zeichenfolge    | true     | false    |              | Schriftart, die verwendet wird, wenn eine Quellschriftart nicht verfügbar ist. |
| OnePagePerSheet           | Boolean         | true     | false    |              | Platziert jedes Arbeitsblatt auf einer separaten PDF-Seite. |
| PrintingPageType          | Zeichenfolge    | true     | false    |              | Gibt den Seitentyp für das Drucken an.                |
| SecurityOptions           | Klasse          | true     | false    |              | Sicherheitseinstellungen wie Passwörter und Berechtigungen. |
| desiredPPI                | Integer         | true     | false    |              | Gewünschte Bildschirmauflösung in DPI.               |
| jpegQuality               | Integer         | true     | false    |              | JPEG-Bildqualität (0–100).                           |
| ImageType                 | Zeichenfolge    | true     | false    |              | Bildtyp für die Rasterung.                           |
| SaveFormat                | Zeichenfolge    | true     | false    |              | Bezeichner des PDF-Dateiformats.                     |
| CachedFileFolder          | Zeichenfolge    | true     | false    |              | Ordner für temporäre Zwischengespeicherte Dateien.    |
| ClearData                 | Boolean         | true     | false    |              | Löscht vorhandene Daten vor dem Speichern.            |
| CreateDirectory           | Boolean         | true     | false    |              | Erstellt das Zielverzeichnis, falls es nicht existiert. |
| EnableHttpCompression     | Boolean         | true     | false    |              | Aktiviert HTTP-Komprimierung für die Antwort.         |
| RefreshChartCache         | Boolean         | true     | false    |              | Aktualisiert zwischengespeicherte Diagrammdaten vor dem Speichern. |
| SortNames                 | Boolean         | true     | false    |              | Sortiert benannte Bereiche alphabetisch.              |
| ValidateMergedAreas       | Boolean         | true     | false    |              | Überprüft verbundene Zellen auf Konsistenz.           |
| MergeAreas                | Boolean         | true     | false    |              | Vereint benachbarte Zellen, wo möglich.               |
| SortExternalNames         | Boolean         | true     | false    |              | Sortiert externe benannte Verweise.                   |
| CheckExcelRestriction     | Boolean         | true     | false    |              | Erzwingt Excel-spezifische Grenzwerte während der Konvertierung. |
| UpdateSmartArt            | Boolean         | true     | false    |              | Aktualisiert SmartArt-Objekte auf die neueste Version. |
| EncryptDocumentProperties | Boolean         | true     | false    |              | Verschlüsselt Dokumenteigenschaften in der Ausgabedatei. |

## PptxSaveOptions-Eigenschaften

| Eigenschaftsname                  | Eigenschaftstyp | Nullable | ReadOnly | Standardwert | Beschreibung                                            |
| --------------------------------- | --------------- | -------- | -------- | ------------ | ------------------------------------------------------- |
| IgnoreHiddenRows                  | Boolean         | true     | false    |              | Überspringt ausgeblendete Zeilen beim Export.           |
| AdjustFontSizeForRowType          | Zeichenfolge    | true     | false    |              | Steuert die Schriftgradanpassung basierend auf Zeilentyp. |
| ExportViewType                    | Zeichenfolge    | true     | false    |              | Bestimmt, welche Ansicht (Folie, Notizen) exportiert wird. |
| DefaultFont                       | Zeichenfolge    | true     | false    |              | Schriftart, die verwendet wird, wenn eine Quellschriftart nicht verfügbar ist. |
| CheckWorkbookDefaultFont          | Boolean         | true     | false    |              | Überprüft, ob die Standardarbeitsmappenschriftart angewendet wird. |
| CheckFontCompatibility            | Boolean         | true     | false    |              | Überprüft Schriftartkompatibilität für das Zielformat.  |
| IsFontSubstitutionCharGranularity | Boolean         | true     | false    |              | Steuert zeichenbasierte Schriftartersatzfunktion.       |
| OnePagePerSheet                   | Boolean         | true     | false    |              | Platziert jedes Arbeitsblatt auf einer separaten Folie. |
| AllColumnsInOnePagePerSheet       | Boolean         | true     | false    |              | Passt alle Spalten eines Blattes auf eine Folie.        |
| IgnoreError                       | Boolean         | true     | false    |              | Ignoriert nicht-kritische Fehler während der Konvertierung. |
| OutputBlankPageWhenNothingToPrint | Boolean         | true     | false    |              | Erzeugt eine leere Folie, wenn nichts gerendert werden soll. |
| PageIndex                         | Integer         | true     | false    |              | Index der ersten zu exportierenden Folie.              |
| PageCount                         | Integer         | true     | false    |              | Anzahl der zu exportierenden Folien.                    |
| PrintingPageType                  | Zeichenfolge    | true     | false    |              | Gibt den Seitentyp für das Drucken an.                  |
| GridlineType                      | Zeichenfolge    | true     | false    |              | Bestimmt, wie Gitterlinien gerendert werden.            |
| TextCrossType                     | Zeichenfolge    | true     | false    |              | Definiert den Kreuztyp für die Textwiedergabe.          |
| DefaultEditLanguage               | Zeichenfolge    | true     | false    |              | Standardsprache für die Textbearbeitung.               |
| EmfRenderSetting                  | Zeichenfolge    | true     | false    |              | Einstellungen für die EMF-Wiedergabe.                   |
| MergeAreas                        | Boolean         | true     | false    |              | Vereint benachbarte Zellen, wo möglich.                 |
| SortExternalNames                 | Boolean         | true     | false    |              | Sortiert externe benannte Verweise.                     |
| UpdateSmartArt                    | Boolean         | true     | false    |              | Aktualisiert SmartArt-Objekte auf die neueste Version.  |
| SaveFormat                        | Zeichenfolge    | true     | false    |              | Bezeichner des PPTX-Dateiformats.                       |
| CachedFileFolder                  | Zeichenfolge    | true     | false    |              | Ordner für temporäre Zwischengespeicherte Dateien.      |
| ClearData                         | Boolean         | true     | false    |              | Löscht vorhandene Daten vor dem Speichern.              |
| CreateDirectory                   | Boolean         | true     | false    |              | Erstellt das Zielverzeichnis, falls es nicht existiert. |
| EnableHttpCompression             | Boolean         | true     | false    |              | Aktiviert HTTP-Komprimierung für die Antwort.           |
| RefreshChartCache                 | Boolean         | true     | false    |              | Aktualisiert zwischengespeicherte Diagrammdaten vor dem Speichern. |
| SortNames                         | Boolean         | true     | false    |              | Sortiert benannte Bereiche alphabetisch.                |
| ValidateMergedAreas               | Boolean         | true     | false    |              | Überprüft verbundene Zellen auf Konsistenz.             |
| CheckExcelRestriction             | Boolean         | true     | false    |              | Erzwingt Excel-spezifische Grenzwerte während der Konvertierung. |
| EncryptDocumentProperties         | Boolean         | true     | false    |              | Verschlüsselt Dokumenteigenschaften in der Ausgabedatei. |

## SqlScriptSaveOptions-Eigenschaften

| Eigenschaftsname          | Eigenschaftstyp | Nullable | ReadOnly | Standardwert | Beschreibung                                              |
| ------------------------- | --------------- | -------- | -------- | ------------ | --------------------------------------------------------- |
| CheckIfTableExists        | Boolean         | true     | false    |              | Überprüft, ob die Zieltabelle bereits existiert.          |
| ColumnTypeMap             | Zeichenfolge    | true     | false    |              | Zuordnung von Spaltennamen zu SQL-Datentypen.             |
| CheckAllDataForColumnType | Boolean         | true     | false    |              | Scannt alle Zeilen, um Spaltentypen abzuleiten.            |
| AddBlankLineBetweenRows   | Boolean         | true     | false    |              | Fügt eine leere Zeile zwischen generierten Zeilen ein.     |
| Separator                 | Zeichenfolge    | true     | false    |              | Zeichenfolge zur Trennung von Spalten (z. B. Komma, Tab). |
| OperatorType              | Zeichenfolge    | true     | false    |              | SQL-Operator (INSERT, UPDATE usw.).                       |
| PrimaryKey                | Integer         | true     | false    |              | Spaltenindex, der als Primärschlüssel fungiert.           |
| CreateTable               | Boolean         | true     | false    |              | Erzeugt eine CREATE TABLE-Anweisung.                      |
| IdName                    | Zeichenfolge    | true     | false    |              | Name der Bezeichnerspalte.                                |
| StartId                   | Integer         | true     | false    |              | Startwert für automatisch erhöhte IDs.                    |
| TableName                 | Zeichenfolge    | true     | false    |              | Name der Ziel-Datenbanktabelle.                           |
| ExportAsString            | Boolean         | true     | false    |              | Exportiert alle Werte als Zeichenfolgen.                  |
| ExportArea                | Klasse          | true     | false    |              | Definiert den zu exportierenden Arbeitsblattbereich.      |
| HasHeaderRow              | Boolean         | true     | false    |              | Gibt an, ob die erste Zeile Spaltenüberschriften enthält. |
| SaveFormat                | Zeichenfolge    | true     | false    |              | Bezeichner der SQL-Skriptdatei.                           |
| CachedFileFolder          | Zeichenfolge    | true     | false    |              | Ordner für temporäre Zwischengespeicherte Dateien.        |
| ClearData                 | Boolean         | true     | false    |              | Löscht vorhandene Daten vor dem Speichern.                |
| CreateDirectory           | Boolean         | true     | false    |              | Erstellt das Zielverzeichnis, falls es nicht existiert.   |
| EnableHttpCompression     | Boolean         | true     | false    |              | Aktiviert HTTP-Komprimierung für die Antwort.             |
| RefreshChartCache         | Boolean         | true     | false    |              | Aktualisiert zwischengespeicherte Diagrammdaten vor dem Speichern. |
| SortNames                 | Boolean         | true     | false    |              | Sortiert benannte Bereiche alphabetisch.                  |
| ValidateMergedAreas       | Boolean         | true     | false    |              | Überprüft verbundene Zellen auf Konsistenz.               |
| MergeAreas                | Boolean         | true     | false    |              | Vereint benachbarte Zellen, wo möglich.                   |
| SortExternalNames         | Boolean         | true     | false    |              | Sortiert externe benannte Verweise.                       |
| CheckExcelRestriction     | Boolean         | true     | false    |              | Erzwingt Excel-spezifische Grenzwerte während der Konvertierung. |
| UpdateSmartArt            | Boolean         | true     | false    |              | Aktualisiert SmartArt-Objekte auf die neueste Version.    |
| EncryptDocumentProperties | Boolean         | true     | false    |              | Verschlüsselt Dokumenteigenschaften in der Ausgabedatei.  |

## SvgSaveOptions-Eigenschaften

| Eigenschaftsname          | Eigenschaftstyp | Nullable | ReadOnly | Standardwert | Beschreibung                                        |
| ------------------------- | --------------- | -------- | -------- | ------------ | --------------------------------------------------- |
| SheetIndex                | Integer         | true     | false    |              | Index des zu exportierenden Arbeitsblattes.        |
| ChartImageType            | Zeichenfolge    | true     | false    |              | Bildformat für die Diagrammwiedergabe.             |
| EmbeddedImageNameInSvg    | Zeichenfolge    | true     | false    |              | Name für eingebettete Bilder in SVG-Ausgaben.      |
| HorizontalResolution      | Integer         | true     | false    |              | Horizontale DPI des exportierten SVG.              |
| ImageFormat               | Zeichenfolge    | true     | false    |              | Zielbildformat für Rasterelemente.                 |
| IsCellAutoFit             | Boolean         | true     | false    |              | Passt Zellinhalte automatisch an die SVG-Größe an. |
| OnePagePerSheet           | Boolean         | true     | false    |              | Rendert jedes Arbeitsblatt auf einer separaten SVG-Seite. |
| OnlyArea                  | Boolean         | true     | false    |              | Exportiert nur den definierten Bereich des Arbeitsblattes. |
| PrintingPage              | Zeichenfolge    | true     | false    |              | Seitenaufbau für das Drucken.                      |
| PrintWithStatusDialog     | Boolean         | true     | false    |              | Zeigt einen Statusdialog während des Druckvorgangs an. |
| Quality                   | Integer         | true     | false    |              | Komprimierungsqualität für Rasterbilder.           |
| TiffCompression           | Zeichenfolge    | true     | false    |              | Komprimierungstyp für in SVG eingebettete TIFF-Bilder. |
| VerticalResolution        | Integer         | true     | false    |              | Vertikale DPI des exportierten SVG.                |
| SaveFormat                | Zeichenfolge    | true     | false    |              | Bezeichner des SVG-Dateiformats.                   |
| CachedFileFolder          | Zeichenfolge    | true     | false    |              | Ordner für temporäre Zwischengespeicherte Dateien. |
| ClearData                 | Boolean         | true     | false    |              | Löscht vorhandene Daten vor dem Speichern.         |
| CreateDirectory           | Boolean         | true     | false    |              | Erstellt das Zielverzeichnis, falls es nicht existiert. |
| EnableHttpCompression     | Boolean         | true     | false    |              | Aktiviert HTTP-Komprimierung für die Antwort.      |
| RefreshChartCache         | Boolean         | true     | false    |              | Aktualisiert zwischengespeicherte Diagrammdaten vor dem Speichern. |
| SortNames                 | Boolean         | true     | false    |              | Sortiert benannte Bereiche alphabetisch.           |
| ValidateMergedAreas       | Boolean         | true     | false    |              | Überprüft verbundene Zellen auf Konsistenz.        |
| MergeAreas                | Boolean         | true     | false    |              | Vereint benachbarte Zellen, wo möglich.            |
| SortExternalNames         | Boolean         | true     | false    |              | Sortiert externe benannte Verweise.                |
| CheckExcelRestriction     | Boolean         | true     | false    |              | Erzwingt Excel-spezifische Grenzwerte während der Konvertierung. |
| UpdateSmartArt            | Boolean         | true     | false    |              | Aktualisiert SmartArt-Objekte auf die neueste Version. |
| EncryptDocumentProperties | Boolean         | true     | false    |              | Verschlüsselt Dokumenteigenschaften in der Ausgabedatei. |

## TxtSaveOptions-Eigenschaften

| Eigenschaftsname          | Eigenschaftstyp | Nullable | ReadOnly | Standardwert | Beschreibung                                                             |
| ------------------------- | --------------- | -------- | -------- | ------------ | ------------------------------------------------------------------------ |
| QuoteType                 | Zeichenfolge    | true     | false    |              | Art des Zitierens (z. B. doppelt, einfach).                             |
| Separator                 | Zeichenfolge    | true     | false    |              | Spaltentrennzeichen (z. B. Komma, Tab).                                 |
| SeparatorString           | Zeichenfolge    | true     | false    |              | Vollständige Zeichenfolge als Trennzeichen, wenn mehrere Zeichen benötigt werden. |
| AlwaysQuoted              | Boolean         | true     | false    |              | Erzwingt, dass alle Felder in Anführungszeichen stehen.                 |
| SaveFormat                | Zeichenfolge    | true     | false    |              | Bezeichner des TXT-Dateiformats.                                        |
| CachedFileFolder          | Zeichenfolge    | true     | false    |              | Ordner für temporäre Zwischengespeicherte Dateien.                      |
| ClearData                 | Boolean         | true     | false    |              | Löscht vorhandene Daten vor dem Speichern.                              |
| CreateDirectory           | Boolean         | true     | false    |              | Erstellt das Zielverzeichnis, falls es nicht existiert.                |
| EnableHttpCompression     | Boolean         | true     | false    |              | Aktiviert HTTP-Komprimierung für die Antwort.                           |
| RefreshChartCache         | Boolean         | true     | false    |              | Aktualisiert zwischengespeicherte Diagrammdaten vor dem Speichern.      |
| SortNames                 | Boolean         | true     | false    |              | Sortiert benannte Bereiche alphabetisch.                               |
| ValidateMergedAreas       | Boolean         | true     | false    |              | Überprüft verbundene Zellen auf Konsistenz.                             |
| MergeAreas                | Boolean         | true     | false    |              | Vereint benachbarte Zellen, wo möglich.                                 |
| SortExternalNames         | Boolean         | true     | false    |              | Sortiert externe benannte Verweise.                                     |
| CheckExcelRestriction     | Boolean         | true     | false    |              | Erzwingt Excel-spezifische Grenzwerte während der Konvertierung.        |
| UpdateSmartArt            | Boolean         | true     | false    |              | Aktualisiert SmartArt-Objekte auf die neueste Version.                 |
| EncryptDocumentProperties | Boolean         | true     | false    |              | Verschlüsselt Dokumenteigenschaften in der Ausgabedatei.               |

## XlsSaveOptions & XlsbSaveOptions-Eigenschaften

| Eigenschaftsname          | Eigenschaftstyp | Nullable | ReadOnly | Standardwert | Beschreibung                                        |
| ------------------------- | --------------- | -------- | -------- | ------------ | --------------------------------------------------- |
| MatchColor                | Boolean         | true     | false    |              | Behält exakte Zellfarben beim Export bei.          |
| WpsCompatibility          | Boolean         | true     | false    |              | Aktiviert Kompatibilität mit WPS Office.          |
| SaveFormat                | Zeichenfolge    | true     | false    |              | Bezeichner des XLS/XLSB-Dateiformats.              |
| CachedFileFolder          | Zeichenfolge    | true     | false    |              | Ordner für temporäre Zwischengespeicherte Dateien. |
| ClearData                 | Boolean         | true     | false    |              | Löscht vorhandene Daten vor dem Speichern.         |
| CreateDirectory           | Boolean         | true     | false    |              | Erstellt das Zielverzeichnis, falls es nicht existiert. |
| EnableHttpCompression     | Boolean         | true     | false    |              | Aktiviert HTTP-Komprimierung für die Antwort.      |
| RefreshChartCache         | Boolean         | true     | false    |              | Aktualisiert zwischengespeicherte Diagrammdaten vor dem Speichern. |
| SortNames                 | Boolean         | true     | false    |              | Sortiert benannte Bereiche alphabetisch.           |
| ValidateMergedAreas       | Boolean         | true     | false    |              | Überprüft verbundene Zellen auf Konsistenz.        |
| MergeAreas                | Boolean         | true     | false    |              | Vereint benachbarte Zellen, wo möglich.            |
| SortExternalNames         | Boolean         | true     | false    |              | Sortiert externe benannte Verweise.                |
| CheckExcelRestriction     | Boolean         | true     | false    |              | Erzwingt Excel-spezifische Grenzwerte während der Konvertierung. |
| UpdateSmartArt            | Boolean         | true     | false    |              | Aktualisiert SmartArt-Objekte auf die neueste Version. |
| EncryptDocumentProperties | Boolean         | true     | false    |              | Verschlüsselt Dokumenteigenschaften in der Ausgabedatei. |

## XmlSaveOptions-Eigenschaften

| Eigenschaftsname          | Eigenschaftstyp | Nullable | ReadOnly | Standardwert | Beschreibung                                              |
| ------------------------- | --------------- | -------- | -------- | ------------ | --------------------------------------------------------- |
| SheetIndexes              | Array           | true     | false    |              | Liste der Arbeitsblattindizes, die in den Export einbezogen werden sollen. |
| ExportArea                | Klasse          | true     | false    |              | Definiert den zu exportierenden Arbeitsblattbereich.      |
| HasHeaderRow              | Boolean         | true     | false    |              | Gibt an, ob die erste Zeile Spaltenüberschriften enthält. |
| XmlMapName                | Zeichenfolge    | true     | false    |              | Name der auf das Arbeitsblatt angewendeten XML-Mappe.     |
| SheetNameAsElementName    | Boolean         | true     | false    |              | Verwendet den Blattnamen als XML-Elementname.             |
| DataAsAttribute           | Boolean         | true     | false    |              | Exportiert Zelldaten als XML-Attribute statt Elemente.   |
| SaveFormat                | Zeichenfolge    | true     | false    |              | Bezeichner des XML-Dateiformats.                          |
| CachedFileFolder          | Zeichenfolge    | true     | false    |              | Ordner für temporäre Zwischengespeicherte Dateien.        |
| ClearData                 | Boolean         | true     | false    |              | Löscht vorhandene Daten vor dem Speichern.                |
| CreateDirectory           | Zeichenfolge    | true     | false    |              | Erstellt das Zielverzeichnis, falls es nicht existiert.   |
| EnableHttpCompression     | Boolean         | true     | false    |              | Aktiviert HTTP-Komprimierung für die Antwort.             |
| RefreshChartCache         | Boolean         | true     | false    |              | Aktualisiert zwischengespeicherte Diagrammdaten vor dem Speichern. |
| SortNames                 | Boolean         | true     | false    |              | Sortiert benannte Bereiche alphabetisch.                  |
| ValidateMergedAreas       | Boolean         | true     | false    |              | Überprüft verbundene Zellen auf Konsistenz.               |
| MergeAreas                | Boolean         | true     | false    |              | Vereint benachbarte Zellen, wo möglich.                   |
| SortExternalNames         | Boolean         | true     | false    |              | Sortiert externe benannte Verweise.                       |
| CheckExcelRestriction     | Boolean         | true     | false    |              | Erzwingt Excel-spezifische Grenzwerte während der Konvertierung. |
| UpdateSmartArt            | Boolean         | true     | false    |              | Aktualisiert SmartArt-Objekte auf die neueste Version.    |
| EncryptDocumentProperties | Boolean         | true     | false    |              | Verschlüsselt Dokumenteigenschaften in der Ausgabedatei.  |

## XpsSaveOptions-Eigenschaften

| Eigenschaftsname                  | Eigenschaftstyp | Nullable | ReadOnly | Standardwert | Beschreibung                                           |
| --------------------------------- | --------------- | -------- | -------- | ------------ | ------------------------------------------------------ |
| DefaultFont                       | Zeichenfolge    | true     | false    |              | Schriftart, die verwendet wird, wenn eine Quellschriftart nicht verfügbar ist. |
| CheckWorkbookDefaultFont          | Boolean         | true     | false    |              | Überprüft, ob die Standardarbeitsmappenschriftart angewendet wird. |
| CheckFontCompatibility            | Boolean         | true     | false    |              | Überprüft Schriftartkompatibilität für das Zielformat. |
| IsFontSubstitutionCharGranularity | Boolean         | true     | false    |              | Steuert zeichenbasierte Schriftartersatzfunktion.     |
| OnePagePerSheet                   | Boolean         | true     | false    |              | Platziert jedes Arbeitsblatt auf einer separaten XPS-Seite. |
| AllColumnsInOnePagePerSheet       | Boolean         | true     | false    |              | Passt alle Spalten eines Blattes auf eine Seite.     |
| IgnoreError                       | Boolean         | true     | false    |              | Ignoriert nicht-kritische Fehler während der Konvertierung. |
| OutputBlankPageWhenNothingToPrint | Boolean         | true     | false    |              | Erzeugt eine leere Seite, wenn nichts gerendert werden soll. |
| PageIndex                         | Integer         | true     | false    |              | Index der ersten zu exportierenden Seite.            |
| PageCount                         | Integer         | true     | false    |              | Anzahl der zu exportierenden Seiten.                  |
| PrintingPageType                  | Zeichenfolge    | true     | false    |              | Gibt den Seitentyp für das Drucken an.                |
| GridlineType                      | Zeichenfolge    | true     | false    |              | Bestimmt, wie Gitterlinien gerendert werden.          |
| TextCrossType                     | Zeichenfolge    | true     | false    |              | Definiert den Kreuztyp für die Textwiedergabe.        |
| DefaultEditLanguage               | Zeichenfolge    | true     | false    |              | Standardsprache für die Textbearbeitung.             |
| EmfRenderSetting                  | Zeichenfolge    | true     | false    |              | Einstellungen für die EMF-Wiedergabe.                 |
| MergeAreas                        | Boolean         | true     | false    |              | Vereint benachbarte Zellen, wo möglich.               |
| SortExternalNames                 | Boolean         | true     | false    |              | Sortiert externe benannte Verweise.                   |
| UpdateSmartArt                    | Boolean         | true     | false    |              | Aktualisiert SmartArt-Objekte auf die neueste Version. |
| SaveFormat                        | Zeichenfolge    | true     | false    |              | Bezeichner des XPS-Dateiformats.                      |
| CachedFileFolder                  | Zeichenfolge    | true     | false    |              | Ordner für temporäre Zwischengespeicherte Dateien.    |
| ClearData                         | Boolean         | true     | false    |              | Löscht vorhandene Daten vor dem Speichern.            |
| CreateDirectory                   | Boolean         | true     | false    |              | Erstellt das Zielverzeichnis, falls es nicht existiert. |
| EnableHttpCompression             | Boolean         | true     | false    |              | Aktiviert HTTP-Komprimierung für die Antwort.         |
| RefreshChartCache                 | Boolean         | true     | false    |              | Aktualisiert zwischengespeicherte Diagrammdaten vor dem Speichern. |
| SortNames                         | Boolean         | true     | false    |              | Sortiert benannte Bereiche alphabetisch.              |
| ValidateMergedAreas               | Boolean         | true     | false    |              | Überprüft verbundene Zellen auf Konsistenz.           |
| CheckExcelRestriction             | Boolean         | true     | false    |              | Erzwingt Excel-spezifische Grenzwerte während der Konvertierung. |
| EncryptDocumentProperties         | Boolean         | true     | false    |              | Verschlüsselt Dokumenteigenschaften in der Ausgabedatei. |
---