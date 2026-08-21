---
title: "Mehrere Excel-Dateien in einer einzigen Arbeitsmappe zusammenführen"
second_title: "Dokument"
linktitle: "Mehrere Excel-Dateien zusammenführen"
type: docs
url: /de/merge-multi-files-into-excel/
aliases: [  /de/merge/multi-files/ ]
keywords: "Aspose.Cells Cloud, mehrere Excel-Dateien zusammenführen, REST-API, Tabellenkalkulation zusammenführen, Cloud SDK"
description: "Erfahren Sie, wie Sie mehrere Excel-Arbeitsmappen mit der Aspose.Cells Cloud REST API (v3.0) in einer einzigen Datei zusammenführen. Enthält HTTPS-Endpunkt, cURL-Befehl, SDK-Beispiele, erforderliche Parameter und Details zur Fehlerbehandlung."
weight: 32
---

## REST API

Diese REST API führt mehrere Excel-Dateien in einer einzigen Excel-Arbeitsmappe zusammen.

```bash
POST https://api.aspose.cloud/v3.0/cells/merge
```

### **Sicherheit und Authentifizierung**

Die Aspose.Cells Cloud APIs sind sicher und erfordern eine <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-Token-basierte Authentifizierung</a>.


### Anforderungsparameter

| Parametername   | Typ     | Ort       | Beschreibung                                                                           | Erforderlich |
| ---------------- | ------- | --------- | -------------------------------------------------------------------------------------- | ------------ |
| files[]          | Datei   | formData  | Eine oder mehrere zusammenzuführende Excel-Arbeitsmappen. Verwenden Sie `file1`, `file2`, … in der Anfrage. | Ja           |
| format           | String  | query     | Gewünschtes Ausgabeformat (z. B. `xlsx`).                                              | Ja           |
| mergeToOneSheet  | Boolean | query     | Auf `true` setzen, um alle Arbeitsblätter in ein einziges Blatt zu kombinieren; Standard ist `false`. | Nein         |

### **Antwort**

```json
{
    "Status" : "OK",
    "Code" : 200,
    "Filename" : "[zusammengeführter Dateiname]",
    "Filesize" : [Dateigröße],
    "FileContent" : "[Base64-Zeichenfolge]"
}
```

**HTTP-Statuscodes**

| Code | Bedeutung                   | Beschreibung                                                |
|------|-----------------------------|-------------------------------------------------------------|
| 200  | OK                          | Filter erfolgreich angewendet; Antwort enthält Details zum Vorgang. |
| 400  | Bad Request                 | Fehlende oder ungültige Parameter (z. B. nicht unterstützter Dateityp). |
| 401  | Unauthorized                | Ungültiges oder fehlendes JWT-Token.                        |
| 413  | Payload Too Large           | Hochgeladene Datei überschreitet das Größenlimit.           |
| 500  | Internal Server Error       | Unerwarteter Serverfehler.                                  |

## So verwenden Sie die PostMerge-API mit SDKs

### PostMerge-API-Spezifikation

Die [OpenAPI-Spezifikation](https://apireference.aspose.cloud/cells/#/LightCells/PostMerge) definiert eine öffentlich zugängliche Programmierschnittstelle und ermöglicht REST-Interaktionen direkt aus einem Webbrowser.

Sie können das cURL-Befehlszeilentool verwenden, um Aspose.Cells-Webdienste einfach aufzurufen. Das folgende Beispiel zeigt, wie Sie mit cURL Aufrufe an die Cloud-API durchführen.

{{< tabs tabTotal="2" tabID="11" tabName11="Anforderung" tabName12="Antwort" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/merge?format=xlsx" \
  -X POST \
  -H "Authorization: Bearer <jwt token>" \
  -F "file1=@file1.xlsx" \
  -F "file2=@file2.xlsx"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  {
    "Filename": "file1.xlsx",
    "FileSize": 274022,
    "FileContent": "-----Base64-Zeichenfolge--------"
  }
}
```

{{< /tab >}}

{{< /tabs >}}

### Verwenden der Aspose.Cells Cloud SDKs

Die Verwendung eines SDKs ist der beste Weg, um die Entwicklung zu beschleunigen. Ein SDK übernimmt die Details der niedrigen Ebene, sodass Sie sich auf Ihre ProjektAufgaben konzentrieren können. Weitere Informationen finden Sie im [GitHub-Repository](https://github.com/aspose-cells-cloud) für eine vollständige Liste der Aspose.Cells Cloud SDKs.

Die folgenden Codebeispiele zeigen, wie Aspose.Cells-Webdienste mit verschiedenen SDKs aufgerufen werden:

{{< tabs tabTotal="9" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Android" tabName7="Perl" tabName8="Go" tabName9="Python" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example-Merge.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example-Merge.java" >}}
{{< /tab >}}

{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-LightCells-Merge.php" >}}
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
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "LightCellsMerge.py" >}}
{{< /tab >}}

{{< /tabs >}}

---