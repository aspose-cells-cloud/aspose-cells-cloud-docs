---
title: "Formatierung des Diagrammbereichs abrufen – Aspose.Cells Cloud API (v3.0)"
type: docs
url: /de/charts/chart-area/fill-format/get/
aliases: [  /de/get-fill-format-of-a-chart-area-from-a-worksheet/ ]
weight: 70
keywords:
  - "Aspose.Cells"
  - "Diagrammbereich"
  - "Füllformat"
  - "REST API"
  - "Excel"
description: "Rufen Sie das Füllformat (Farbe, Muster, Farbverlauf) eines Diagrammbereichs in einer Excel-Arbeitsmappe über die Aspose.Cells Cloud API ab. Enthält cURL-Beispiel, SDK-Code-Snippets, Authentifizierungsschritte und Antwortdetails."
ArticleTitle: "Formatierung des Diagrammbereichs abrufen – Aspose.Cells Cloud API v3.0"
---

Diese REST-API ruft die Füllformatinformationen eines **Diagrammbereichs** ab.

**Voraussetzungen**  
Um diesen Endpunkt aufzurufen, benötigen Sie ein gültiges OAuth/JWT-Zugriffstoken. Holen Sie sich das Token über den Authentifizierungsflow der Aspose.Cells Cloud und fügen Sie es in den `Authorization`-Header als `Bearer <jwt token>` ein. Falls Sie eines der SDKs verwenden, stellen Sie sicher, dass das SDK mit Ihren `client_id`- und `client_secret`-Werten konfiguriert ist, bevor Sie die Methode aufrufen.

## GetChartAreaFillFormat API

```http
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/charts/{chartIndex}/chartArea/fillFormat
```

### **Sicherheit und Authentifizierung**

Die Aspose.Cells Cloud APIs sind sicher und erfordern eine <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-Token-basierte Authentifizierung</a>.

### Anforderungsparameter

| Parametername | Typ    | Ort   | Beschreibung                         |
| -------------- | ------- | ----- | ------------------------------------ |
| name           | string  | path  | Name der Arbeitsmappe.               |
| sheetName      | string  | path  | Name des Arbeitsblatts.              |
| chartIndex     | integer | path  | Index des Diagramms.                 |
| folder         | string  | query | Ordner, der die Arbeitsmappe enthält.|
| storageName    | string  | query | Name des Speichers.                  |

Die [OpenAPI-Spezifikation](https://apireference.aspose.cloud/cells/#/ChartArea/GetChartAreaFillFormat) definiert eine öffentlich zugängliche Programmierschnittstelle und ermöglicht REST-Interaktionen direkt aus einem Webbrowser.

Sie können das cURL-Befehlszeilentool verwenden, um auf die Aspose.Cells-Webdienste zuzugreifen. Das folgende Beispiel zeigt, wie die API mit cURL aufgerufen wird.

{{< tabs tabTotal="2" tabID="11" tabName11="Anforderung" tabName12="Antwort" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Sample_Test_Book.xls/worksheets/Sheet5/charts/0/chartArea/fillFormat" \
  -X GET \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "FillFormat": {
    "Type": "Automatic"
  },
  "Code": 200,
  "Status": "OK"
}
```

**Hinweise**  
- Ein erfolgreicher Aufruf gibt HTTP 200 mit den Details des Füllformats zurück.  
- HTTP 401 zeigt eine Authentifizierungsfehler an (ungültiges oder fehlendes Token).  
- HTTP 404 wird zurückgegeben, wenn die angegebene Arbeitsmappe, das Arbeitsblatt oder der Diagrammindex nicht existiert.  
- HTTP 500 kennzeichnet einen serverseitigen Fehler; wiederholen Sie die Anfrage oder kontaktieren Sie den Support, falls das Problem weiterhin besteht.

| Code | Bedeutung                                           |
|------|-----------------------------------------------------|
| 200  | Erfolg – Füllformat zurückgegeben                   |
| 401  | Nicht autorisiert – ungültiges oder fehlendes Token |
| 404  | Nicht gefunden – Arbeitsmappe, Arbeitsblatt oder Diagramm nicht gefunden |
| 500  | Interner Serverfehler                               |

Weitere verwandte Vorgänge finden Sie in den Endpunkten **Get Chart Area Border** (Rand des Diagrammbereichs abrufen) und **Get Chart Title** (Titel des Diagramms abrufen).

{{< /tab >}}

{{< /tabs >}}

## Cloud SDK Family

Die Verwendung eines SDKs ist der beste Weg, die Entwicklung zu beschleunigen. Ein SDK übernimmt die Details der niedrigen Ebene, sodass Sie sich auf Ihre Projekt Aufgaben konzentrieren können. Besuchen Sie das <a href="https://github.com/aspose-cells-cloud" target="_blank" rel="noopener noreferrer">GitHub-Repository</a>, um eine vollständige Liste der Aspose.Cells Cloud SDKs zu erhalten.

Die folgenden Codebeispiele zeigen, wie Aspose.Cells-Webdienste mit verschiedenen SDKs aufgerufen werden:

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Objective C" tabName8="Android" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNET-CSharp-Charts-GetChartFillFormat-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-chart-GetChartFillFormat-get-fill-format.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Charts-GetChartAreaFillFormat-.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Charts-get_chart_area_fill_format_info-.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "GetFillFormatOfChartAreaFromWorksheet.py" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-Charts-GetChartFillFormat-1.js" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "9d725d4678edaac53f95c5208e17783c" "Examples-Android-chart-GetChartFillFormat-get-fill-format.java" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-Charts-GetChartFillFormat-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< gist "aspose-cells-cloud-gists" "d9af13f9a5cf8dee333f8d5e26c32866" >}}

{{< /tab >}}

{{< /tabs >}}