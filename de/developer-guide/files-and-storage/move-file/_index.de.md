---
title: "Aspose.Cells Cloud Move File API – Schnittstelle zum schnellen Verschieben von Dateien in der Cloud"
second_title: "Dokument"
ArticleTitle: "Cloud-basierte Excel-Dateiverwaltungslösung – Schnittstelle zum schnellen Verschieben von Dateien in der Cloud"
linktitle: "Datei verschieben"
type: docs
url: /de/move-file/
keywords: "Aspose.Cells, Move File API, Cloud-Speicher, Excel-API, Dateiverwaltung"
description: "Wie Sie Dateien zwischen Ordnern im Aspose.Cells Cloud-Speicher mithilfe der v4.0 Move File API verschieben – Endpunkt, Parameter, Beispiele und SDK-Links."
weight: 100
---

Die **moveFile** API verschiebt eine Datei von einem Speicherort zu einem anderen innerhalb des Aspose.Cells Cloud-Speichers. Sie hilft Ihnen dabei, Dateien zu organisieren und den Speicher effizient zu verwalten.

## **Excel-API: Datei verschieben**

### Web-API

```bash
PUT https://api.aspose.cloud/v4.0/cells/storage/file/move/{srcPath}
```

### **Sicherheit und Authentifizierung**

Die Aspose.Cells Cloud APIs sind sicher und erfordern eine <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-Token-basierte Authentifizierung</a>.

```bash
-H "Authorization: Bearer {access_token}"
```

### Die Anforderungsparameter der **moveFile** API sind

| Parametername   | Typ    | Pfad/Abfragezeichenfolge/HTTP-Body | Beschreibung                                               |
| --------------- | ------ | ---------------------------------- | ---------------------------------------------------------- |
| srcPath         | String | Pfad                               | Der Quellpfad der zu verschiebenden Datei.                |
| destPath        | String | Abfrage                            | Der Zielpfad, an den die Datei verschoben wird.           |
| srcStorageName  | String | Abfrage                            | Der Name des Quellspeichers (falls zutreffend).           |
| destStorageName | String | Abfrage                            | Der Name des Zieldateispeichers (falls zutreffend).       |
| versionId       | String | Abfrage                            | Die Dateiversion-ID (falls zutreffend).                   |

### **Antwort**

Eine erfolgreiche Anfrage gibt **HTTP 200 OK** mit einem leeren JSON-Body zurück.

```json
{}
```

**HTTP-Statuscodes**

| HTTP-Code | HTTP-Status           | Beschreibung                                                                   |
| --------- | --------------------- | ------------------------------------------------------------------------------ |
| 200       | OK                    | Web-API erfolgreich aufgerufen; Antwort enthält Details zum Vorgang.         |
| 400       | Bad Request           | Fehlende oder ungültige Parameter (z. B. nicht unterstützter Dateityp).       |
| 401       | Unauthorized          | Ungültiges oder fehlendes JWT-Token.                                          |
| 413       | Payload Too Large     | Die hochgeladene Datei überschreitet die Größeinschränkung.                   |
| 500       | Internal Server Error | Unerwarteter Serverfehler.                                                    |

## OpenAPI-Spezifikation

Die [OpenAPI-Spezifikation](https://reference.aspose.cloud/cells/#/FileController/MoveFile) definiert eine öffentlich zugängliche Programmierschnittstelle und ermöglicht es Ihnen, REST-Interaktionen direkt über einen Webbrowser durchzuführen.

Sie können das cURL-Befehlszeilentool verwenden, um Aspose.Cells-Webservices einfach aufzurufen. Das folgende Beispiel zeigt, wie Sie mit cURL Aufrufe an die Cloud-API durchführen.

{{< tabs tabTotal="2" tabID="11" tabName11="Anforderung" tabName12="Antwort" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/storage/file/move/{srcPath}?destPath={destPath}" \
     -H "Authorization: Bearer {access_token}"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{}
```

{{< /tab >}}

{{< /tabs >}}

Die Verwendung eines SDK ist der beste Weg, um die Entwicklung zu beschleunigen. Ein SDK kümmert sich um die Low-Level-Details und lässt Sie sich auf Ihre Projektaufgaben konzentrieren. Bitte besuchen Sie das [GitHub-Repository](https://github.com/aspose-cells-cloud), um eine vollständige Liste der Aspose.Cells Cloud SDKs zu erhalten.

Die folgenden Codebeispiele zeigen, wie Aufrufe an Aspose.Cells-Webservices mithilfe verschiedener SDKs durchgeführt werden:

---