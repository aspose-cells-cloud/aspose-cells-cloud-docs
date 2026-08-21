---
title: "Tabellenkalkulationsoperationen"
second_title: "Dokument"
type: docs
url: /de/spreadsheet-operations/
keywords: "Aspose Cells Cloud, Excel API, Tabellenkalkulationsoperationen, automatische Anpassung, Batch-Verarbeitung, Dateischutz, Konvertierung, Import/Export, Textverarbeitung"
description: "Erfahren Sie, wie Sie Tabellenkalkulationsoperationen wie automatische Anpassung, Batch-Konvertierung, Schutz, Zusammenführung sowie Suchen und Ersetzen mithilfe der Aspose.Cells Cloud REST API durchführen können. Enthält knappe Nutzungshinweise und Codebeispiel-Anleitungen."
weight: 100
ArticleTitle: "Tabellenkalkulationsoperationen – Aspose.Cells Cloud API-Anleitung"
---

Die **Tabellenkalkulationsoperationen** bieten eine knappe Anleitung zu den gängigsten Aktionen, die Sie mit Excel-Arbeitsmappen mithilfe von **Aspose.Cells Cloud** (v3.0) durchführen können. Egal, ob Sie Spaltenbreiten automatisch anpassen, Dateien im Batch-Modus verarbeiten, Arbeitsblätter schützen oder Text manipulieren müssen: Die REST API bietet spezielle Endpunkte, die plattformunabhängig in Sprachen wie Python, C# und Java genutzt werden können. Die nachfolgende Liste verlinkt auf die detaillierte Dokumentation für jede Operation und enthält jeweils kurze Nutzungshinweise, um Ihnen den Einstieg zu erleichtern.

**Voraussetzungen**: Um diese Endpunkte aufzurufen, benötigen Sie einen gültigen API-Schlüssel für Aspose.Cells Cloud und müssen den `Authorization`-Header (`Bearer <access-token>`) angeben. Die Beispiele setzen API-Version v3.0 voraus.

- **[Auto-Fitter-Optionen](/cells/auto-fitter-options/)** – Passt Spaltenbreiten und Zeilenhöhen automatisch an. `POST /cells/{file}/worksheets/{sheet}/autoFitColumns`  
  ```http
  POST https://api.aspose.cloud/v3.0/cells/MyWorkbook.xlsx/worksheets/Sheet1/autoFitColumns
  Authorization: Bearer {access-token}
  Content-Type: application/json

  {
    "autoFitOptions": {
      "autoFitType": "All",
      "autoFitMergedCells": true
    }
  }
  ```
- **[Batch-Verarbeitung von Excel-Dateien: Konvertierung, Sperren, Schutz, Teilen und Entsperren](/cells/batch/)** – Führt Massenaktionen (Konvertieren, Sperren, Schützen, Teilen, Entsperren) für bis zu 100 Dateien pro Anforderung durch. `POST /cells/batch`  
  ```http
  POST https://api.aspose.cloud/v3.0/cells/batch
  Authorization: Bearer {access-token}
  Content-Type: application/json

  {
    "tasks": [
      { "file": "Book1.xlsx", "action": "convert", "format": "pdf" },
      { "file": "Book2.xlsx", "action": "protect", "password": "Secret123" }
    ]
  }
  ```
- **[Excel-Dateien komprimieren und reparieren](/cells/compress-and-repair-excel-files/)** – Reduziert die Dateigröße und behebt strukturelle Probleme. `POST /cells/{file}/compressAndRepair`  
  ```http
  POST https://api.aspose.cloud/v3.0/cells/Report.xlsx/compressAndRepair
  Authorization: Bearer {access-token}
  ```
- **[Excel-Dateien in ein anderes Format konvertieren oder anders speichern](/cells/conversion-and-save-as/)** – Konvertiert Excel in PDF, CSV, HTML usw. oder ändert das Ausgabeformat. `GET /cells/{file}/saveAs`  
  ```http
  GET https://api.aspose.cloud/v3.0/cells/Financials.xlsx/saveAs?format=pdf
  Authorization: Bearer {access-token}
  ```
- **[Optionen für die Arbeitsmappen-Konvertierung](/cells/convert-workbook-options/)** – Feinabstimmung von Konvertierungseinstellungen wie Seitengröße, Rendereinstellungen und Passwortschutz. `POST /cells/{file}/convert`  
  ```http
  POST https://api.aspose.cloud/v3.0/cells/Presentation.xlsx/convert
  Authorization: Bearer {access-token}
  Content-Type: application/json

  {
    "format": "pdf",
    "options": {
      "pageSetup": { "orientation": "landscape" },
      "pdfSaveOptions": { "compressImages": true }
    }
  }
  ```
- **[Excel-Dateien erstellen oder Excel-Berichte generieren](/cells/creating-files-and-reports/)** – Erstellt neue Arbeitsmappen von Grund auf oder auf Basis von Vorlagen. `PUT /cells/{newFile}`  
  ```http
  PUT https://api.aspose.cloud/v3.0/cells/NewReport.xlsx
  Authorization: Bearer {access-token}
  Content-Type: application/json

  {
    "templateFile": "Template.xlsx",
    "dataSource": { "name": "Q1 Umsatz", "value": 12345 }
  }
  ```
- **[Daten in Excel-Dateien importieren und aus Excel-Dateien exportieren](/cells/data-import-and-export/)** – Lädt Daten aus CSV, JSON oder Datenbanken und exportiert Arbeitsblattdaten. `POST /cells/{file}/importData`  
  ```http
  POST https://api.aspose.cloud/v3.0/cells/Orders.xlsx/importData
  Authorization: Bearer {access-token}
  Content-Type: application/json

  {
    "importOptions": {
      "source": "json",
      "jsonData": [{ "OrderId": 1, "Amount": 250.0 }]
    }
  }
  ```
- **[Excel-Dateien verschlüsseln, entschlüsseln und digital signieren](/cells/protect/)** – Wendet Passwortschutz, Verschlüsselung oder digitale Signaturen an. `POST /cells/{file}/encrypt`  
  ```http
  POST https://api.aspose.cloud/v3.0/cells/Sensitive.xlsx/encrypt
  Authorization: Bearer {access-token}
  Content-Type: application/json

  {
    "password": "StrongPass!23",
    "encryptionType": "Standard"
  }
  ```
- **[Dateiinformationen](/cells/file-info/)** – Ruft Metadaten wie Dateigröße, Format und Erstellungsdatum ab. `GET /cells/{file}/info`  
  ```http
  GET https://api.aspose.cloud/v3.0/cells/Archive.xlsx/info
  Authorization: Bearer {access-token}
  ```
- **[Excel-Dateien zusammenführen und teilen](/cells/merge-and-split/)** – Kombiniert mehrere Arbeitsmappen zu einer einzigen oder teilt eine Arbeitsmappe in mehrere Dateien. `POST /cells/merge` / `POST /cells/split`  
  ```http
  POST https://api.aspose.cloud/v3.0/cells/merge
  Authorization: Bearer {access-token}
  Content-Type: application/json

  {
    "files": ["Q1.xlsx", "Q2.xlsx"],
    "outputFile": "FullYear.xlsx"
  }
  ```
- **[Textinhalte in Excel-Dateien suchen und ersetzen](/cells/search-and-replace/)** – Findet und ersetzt Zeichenfolgen über Arbeitsblätter hinweg. `POST /cells/{file}/searchReplace`  
  ```http
  POST https://api.aspose.cloud/v3.0/cells/Report.xlsx/searchReplace
  Authorization: Bearer {access-token}
  Content-Type: application/json

  {
    "text": "Entwurf",
    "newText": "Endgültig",
    "options": { "matchCase": false }
  }
  ```
- **[Excel-Textverarbeitung: Text hinzufügen, Zeichen entfernen, Text kürzen, Groß-/Kleinschreibung ändern und mehr](/cells/text-processing/)** – Führt erweiterte Textmanipulationen an Zellwerten durch. `POST /cells/{file}/textProcessing`  
  ```http
  POST https://api.aspose.cloud/v3.0/cells/Notes.xlsx/textProcessing
  Authorization: Bearer {access-token}
  Content-Type: application/json

  {
    "operations": [
      { "type": "trim", "range": "A1:A10" },
      { "type": "toUpper", "range": "B1:B5" }
    ]
  }
  ```
- **[Wasserzeichen einfügen oder Hintergründe in Excel-Dateien festlegen](/cells/watermark-and-background/)** – Fügt Bild- oder Textwasserzeichen hinzu und legt Arbeitsblatt-Hintergründe fest. `POST /cells/{file}/watermark`  
  ```http
  POST https://api.aspose.cloud/v3.0/cells/Presentation.xlsx/watermark
  Authorization: Bearer {access-token}
  Content-Type: application/json

  {
    "type": "text",
    "text": "Vertraulich",
    "fontSize": 36,
    "color": "FF0000"
  }
  ```
- **[Arbeiten mit Excel-Dateien: Formelberechnung, automatische Anpassung, Objekte löschen usw.](/cells/workbook/)** – Führt gängige Arbeitsmappenaufgaben wie Berechnen von Formeln, Löschen von Objekten und automatische Anpassung aus. `POST /cells/{file}/workbookOperations`  
  ```http
  POST https://api.aspose.cloud/v3.0/cells/Analytics.xlsx/workbookOperations
  Authorization: Bearer {access-token}
  Content-Type: application/json

  {
    "operations": [
      { "type": "calculateFormula" },
      { "type": "clearObjects", "objectType": "charts" }
    ]
  }
  ```
---