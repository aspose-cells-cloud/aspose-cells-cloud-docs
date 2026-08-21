---
title: "Stil für Pivot-Tabelle aktualisieren"
second_title: "Dokument"
linktitle: "Alle formatieren"
type: docs
url: /pivot-tables/format-all/
aliases: [/update-style-for-pivot-table/]
keywords: "Pivot-Tabelle, Stil aktualisieren, Aspose.Cells Cloud, REST-API, Excel, Tabellendokument, API, Pivot-Tabellenstil, alle formatieren"
description: "Erfahren Sie, wie Sie den Stil einer gesamten Pivot-Tabelle mithilfe der Aspose.Cells Cloud REST-API aktualisieren können. Enthält Anforderungsdetails, ein cURL-Beispiel und SDK-Snippets für mehrere Programmiersprachen."
weight: 100
ArticleTitle: "Stil für Pivot-Tabelle aktualisieren – Aspose.Cells Cloud API"
---

Diese REST-API aktualisiert den Stil einer Pivot-Tabelle.

## PostPivotTableStyle API

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/pivottables/{pivotTableIndex}/FormatAll
```

**Voraussetzungen / Authentifizierung**  
Ein gültiges JWT-Zugriffstoken muss im `Authorization`-Header bereitgestellt werden (z. B. `Bearer <jwt token>`). Stellen Sie sicher, dass das Token über die erforderlichen Berechtigungen verfügt, um auf die angegebene Arbeitsmappe und das angegebene Arbeitsblatt zuzugreifen.

### **Sicherheit und Authentifizierung**

Die Aspose.Cells Cloud-APIs sind sicher und erfordern eine <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-Token-basierte Authentifizierung</a>.

### **Anforderungsparameter**

| Parametername    | Typ     | Speicherort | Beschreibung                                                                                      |
| ---------------- | ------- | ----------- | ------------------------------------------------------------------------------------------------- |
| name             | string  | path        | Der Name der Arbeitsmappe (Datei).                                                                |
| sheetName        | string  | path        | Das Arbeitsblatt, das die Pivot-Tabelle enthält.                                                  |
| pivotTableIndex  | integer | path        | Nullbasierter Index der zu formatierenden Pivot-Tabelle.                                         |
| style            | object  | body        | Ein Style-DTO, der das anzuwendende Format definiert.                                             |
| needReCalculate  | boolean | query       | Auf **true** setzen, um die Pivot-Tabelle nach dem Formatieren neu zu berechnen; Standard ist **false**. |
| folder           | string  | query       | Der Ordner, in dem die Arbeitsmappe gespeichert ist.                                             |
| storageName      | string  | query       | Der Name des Speicherdienstes.                                                                    |

Die [OpenAPI-Spezifikation](https://apireference.aspose.cloud/cells/#/PivotTables/PostPivotTableStyle) definiert eine öffentlich zugängliche Programmierschnittstelle und ermöglicht REST-Interaktionen direkt aus einem Webbrowser.

Sie können das cURL-Befehlszeilentool verwenden, um einfach auf Aspose.Cells-Webdienste zuzugreifen. Das folgende Beispiel zeigt, wie ein Aufruf an die Cloud-API mit cURL durchgeführt wird.

{{< tabs tabTotal="2" tabID="1" tabName1="Anforderung" tabName2="Antwort" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Sample_Pivot_Table_Example.xls/worksheets/Sheet2/pivottables/0/FormatAll" \
  -X POST \
  -d '{"Font":{"Name":"Arial","Size":10}}' \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

**HTTP-Statuscodes**

| Code | Bedeutung               | Beschreibung                                                                 |
|------|-------------------------|------------------------------------------------------------------------------|
| 200  | OK                      | Filter erfolgreich angewendet; Antwort enthält Details zum Vorgang.         |
| 400  | Bad Request             | Fehlende oder ungültige Parameter (z. B. nicht unterstützter Dateityp).     |
| 401  | Unauthorized            | Ungültiges oder fehlendes JWT-Token.                                        |
| 413  | Payload Too Large       | Die hochgeladene Datei überschreitet das Größenlimit.                       |
| 500  | Internal Server Error   | Unerwarteter Serverfehler.                                                  |

{{< /tab >}}

{{< /tabs >}}

## Cloud SDK-Familie

Die Verwendung eines SDKs ist die schnellste Möglichkeit, API-basierte Anwendungen zu entwickeln. Das SDK abstrahiert die Low-Level-Details, sodass Sie sich auf Ihre Geschäftslogik konzentrieren können. Eine vollständige Liste der Aspose.Cells Cloud SDKs finden Sie im <a href="https://github.com/aspose-cells-cloud" target="_blank" rel="noopener noreferrer">GitHub-Repository</a>.

Das folgende Codebeispiel zeigt, wie die API mithilfe des Go SDK aufgerufen wird:

{{< tabs tabTotal="1" tabID="4" tabName1="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "0b2caae7acfa3e947b856c07b6e8633a" >}}

{{< /tab >}}

{{< /tabs >}}