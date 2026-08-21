---
title: "Aspose.Cells Cloud – GetFileVersions API – Schneller Zugriff auf die Dateiversionshistorie"
second_title: "Dokument"
ArticleTitle: "Cloud‑basiertes Excel‑Management – Ermitteln Sie die Dateiversionshistorie in Aspose.Cells Cloud"
linktype: "docs"
url: "/de/get-file-versions/"
keywords: "Aspose Cells API, Dateiversionen, Versionierung von Tabellenkalkulationen, Cloud‑Speicher-API, REST, Excel‑Dateiverlauf"
description: "Rufen Sie eine vollständige Liste der Versionshistorie für jede in Aspose.Cells Cloud gespeicherte Excel‑Datei ab. Unterstützt die Speichererauswahl, Authentifizierung und detaillierte Fehlercodes."
weight: 100
---

Rufen Sie eine vollständige Liste der Versionsdatensätze für eine bestimmte Tabellenkalkulation ab, die in Aspose.Cells Cloud gespeichert ist. Dieser Endpunkt ermöglicht es Entwicklern, Änderungen nachzuverfolgen, Änderungen zu auditieren und Versionierungsworkflows direkt aus dem Cloud‑Speicher heraus zu implementieren.

Die **GetFileVersions** API gibt alle Versionsdatensätze für eine angegebene Tabellenkalkulation zurück, die in Aspose.Cells Cloud gespeichert ist. Sie hilft Ihnen, einen vollständigen Änderungsverlauf für jede Datei zu pflegen.

## **Excel API: Get File Versions**

### Web-API

```
GET https://api.aspose.cloud/v4.0/cells/storage/version/{path}
```

### **Sicherheit und Authentifizierung**

Die Aspose.Cells Cloud APIs sind sicher und erfordern eine <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-Token-basierte Authentifizierung</a>.

### Die Anforderungsparameter der **GetFileVersions** API lauten

| Parametername | Typ    | Speicherort | Beschreibung                                                                                      |
| ------------- | ------ | ----------- | ------------------------------------------------------------------------------------------------- |
| `path`        | String | Pfad        | **Erforderlich.** Vollständiger Pfad zur Datei, deren Versionen abgerufen werden sollen.        |
| `storageName` | String | Abfrage     | Optional. Name des Speichers, der die Datei enthält. Falls nicht angegeben, wird der Standard verwendet. |

### **Antwort**

```json
{
  "Name": "FileVersions",
  "Description": [
    "Enthält eine Liste der Dateiversionen für das angegebene Dokument."
  ],
  "Type": "Class",
  "IsAbstract": false,
  "Properties": [
    {
      "Name": "Value",
      "Description": ["Eine Sammlung von Details zu den Dateiversionen."],
      "Nullable": true,
      "ReadOnly": false,
      "IsInherit": false,
      "DataType": {
        "Identifier": "Container",
        "Reference": "FileVersion",
        "ElementDataType": {
          "Identifier": "Class",
          "Reference": "FileVersion",
          "Name": "class:fileversion"
        },
        "Name": "container"
      }
    }
  ]
}
```

Im Erfolgsfall gibt die API **HTTP 200 OK** mit einer JSON‑Payload zurück, die das `Value`-Array mit Dateiversionsobjekten enthält, wie oben dargestellt.

**HTTP‑Statuscodes**

| Code | Bedeutung             | Beschreibung                                                       |
| ---- | --------------------- | ------------------------------------------------------------------ |
| 200  | OK                    | Filter erfolgreich angewendet; Antwort enthält Operationsdetails. |
| 400  | Bad Request           | Fehlende oder ungültige Parameter (z. B. nicht unterstützter Dateityp). |
| 401  | Unauthorized          | Ungültiges oder fehlendes JWT‑Token.                              |
| 413  | Payload Too Large     | Die hochgeladene Datei überschreitet die Größeinschränkung.       |
| 500  | Internal Server Error | Unerwarteter Serverfehler.                                        |

## OpenAPI-Spezifikation

Die [OpenAPI-Spezifikation](https://reference.aspose.cloud/cells/#/StorageController/GetFileVersions) bietet eine umfassende Programmierschnittstelle für die Durchführung von REST-Interaktionen direkt aus einem Webbrowser.

Sie können das cURL-Befehlszeilentool verwenden, um problemlos auf die Aspose.Cells-Webservices zuzugreifen. Das folgende Beispiel zeigt, wie Aufrufe an die Cloud-API mit cURL durchgeführt werden.

{{< tabs tabTotal="2" tabID="11" tabName11="Anforderung" tabName12="Antwort" >}}

{{< tab tabNum="11" >}}

```bash
curl -X GET "https://api.aspose.cloud/v4.0/cells/storage/version/MyFolder/MyFile.xlsx" \
     -H "Authorization: Bearer {access_token}" \
     -H "Accept: application/json"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Value": [
    {
      "VersionId": "1",
      "IsLatest": false,
      "ModifiedDate": "2024-01-15T12:34:56Z",
      "Size": 10240
    },
    {
      "VersionId": "2",
      "IsLatest": true,
      "ModifiedDate": "2024-03-01T08:22:10Z",
      "Size": 10300
    }
  ]
}
```

{{< /tab >}}

{{< /tabs >}}

### Verwendung der Aspose.Cells Cloud SDKs

Die Verwendung eines SDKs vereinfacht die Entwicklung, indem komplexe Details abstrahiert werden, sodass sich Entwickler auf die Kernfunktionen konzentrieren können. Besuchen Sie das [GitHub-Repository](https://github.com/aspose-cells-cloud), um eine vollständige Liste der Aspose.Cells Cloud SDKs zu erhalten.

Die folgenden Codebeispiele zeigen, wie Sie mit Aspose.Cells-Webservices in verschiedenen Programmiersprachen interagieren können:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_GetFileVersions.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_GetFileVersions.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_GetFileVersions.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_GetFileVersions.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_GetFileVersions.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_GetFileVersions.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_GetFileVersions.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_GetFileVersions.go" >}}
{{</tab>}}
{{< /tabs >}}

---