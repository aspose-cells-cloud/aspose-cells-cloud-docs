---
title: "Ordner erstellen – Aspose.Cells Cloud API | Excel-Speicherverwaltung"
second_title: "Dokument"
ArticleTitle: "Ordner erstellen – Aspose.Cells Cloud API"
linktype: "Create Folder"
type: docs
url: /de/create-folder/
keywords: "Aspose.Cells, Cloud API, Ordner erstellen, Speicherverwaltung, Excel"
description: "Erstellen Sie einen neuen Ordner im Aspose.Cells Cloud-Speicher über eine einfache PUT-Anforderung. Sehen Sie sich das Anforderungsformat, die Parameter, die Antwort und die Fehlerbehandlung an."
weight: 100
---

Die **createFolder**-Operation erstellt einen neuen Ordner am angegebenen Speicherort im Cloud-Speicher, der von der Excel-API verwendet wird. Dies ist entscheidend für die Organisation von Dateien und die Aufrechterhaltung einer strukturierten Verzeichnishierarchie.

## **Excel API: Ordner erstellen**

### Web-API

```
PUT https://api.aspose.cloud/v4.0/cells/storage/folder/{path}
```

### **Sicherheit und Authentifizierung**

Die Aspose.Cells Cloud APIs sind sicher und erfordern eine <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-Token-basierte Authentifizierung</a>.

### Die Anforderungsparameter der **createFolder**-API sind

| Parametername   | Typ    | Ort    | Erforderlich | Standardwert | Beschreibung                                                                 |
| --------------- | ------ | ------ | ------------ | ------------ | ---------------------------------------------------------------------------- |
| `path`          | String | Pfad   | Ja           | –            | Der zu erstellende Ordnerpfad (z. B. `myFolder/subFolder`).                 |
| `storageName`   | String | Query  | Nein         | –            | Der Name des zu verwendenden Speichers. Falls weggelassen, wird der Standardspeicher verwendet. |

### Antwortbeschreibung

```json
{}
```

Die Operation gibt bei Erfolg keinen Inhalt zurück. Typische HTTP-Statuscodes sind:

**HTTP-Statuscodes**

| HTTP-Code | HTTP-Status           | Beschreibung                                                       |
| --------- | --------------------- | ------------------------------------------------------------------ |
| 200       | OK                    | Web-API erfolgreich aufgerufen; Antwort enthält Details zum Vorgang. |
| 400       | Bad Request           | Fehlende oder ungültige Parameter (z. B. nicht unterstützter Dateityp). |
| 401       | Unauthorized          | Ungültiges oder fehlendes JWT-Token.                              |
| 413       | Payload Too Large     | Die hochgeladene Datei überschreitet das Größenlimit.             |
| 500       | Internal Server Error | Unerwarteter Serverfehler.                                        |

## OpenAPI-Spezifikation

Die [OpenAPI-Spezifikation](https://reference.aspose.cloud/cells/#/FolderController/CreateFolder) definiert eine öffentlich zugängliche Programmierschnittstelle und ermöglicht es Ihnen, REST-Interaktionen direkt aus einem Webbrowser heraus durchzuführen.

Sie können das cURL-Befehlszeilentool verwenden, um Aspose.Cells-Webdienste einfach aufzurufen. Das folgende Beispiel zeigt, wie Aufrufe an die Cloud-API mit cURL durchgeführt werden.

{{< tabs tabTotal="2" tabID="11" tabName11="Anforderung" tabName12="Antwort" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/storage/folder/myFolder/subFolder" \
     -H "Authorization: Bearer {access_token}" \
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

Die Verwendung eines SDKs ist der beste Weg, die Entwicklung zu beschleunigen. Ein SDK verwaltet die Details auf unterster Ebene und lässt Sie sich auf Ihre Projektaufgaben konzentrieren. Bitte besuchen Sie das <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub-Repository</a> für eine vollständige Liste der Aspose.Cells Cloud SDKs.

Die folgenden Codebeispiele zeigen, wie Aufrufe an Aspose.Cells-Webdienste unter Verwendung verschiedener SDKs durchgeführt werden:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_CreateFolder.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_CreateFolder.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_CreateFolder.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_CreateFolder.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_CreateFolder.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_CreateFolder.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_CreateFolder.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_CreateFolder.go" >}}
{{</tab>}}
{{< /tabs >}}