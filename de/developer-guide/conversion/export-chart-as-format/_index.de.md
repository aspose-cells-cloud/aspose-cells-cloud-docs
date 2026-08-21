---
title: "Excel-Diagramm exportieren – Aspose.Cells Cloud API"
second_title: "Dokument"
description: "Konvertieren Sie ein Diagramm aus einer in der Cloud gespeicherten Excel-Arbeitsmappe mit einem einzigen REST-Aufruf in PDF, PNG, SVG oder andere Formate."
ArticleTitle: "So konvertieren Sie ein lokales Arbeitsblatt einer Tabellenkalkulation in eine PDF-Datei: Schritt-für-Schritt-Anleitung"
linktype: "Dokumentation"
type: docs
url: /de/export-chart-as-format/
keywords: "Aspose.Cells Cloud, Diagramm exportieren, API, PDF, PNG, SVG, Excel, REST, Cloud-Konvertierung"
weight: 100
---

Konvertieren Sie ein Diagramm, das sich in einer Arbeitsmappe befindet, die bei Aspose Cloud gespeichert ist, in ein anderes Dateiformat (PDF, PNG, SVG, …), ohne die Quelldatei herunterzuladen.

## ExportChartAsFormat-API

```http
GET https://api.aspose.cloud/v4.0/cells/{name}/worksheets/{worksheet}/charts/{chartIndex}
```

### **Sicherheit und Authentifizierung**

Die Aspose.Cells Cloud-APIs sind sicher und erfordern eine <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-Token-basierte Authentifizierung</a>.

### 📦 Anforderungsparameter

| Name               | Typ     | Ort     | Erforderlich | Beschreibung                                                     |
| ------------------ | ------- | ------- | ------------ | ---------------------------------------------------------------- |
| **name**           | string  | Pfad    | Ja           | Dateiname der Arbeitsmappe.                                      |
| **worksheet**      | string  | Pfad    | Ja           | Name des Arbeitsblatts, das das Diagramm enthält.              |
| **chartIndex**     | integer | Pfad    | Ja           | Nullbasierten Index des zu exportierenden Diagramms.           |
| **format**         | string  | Abfrage | Ja           | Gewünschtes Ausgabeformat (z. B. `png`, `pdf`, `svg`).          |
| **folder**         | string  | Abfrage | Nein         | Ordnerpfad, in dem die Arbeitsmappe gespeichert ist (Standard: Root). |
| **storageName**    | string  | Abfrage | Nein         | Benutzerdefinierter Speichername; weglassen, um den Standardspeicher zu verwenden. |
| **outPath**        | string  | Abfrage | Nein         | Ordnerpfad, in dem die konvertierte Datei gespeichert wird.    |
| **outStorageName** | string  | Abfrage | Nein         | Speichername für die Ausgabedatei.                              |
| **fontsLocation**  | string  | Abfrage | Nein         | Pfad zu einem Ordner, der benutzerdefinierte Schriftarten enthält. |
| **region**         | string  | Abfrage | Nein         | Gebietsschema-Einstellung (z. B. `de-DE`, `en-US`, `fr-FR`).   |
| **password**       | string  | Abfrage | Nein         | Passwort zum Öffnen einer geschützten Arbeitsmappe.             |

### **Antwort**

```json
[
  {
    "Name": "ResponseFile",
    "DataType": {
      "Identifier": "File",
      "Reference": "Stream",
      "Name": "file"
    }
  }
]
```

**HTTP-Statuscodes**

| Code | Bedeutung             | Beschreibung                                                     |
| ---- | --------------------- | ---------------------------------------------------------------- |
| 200  | OK                    | Filter erfolgreich angewendet; Antwort enthält Operationsdetails. |
| 400  | Bad Request           | Fehlende oder ungültige Parameter (z. B. nicht unterstützter Dateityp). |
| 401  | Unauthorized          | Ungültiges oder fehlendes JWT-Token.                            |
| 413  | Payload Too Large     | Die hochgeladene Datei überschreitet das Größenlimit.           |
| 500  | Internal Server Error | Unerwarteter Serverfehler.                                      |

## Wie verwende ich die „Diagramm exportieren als Format“-API mit SDKs?

### API-Spezifikation für „Diagramm exportieren als Format“

Die [API-Spezifikation für „Diagramm exportieren als Format“](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Conversion/ExportChartAsFormat) bietet eine öffentlich zugängliche Programmierschnittstelle und ermöglicht REST-Interaktionen direkt aus einem Webbrowser.

Sie können das cURL-Befehlszeilentool verwenden, um bequem auf Aspose.Cells-Webservices zuzugreifen. Das folgende Beispiel zeigt, wie Aufrufe an die Cloud-API mit cURL durchgeführt werden.

{{< tabs tabTotal="2" tabID="11" tabName11="Anforderung" tabName12="Antwort" >}}

{{< tab tabNum="11" >}}

```bash
curl -X GET "https://api.aspose.cloud/v4.0/cells/{name}/worksheets/{worksheet}/charts/{chartIndex}?format={format}" \
  -H "Authorization: Bearer {access_token}"
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

Die Verwendung eines SDKs ist der schnellste Weg zur Entwicklung, da sie Low-Level-Details abstrahieren und es Ihnen ermöglichen, Tabellendaten einer Spreadsheet-Datei mit minimalem Code in eine PDF-Datei zu konvertieren. Bitte prüfen Sie das [GitHub-Repository](https://github.com/aspose-cells-cloud), um eine vollständige Liste der Aspose.Cells Cloud SDKs zu erhalten.

Die folgenden Codebeispiele zeigen, wie Aspose.Cells-Webservices mit verschiedenen SDKs aufgerufen werden:

---