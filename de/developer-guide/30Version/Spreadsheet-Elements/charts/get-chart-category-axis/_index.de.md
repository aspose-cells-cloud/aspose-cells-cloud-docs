---
title: "Diagrammkategorieachse abrufen"
type: docs
url: /charts/category-axis/get/
weight: 60
keywords: "Aspose.Cells, Diagrammkategorieachse, Excel, REST-API, Cloud-Speicher, OAuth2, API-Dokumentation"
description: "Ruft die Kategorieachse eines Diagramms in einem Excel-Arbeitsblatt mithilfe der Aspose.Cells Cloud REST API ab."
ArticleTitle: "Diagrammkategorieachse abrufen – Aspose.Cells Cloud API-Dokumentation"
---

Diese REST API ruft die **Kategorieachse** eines Diagramms ab.  
Um diesen Endpunkt aufzurufen, müssen Sie ein gültiges OAuth 2.0-Zugriffstoken bereitstellen, und die Arbeitsmappe muss im Aspose Cloud-Speicher gespeichert sein.

**Voraussetzungen**  
Bevor Sie diesen Endpunkt verwenden, stellen Sie sicher, dass:  

- Ein OAuth 2.0-Token abgerufen wurde und für die Aspose Cloud-Dienste gültig ist.  
- Die Arbeitsmappendatei in den Aspose Cloud-Speicher (Standardordner oder ein angegebener Ordner) hochgeladen wurde.  
- Sie die API-Version **v3.0** verwenden, wie in der Anforderungs-URL dargestellt.  
- Die aufrufende Anwendung über die Berechtigung zum Lesen der Arbeitsmappe und zum Zugriff auf deren Arbeitsblätter verfügt.

## GetChartCategoryAxis API

```http
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/charts/{chartIndex}/categoryaxis
```

**Hintergrund** – Das Entfernen aller Diagramme aus einem Arbeitsblatt ist nützlich, wenn Sie das visuelle Layout einer Tabelle zurücksetzen, veraltete Visualisierungen ersetzen oder eine Arbeitsmappe für die Wiederverwendung vorbereiten möchten, ohne vorherige Diagrammdaten beizubehalten.

### **Sicherheit und Authentifizierung**

Die Aspose.Cells Cloud APIs sind sicher und erfordern eine <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-Token-basierte Authentifizierung</a>.

### Anforderungsparameter

| Parametername | Typ    | Standort | Beschreibung                                              |
| ------------- | ------ | -------- | --------------------------------------------------------- |
| name          | string | path     | Der Name der Arbeitsmappendatei.                          |
| sheetName     | string | path     | Der Name des Arbeitsblatts, das das Diagramm enthält.    |
| chartIndex    | integer| path     | Der nullbasierte Index des Diagramms, dessen Achse angefordert wird. |
| folder        | string | query    | Der Ordnerpfad im Speicher, in dem sich die Arbeitsmappe befindet. |
| storageName   | string | query    | Der Name des Speicherdienstes (sofern nicht der Standarddienst). |

### **Antwort**

```json
{
  "Code": 200,
  "Status": "OK",
  "CategoryAxis": {
    "AxisBetweenCategories": true,
    "AxisLine": {
      "IsVisible": true,
      "Weight": 1.0
    },
    "MajorTickMark": "Cross",
    "MinorTickMark": "None",
    "Title": {
      "Text": "Kategorieachse",
      "IsVisible": true
    },
    "Labels": {
      "IsAutoRotation": false,
      "RotationAngle": 0,
      "IsVisible": true
    }
  }
}
```

**HTTP-Statuscodes**

| Code | Bedeutung                   | Beschreibung                                         |
|------|-----------------------------|------------------------------------------------------|
| 200  | OK                          | Filter erfolgreich angewendet; Antwort enthält Details zum Vorgang. |
| 400  | Bad Request                 | Fehlende oder ungültige Parameter (z. B. nicht unterstützter Dateityp). |
| 401  | Unauthorized                | Ungültiges oder fehlendes JWT-Token. |
| 413  | Payload Too Large           | Die hochgeladene Datei überschreitet das Größenlimit. |
| 500  | Internal Server Error       | Unerwarteter Serverfehler. |

## Verwendung der GetChartCategoryAxis API mit SDKs

### GetChartCategoryAxis API-Spezifikation

Die <a href="https://apireference.aspose.cloud/cells/#/Charts/GetChartCategoryAxis" rel="noopener noreferrer">OpenAPI-Spezifikation</a> definiert eine öffentlich zugängliche Programmierschnittstelle und ermöglicht es Ihnen, REST-Interaktionen direkt aus einem Webbrowser durchzuführen.

Sie können das cURL-Befehlszeilentool verwenden, um Aspose.Cells-Webdienste einfach aufzurufen. Das folgende Beispiel zeigt, wie ein Aufruf der Cloud-API mit cURL durchgeführt wird.

{{< tabs tabTotal="2" tabID="1" tabName1="Anforderung" tabName2="Antwort" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/charts/{chartIndex}/categoryaxis" \
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
  "CategoryAxis": {
    "AxisBetweenCategories": true,
    "AxisLine": {
      "IsVisible": true,
      "Weight": 1.0
    },
    "MajorTickMark": "Cross",
    "MinorTickMark": "None",
    "Title": {
      "Text": "Kategorieachse",
      "IsVisible": true
    },
    "Labels": {
      "IsAutoRotation": false,
      "RotationAngle": 0,
      "IsVisible": true
    }
  }
}
```

{{< /tab >}}

{{< /tabs >}}

### Verwendung der Aspose.Cells Cloud SDKs

Die Verwendung eines SDKs ist der beste Weg, um die Entwicklung zu beschleunigen. Ein SDK übernimmt Details auf niedriger Ebene und lässt Sie sich auf Ihre Projektziele konzentrieren. Bitte überprüfen Sie das <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub-Repository</a> für eine vollständige Liste der Aspose.Cells Cloud SDKs.

Die folgenden Codebeispiele zeigen, wie Aspose.Cells-Webdienste mithilfe verschiedener SDKs aufgerufen werden:

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
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example-Get-ChartCategoryAxis.js" >}}
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
---