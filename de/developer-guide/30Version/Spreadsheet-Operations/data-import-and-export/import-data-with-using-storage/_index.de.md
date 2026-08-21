---
title: "Daten mit Speicher importieren"
second_title: "Dokument"
linktype: docs
url: /import-data-with-using-storage/
aliases:
  - /import-data-into-excel-worksheet/
  - /import-data-into-worksheet/
  - /import-data-in-excel-worksheet/
  - /import-data/
  - /import/with-using-storage/
description: "Daten mit Speicher importieren: Importieren Sie Daten in eine Excel-Arbeitsmappe mithilfe der Aspose.Cells Cloud API aus verschiedenen Speicherquellen. Unterstützt JSON, CSV und andere Formate über HTTPS."
keywords: "Aspose.Cells Cloud, Excel, Daten importieren, REST API, Cloud-Speicher, JSON, CSV, PDF, Markdown, HTTPS"
weight: 10
ArticleTitle: "Daten mit Speicher importieren – Aspose.Cells Cloud API-Dokumentation"
---

Diese REST API importiert Daten in eine Excel-Datei.

## PostImportData API

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/importdata
```

### **Sicherheit und Authentifizierung**

Die Aspose.Cells Cloud APIs sind sicher und erfordern eine <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-Token-basierte Authentifizierung</a>.

### Die Anforderungsparameter sind:

| Parametername   | Typ    | Ort   | Beschreibung                                               |
|-----------------|--------|-------|------------------------------------------------------------|
| name            | string | path  | Der Name der Excel-Datei.                                  |
| folder          | string | query | Der Ordnerpfad im Speicher, in dem sich die Datei befindet. |
| storageName     | string | query | Der Name des Speicherdiensts.                              |
| importData      | object | body  | JSON-Objekt, das die zu importierenden Daten enthält.     |

**Die Importdaten-Optionsparameter** sind unter [dem Referenzlink](/cells/import/#import-data-option-parameter) beschrieben.

**Voraussetzungen:** Sie müssen ein gültiges JWT-Token im `Authorization`-Header bereitstellen und sicherstellen, dass die Ziel-Arbeitsmappe bereits am angegebenen Speicherort vorhanden ist.

### Antwort

```json
{
  "Status":"OK",
  "Code":200
}
```

**HTTP-Statuscodes**

| Code | Bedeutung                   | Beschreibung                                                 |
|------|-----------------------------|--------------------------------------------------------------|
| 200  | OK                          | Filter erfolgreich angewendet; Antwort enthält Details zum Vorgang. |
| 400  | Bad Request                 | Fehlende oder ungültige Parameter (z. B. nicht unterstützter Dateityp). |
| 401  | Unauthorized                | Ungültiges oder fehlendes JWT-Token.                         |
| 413  | Payload Too Large           | Die hochgeladene Datei überschreitet die Größenbeschränkung. |
| 500  | Internal Server Error       | Unerwarteter Serverfehler.                                   |

## So verwenden Sie die PostImportData API mit SDKs

### PostImportData API-Spezifikation

Die <a href="https://apireference.aspose.cloud/cells/#/Workbook/PostImportData" rel="noopener noreferrer">OpenAPI-Spezifikation</a> definiert eine öffentlich zugängliche Programmierschnittstelle und ermöglicht es Ihnen, REST-Interaktionen direkt aus einem Webbrowser durchzuführen.

Sie können das cURL-Befehlszeilentool verwenden, um problemlos auf Aspose.Cells-Webdienste zuzugreifen. Das folgende Beispiel zeigt, wie die Cloud API mit cURL aufgerufen wird.

{{< tabs tabTotal="2" tabID="1" tabName1="Anforderung" tabName2="Antwort" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/importdata" \
     -X POST \
     -d '{"Data":[1,2,4],"DestinationWorksheet":"Sheet1","FirstRow":1,"FirstColumn":2,"IsVertical":true,"IsInsert":true,"importDataType":"IntArray"}' \
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

{{< /tab >}}

{{< /tabs >}}

### Verwenden von Aspose.Cells Cloud SDKs

Die Verwendung eines SDKs ist der beste Weg, die Entwicklung zu beschleunigen. Ein SDK abstractiert Low-Level-Details, sodass Sie sich auf Ihre Geschäftslogik konzentrieren können. Besuchen Sie das [GitHub-Repository](https://github.com/aspose-cells-cloud), um eine vollständige Liste der Aspose.Cells Cloud SDKs zu erhalten.

Das folgende Codebeispiel zeigt, wie der Aspose.Cells-Webdienst mithilfe des PHP-SDK aufgerufen wird:
---