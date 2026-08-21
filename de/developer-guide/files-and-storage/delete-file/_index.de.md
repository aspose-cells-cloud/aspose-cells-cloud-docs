---
title: "Aspose.Cells Cloud – API zum Löschen von Dateien"
second_title: "Dokument"
ArticleTitle: "Aspose.Cells Cloud – API zum Löschen von Dateien"
linktitle: "Datei löschen"
type: docs
url: /de/delete-file/
keywords: "Aspose Cells, API zum Löschen von Dateien, Excel-Cloud-Speicher, REST-API, Dateiverwaltung"
description: "Löschen Sie eine Excel-Datei aus dem Aspose.Cells Cloud-Speicher mithilfe der RESTful API zum Löschen von Dateien. Enthält Endpunkt, Parameter, Authentifizierung und Beispielcode."
weight: 100
---

Die **deleteFile**-API entfernt die angegebene Datei aus dem Cloud-Speicher und hilft Ihnen so, Ressourcen und Daten effizient zu verwalten.

## **Excel-API: Datei löschen**

### Web-API

```http
DELETE https://api.aspose.cloud/v4.0/cells/storage/file/{path}
```

### **Sicherheit und Authentifizierung**

Die Aspose.Cells Cloud-APIs sind sicher und erfordern eine <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-Token-basierte Authentifizierung</a>.

```bash
-H "Authorization: Bearer {access_token}"
```

### Anforderungsparameter

| Parametername   | Typ    | Ort   | Beschreibung                                                                                  |
| :-------------- | :----- | :---- | :-------------------------------------------------------------------------------------------- |
| `path`          | string | Path  | Der URL-kodierte Pfad zur Datei, die gelöscht werden soll.                                   |
| `storageName`   | string | Query | Der Name des Speichers, in dem sich die Datei befindet. Weglassen, wenn der Standardspeicher verwendet wird. |
| `versionId`     | string | Query | Bezeichner einer bestimmten Dateiversion zum Löschen. Falls weggelassen, wird die neueste Version entfernt. |

### Antwortbeschreibung

Bei einer erfolgreichen Anforderung wird **HTTP 200** mit einem leeren Antworttext zurückgegeben. Es wird kein JSON-Payload zurückgegeben.

```json
{}
```

**HTTP-Statuscodes**

| Code | Bedeutung             | Beschreibung                                                     |
| ---- | --------------------- | ---------------------------------------------------------------- |
| 200  | OK                    | Filter erfolgreich angewendet; Antwort enthält Operationsdetails. |
| 400  | Bad Request           | Fehlende oder ungültige Parameter (z. B. nicht unterstützter Dateityp). |
| 401  | Unauthorized          | Ungültiges oder fehlendes JWT-Token.                            |
| 413  | Payload Too Large     | Die hochgeladene Datei überschreitet die Größenbeschränkung.    |
| 500  | Internal Server Error | Unerwarteter Serverfehler.                                       |

## OpenAPI-Spezifikation

Die [OpenAPI-Spezifikation](https://reference.aspose.cloud/cells/#/FileController/DeleteFile) definiert eine öffentlich zugängliche Programmierschnittstelle und ermöglicht REST-Interaktionen direkt aus einem Webbrowser.

Sie können das cURL-Befehlszeilentool nutzen, um problemlos auf Aspose.Cells-Webdienste zuzugreifen. Das folgende Beispiel zeigt, wie Aufrufe an die Cloud-API mit cURL durchgeführt werden.

{{< tabs tabTotal="2" tabID="11" tabName11="Anforderung" tabName12="Antwort" >}}

{{< tab tabNum="11" >}}

```bash
curl -X DELETE "https://api.aspose.cloud/v4.0/cells/storage/file/Example.xlsx?storageName=MyStorage" \
     -H "Authorization: Bearer IHR_ZUGRIFFSTOKEN" \
     -H "Accept: application/json"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```
{
}
```

{{< /tab >}}

{{< /tabs >}}

### Verwenden Sie Aspose.Cells Cloud SDKs

Die Verwendung eines SDKs ist der beste Weg, um die Entwicklung zu beschleunigen. Ein SDK verwaltet die Details der unteren Schicht, sodass Sie sich auf Ihre Projekt-Aufgaben konzentrieren können. Besuchen Sie das [GitHub-Repository](https://github.com/aspose-cells-cloud), um eine vollständige Liste der Aspose.Cells Cloud SDKs zu erhalten.

Die folgenden Codebeispiele zeigen, wie Aufrufe an Aspose.Cells-Webdienste mithilfe verschiedener SDKs durchgeführt werden.