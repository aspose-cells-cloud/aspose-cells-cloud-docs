---
title: "Legende eines Diagramms in einem Excel-Arbeitsblatt ausblenden – Aspose.Cells Cloud API"
type: docs
url: /charts/legend/hide/
aliases: [/hide-chart-legend-in-a-worksheet/]
weight: 110
keywords: "Aspose.Cells, Excel, Diagrammlegende ausblenden, REST-API, Cloud-SDK, Diagrammlegende"
description: "Erfahren Sie, wie Sie die Legende eines Diagramms in einem Excel-Arbeitsblatt mithilfe der Aspose.Cells Cloud REST API ausblenden. Enthält HTTPS-Endpunkt, erforderliche Authentifizierung, Anforderungssyntax, Antwortdetails, Fehlerbehandlung und SDK-Beispiele."
---

Diese REST-API blendet die Legende in einem Diagramm aus. Eine **Diagrammlegende** ist das Feld, das die im Diagramm dargestellten Datenreihen identifiziert.

Die API erfordert ein gültiges Aspose Cloud JWT-Token, die Arbeitsmappe muss in den Aspose Cloud-Speicher hochgeladen sein, und die verwendete API-Version ist **v3.0**.

## Sicherheit und Authentifizierung
Die Aspose.Cells Cloud APIs sind sicher und erfordern eine [JWT-Token-basierte Authentifizierung](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/).

## REST-API

```http
DELETE https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/charts/{chartIndex}/legend
```

### Anforderungsparameter

| Parametername   | Typ     | Ort    | Beschreibung                          |
| --------------- | ------- | ------ | ------------------------------------- |
| **name**        | string  | path   | Name der Arbeitsmappe.                |
| **sheetName**   | string  | path   | Name des Arbeitsblatts.               |
| **chartIndex**  | integer | path   | Index des Diagramms.                  |
| **folder**      | string  | query  | Ordner der Arbeitsmappe (optional).   |
| **storageName** | string  | query  | Name des Speichers (optional).        |

Die [OpenAPI-Spezifikation](https://apireference.aspose.cloud/cells/#/Charts/DeleteWorksheetChartLegend) definiert diese öffentlich zugängliche Programmierschnittstelle.

Sie können das cURL-Befehlszeilentool verwenden, um die API einfach aufzurufen. Das folgende Beispiel zeigt eine Anforderung, die die Legende des Diagramms 0 in _Sample_Test_Book.xls_ ausblendet.

{{< tabs tabTotal="2" tabID="11" tabName11="Anforderung" tabName12="Antwort" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Sample_Test_Book.xls/worksheets/Sheet5/charts/0/legend" \
  -X DELETE \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

## Antworten

| HTTP-Status                   | Beschreibung                                            | Beispiel-JSON                                                 |
| ----------------------------- | ------------------------------------------------------- | ------------------------------------------------------------- |
| **200 OK**                    | Legende erfolgreich ausgeblendet.                       | `{ "Code": 200, "Status": "OK" }`                             |
| **401 Unauthorized**          | Fehlendes oder ungültiges JWT-Token.                   | `{ "Code": 401, "Message": "Invalid access token." }`         |
| **404 Not Found**             | Arbeitsmappe, Arbeitsblatt oder Diagramm existiert nicht. | `{ "Code": 404, "Message": "Chart not found." }`              |
| **500 Internal Server Error** | Unerwarteter Serverfehler.                              | `{ "Code": 500, "Message": "An unexpected error occurred." }` |

## Häufig gestellte Fragen (FAQ)

**Q:** _Wie blende ich die Legende eines Diagramms mit Aspose.Cells Cloud aus?_  
**A:** Senden Sie eine `DELETE`-Anforderung an `https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/charts/{chartIndex}/legend` mit einem gültigen JWT-Token im `Authorization`-Header. Eine Antwort mit `200 OK` zeigt an, dass der Vorgang erfolgreich war.

**Q:** _Welche Authentifizierung ist für die API zum Ausblenden der Diagrammlegende erforderlich?_  
**A:** Geben Sie einen Header `Authorization: Bearer <jwt token>` an. Das Token erhalten Sie über den Aspose Cloud OAuth-Flow.

**Q:** _Welche Fehlerantwort erhalte ich, wenn der Diagrammindex ungültig ist?_  
**A:** Der Dienst gibt `404 Not Found` zurück, mit einem JSON-Body, der `Code: 404` und eine Nachricht enthält, die das fehlende Diagramm beschreibt.

**Q:** _Kann ich HTTP anstelle von HTTPS verwenden?_  
**A:** Nein. Alle Aspose Cloud-Endpunkte erfordern HTTPS aus Sicherheitsgründen.

## Cloud SDK-Familie

Die Verwendung eines SDKs ist die schnellste Möglichkeit zur Entwicklung. Ein SDK abstrahiert die Low-Level-Details, sodass Sie sich auf Ihre Projekt Aufgaben konzentrieren können. Eine vollständige Liste der Aspose.Cells Cloud SDKs finden Sie im [GitHub-Repository](https://github.com/aspose-cells-cloud).

Die folgenden Codebeispiele zeigen, wie Aspose.Cells-Webservices mit verschiedenen SDKs aufgerufen werden:

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNET-CSharp-Charts-HideChartLegend-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-chart-HideChartLegend-hide-chart-legend.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Charts-DeleteWorksheetChartLegend-.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Charts-hide_legend_in_chart-.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "HideChartLegendInWorkSheet.py" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-Charts-HideChartLegend-1.js" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "9d725d4678edaac53f95c5208e17783c" "Examples-Android-chart-HideChartLegend-hide-chart-legend.java" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}
**Demnächst verfügbar** – Swift SDK-Beispiel wird in Kürze hinzugefügt.  
{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-Charts-HideChartLegend-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< gist "aspose-cells-cloud-gists" "3eb15aa10e3d2cd8931e60f8d001fd1c" >}}

{{< /tab >}}

{{< /tabs >}}

<script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@type": "WebPage",
  "name": "Legende eines Diagramms in einem Excel-Arbeitsblatt ausblenden – Aspose.Cells Cloud API",
  "description": "Schritt-für-Schritt-Anleitung zum Ausblenden der Diagrammlegende in einem Excel-Arbeitsblatt mithilfe der Aspose.Cells Cloud REST API. Enthält HTTPS-Endpunkt, Authentifizierung, Anforderungssyntax, Antwortdetails, Fehlerbehandlung und SDK-Beispiele.",
  "breadcrumb": {
    "@type": "BreadcrumbList",
    "itemListElement": [
      { "@type": "ListItem", "position": 1, "name": "Startseite", "item": "https://docs.aspose.cloud/" },
      { "@type": "ListItem", "position": 2, "name": "Cells", "item": "https://docs.aspose.cloud/cells/" },
      { "@type": "ListItem", "position": 3, "name": "Charts", "item": "https://docs.aspose.cloud/cells/charts/" },
      { "@type": "ListItem", "position": 4, "name": "Legende eines Diagramms ausblenden", "item": "https://docs.aspose.cloud/cells/charts/legend/hide/" }
    ]
  },
  "about": "Diagrammlegende mit Aspose.Cells Cloud API ausblenden"
}
</script>