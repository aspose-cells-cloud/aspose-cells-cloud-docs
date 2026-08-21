---
title: "Aspose.Cells Cloud Data Import API – Eine Cloud-Lösung zum automatischen Importieren von CSV-, JSON- und XML-Daten in Excel-Arbeitsmappen."
second_title: "Dokument"
ArticleTitle: "Multi-Source-Datenintegrations-Excel-Plattform – Aspose.Cells Cloud API für automatisierten Datenimport und -transformation."
linktitle: "Daten in Arbeitsmappe importieren"
type: docs
url: /import-data-into-spreadsheet/
keywords: "Aspose Cells, Datenimport-API, CSV nach Excel, JSON nach Excel, XML nach Excel, Cloud-Arbeitsmappe, REST-API"
description: "Importieren Sie CSV-, JSON- oder XML-Daten in Excel-Arbeitsmappen mit der Aspose.Cells Cloud REST API. Erfahren Sie mehr über das Anfrageformat, Parameter, Beispiel-SDK-Code und Fehlerbehandlung."
weight: 100
---

## Kernfunktionen

### Unterstützung mehrerer Datenformate

- **<a href="https://docs.fileformat.com/spreadsheet/csv/" rel="noopener noreferrer">CSV</a>-Datenimport**: Unterstützt verschiedene Trennzeichen und erkennt automatisch die Kodierung.
- **<a href="https://docs.fileformat.com/web/json/" rel="noopener noreferrer">JSON</a>-Datenverarbeitung**: Wandelt komplexe JSON-Strukturen in Excel-Tabellen um.
- **<a href="https://docs.fileformat.com/web/xml/" rel="noopener noreferrer">XML</a>-Dateikonvertierung**: Ordnet Knotendaten der Excel-Zeilen- und Spaltenstruktur zu.

## **API-Beschreibung: Daten in Arbeitsmappe importieren**

### Web-API

```http
PUT https://api.aspose.cloud/v4.0/cells/import/data
```

### **Sicherheit und Authentifizierung**

Die Aspose.Cells Cloud APIs sind sicher und erfordern eine <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-Token-basierte Authentifizierung</a>.

### Anfrageparameter

| Parametername      | Typ    | Standort           | Beschreibung                                                                 |
| ------------------ | ------ | ------------------ | ---------------------------------------------------------------------------- |
| datafile           | Datei  | FormData           | Die zu importierende Datendatei (CSV, JSON oder XML).                       |
| spreadsheet        | Datei  | FormData           | Die Ziel-Arbeitsmappe, in die die importierten Daten eingefügt werden.      |
| worksheet          | string | Query              | Name des Arbeitsblatts, in dem die Daten platziert werden sollen.           |
| startCell          | string | Query              | Obere linke Zelle (z. B. `A1`), die die Startposition für den Import markiert. |
| insert             | bool   | Query              | `true`, um Zeilen einzufügen; `false`, um vorhandene Daten zu überschreiben. |
| convertNumericData | bool   | Query              | `true`, um numerische Zeichenfolgen beim Import in Zahlen umzuwandeln.      |
| splitter           | string | Query              | Einzelnes Zeichen als CSV-Trennzeichen (Standard: `,`).                     |
| outPath            | string | Query (optional)   | Ordnerpfad, in dem die aktualisierte Arbeitsmappe gespeichert wird.         |
| outStorageName     | string | Query (optional)   | Name des Speicherorts für die Ausgabedatei.                                 |
| fontsLocation      | string | Query (optional)   | Pfad zu einem benutzerdefinierten Schriftartenordner, falls erforderlich.   |
| region             | string | Query (optional)   | Regionalkonfiguration der Arbeitsmappe (z. B. `de-DE`).                     |
| password           | string | Query (optional)   | Passwort zum Öffnen einer geschützten Arbeitsmappe.                         |

### Antwort

```json
[
  {
    "Name": "ResponseFile",
    "DataType": {
      "Identifier": "File",
      "Reference": "Stream"
    }
  }
]
```

**HTTP-Statuscodes**

| Code | Bedeutung             | Beschreibung                                                          |
| ---- | --------------------- | --------------------------------------------------------------------- |
| 200  | OK                    | Filter erfolgreich angewendet; Antwort enthält Vorgangsdetails.      |
| 400  | Bad Request           | Fehlende oder ungültige Parameter (z. B. nicht unterstützter Dateityp). |
| 401  | Unauthorized          | Ungültiges oder fehlendes JWT-Token.                                  |
| 413  | Payload Too Large     | Die hochgeladene Datei überschreitet die Größenbeschränkung.         |
| 500  | Internal Server Error | Unerwarteter Serverfehler.                                            |

## Warum Sie diese API verwenden sollten

- **Effizientes Laden von Daten** – Ermöglicht den Bulk-Import großer Datensätze direkt in eine Arbeitsmappe, ohne Zwischendateien zu erstellen.
- **Breite SDK-Unterstützung** – Bietet Client-Bibliotheken für .NET, Java, PHP, Ruby, Node.js, Python, Go und Perl zur vereinfachten Integration.
- **In-Memory-Verarbeitung** – Führt Transformationen im Speicher durch, wodurch der Bedarf an temporärem Speicherplatz reduziert wird.

## So verwenden Sie die API „Daten in Arbeitsmappe importieren“ mit SDKs

**Hinweise / Einschränkungen:** Die API unterstützt bis zu 1 000 000 Zeilen pro Import. Standardmäßig ist nur das Komma als CSV-Trennzeichen zulässig; andere einzeilige Trennzeichen können über den Parameter `splitter` angegeben werden. Große XML-Dateien können die Verarbeitungszeit erhöhen.

Weitere verwandte Vorgänge wie der Datenexport oder die Konvertierung von Arbeitsmappenformaten finden Sie in der Dokumentation zu **Daten exportieren** und **Arbeitsmappe konvertieren**.

### API-Spezifikation: Daten in Arbeitsmappe importieren

Die <a href="https://reference.aspose.cloud/cells/#/DataProcessingController/ImportDataIntoSpreadsheet" rel="noopener noreferrer">API-Spezifikation: Daten in Arbeitsmappe importieren</a> bietet eine öffentlich zugängliche Programmierschnittstelle, über die REST-Interaktionen direkt aus Ihrem Webbrowser möglich sind.
Sie können das cURL-Befehlszeilentool verwenden, um problemlos auf Aspose.Cells-Webdienste zuzugreifen. Das folgende Beispiel zeigt, wie Sie mit cURL Aufrufe an die Cloud-API durchführen.

{{< tabs tabTotal="2" tabID="11" tabName11="Anfrage" tabName12="Antwort" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/import/data?worksheet=Sheet1&startCell=A1&insert=true" \
  -H "Authorization: Bearer {access_token}" \
  -F "datafile=@/path/to/data.csv" \
  -F "spreadsheet=@/path/to/workbook.xlsx"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```
{
  "type": "FileContentResult",
  "fileContents": "byte[] (Base64-codiert)",
  "contentType": "MIME-Typ",
  "fileDownloadName": "optionaler Dateiname"
}
```

{{< /tab >}}

{{< /tabs >}}

### Verwenden der Aspose.Cells Cloud SDKs

Die Verwendung eines SDKs ist der schnellste Weg zur Entwicklung, da sie detaillierte Low-Level-Details abstrahieren und es Ihnen ermöglichen, Daten mit wenig Code in ein Arbeitsblatt zu importieren. Besuchen Sie das <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub-Repository</a>, um eine vollständige Liste der Aspose.Cells Cloud SDKs zu erhalten.

---