---
title: "Hinzufügen eines Diagramms zu einem Arbeitsblatt"
type: docs
url: /charts/add/
aliases: [/add-a-chart-in-a-worksheet/]
weight: 20
description: "Erfahren Sie, wie Sie mithilfe der Aspose.Cells Cloud API v3.0 ein Diagramm zu einem Excel-Arbeitsblatt hinzufügen. Enthält Endpunkt, Parameter, cURL-Beispiel und SDK-Snippets."
keywords:
  - "Diagramm hinzufügen Aspose.Cells"
  - "Aspose.Cells Diagramm hinzufügen API"
  - "Diagramm-API REST"
  - "Aspose.Cells SDK-Beispiele"
ArticleTitle: "Hinzufügen eines Diagramms zu einem Arbeitsblatt – Aspose.Cells Cloud API-Anleitung"
---

Diese REST-API fügt ein neues Diagramm zu einem Arbeitsblatt hinzu.

**Voraussetzungen**  
Bevor Sie diesen Vorgang aufrufen, holen Sie sich ein gültiges JWT-Zugriffstoken und stellen Sie sicher, dass die Zielarbeitsmappe im angegebenen Ordner oder Speicherort gespeichert ist.

## PutWorksheetAddChart API

```http
PUT https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/charts
```

### **Sicherheit und Authentifizierung**

Die Aspose.Cells Cloud APIs sind sicher und erfordern eine <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-Token-basierte Authentifizierung</a>.

### Anforderungsparameter

| Parametername           | Typ     | Speicherort | Beschreibung                                                                                                                                                                                                 |
| ----------------------- | ------- | ----------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| **name**                | string  | path        | Name der Arbeitsmappe.                                                                                                                                                                                       |
| **sheetName**           | string  | path        | Name des Arbeitsblatts.                                                                                                                                                                                      |
| **chartType**           | string  | query       | Diagrammtyp (siehe Eigenschaft **Type** in der Diagrammressource). Unterstützte Diagrammtypen sind unter anderem **Bar**, **Column**, **Line**, **Pie**, **Scatter**, **Area**, **Doughnut**, **Radar** usw. |
| **upperLeftRow**        | integer | query       | Zeilenindex der oberen linken Ecke des Diagrammbereichs (0-basiert).                                                                                                                                        |
| **upperLeftColumn**     | integer | query       | Spaltenindex der oberen linken Ecke des Diagrammbereichs (0-basiert).                                                                                                                                       |
| **lowerRightRow**       | integer | query       | Zeilenindex der unteren rechten Ecke des Diagrammbereichs (0-basiert).                                                                                                                                      |
| **lowerRightColumn**    | integer | query       | Spaltenindex der unteren rechten Ecke des Diagrammbereichs (0-basiert).                                                                                                                                     |
| **area**                | string  | query       | Bereich, der die darzustellenden Werte bereitstellt (z. B. `A1:B5`).                                                                                                                                         |
| **isVertical**          | boolean | query       | Gibt an, ob die Diagrammausrichtung vertikal ist.                                                                                                                                                            |
| **categoryData**        | string  | query       | Bereich der Kategorieachsenwerte (z. B. `D1:E10`).                                                                                                                                                           |
| **isAutoGetSerialName** | boolean | query       | Wenn **true**, werden Seriennamen automatisch generiert.                                                                                                                                                    |
| **title**               | string  | query       | Titel des Diagramms.                                                                                                                                                                                         |
| **folder**              | string  | query       | Ordner, der die Arbeitsmappe enthält.                                                                                                                                                                        |
| **storageName**         | string  | query       | Name des Speichers.                                                                                                                                                                                          |
| **dataLabels**          | boolean | query       | Zeigt Datenbeschriftungen an, wenn **true**.                                                                                                                                                                 |
| **dataLabelsPosition**  | string  | query       | Position der Datenbeschriftungen (z. B. `Above`).                                                                                                                                                            |
| **pivotTableSheet**     | string  | query       | Name des Arbeitsblatts, das die Pivot-Tabelle enthält.                                                                                                                                                      |
| **pivotTableName**      | string  | query       | Name der Pivot-Tabelle.                                                                                                                                                                                      |

### **Antwort**

```json
{
    "Status":"OK",
    "Code":200
}
```

**HTTP-Statuscodes**

| Code | Bedeutung                   | Beschreibung                                                                                      |
|------|-----------------------------|---------------------------------------------------------------------------------------------------|
| 200  | OK                          | Filter erfolgreich angewendet; Antwort enthält Vorgangsdetails.                                  |
| 400  | Bad Request                 | Fehlende oder ungültige Parameter (z. B. nicht unterstützter Dateityp).                          |
| 401  | Unauthorized                | Ungültiges oder fehlendes JWT-Token.                                                             |
| 413  | Payload Too Large           | Die hochgeladene Datei überschreitet das Größenlimit.                                            |
| 500  | Internal Server Error       | Unerwarteter Serverfehler.                                                                        |

## Verwendung der PutWorksheetAddChart API mit SDKs

### PutWorksheetAddChart API-Spezifikation

Die [OpenAPI-Spezifikation](https://apireference.aspose.cloud/cells/#/Charts/PutWorksheetAddChart) definiert eine öffentlich zugängliche Programmierschnittstelle und ermöglicht REST-Interaktionen direkt aus einem Webbrowser.

Sie können das cURL-Befehlszeilentool verwenden, um problemlos auf Aspose.Cells-Webdienste zuzugreifen. Im folgenden Beispiel wird gezeigt, wie ein Aufruf der Cloud-API mit cURL durchgeführt wird.

{{< tabs tabTotal="2" tabID="11" tabName11="Anforderung" tabName12="Antwort" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/myWorkbook.xlsx/worksheets/Sheet1/charts?chartType=Bar&area=B1:F2&title=SalesState" \
-X PUT \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"
# Für diesen Vorgang ist kein Anforderungstext erforderlich
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

### Verwenden der Aspose.Cells Cloud SDKs

Die Verwendung eines SDK ist der beste Weg, die Entwicklung zu beschleunigen. Ein SDK abstrahiert die Low-Level-Details und ermöglicht es Ihnen, sich auf Ihre Projektaufgaben zu konzentrieren. Eine vollständige Liste der Aspose.Cells Cloud SDKs finden Sie im [GitHub-Repository](https://github.com/aspose-cells-cloud).

Die folgenden Codebeispiele zeigen, wie Aufrufe an Aspose.Cells-Webdienste mit verschiedenen SDKs durchgeführt werden:

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Objective C" tabName8="Perl" tabName9="Android" tabName10="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNET-CSharp-Charts-AddChart-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-chart-AddChart-1.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Charts-PutWorksheetAddChart-.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Charts-add_new_chart_to_worksheet-.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "AddChartToWorksheet.py" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-Charts-AddChart-1.js" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-Charts-AddChart-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Examples-Android-chart-AddChart-AddChart.jave" >}}

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< gist "aspose-cells-cloud-gists" "7fa79c30fca0c594c18c0f3937b6bcc9" >}}

{{< /tab >}}

{{< /tabs >}}