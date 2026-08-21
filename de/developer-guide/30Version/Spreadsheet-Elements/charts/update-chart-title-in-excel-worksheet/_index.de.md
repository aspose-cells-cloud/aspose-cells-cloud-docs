---
title: "Diagrammtitel in Excel-Arbeitsmappe aktualisieren"
type: docs
url: /de/charts/title/update/
aliases: [  /de/update-chart-title-in-excel-worksheet/ ]
weight: 160
keywords: Excel, Aspose.Cells, REST API, Diagrammtitel, Aktualisieren, Cloud SDK
description: Erfahren Sie, wie Sie den Diagrammtitel in einer Excel-Arbeitsmappe mithilfe der Aspose.Cells Cloud REST API, cURL und verschiedenen SDKs aktualisieren.
ArticleTitle: "Diagrammtitel in Excel-Arbeitsmappe aktualisieren – Aspose.Cells Cloud-Dokumentation"
---

Diese REST API aktualisiert den Diagrammtitel.

**Voraussetzungen:** Sie benötigen ein gültiges Aspose Cloud-Konto sowie ein JWT-Token zur Autorisierung. Die typischen Schritte umfassen:

- Registrieren Sie sich für ein Aspose Cloud-Konto.  
- Generieren Sie ein JWT-Token über den Authentifizierungsendpunkt.  
- Stellen Sie sicher, dass die Zielarbeitsmappe in einem unterstützten Cloud-Speicher gespeichert ist (Standard- oder benutzerdefinierter Speicher).

## PostWorksheetChartTitle API

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/charts/{chartIndex}/title
```

Alle API-Aufrufe müssen über **HTTPS** erfolgen, um Warnungen aufgrund gemischter Inhalte zu vermeiden.

### **Sicherheit und Authentifizierung**

Die Aspose.Cells Cloud APIs sind sicher und erfordern eine <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-Token-basierte Authentifizierung</a>.

### Anforderungsparameter

| Parametername   | Typ    | Ort    | Beschreibung                         |
| --------------- | ------ | ------ | ------------------------------------ |
| name            | string | path   | Name der Arbeitsmappe.               |
| sheetName       | string | path   | Name des Arbeitsblatts.              |
| chartIndex      | integer| path   | Nullbasierter Index des Diagramms.   |
| title           | string | body   | Neuer Diagrammtitel.                 |
| folder          | string | query  | Ordner der Arbeitsmappe.             |
| storageName     | string | query  | Name des Speichers.                  |

### Antwortstatuscodes

| Code | Beschreibung                                                |
| ---- | ----------------------------------------------------------- |
| 200  | OK – Der Diagrammtitel wurde erfolgreich aktualisiert.     |
| 400  | Bad Request – Fehlende oder ungültige Parameter.           |
| 401  | Unauthorized – Ungültiges oder fehlendes JWT-Token.        |
| 404  | Not Found – Arbeitsmappe, Arbeitsblatt oder Diagramm nicht gefunden. |
| 500  | Internal Server Error – Unerwarteter Serverfehler.         |

**Hinweis:** Der `chartIndex` ist nullbasiert; das erste Diagramm auf einem Arbeitsblatt wird mit `0` referenziert.

Die <a href="https://apireference.aspose.cloud/cells/#/Charts/PostWorksheetChartTitle" target="_blank" rel="noopener noreferrer">OpenAPI-Spezifikation</a> definiert eine öffentlich zugängliche Programmierschnittstelle und ermöglicht REST-Interaktionen direkt aus einem Webbrowser.

Sie können das cURL-Befehlszeilentool verwenden, um problemlos auf Aspose.Cells-Webdienste zuzugreifen. Das folgende Beispiel zeigt, wie API-Aufrufe mit cURL durchgeführt werden.

{{< tabs tabTotal="2" tabID="11" tabName11="Anforderung" tabName12="Antwort" >}}

{{< tab tabNum="11" >}}

```bash
curl -v POST "https://api.aspose.cloud/v3.0/cells/Sample_Test_Book.xls/worksheets/Sheet5/charts/0/title" \
-d '{"title":"Börse"}' \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Code": "200",
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

## Cloud SDK-Familie

Die Verwendung eines SDKs ist die beste Möglichkeit, die Entwicklung zu beschleunigen. Ein SDK übernimmt die Details auf unterster Ebene und ermöglicht es Ihnen, sich auf die Aufgaben Ihres Projekts zu konzentrieren. Besuchen Sie das <a href="https://github.com/aspose-cells-cloud" target="_blank" rel="noopener noreferrer">GitHub-Repository</a> für eine vollständige Liste der Aspose.Cells Cloud SDKs.

Die folgenden Codebeispiele zeigen, wie Aufrufe an Aspose.Cells-Webdienste mit verschiedenen SDKs durchgeführt werden:

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNET-CSharp-Charts-UpdateChartTitle-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-chart-UpdateChartTitle-update-chart-title.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Charts-PostWorksheetChartTitle-.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Charts-update_chart_title-.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "UpdateChartTitleInExcelWorkbook.py" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-Charts-UpdateChartTitle-1.js" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "9d725d4678edaac53f95c5208e17783c" "Examples-Android-chart-UpdateChartTitle-update-chart-title.java" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-Charts-UpdateChartTitle-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< gist "aspose-cells-cloud-gists" "aab21ae55930321e6eaa46ffe5b8e7bf" >}}

{{< /tab >}}

{{< /tabs >}}
---