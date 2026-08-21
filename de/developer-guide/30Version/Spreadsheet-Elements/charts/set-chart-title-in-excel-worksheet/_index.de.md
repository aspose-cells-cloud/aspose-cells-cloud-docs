---
title: "Aspose.Cells Cloud API – Diagrammtitel in einer Excel-Arbeitsmappe festlegen"
type: docs
url: /de/chart/title/add/
aliases: [  /de/set-chart-title-in-excel-worksheet/ ]
weight: 30
keywords: "Aspose.Cells Cloud, API für Diagrammtitel, Excel-Diagrammtitel, REST API, SDK-Beispiele"
description: "Erfahren Sie, wie Sie mithilfe der Aspose.Cells Cloud REST API einen Diagrammtitel in einer Excel-Arbeitsmappe hinzufügen oder aktualisieren. Enthält cURL-Beispiele, SDK-Beispiele, erforderliche Parameter, Authentifizierungsschritte und Fehlerbehandlung."
---

Fügt einen Diagrammtitel hinzu oder macht einen vorhandenen Titel sichtbar.

## PutWorksheetChartTitle API

```http
PUT http://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/charts/{chartIndex}/title
```

### **Sicherheit und Authentifizierung**

Die Aspose.Cells Cloud APIs sind sicher und erfordern eine <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-Token-basierte Authentifizierung</a>.

### Anforderungsparameter

| Parametername | Typ     | Ort      | Beschreibung                                |
| ------------- | ------- | -------- | ------------------------------------------- |
| name          | string  | path     | Name der Arbeitsmappe.                      |
| sheetName     | string  | path     | Name des Arbeitsblatts.                     |
| chartIndex    | integer | path     | Index des Diagramms.                        |
| title         | string  | body     | Text des Diagrammtitels.                    |
| folder        | string  | query    | Ordner, der die Arbeitsmappe enthält.       |
| storageName   | string  | query    | Name des Speichers.                         |

Die [OpenAPI-Spezifikation](https://apireference.aspose.cloud/cells/#/Charts/PutWorksheetChartTitle) definiert eine öffentlich zugängliche Programmierschnittstelle und ermöglicht Ihnen, REST-Interaktionen direkt aus einem Webbrowser durchzuführen.

Sie können das cURL-Befehlszeilentool nutzen, um Aspose.Cells-Webdienste einfach aufzurufen. Das folgende Beispiel zeigt, wie ein Aufruf an die Cloud API mit cURL durchgeführt wird.

{{< tabs tabTotal="2" tabID="11" tabName11="Anforderung" tabName12="Antwort" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "http://api.aspose.cloud/v3.0/cells/Sample_Test_Book.xls/worksheets/Sheet5/charts/0/title" \
  -d '{"Text":"Verkaufsdigramm"}' \
  -X PUT \
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

**Fehlerantworten**

| HTTP-Code | Beispiel-Payload                                                                       | Beschreibung                                               |
| --------- | -------------------------------------------------------------------------------------- | ---------------------------------------------------------- |
| 400       | `{ "Code": "400", "Message": "Ungültige Anforderungsnutzlast." }`                      | Der Anforderungstext ist fehlerhaft oder benötigte Felder fehlen. |
| 401       | `{ "Code": "401", "Message": "Authentifizierung fehlgeschlagen. Ungültiges oder abgelaufenes JWT-Token." }` | Das Bearer-Token fehlt, ist ungültig oder abgelaufen.      |
| 404       | `{ "Code": "404", "Message": "Arbeitsmappe, Arbeitsblatt oder Diagramm nicht gefunden." }` | Die angegebene Ressource existiert nicht.                  |
| 500       | `{ "Code": "500", "Message": "Interner Serverfehler." }`                               | Auf dem Server ist ein unerwarteter Fehler aufgetreten.   |

## Cloud SDK-Familie

Die Verwendung eines SDKs ist die schnellste Möglichkeit zur Entwicklung. Ein SDK abstrahiert die Low-Level-Details, sodass Sie sich auf Ihre Projektaufgaben konzentrieren können. Eine vollständige Liste der Aspose.Cells Cloud SDKs finden Sie im [GitHub-Repository](https://github.com/aspose-cells-cloud).

Die folgenden Codebeispiele zeigen, wie Aspose.Cells-Webdienste mithilfe verschiedener SDKs aufgerufen werden:

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNET-CSharp-Charts-SetChartTitle-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-chart-SetChartTitle-set-chart-title.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Charts-PutWorksheetChartTitle-.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Charts-add_chart_title-.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "SetChartTitle.py" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-Charts-SetChartTitle-1.js" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "9d725d4678edaac53f95c5208e17783c" "Examples-Android-chart-SetChartTitle-set-chart-title.java" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-Charts-SetChartTitle-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< gist "aspose-cells-cloud-gists" "728d523e11f8751f5f601bafb04ab86f" >}}

{{< /tab >}}

{{< /tabs >}}