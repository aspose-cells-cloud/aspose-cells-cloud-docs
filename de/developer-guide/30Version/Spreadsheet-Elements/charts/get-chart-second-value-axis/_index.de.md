---
title: "Zweite Wertachse eines Diagramms abrufen"
type: docs
url: /charts/second-value-axis/get/
weight: 60
keywords: Aspose.Cells, zweite Wertachse eines Diagramms, Excel, REST-API, Cloud, API, Excel-Diagramm-Achse
description: Ruft die zweite Wertachse eines angegebenen Diagramms in einer Excel-Arbeitsmappe mithilfe der Aspose.Cells Cloud REST-API ab.
ArticleTitle: "Zweite Wertachse eines Diagramms abrufen – Aspose.Cells Cloud API"
---

Diese REST-API ruft die zweite Wertachse eines Diagramms ab.

## GetChartSecondValueAxis API

```http
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/charts/{chartIndex}/secondvalueaxis
```

### **Sicherheit und Authentifizierung**

Die Aspose.Cells Cloud APIs sind sicher und erfordern eine <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-Token-basierte Authentifizierung</a>.

### Anforderungsparameter

| Parametername   | Typ    | Ort   | Beschreibung                                           |
| --------------- | ------ | ----- | ------------------------------------------------------ |
| name            | string | path  | Der Name der Excel-Datei.                              |
| sheetName       | string | path  | Der Name des Arbeitsblatts, das das Diagramm enthält. |
| chartIndex      | integer| path  | Der nullbasierte Index des Diagramms.                  |
| folder          | string | query | Der Ordner, in dem die Datei gespeichert ist.         |
| storageName     | string | query | Der Name des Aspose Cloud-Speichers.                   |

**Voraussetzungen**: Ein gültiges JWT-Zugriffstoken, das über den Aspose Cloud OAuth2-Flow erhalten wurde, muss im `Authorization`-Header jeder Anforderung übermittelt werden.

Die [OpenAPI-Spezifikation](https://apireference.aspose.cloud/cells/#/Charts/GetChartSecondValueAxis) definiert eine öffentlich zugängliche Programmierschnittstelle und ermöglicht REST-Interaktionen direkt aus einem Webbrowser.

Sie können das cURL-Befehlszeilentool nutzen, um Aspose.Cells-Webservices problemlos aufzurufen. Das folgende Beispiel zeigt, wie ein Aufruf der Cloud-API mit cURL erfolgt. Alle Aspose Cloud-Endpunkte erfordern HTTPS.

{{< tabs tabTotal="2" tabID="1" tabName1="Anforderung" tabName2="Antwort" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/" \
  -X GET \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Code": 200,
  "Status": "OK",
  "Axis": {
    "AxisId": 1,
    "IsVisible": true,
    "MinimumScale": 0,
    "MaximumScale": 100,
    "MajorUnit": 10,
    "MinorUnit": 5,
    "Title": "Zweite Wertachse"
  }
}
```

**Antwortfelder**

- **Code** – HTTP-Statuscode des Vorgangs (z. B. `200` für Erfolg).  
- **Status** – Textuelle Beschreibung des Status (`"OK"` für Erfolg).  
- **Axis** – Objekt mit Details zur zweiten Wertachse:  
  - **AxisId** – Bezeichner der Achse.  
  - **IsVisible** – Boolescher Wert, der angibt, ob die Achse angezeigt wird.  
  - **MinimumScale** – Minimalwert, der auf der Achse angezeigt wird.  
  - **MaximumScale** – Maximalwert, der auf der Achse angezeigt wird.  
  - **MajorUnit** – Abstand zwischen Haupttickmarks.  
  - **MinorUnit** – Abstand zwischen Nebentickmarks.  
  - **Title** – Titeltext der Achse.

**Fehlerantworten** (nicht 200)

- `400 Bad Request` – Ungültige Parameter oder fehlerhafte Anforderung.  
- `401 Unauthorized` – Fehlender oder ungültiges JWT-Token.  
- `404 Not Found` – Die angegebene Datei, das angegebene Arbeitsblatt oder das angegebene Diagramm existiert nicht.  
- `500 Internal Server Error` – Unerwarteter Serverfehler.

{{< /tab >}}

{{< /tabs >}}

## Cloud SDK-Familie

Die Verwendung eines SDKs ist die beste Möglichkeit, die Entwicklung zu beschleunigen. Ein SDK übernimmt die Low-Level-Details und ermöglicht es Ihnen, sich auf Ihre Projektaufgaben zu konzentrieren. Eine vollständige Liste der Aspose.Cells Cloud SDKs finden Sie im <a href="https://github.com/aspose-cells-cloud" target="_blank" rel="noopener noreferrer">GitHub-Repository</a>.

Die folgenden Codebeispiele zeigen, wie Aufrufe an Aspose.Cells-Webservices mit verschiedenen SDKs durchgeführt werden:

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

<!-- C# example placeholder -->

{{< /tab >}}

{{< tab tabNum="2" >}}

<!-- Java example placeholder -->

{{< /tab >}}

{{< tab tabNum="3" >}}

<!-- PHP example placeholder -->

{{< /tab >}}

{{< tab tabNum="4" >}}

<!-- Ruby example placeholder -->

{{< /tab >}}

{{< tab tabNum="5" >}}

<!-- Python example placeholder -->

{{< /tab >}}

{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example-Get-ChartSecondValueAxis.js" >}}
{{< /tab >}}

{{< tab tabNum="7" >}}

<!-- Android example placeholder -->

{{< /tab >}}

{{< tab tabNum="8" >}}

<!-- Swift example placeholder -->

{{< /tab >}}

{{< tab tabNum="9" >}}

<!-- Perl example placeholder -->

{{< /tab >}}

{{< tab tabNum="10" >}}

<!-- Go example placeholder -->

{{< /tab >}}

{{< /tabs >}}