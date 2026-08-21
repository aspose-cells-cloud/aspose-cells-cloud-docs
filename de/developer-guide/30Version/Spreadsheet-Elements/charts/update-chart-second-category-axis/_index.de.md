---
title: "Zweite Kategorienachse eines Diagramms aktualisieren"
type: docs
url: /charts/second-category-axis/update/
weight: 160
keywords: "Aspose.Cells, Diagramm, Zweite Kategorienachse, REST API, Diagramm aktualisieren, Excel, Cloud API"
description: "Erfahren Sie, wie Sie die zweite Kategorienachse eines Diagramms in einer Excel-Arbeitsmappe mithilfe der Aspose.Cells Cloud REST API aktualisieren."
ArticleTitle: "Zweite Kategorienachse eines Diagramms aktualisieren – Aspose.Cells Cloud API"
---

Diese REST API aktualisiert die zweite Kategorienachse eines Diagramms.

## PostChartSecondCategoryAxis API

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/charts/{chartIndex}/secondcategoryaxis
```

### **Sicherheit und Authentifizierung**

Die Aspose.Cells Cloud APIs sind sicher und erfordern eine <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-Token-basierte Authentifizierung</a>.

### Anforderungsparameter

| Parametername     | Typ    | Ort    | Beschreibung                                                  |
|-------------------|--------|--------|---------------------------------------------------------------|
| name              | string | path   | Der Name der Excel-Datei.                                     |
| sheetName         | string | path   | Der Name des Arbeitsblatts, das das Diagramm enthält.         |
| chartIndex        | integer| path   | Der nullbasierte Index des zu aktualisierenden Diagramms.     |
| axis              | object | body   | Das Objekt der zweiten Kategorienachse mit den neuen Einstellungen. |
| folder            | string | query  | Der Ordnerpfad, in dem die Datei gespeichert ist.             |
| storageName       | string | query  | Der Name des Speicherdienstes.                                |

**Authentifizierung** – Die API erfordert ein gültiges OAuth 2.0-Access-Token. Erzeugen Sie ein JWT-Token gemäß der [Authentifizierungsanleitung](https://docs.aspose.cloud/cells/authentication/). Geben Sie das Token im `Authorization`-Header an, wie im folgenden cURL-Beispiel gezeigt.

Die [OpenAPI-Spezifikation](https://apireference.aspose.cloud/cells/#/Charts/PostChartSecondCategoryAxis) definiert eine öffentlich zugängliche Programmierschnittstelle und ermöglicht REST-Interaktionen direkt aus einem Webbrowser.

Sie können das cURL-Befehlszeilentool nutzen, um Aspose.Cells-Webdienste einfach anzusprechen. Das folgende Beispiel zeigt, wie Sie mithilfe von cURL Aufrufe an die Cloud API durchführen.

{{< tabs tabTotal="2" tabID="1" tabName1="Anforderung" tabName2="Antwort" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/charts/{chartIndex}/secondcategoryaxis?folder={folder}&storageName={storageName}" \
  -X POST \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>" \
  -d '{ 
        "axis": {
          /* Achseneinstellungen, z. B. "Title": "Neuer Achsentitel", "IsVisible": true */
        }
      }'
```

*Ersetzen Sie `{name}`, `{sheetName}`, `{chartIndex}`, `{folder}` und `{storageName}` durch Ihre tatsächlichen Werte. Der Anforderungstext muss das `axis`-Objekt mit den gewünschten Einstellungen enthalten.*

{{< /tab >}}

{{< tab tabNum="2" >}}

**Erfolgreiche Antwort (200)**  

```json
{
  "Code": 200,
  "Status": "OK",
  "Chart": {
    "Id": "chart_1",
    "SecondCategoryAxis": {
      "Title": "Neuer Achsentitel",
      "IsVisible": true,
      /* zusätzliche Achseneigenschaften */
    }
  }
}
```

**Fehlerantworten**  

| Statuscode | Beschreibung                                           |
|------------|--------------------------------------------------------|
| 400        | Ungültige Anforderung – fehlende oder ungültige Parameter. |
| 401        | Nicht autorisiert – ungültiges oder fehlendes JWT-Token. |
| 404        | Nicht gefunden – die angegebene Datei, das Arbeitsblatt oder Diagramm existiert nicht. |
| 500        | Interner Serverfehler – unerwarteter Zustand auf dem Server. |

```json
{
  "Code": 400,
  "Message": "Ungültige Anforderungsnutzlast."
}
```

{{< /tab >}}

{{< /tabs >}}

## Cloud SDK-Familie

SDKs vereinfachen die Entwicklung, indem sie Details auf niedriger Ebene abstrahieren und Ihnen ermöglichen, sich auf Ihre Geschäftslogik zu konzentrieren. Besuchen Sie das [GitHub-Repository](https://github.com/aspose-cells-cloud), um eine vollständige Liste der Aspose.Cells Cloud SDKs einzusehen.

Die folgenden Codebeispiele zeigen, wie Aufrufe an Aspose.Cells-Webdienste mithilfe verschiedener SDKs durchgeführt werden:

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

<!-- C# Beispiel-Platzhalter -->

{{< /tab >}}

{{< tab tabNum="2" >}}

<!-- Java Beispiel-Platzhalter -->

{{< /tab >}}

{{< tab tabNum="3" >}}

<!-- PHP Beispiel-Platzhalter -->

{{< /tab >}}

{{< tab tabNum="4" >}}

<!-- Ruby Beispiel-Platzhalter -->

{{< /tab >}}

{{< tab tabNum="5" >}}

<!-- Python Beispiel-Platzhalter -->

{{< /tab >}}

{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example-Post-ChartSecondCategoryAxis.js" >}}
{{< /tab >}}

{{< tab tabNum="7" >}}

<!-- Android Beispiel-Platzhalter -->

{{< /tab >}}

{{< tab tabNum="8" >}}

<!-- Swift Beispiel-Platzhalter -->

{{< /tab >}}

{{< tab tabNum="9" >}}

<!-- Perl Beispiel-Platzhalter -->

{{< /tab >}}

{{< tab tabNum="10" >}}

<!-- Go Beispiel-Platzhalter -->

{{< /tab >}}

{{< /tabs >}}

**Hinweise und Best Practices**

* Der `chartIndex`-Parameter ist nullbasiert; das erste Diagramm in einem Arbeitsblatt hat den Index 0.  
* Die API unterstützt sowohl die Arbeitsmappenformate `.xlsx` als auch `.xls`.  
* Geben Sie im `axis`-Objekt nur die gewünschten Eigenschaften an; nicht angegebene Eigenschaften behalten ihre aktuellen Werte bei.  
* Halten Sie sich an die Richtlinien zur Anfragelimitierung (typischerweise 100 Anfragen pro Minute pro Konto), um Throttling zu vermeiden.  
---