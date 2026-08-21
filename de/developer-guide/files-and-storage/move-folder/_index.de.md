---
title: "Aspose.Cells Cloud Move Folder API – Ordner schnell in der Cloud verschieben"
second_title: "Dokument"
ArticleTitle: "Cloud-basiertes Excel-Dateimanagement – Ordner schnell in der Cloud verschieben"
linktype: "Move Folder"
type: docs
url: /de/move-folder/
keywords: "Aspose.Cells, Ordner verschieben, Cloud-Speicher, Excel-API"
description: "Erfahren Sie, wie Sie Ordner im Aspose.Cells Cloud-Speicher über die REST-basierte Move Folder API verschieben können. Enthält Endpunkt, Parameter, Beispiel-cURL-Aufrufe, Fehlercodes und SDK-Beispiele für C#, Java, Python und mehr."
weight: 100
---

Diese API verschiebt einen Ordner von einem Speicherort zu einem anderen innerhalb des Aspose.Cells Cloud-Speichers. Sie hilft dabei, Dateien zu organisieren und den Cloud-Speicher effizient zu verwalten.

## **Excel-API: Ordner verschieben**

### Web-API

```http
PUT https://api.aspose.cloud/v4.0/cells/storage/folder/move/{srcPath}
```

**Beispiel-cURL-Anforderung**

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/storage/folder/move/FolderA?destPath=FolderB" \
     -H "Authorization: Bearer {access_token}"
```

### **Sicherheit und Authentifizierung**

Die Aspose.Cells Cloud APIs sind sicher und erfordern eine <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-Token-basierte Authentifizierung</a>.

### Die Anforderungsparameter der **moveFolder** API sind:

| Parametername     | Typ    | Ort    | Beschreibung                                                             |
| ----------------- | ------ | ------ | ------------------------------------------------------------------------ |
| srcPath           | string | Path   | Der vollständige Pfad des zu verschiebenden Ordners, z. B. `FolderA/`.   |
| destPath          | string | Query  | Der Zielpfad, an den der Ordner verschoben wird, z. B. `FolderB/`.      |
| srcStorageName    | string | Query  | (Optional) Name des Quellspeichers.                                      |
| destStorageName   | string | Query  | (Optional) Name des Zielspeichers.                                       |

**Parameterdetails**

- **srcPath** – erforderlich. Der Pfad des Quellordners.
- **destPath** – erforderlich. Der Pfad des Zielordners.
- **srcStorageName** – optional. Bezeichner des Quellspeichers.
- **destStorageName** – optional. Bezeichner des Zielspeichers.

### **Antwort**

Im Erfolgsfall gibt die API einen leeren Antworttext mit dem HTTP-Status **200 OK** zurück. Fehler werden als JSON-Objekte mit einem Feld `error` zurückgegeben.

**HTTP-Statuscodes**

| HTTP-Code | HTTP-Status           | Beschreibung                                                           |
| --------- | --------------------- | ---------------------------------------------------------------------- |
| 200       | OK                    | Web-API erfolgreich aufgerufen; Antwort enthält Operationsdetails.    |
| 400       | Bad Request           | Fehlende oder ungültige Parameter (z. B. nicht unterstützter Dateityp).|
| 401       | Unauthorized          | Ungültiges oder fehlendes JWT-Token.                                  |
| 413       | Payload Too Large     | Die hochgeladene Datei überschreitet die Größenbeschränkung.          |
| 500       | Internal Server Error | Unerwarteter Serverfehler.                                            |

## OpenAPI-Spezifikation

Die [OpenAPI-Spezifikation](https://reference.aspose.cloud/cells/#/FolderController/MoveFolder) definiert eine öffentlich zugängliche Programmierschnittstelle und ermöglicht REST-Interaktionen direkt aus einem Webbrowser.

Sie können das cURL-Befehlszeilentool verwenden, um problemlos auf Aspose.Cells-Webdienste zuzugreifen. Das folgende Beispiel zeigt, wie Sie mithilfe von cURL Aufrufe an die Cloud-API durchführen.

{{< tabs tabTotal="2" tabID="11" tabName11="Anforderung" tabName12="Antwort" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/storage/folder/move/{srcPath}?destPath={destPath}" \
     -H "Authorization: Bearer {access_token}"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{}
```

{{< /tab >}}

{{< /tabs >}}

Die Verwendung eines SDK ist der beste Weg, die Entwicklung zu beschleunigen. Ein SDK übernimmt die Low-Level-Details und lässt Sie sich auf Ihre Projekt Aufgaben konzentrieren. Eine vollständige Liste der Aspose.Cells Cloud SDKs finden Sie im [GitHub-Repository](https://github.com/aspose-cells-cloud).

Die folgenden Codebeispiele zeigen, wie Aufrufe an Aspose.Cells-Webdienste mithilfe verschiedener SDKs durchgeführt werden:

---