---
title: "Batch Split"
second_title: "Dokumentation"
type: docs
url: /de/batch/split
keywords: "Batch Split, Aspose.Cells Cloud, REST API, Excel, PDF, CSV, JSON, Tabellenkalkulation, Cloud SDK"
description: "Dokumentation für die Aspose.Cells Cloud Batch Split API, die Tabellenkalkulationsdateien in verschiedene Formate wie PDF, CSV oder JSON aufteilt. Enthält Anforderungsdetails, Beispiel-cURL-Befehle und SDK-Nutzung in verschiedenen Programmiersprachen."
weight: 100
---

Diese REST API führt eine **Batch-Aufteilung** (Batch Split) geeigneter Dateien durch.

## REST API

```bash
POST http://api.aspose.cloud/v3.0/cells/batch/split
```

### **Sicherheit und Authentifizierung**

Die Aspose.Cells Cloud APIs sind sicher und erfordern eine <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-Token-basierte Authentifizierung</a>.

### Anforderungsparameter

| Parametername     | Typ                | Pfad/Query/String/HTTPBody | Beschreibung                                         |
|-------------------|--------------------|----------------------------|------------------------------------------------------|
| BatchSplitRequest | BatchSplitRequest  | body                       | Anforderungstext mit Optionen für die Aufteilung.  |

### **BatchSplitRequest**-Eigenschaften

| Name             | Typ                  | Beschreibung                                         | Anmerkungen  |
|------------------|----------------------|------------------------------------------------------|--------------|
| SourceFolder     | string               | Ordner, der die Quelldatei enthält.                 | [optional]   |
| SourceStorage    | string               | Speichername, in dem sich die Quelldatei befindet.  | [optional]   |
| MatchCondition   | MatchConditionRequest| Bedingungen zur Auswahl der Dateien für die Aufteilung.| [optional]   |
| Format           | string               | Gewünschtes Ausgabeformat (z. B. pdf, csv).         | [optional]   |
| FromIndex        | integer              | Startindex der zu teilenden Seiten.                 | [optional]   |
| ToIndex          | integer              | Endindex der zu teilenden Seiten.                   | [optional]   |
| OutFolder        | string               | Zielordner für die aufgeteilten Dateien.            | [optional]   |
| SaveOptions      | SaveOptions          | Zusätzliche Optionen zum Speichern der Ausgabe.     | [optional]   |

### **MatchConditionRequest**-Eigenschaften

| Name               | Typ       | Beschreibung                                     | Anmerkungen  |
|--------------------|-----------|--------------------------------------------------|--------------|
| RegexPattern       | string    | Regulärer Ausdruck zur Übereinstimmung mit Dateinamen. | [optional]   |
| FullMatchConditions| string[]  | Liste exakter Übereinstimmungsbedingungen.      | [optional]   |

### Anforderungstext-Parameter

| Parametername | Typ  | Beschreibung                                  |
| ------------- | ---- | --------------------------------------------- |
| data          | file | Binärer Inhalt der zu erstellenden Arbeitsmappe. |

### **Antwort**

```json
{
    "Name": "ResponseFile",
    "DataType": {
        "Identifier": "File",
        "Reference": "Stream",
        "Name": "file"
    }
}
```

**HTTP-Statuscodes**

| Code | Bedeutung                            | Wann zurückgegeben                         |
|------|--------------------------------------|--------------------------------------------|
| 200 OK | Arbeitsmappe erfolgreich erstellt    | Normaler Ablauf                            |
| 201 Created | Arbeitsmappe erstellt (alternative Antwort) | Wenn die API den Status „Created“ zurückgibt |
| 400 Bad Request | Ungültige Parameter                 | Client-seitiger Fehler                     |
| 401 Unauthorized | Fehlendes oder ungültiges Token    | Authentifizierungsfehler                   |
| 409 Conflict | Datei existiert und `isWriteOver=false` | Konflikt mit vorhandener Datei            |


## Verwendung der PostBatchSplit API mit SDKs

### PostBatchSplit API-Spezifikation

Die [OpenAPI-Spezifikation](https://reference.aspose.cloud/cells/#/Batch/PostBatchSplit) definiert eine öffentlich zugängliche Programmierschnittstelle und ermöglicht es Ihnen, REST-Interaktionen direkt aus einem Webbrowser heraus durchzuführen.

Sie können das cURL-Befehlszeilentool nutzen, um Aspose.Cells-Webdienste einfach anzusprechen. Das folgende Beispiel zeigt, wie Sie mit cURL Aufrufe an die Cloud API durchführen.

{{< tabs tabTotal="2" tabID="11" tabName11="Anforderung" tabName12="Antwort" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "http://api.aspose.cloud/v3.0/cells/batch/split" \
-X POST \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>" \
-D "{\"SourceFolder\":\"CellsTests\",\"OutFolder\":\"Output\",\"MatchCondition\":{\"RegexPattern\":\"(^Book)(.+)(xlsx$)\"},\"Format\":\"pdf\"}"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

### Verwendung der Aspose.Cells Cloud SDKs

Die Verwendung eines SDKs ist der beste Weg, um die Entwicklung zu beschleunigen. Ein SDK übernimmt die Low-Level-Details und ermöglicht es Ihnen, sich auf Ihre Aufteilungsaufgaben zu konzentrieren. Bitte prüfen Sie das [GitHub-Repository](https://github.com/aspose-cells-cloud), um eine vollständige Liste der Aspose.Cells Cloud SDKs zu erhalten.

Die folgenden Codebeispiele zeigen, wie Aufrufe an Aspose.Cells-Webdienste mit verschiedenen SDKs durchgeführt werden:

{{< tabs tabTotal="9" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js"  tabName7="Swift" tabName8="Perl" tabName9="Go" >}}

{{< tab tabNum="1" >}}
{{< /tab >}}

{{< tab tabNum="2" >}}
{{< /tab >}}

{{< tab tabNum="3" >}}
{{< /tab >}}

{{< tab tabNum="4" >}}
{{< /tab >}}

{{< tab tabNum="5" >}}
{{< /tab >}}

{{< tab tabNum="6" >}}
{{< /tab >}}

{{< tab tabNum="7" >}}
{{< /tab >}}

{{< tab tabNum="8" >}}
{{< /tab >}}

{{< tab tabNum="9" >}}
{{< /tab >}}

{{< /tabs >}}
---