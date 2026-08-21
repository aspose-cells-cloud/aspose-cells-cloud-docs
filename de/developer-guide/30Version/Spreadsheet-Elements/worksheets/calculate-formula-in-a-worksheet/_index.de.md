---
title: "Berechnen einer Formel in einem Excel-Arbeitsblatt"
second_title: "Dokument"
linktitle: "Berechnen"
type: docs
url: /worksheets/calculate-formula/
aliases: [/calculate-formula-in-a-worksheet/]
keywords: "Aspose.Cells Cloud, Excel, Formelberechnung, REST API, SDKs, C#, Java, PHP, Ruby, Node.js, Python, Perl, Go, Swift"
description: "Berechnen von Formeln in einem Excel-Arbeitsblatt mithilfe der Aspose.Cells Cloud REST API. Unterstützt mehrere SDKs (C#, Java, PHP, Ruby, Node.js, Python, Perl, Go, Swift) mit sofort verwendbaren Beispielen."
weight: 20
ArticleTitle: "Berechnen einer Formel in einem Excel-Arbeitsblatt – Aspose.Cells Cloud-Dokumentation"
---

Diese REST-API gibt den **berechneten Wert einer Formel** in einem Arbeitsblatt zurück. Sie kann verwendet werden, um eine **Excel-Formel direkt aus Ihrer Anwendung heraus auszuwerten**.

## REST API

```bash
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/formulaResult
```

### **Anfrageparameter**

| Parametername | Typ   | Speicherort | Beschreibung                                      |
| -------------- | ------ | -------- | -------------------------------------------------- |
| name           | string | path     | Name der Excel-Datei.                            |
| sheetName      | string | path     | Name des Arbeitsblatts, das die Formel enthält.  |
| formula        | string | query    | Die auszuwertende Formel (z. B. `SUMME(A5:A10)`). |
| folder         | string | query    | Ordner, in dem das Dokument gespeichert ist.      |
| storageName    | string | query    | Name des Speicherdienstes (sofern zutreffend).    |

Die [OpenAPI-Spezifikation](https://apireference.aspose.cloud/cells/#/Worksheets/GetWorksheetCalculateFormula) definiert eine öffentlich zugängliche Programmierschnittstelle und ermöglicht es Ihnen, REST-Interaktionen direkt aus einem Webbrowser durchzuführen.

### Authentifizierung

Alle Anfragen müssen ein gültiges **Bearer JWT-Token** im `Authorization`-Header enthalten:

```
Authorization: Bearer <your_jwt_token>
```

Ein Token erhalten Sie, indem Sie den in der Aspose.Cells Cloud-Authentifizierungsanleitung beschriebenen OAuth 2.0-Fluss durchlaufen.

### Mögliche Antwort-Statuscodes

| Code | Beschreibung                                 |
|------|---------------------------------------------|
| 200  | Anfrage erfolgreich; der Formelwert wird zurückgegeben. |
| 400  | Ungültige Anfrage – fehlende oder ungültige Parameter. |
| 401  | Nicht autorisiert – ungültiges oder fehlendes JWT-Token. |
| 404  | Nicht gefunden – die angegebene Datei oder das angegebene Arbeitsblatt existiert nicht. |
| 500  | Interner Serverfehler – unerwarteter Zustand auf dem Server. |

Sie können das **cURL**-Befehlszeilentool verwenden, um Aspose.Cells Cloud-Webdienste problemlos aufzurufen. Das folgende Beispiel zeigt, wie Sie mit cURL ein Formelergebnis anfordern.

{{< tabs tabTotal="2" tabID="1" tabName1="Anfrage" tabName2="Antwort" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Sample_Test_Book.xls/worksheets/Sheet2/formulaResult?formula=SUMME(A5:A10)" \
-X GET \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Value": {
    "Value": "0"
  },
  "Code": "200",
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

## Cloud SDK-Familie

Die Verwendung eines SDKs ist der schnellste Weg, die API zu integrieren. Ein SDK übernimmt die Details auf niedriger Ebene, sodass Sie sich auf Ihre Geschäftslogik konzentrieren können. Eine vollständige Liste der Aspose.Cells Cloud SDKs finden Sie im [GitHub-Repository](https://github.com/aspose-cells-cloud).

Die folgenden Codebeispiele zeigen, wie Aspose.Cells-Webdienste mit verschiedenen SDKs aufgerufen werden:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "d1a2b3c4e5f67890abcd1234ef567890" "ExampleGetWorksheetCalculateFormula.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "a1b2c3d4e5f67890abcd1234ef567890" "ExampleGetWorksheetCalculateFormula.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "b1c2d3e4f5g67890abcd1234ef567890" "ExampleGetWorksheetCalculateFormula.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "c1d2e3f4g5h67890abcd1234ef567890" "ExampleGetWorksheetCalculateFormula.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "d1e2f3g4h5i67890abcd1234ef567890" "ExampleGetWorksheetCalculateFormula.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "e1f2g3h4i5j67890abcd1234ef567890" "ExampleGetWorksheetCalculateFormula.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f1g2h3i4j5k67890abcd1234ef567890" "ExampleGetWorksheetCalculateFormula.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "g1h2i3j4k5l67890abcd1234ef567890" "ExampleGetWorksheetCalculateFormula.go" >}}

{{< /tab >}}

{{< /tabs >}}

---

**Siehe auch:**  
- [Arbeitsblatt abrufen](https://docs.aspose.cloud/cells/worksheets/get-worksheet/)  
- [Arbeitsblatt aktualisieren](https://docs.aspose.cloud/cells/worksheets/update-worksheet/)  
- [Alle Formeln berechnen](https://docs.aspose.cloud/cells/worksheets/calculate-all-formulas/)  
---