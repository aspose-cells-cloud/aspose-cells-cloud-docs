---
title: "Aspose.Cells Cloud API – Speicherplatzverbrauch abrufen | Echtzeit-Speichermetriken"
second_title: "Dokument"
ArticleTitle: "Cloud-basierte Excel-Dateiverwaltungslösung – Schnelle Abfrage des Speicherplatzverbrauchs in der Cloud."
linktype: "Get Disk Usage"
type: docs
url: /de/get-disk-usage/
keywords: "Aspose Cells, Cloud API, Speicherplatzverbrauch, Speichermetriken, Excel, REST"
description: "Rufen Sie den aktuellen Speicherplatzverbrauch für Aspose.Cells Cloud ab. Erfahren Sie mehr über den GET /v4.0/cells/storage/disk-Endpunkt, die erforderliche Authentifizierung und eine Beispiel-Antwort."
weight: 100
---

Der Vorgang **Speicherplatzverbrauch abrufen** gibt Echtzeit-Speichermetriken für Ihr Aspose.Cells Cloud-Konto zurück. Nutzen Sie diesen Endpunkt, um den verwendeten und den gesamten verfügbaren Speicherplatz zu überwachen.

- Ruft den aktuellen Speicherplatzverbrauch der Excel-API in der Aspose Cloud-Umgebung ab.
- Ermöglicht Entwicklern, den von ihren Anwendungen verbrauchten Speicherplatz zu überwachen.
- Ermöglicht eine proaktive Verwaltung von Speichergrenzen und Kostenkontrolle.

## Excel API: GetDiskUsage

### Web-API

```http
GET https://api.aspose.cloud/v4.0/cells/storage/disk
```

### **Sicherheit und Authentifizierung**

Die Aspose.Cells Cloud APIs sind sicher und erfordern eine <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-Token-basierte Authentifizierung</a>.

### Anforderungsparameter

| Parametername   | Typ    | Ort    | Beschreibung                                          | Erforderlich |
| --------------- | ------ | ------ | ----------------------------------------------------- | ------------ |
| storageName     | String | Query  | Der Name des Speichers, für den der Verbrauch abgerufen werden soll. | Optional     |

### **Antwort**

```json
{
  "Name": "DiskUsage",
  "Description": ["Klasse für Speicherplatzinformationen."],
  "Type": "Class",
  "IsAbstract": false,
  "Properties": [
    {
      "Name": "UsedSize",
      "Description": ["Menge des vom Anwendungsprogramm verwendeten Speicherplatzes."],
      "Nullable": true,
      "ReadOnly": false,
      "IsInherit": false,
      "DataType": {
        "Identifier": "Long",
        "Name": "long"
      }
    },
    {
      "Name": "TotalSize",
      "Description": ["Gesamter verfügbarer Speicherplatz."],
      "Nullable": true,
      "ReadOnly": false,
      "IsInherit": false,
      "DataType": {
        "Identifier": "Long",
        "Name": "long"
      }
    }
  ]
}
```

**HTTP-Statuscodes**

| Code | Bedeutung             | Beschreibung                                                      |
| ---- | --------------------- | ----------------------------------------------------------------- |
| 200  | OK                    | Filter erfolgreich angewendet; Antwort enthält Vorgangsdetails.  |
| 400  | Bad Request           | Fehlende oder ungültige Parameter (z. B. nicht unterstützter Dateityp). |
| 401  | Unauthorized          | Ungültiges oder fehlendes JWT-Token.                             |
| 413  | Payload Too Large     | Die hochgeladene Datei überschreitet die Größenbeschränkung.     |
| 500  | Internal Server Error | Unerwarteter Serverfehler.                                       |

## OpenAPI-Spezifikation

Die [OpenAPI-Spezifikation](https://reference.aspose.cloud/cells/#/StorageController/GetDiskUsage) definiert eine öffentlich zugängliche Programmierschnittstelle und ermöglicht REST-Interaktionen direkt aus einem Webbrowser.

Sie können das cURL-Befehlszeilentool verwenden, um problemlos auf Aspose.Cells-Webservices zuzugreifen. Das folgende Beispiel zeigt, wie Aufrufe an die Cloud-API mit cURL durchgeführt werden.

{{< tabs tabTotal="2" tabID="11" tabName11="Anforderung" tabName12="Antwort" >}}

{{< tab tabNum="11" >}}

```bash
curl -X GET "https://api.aspose.cloud/v4.0/cells/storage/disk?storageName=MyStorage" \
     -H "Authorization: Bearer IHRE_ZUGRIFFSTOKEN"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "UsedSize": 12345678,
  "TotalSize": 10737418240
}
```

{{< /tab >}}

{{< /tabs >}}

### Verwendung der Aspose.Cells Cloud SDKs

Die Verwendung eines SDKs ist der beste Weg, um die Entwicklung zu beschleunigen. Ein SDK übernimmt die Details der unteren Schicht, sodass Sie sich auf Ihre Projektaufgaben konzentrieren können. Bitte besuchen Sie das [GitHub-Repository](https://github.com/aspose-cells-cloud), um eine vollständige Liste der Aspose.Cells Cloud SDKs zu erhalten.

Die folgenden Codebeispiele zeigen, wie Aufrufe an Aspose.Cells-Webservices mit verschiedenen SDKs durchgeführt werden:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_GetDiskUsage.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_GetDiskUsage.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_GetDiskUsage.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_GetDiskUsage.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_GetDiskUsage.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_GetDiskUsage.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_GetDiskUsage.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_GetDiskUsage.go" >}}
{{</tab>}}
{{< /tabs >}}

---