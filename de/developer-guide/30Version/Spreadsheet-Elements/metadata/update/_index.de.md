---
title: "Metadaten aktualisieren"
second_title: "Dokument"
linktitle: "Aktualisierung ohne Verwendung von Speicher"
type: docs
url: /metadata/update/
keywords: "Metadaten, Excel, Aspose.Cells Cloud, REST API, aktualisieren, Tabellenkalkulation"
description: "Die Aspose.Cells Cloud REST API ermöglicht die Aktualisierung von Metadaten in Excel-Dateien. Sie unterstützt mehrere SDKs (C#, Java, Python, Ruby, Go usw.), um eine nahtlose Integration in verschiedene Programmiersprachen zu gewährleisten."
weight: 35
ArticleTitle: "Metadaten aktualisieren – Aspose.Cells Cloud API-Dokumentation"
---

Diese REST API aktualisiert **Metadaten** in mehreren Excel-Dateien.

**Voraussetzungen:** Ein aktives Aspose Cloud-Konto, ein gültiges JWT-Zugriffstoken sowie die hochzuladenden Excel-Dateien.

## REST API

```bash
POST https://api.aspose.cloud/v3.0/cells/metadata/update
```

### **Sicherheit und Authentifizierung**

Die Aspose.Cells Cloud APIs sind sicher und erfordern eine <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-Token-basierte Authentifizierung</a>.

### Anforderungsparameter

| Parametername      | Typ    | Speicherort      | Beschreibung                                   |
| ------------------ | ------ | ---------------- | ---------------------------------------------- |
| file               | Datei  | formData         | Die hochzuladende Excel-Datei.                 |
| DocumentProperties | Objekt | HTTP-Body (JSON) | Dokumenteigenschaften, die für die Excel-Datei festgelegt werden sollen. |

**Hinweise:** In einer einzigen Anforderung können bis zu 10 Dateien hochgeladen werden. Unterstützte Formate sind `.xlsx`, `.xls` und `.csv`. Die Gesamtanforderungsgröße darf 100 MB nicht überschreiten.

Die [OpenAPI-Spezifikation](https://apireference.aspose.cloud/cells/#/PostMetadata) definiert eine öffentlich zugängliche Programmierschnittstelle und ermöglicht REST-Interaktionen direkt aus einem Webbrowser.

Sie können das cURL-Befehlszeilentool verwenden, um einfach auf Aspose.Cells-Webdienste zuzugreifen. Das folgende Beispiel zeigt, wie mithilfe von cURL Aufrufe an die Cloud-API durchgeführt werden.

{{< tabs tabTotal="2" tabID="11" tabName11="Anforderung" tabName12="Antwort" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/metadata/update" \
  -X POST \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>" \
  -F 'xxxxx1=@xxxx1.xlsx' \
  -F 'xxxxx2=@xxxx2.xlsx' \
  -d '[{ "name": "test", "value": "test" }]'
```

Die Anforderung erfordert einen **Authorization**-Header mit einem Bearer-JWT-Token. Stellen Sie sicher, dass das Token mithilfe Ihrer Aspose Cloud-Clientanmeldeinformationen generiert wurde.

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Files": [
    {
      "Filename": "xxxxx",
      "FileSize": 274022,
      "FileContent": "-----Base64String--------"
    },
    {
      "Filename": "xxxxx",
      "FileSize": 274022,
      "FileContent": "-----Base64String--------"
    }
  ]
}
```

{{< /tab >}}

{{< /tabs >}}

## Cloud SDK-Familie

Die Verwendung eines SDKs ist der beste Weg, die Entwicklung zu beschleunigen. Ein SDK übernimmt die Low-Level-Details, sodass Sie sich auf Ihre ProjektAufgaben konzentrieren können. Besuchen Sie das [GitHub-Repository](https://github.com/aspose-cells-cloud), um eine vollständige Liste der Aspose.Cells Cloud SDKs zu erhalten.

Die folgenden Codebeispiele zeigen, wie Aspose.Cells-Webdienste mithilfe verschiedener SDKs aufgerufen werden:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostMetadata.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostMetadata.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostMetadata.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostMetadata.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostMetadata.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostMetadata.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostMetadata.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostMetadata.go" >}}

{{< /tab >}}

{{< /tabs >}}

**Siehe auch:**  
- [Metadaten abrufen](/metadata/get/)  
- [Metadaten löschen](/metadata/delete/)  
---