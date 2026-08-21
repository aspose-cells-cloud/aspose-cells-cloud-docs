---
title: "Kategorieachse eines Diagramms aktualisieren"
type: docs
url: /charts/category-axis/update/
weight: 160
keywords: "Aspose.Cells, Diagramm, Kategorieachse, REST API, Excel, Cloud SDK"
description: "Aktualisiert die Kategorieachse eines Diagramms in einer Excel-Arbeitsmappe mithilfe der Aspose.Cells Cloud REST API."
ArticleTitle: "Kategorieachse eines Diagramms aktualisieren – Aspose.Cells Cloud API"
---

Diese REST API aktualisiert die Kategorieachse eines Diagramms.

## PostChartCategoryAxis API

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/charts/{chartIndex}/categoryaxis
```

### **Sicherheit und Authentifizierung**

Die Aspose.Cells Cloud APIs sind sicher und erfordern eine <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-Token-basierte Authentifizierung</a>.

### Anforderungsparameter

| Parametername   | Typ    | Ort    | Beschreibung |
| --------------- | ------ | ------ | ------------ |
| name            | string | path   | Name der Excel-Datei. |
| sheetName       | string | path   | Name des Arbeitsblatts, das das Diagramm enthält. |
| chartIndex      | integer | path  | Nullbasierter Index des zu aktualisierenden Diagramms. |
| axis            | object | body  | JSON-Objekt, das die Eigenschaften der Kategorieachse definiert. |
| folder          | string | query | Ordner im Cloud-Speicher, in dem sich die Datei befindet (optional). |
| storageName     | string | query | Name des Speichers (optional). |

**Anforderungstext-Schema – `axis`-Objekt**

| Eigenschaft             | Typ     | Beschreibung |
|-------------------------|---------|--------------|
| IsAutomaticMajorUnit    | boolean | Gibt an, ob die Haupteinheit automatisch berechnet wird. |
| MajorUnit               | number  | Wert der Haupteinheit, wenn `IsAutomaticMajorUnit` `false` ist. |
| IsAutomaticMinorUnit    | boolean | Gibt an, ob die Nebeneinheit automatisch berechnet wird. |
| MinorUnit               | number  | Wert der Nebeneinheit, wenn `IsAutomaticMinorUnit` `false` ist. |
| Title                   | object  | Titel-Einstellungen für die Achse (z. B. `Text`, `Font`, `Visible`). |
| TickLabelPosition       | string  | Position der Beschriftungen (z. B. `Low`, `High`, `NextToAxis`). |
| ...                     | ...     | Weitere Achseneigenschaften gemäß der API-Spezifikation. |

**HTTP-Statuscodes**

| Code | Bedeutung                   | Beschreibung |
|------|-----------------------------|--------------|
| 200  | OK                          | Filter erfolgreich angewendet; Antwort enthält Details zur Operation. |
| 400  | Bad Request                 | Fehlende oder ungültige Parameter (z. B. nicht unterstützter Dateityp). |
| 401  | Unauthorized                | Ungültiges oder fehlendes JWT-Token. |
| 413  | Payload Too Large           | Die hochgeladene Datei überschreitet das Größenlimit. |
| 500  | Internal Server Error       | Unerwarteter Serverfehler. |

**Voraussetzungen / Authentifizierung**

Um diesen Endpunkt aufzurufen, müssen Sie ein JWT-Zugriffstoken vom Aspose.Cells Cloud-Authentifizierungsdienst (`/connect/token`) erhalten. Geben Sie das Token im `Authorization`-Header an, wie im folgenden Beispiel gezeigt.

{{< tabs tabTotal="2" tabID="1" tabName1="Anforderung" tabName2="Antwort" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/charts/{chartIndex}/categoryaxis?folder={folder}&storageName={storageName}" \
  -X POST \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>" \
  -d '{
        "axis": {
          "IsAutomaticMajorUnit": true,
          "IsAutomaticMinorUnit": true,
          "Title": {
            "Text": "Kategorieachse",
            "Visible": true
          }
        }
      }'
```

{{< /tab >}}

{{< tab tabNum="2" >}}

**Beispielantwort**

```json
{
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

Die [OpenAPI-Spezifikation](https://apireference.aspose.cloud/cells/#/Charts/PostChartCategoryAxis) definiert eine öffentlich zugängliche Programmierschnittstelle und ermöglicht es Ihnen, REST-Interaktionen direkt aus einem Webbrowser heraus durchzuführen.

### Hinweise

* Der Endpunkt erfordert HTTPS; die Verwendung von HTTP kann in Browsern Warnungen aufgrund gemischter Inhalte auslösen.
* Alle Platzhalterwerte (`{name}`, `{sheetName}`, `{chartIndex}`, `{folder}`, `{storageName}`) müssen durch tatsächliche Bezeichner ersetzt werden.
* Unterstützte Diagrammtypen für die Aktualisierung der Kategorieachse sind in der API-Referenz aufgeführt.

## Cloud SDK-Familie

Die Verwendung eines SDKs ist die beste Möglichkeit, die Entwicklung zu beschleunigen. Ein SDK übernimmt die Details auf niedriger Ebene und ermöglicht es Ihnen, sich auf Ihre Projekt-Aufgaben zu konzentrieren. Besuchen Sie das [GitHub-Repository](https://github.com/aspose-cells-cloud), um eine vollständige Liste der Aspose.Cells Cloud SDKs zu erhalten.

Die folgenden Codebeispiele zeigen, wie Aufrufe an Aspose.Cells-Webservices mithilfe verschiedener SDKs durchgeführt werden:

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example-Post-ChartCategoryAxis.js" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< /tab >}}

{{< /tabs >}}