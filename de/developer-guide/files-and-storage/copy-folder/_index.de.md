---
title: "Aspose.Cells Cloud Folder Copy API – Schnelles Kopieren von Ordnern in der Cloud"
second_title: "Dokument"
ArticleTitle: "Cloud-basierte Excel-Dateiverwaltungslösung – Detaillierte Erklärung der Stapelkopierfunktion der Aspose.Cells Copy Folder API"
linktype: "docs"
url: /de/copy-folder/
keywords: "Ordner kopieren, Aspose.Cells Cloud, REST API, Cloud-Speicher, Tabellenkalkulationsverwaltung"
description: "Erfahren Sie, wie Sie Ordner im Aspose.Cells Cloud-Speicher mit einem einzigen REST-Aufruf kopieren. Enthält Endpunkt, Parameter, Beispielanfragen, Fehlercodes und SDK-Beispiele."
weight: 100
---

Die **CopyFolder**-API dupliziert einen vorhandenen Ordner im Aspose.Cells Cloud-Speicher. Dies ist nützlich, um Sicherungskopien zu erstellen, Daten neu zu organisieren oder eine Ordnerstruktur für weitere Verarbeitungsschritte vorzubereiten, ohne manuelle Dateibewegungen durchführen zu müssen.

## **Excel-API: Ordner kopieren**

### Web-API

```
PUT https://api.aspose.cloud/v4.0/cells/storage/folder/copy/{srcPath}
```

### **Sicherheit und Authentifizierung**

Die Aspose.Cells Cloud APIs sind sicher und erfordern eine <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-Token-basierte Authentifizierung</a>.

### Die CopyFolder API akzeptiert folgende Parameter

| Parametername     | Erforderlich | Typ    | Speicherort (Pfad/Abfrage) | Beschreibung                                                                 |
| ----------------- | ------------ | ------ | ------------------------- | --------------------------------------------------------------------------- |
| `srcPath`         | Ja           | String | Pfad                      | Der Pfad des zu kopierenden Quellordners.                                   |
| `destPath`        | Ja           | String | Abfrage                   | Der Pfad, unter dem der neue Ordner erstellt werden soll.                   |
| `srcStorageName`  | Nein         | String | Abfrage                   | Der Name des Speichers, der den Quellordner enthält.                        |
| `destStorageName` | Nein         | String | Abfrage                   | Der Name des Ziel-Speichers, in den der Ordner kopiert werden soll.         |

### Beispielantwort

Ein erfolgreicher Aufruf gibt **HTTP 200** mit einem leeren JSON-Body zurück:

```json
{}
```

**Beispiel-cURL-Anfrage**

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/storage/folder/copy/MyFolder?destPath=MyFolderCopy" \
     -H "Authorization: Bearer {access_token}"
```

**HTTP-Statuscodes**

| Code | Bedeutung             | Beschreibung                                                     |
| ---- | --------------------- | --------------------------------------------------------------- |
| 200  | OK                    | Filter erfolgreich angewendet; Antwort enthält Vorgangsdetails. |
| 400  | Bad Request           | Fehlende oder ungültige Parameter (z. B. nicht unterstützter Dateityp). |
| 401  | Unauthorized          | Ungültiges oder fehlendes JWT-Token.                            |
| 413  | Payload Too Large     | Die hochgeladene Datei überschreitet das Größenlimit.           |
| 500  | Internal Server Error | Unerwarteter Serverfehler.                                      |

## OpenAPI-Spezifikation

Die [OpenAPI-Spezifikation](https://reference.aspose.cloud/cells/#/FolderController/CopyFolder) definiert eine öffentlich zugängliche Programmierschnittstelle und ermöglicht REST-Interaktionen direkt aus einem Webbrowser.

Sie können das cURL-Befehlszeilentool nutzen, um Aspose.Cells-Webservices einfach anzusprechen. Das folgende Beispiel zeigt, wie Sie mit cURL Aufrufe an die Cloud-API durchführen.

{{< tabs tabTotal="2" tabID="11" tabName11="Anfrage" tabName12="Antwort" >}}

{{< tab tabNum="11" >}}

```http
PUT https://api.aspose.cloud/v4.0/cells/storage/folder/copy/MyFolder?destPath=MyFolderCopy
Authorization: Bearer {access_token}
Content-Type: application/json
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```
{
}
```

{{< /tab >}}

{{< /tabs >}}
Die Verwendung eines SDKs ist der beste Weg, um die Entwicklungsgeschwindigkeit zu erhöhen. Ein SDK übernimmt die Low-Level-Details und ermöglicht es Ihnen, sich auf Ihre Projektaufgaben zu konzentrieren. Eine vollständige Liste der Aspose.Cells Cloud SDKs finden Sie im [GitHub-Repository](https://github.com/aspose-cells-cloud).

Die folgenden Codebeispiele zeigen, wie Aufrufe an Aspose.Cells-Webservices mit verschiedenen SDKs durchgeführt werden:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_CopyFolder.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_CopyFolder.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_CopyFolder.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_CopyFolder.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_CopyFolder.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_CopyFolder.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_CopyFolder.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_CopyFolder.go" >}}
{{</tab>}}
{{< /tabs >}}