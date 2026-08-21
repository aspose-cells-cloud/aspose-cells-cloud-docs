---
title: "Excel-Dateien sperren"
second_title: "Dokument"
linktitle: "Excel-Dateien sperren"
type: docs
url: /lock-excel-files/
aliases: [/lock/without-storage/, /lock/, /lock/without-using-storage/]
keywords: "Sperren, Excel, API, Aspose.Cells, Cloud, REST, Arbeitsmappe, Tabellenkalkulation, SDK"
description: "Erfahren Sie, wie Sie Excel-Arbeitsmappen mithilfe der Aspose.Cells Cloud REST API (v3.0) sperren können. Enthält HTTPS-Endpunkt, Authentifizierung, cURL-Anforderung, Antwort-Schema und SDK-Codebeispiele für C#, Java, Python und mehr."
ArticleTitle: "Excel-Dateien sperren – Aspose.Cells Cloud API-Dokumentation"
weight: 70
---

**API-Version:** v3.0 (aktuell)

Diese REST-API **sperrt** Excel-Arbeitsmappen.

## PostLock API

```http
POST https://api.aspose.cloud/v3.0/cells/lock
```

**Voraussetzungen** – Die Anforderung muss über **HTTPS** gesendet werden und einen gültigen OAuth 2.0-Bearer-Token im `Authorization`-Header enthalten.

### Die Anforderungsparameter sind

| Parametername | Typ   | Speicherort                   | Beschreibung                                     |
| ------------- | ----- | ----------------------------- | ------------------------------------------------ |
| file          | Datei | Formular-Daten (multipart body) | Die hochzuladende und zu sperrende Excel-Arbeitsmappe. |
| password      | Zeichenkette | Abfragezeichenfolge         | Passwort für die Arbeitsmappe (optional).        |

Die <a href="https://apireference.aspose.cloud/cells/#/LightCells/PostLock" target="_blank" rel="noopener noreferrer">OpenAPI-Spezifikation</a> definiert eine öffentlich zugängliche Programmierschnittstelle und ermöglicht es Ihnen, REST-Interaktionen direkt aus einem Webbrowser heraus durchzuführen.

Sie können das cURL-Befehlszeilentool verwenden, um problemlos auf Aspose.Cells-Webdienste zuzugreifen. Das folgende Beispiel zeigt, wie die Cloud-API mit cURL **aufgerufen** wird.

{{< tabs tabTotal="2" tabID="1" tabName1="Anforderung" tabName2="Antwort" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/lock?password=123456" \
  -X POST \
  -H "Content-Type: multipart/form-data" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <access_token>" \
  -F "file=@Sample.xlsx"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Files": [
    {
      "Filename": "Sample.xlsx",
      "FileSize": 274022,
      "FileContent": "-----Base64String--------"
    }
  ]
}
```

{{< /tab >}}

{{< /tabs >}}

*Sie können eine Beispieldatei herunterladen — [Sample.xlsx](https://example.com/Sample.xlsx) — um die Anforderung zu testen.*

**Hinweis:** Die API unterstützt Dateien bis zu einer Größe von 100 MB; größere Nutzdaten können zu einer Antwort mit dem Statuscode 413 („Payload Too Large“) führen.

### **Antwortdetails**

| Feld         | Typ             | Beschreibung                                           |
| ------------ | --------------- | ------------------------------------------------------ |
| Filename     | Zeichenkette    | Name der von dem Dienst zurückgegebenen gesperrten Arbeitsmappe. |
| FileSize     | Ganzzahl        | Größe der gesperrten Datei in Bytes.                   |
| FileContent  | Zeichenkette (Base64) | Die gesperrte Arbeitsmappe, codiert als Base64-Zeichenkette. |

Um die gesperrte Arbeitsmappe abzurufen, dekodieren Sie den `FileContent`-Wert von Base64 und speichern Sie ihn unter dem in der Antwort angegebenen `Filename`.

### **Fehlerbehandlung**

– Die API gibt Standard-HTTP-Statuscodes (z. B. `400 Bad Request`, `401 Unauthorized`, `500 Internal Server Error`) zusammen mit einem JSON-Fehlerobjekt zurück, das die Felder `Code` und `Message` enthält.

## Cloud SDK-Familie

Die Verwendung eines SDK ist der beste Weg, die Entwicklung zu beschleunigen. Ein SDK abstrahiert niedrigstufige Details, sodass Sie sich auf die Aufgaben Ihres Projekts konzentrieren können. Besuchen Sie das <a href="https://github.com/aspose-cells-cloud" target="_blank" rel="noopener noreferrer">GitHub-Repository</a>, um eine vollständige Liste der Aspose.Cells Cloud SDKs zu erhalten.

Die folgenden Codebeispiele zeigen, wie Aufrufe an Aspose.Cells-Webdienste mithilfe verschiedener SDKs durchgeführt werden:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostLock.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostLock.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostLock.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostLock.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostLock.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostLock.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostLock.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostLock.go" >}}

{{< /tab >}}

{{< /tabs >}}