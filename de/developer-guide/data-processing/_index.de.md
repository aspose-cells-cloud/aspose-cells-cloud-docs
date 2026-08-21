---
title: "Aspose.Cells Cloud – Zusammenführen, Aufteilen & Importieren von Tabellendaten"
second_title: "Dokument"
ArticleTitle: "Verarbeitung von Tabellendaten – Zusammenführen, Aufteilen & Importieren"
linktitle: "Datenverarbeitung"
type: docs
url: /de/data-processing/
keywords: "Aspose.Cells Cloud, Verarbeitung von Tabellendaten, Excel zusammenführen, Excel aufteilen, CSV-Import, JSON-Import, API"
description: "Detaillierte Anleitung zum Importieren von CSV-/JSON-Daten, zum Zusammenführen entfernter Excel-Arbeitsmappen und zum Aufteilen großer Tabellendateien mithilfe der Aspose.Cells Cloud REST API, einschließlich Beispielanfragen und -antworten."
weight: 30
---

**Aspose.Cells Cloud** – ein REST-basierter Dienst, der die programmgesteuerte Bearbeitung von Excel-Dateien in der Cloud ermöglicht. Er unterstützt den Import von Daten aus verschiedenen Formaten sowie das Zusammenführen und Aufteilen von Arbeitsmappen.

Der Abschnitt **Datenverarbeitung** der Aspose.Cells Cloud API ermöglicht es Ihnen, Tabellendaten programmgesteuert zu importieren, zusammenzuführen und aufzuteilen. Verwenden Sie die unten aufgeführten Endpunkte, um CSV-/JSON-Importe durchzuführen, Arbeitsmappen zu kombinieren oder große Dateien in handhabbare Teile aufzuteilen.

## Datenimport und -verwaltung

- **[Importieren von CSV-, JSON- und XML-Daten in Excel-Dateien](https://docs.aspose.cloud/cells/import-data-into-spreadsheet/)**  

Der Importvorgang akzeptiert CSV-, JSON- oder XML-Payloads und erstellt ein neues Arbeitsblatt (oder aktualisiert ein vorhandenes) in der Zielarbeitsmappe.

**Endpunktdetails**

| HTTP-Methode | Endpunkt | Anforderungstext | Erfolgsantwort |
|-------------|----------|--------------|------------------|
| POST | `https://api.aspose.cloud/v3.0/cells/{fileName}/import` | `application/json` oder `text/csv` (abhängig vom Format) | `200 OK` mit JSON, das Metadaten der aktualisierten Arbeitsmappe enthält |
| GET | `https://api.aspose.cloud/v3.0/cells/{fileName}?format=excel` | *keine* | Gibt die verarbeitete Arbeitsmappendatei zurück |

**Beispiel-cURL-Anfrage (CSV-Import)**

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/MyWorkbook.xlsx/import" \
     -H "Authorization: Bearer {access_token}" \
     -H "Content-Type: text/csv" \
     --data-binary @data.csv
```

**Beispiel-JSON-Antwort**

```json
{
  "Code": 200,
  "Status": "OK",
  "Workbook": {
    "FileName": "MyWorkbook.xlsx",
    "Worksheets": 3
  }
}
```

> **Voraussetzungen**: Ein OAuth2-Zugriffstoken ist erforderlich. Die Quelldatei muss sich im Aspose-Cloud-Speicher befinden oder über einen Multipart-Upload bereitgestellt werden.

## Dateizusammenführungsoperation

- **[Zusammenführen entfernter Excel-Dateien in einer angegebenen Arbeitsmappe](https://docs.aspose.cloud/cells/merge-remote-spreadsheet/)**
- **[Zusammenführen mehrerer Excel-Dateien in einer einzigen Arbeitsmappe](https://docs.aspose.cloud/cells/merge-spreadsheets/)**
- **[Zusammenführen von Excel-Dateien, die in einem entfernten Ordner übereinstimmen](https://docs.aspose.cloud/cells/merge-spreadsheets-in-remote-folder/)**  

Beim Zusammenführen werden zwei oder mehr Arbeitsmappen in einer einzigen Zielarbeitsmappe kombiniert. Die API unterstützt sowohl explizite Dateilisten als auch musterbasierte Zusammenführungen innerhalb eines Speicherordners.

**Endpunktdetails**

| HTTP-Methode | Endpunkt | Parameter | Erfolgsantwort |
|-------------|----------|------------|------------------|
| POST | `https://api.aspose.cloud/v3.0/cells/merge` | `files` (Array von Dateinamen), `target` (optionaler Name der Zielarbeitsmappe) | `200 OK` mit JSON, das die zusammengeführte Arbeitsmappe beschreibt |
| POST | `https://api.aspose.cloud/v3.0/cells/merge/remote` | `sourceFolder`, `pattern`, `target` | `200 OK` mit Metadaten der zusammengeführten Arbeitsmappe |

**Beispiel-cURL-Anfrage (Zusammenführen einer expliziten Liste)**

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/merge" \
     -H "Authorization: Bearer {access_token}" \
     -H "Content-Type: application/json" \
     -d '{
           "files": ["Book1.xlsx", "Book2.xlsx"],
           "target": "Combined.xlsx"
         }'
```

**Beispiel-JSON-Antwort**

```json
{
  "Code": 200,
  "Status": "OK",
  "MergedWorkbook": {
    "FileName": "Combined.xlsx",
    "Worksheets": 10
  }
}
```

> **Voraussetzungen**: Alle Quellarbeitsmappen müssen sich am gleichen Cloud-Speicherort befinden, und der Aufrufer muss Lese-/Schreibberechtigungen besitzen.

## Dateiaufteilungsoperation

- **[Aufteilen einer Excel-Datei in mehrere Dateien basierend auf Arbeitsblättern](https://docs.aspose.cloud/cells/split-remote-spreadsheet/)**
- **[Aufteilen einer Excel-Datei gemäß benutzerdefinierten Regeln](https://docs.aspose.cloud/cells/split-spreadsheet/)**  

Beim Aufteilen werden einzelne Arbeitsblätter oder Gruppen von Zeilen/Spalten in separate Arbeitsmappendateien extrahiert.

**Endpunktdetails**

| HTTP-Methode | Endpunkt | Parameter | Erfolgsantwort |
|-------------|----------|------------|------------------|
| POST | `https://api.aspose.cloud/v3.0/cells/{fileName}/split` | `splitBy` (z. B. `worksheet`), `outputFolder` | `200 OK` mit Liste der erzeugten Datei-URLs |
| POST | `https://api.aspose.cloud/v3.0/cells/{fileName}/split/custom` | Benutzerdefinierte Regel als JSON (Seitengröße, Zeilenbereich usw.) | `200 OK` mit Details der aufgeteilten Dateien |

**Beispiel-cURL-Anfrage (Aufteilen nach Arbeitsblatt)**

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/BigReport.xlsx/split" \
     -H "Authorization: Bearer {access_token}" \
     -H "Content-Type: application/json" \
     -d '{
           "splitBy": "worksheet",
           "outputFolder": "Splits/"
         }'
```

**Beispiel-JSON-Antwort**

```json
{
  "Code": 200,
  "Status": "OK",
  "Splits": [
    {"FileName": "BigReport_Sheet1.xlsx", "Url": "https://storage.aspose.cloud/..."},
    {"FileName": "BigReport_Sheet2.xlsx", "Url": "https://storage.aspose.cloud/..."}
  ]
}
```

> **Voraussetzungen**: Die Quellarbeitsmappe muss im Aspose-Cloud-Speicher zugänglich sein, und der Aufrufer benötigt Schreibberechtigung für den Zielordner.