---
title: "Seitenlayout für ein Arbeitsblatt festlegen"
second_title: "Dokument"
linktitle: "Seitenlayout festlegen"
type: docs
url: /de/set-page-setup/
keywords: "Aspose.Cells, Excel, Seitenlayout, REST API, Arbeitsblatt, Cloud SDK"
description: "Erfahren Sie, wie Sie das Seitenlayout für ein Excel-Arbeitsblatt mithilfe der Aspose.Cells Cloud REST API festlegen. Enthält Anforderungsdetails, ein sicheres HTTPS-cURL-Beispiel, Antwort-Statuscodes und SDK-Codeausschnitte für mehrere Programmiersprachen."
weight: 20
ArticleTitle: "Seitenlayout für ein Arbeitsblatt festlegen – Aspose.Cells Cloud API-Anleitung"
---

Voraussetzungen: Um diese API aufzurufen, müssen Sie über ein gültiges JWT (OAuth)-Token verfügen, und die Arbeitsmappe muss sich in einem Aspose Cloud-Speicherort befinden, auf den Sie Lese-/Schreibrechte besitzen. Stellen Sie sicher, dass das Token im **Authorization**-Header enthalten ist und Ihr Konto über die erforderliche API-Quota verfügt.

Diese REST API legt das Seitenlayout für ein Excel-Arbeitsblatt fest.

## REST API

```bash
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/pagesetup
```

### **Sicherheit und Authentifizierung**

Die Aspose.Cells Cloud APIs sind sicher und erfordern eine <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-Token-basierte Authentifizierung</a>.

### **Anforderungsparameter**

| Parametername   | Typ    | Ort    | Beschreibung               |
| --------------- | ------ | ------ | -------------------------- |
| name            | string | path   | Dokumentname.              |
| sheetName       | string | path   | Name des Arbeitsblatts.    |
| pageSetup       | object | body   | Beschreibung des Seitenlayouts. |
| folder          | string | query  | Dokumentordner.            |
| storageName     | string | query  | Speichername.              |

**Beispiel-JSON-Payload für das `pageSetup`-Objekt**

```json
{
  "pageSetup": {
    "orientation": "Portrait",
    "paperSize": "A4",
    "fitToPagesTall": 1,
    "fitToPagesWide": 1,
    "centerHorizontally": true,
    "centerVertically": false
  }
}
```

Die <a href="https://reference.aspose.cloud/cells/#/PageSetup/PostPageSetup" target="_blank" rel="noopener noreferrer">OpenAPI-Spezifikation</a> definiert eine öffentlich zugängliche Programmierschnittstelle und ermöglicht es Ihnen, REST-Interaktionen direkt aus einem Webbrowser heraus durchzuführen.

Sie können das cURL-Befehlszeilentool verwenden, um problemlos auf Aspose.Cells-Webdienste zuzugreifen. Das folgende Beispiel zeigt, wie Sie mit cURL Aufrufe an die Cloud-API durchführen.

{{< tabs tabTotal="2" tabID="1" tabName1="Anforderung" tabName2="Antwort" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/myWorkbook.xlsx/worksheets/Tasks/pagesetup" \
-X POST \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>" \
-d '{
  "pageSetup": {
    "orientation": "Portrait",
    "paperSize": "A4",
    "fitToPagesTall": 1,
    "fitToPagesWide": 1,
    "centerHorizontally": true,
    "centerVertically": false
  }
}'
```

{{< /tab >}}

{{< tab tabNum="2" >}}

Die API gibt ein JSON-Objekt zurück, das das Ergebnis des Vorgangs angibt:

```json
{
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

**Mögliche Antwort-Statuscodes**

| Code | Bedeutung                   | Wenn                                                       |
|------|-----------------------------|------------------------------------------------------------|
| 200  | OK                          | Erfolgreiche Aktualisierung des Seitenlayouts             |
| 400  | Bad Request                 | Ungültige JSON-Payload oder fehlende erforderliche Felder |
| 401  | Unauthorized                | Fehlendes oder ungültiges JWT-Token                       |
| 404  | Not Found                   | Arbeitsmappe oder Arbeitsblattname existiert nicht        |
| 500  | Internal Server Error       | Unerwarteter Serverfehler                                  |

## Cloud SDK-Familie

Die Verwendung eines SDK ist der beste Weg, die Entwicklung zu beschleunigen. Ein SDK übernimmt Details auf niedriger Ebene und ermöglicht es Ihnen, sich auf Ihre Projekt Aufgaben zu konzentrieren. Bitte besuchen Sie das <a href="https://github.com/aspose-cells-cloud" target="_blank" rel="noopener noreferrer">GitHub-Repository</a>, um eine vollständige Liste der Aspose.Cells Cloud SDKs zu erhalten.

Die folgenden Codebeispiele zeigen, wie Aufrufe an Aspose.Cells-Webdienste mit verschiedenen SDKs durchgeführt werden:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example_PostPageSetup.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostPageSetup.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostPageSetup.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostPageSetup.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostPageSetup.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostPageSetup.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostPageSetup.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostPageSetup.go" >}}

{{< /tab >}}

{{< /tabs >}}