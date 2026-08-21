---
title: "Mehrere Excel-Arbeitsblätter löschen"
second_title: "Dokument"
linktitle: "Mehrere Arbeitsblätter"
type: docs
url: /de/worksheets/delete-multiple/
aliases: [/de/delete-excel-worksheets/]
keywords: "Aspose.Cells Cloud, mehrere Arbeitsblätter löschen, Excel-API, REST-API, v3.0, Arbeitsblätter löschen"
description: "Erfahren Sie, wie Sie mehrere Arbeitsblätter aus einer Excel-Arbeitsmappe mithilfe der Aspose.Cells Cloud REST-API (v3.0) löschen können. Enthält einen sicheren HTTPS-Endpunkt, erforderliche Parameter, ein korrigiertes cURL-Beispiel und SDK-Ausschnitte für mehrere Programmiersprachen."
weight: 20
ArticleTitle: "Mehrere Excel-Arbeitsblätter mithilfe der Aspose.Cells Cloud REST-API löschen"
---

Diese REST-API löscht mehrere Arbeitsblätter aus einer Arbeitsmappe.

## Sicherheit und Authentifizierung
Die Aspose.Cells Cloud APIs sind sicher und erfordern eine [JWT-Token-basierte Authentifizierung](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/).

## REST-API

```bash
DELETE https://api.aspose.cloud/v3.0/cells/{name}/worksheets
```

### **Anforderungsparameter**

| Parametername      | Typ    | Ort    | Beschreibung                                                       |
| ------------------ | ------ | ------ | ------------------------------------------------------------------ |
| name               | string | path   | Der Name der Excel-Datei.                                          |
| matchCondition     | object | body   | Ein `MatchConditionRequest`-Objekt, das festlegt, welche Arbeitsblätter gelöscht werden sollen. |
| folder             | string | query  | Ordnerpfad im Speicher, in dem sich die Datei befindet.           |
| storageName        | string | query  | Name des Speicherdiensts.                                          |

**Eigenschaften von MatchConditionRequest**

| Name                | Typ      | Beschreibung                                  | Anmerkungen |
| ------------------- | -------- | --------------------------------------------- | ----------- |
| RegexPattern        | string   | Regulärer Ausdruck zum Abgleich von Arbeitsblattnamen. | optional    |
| FullMatchConditions | string[] | Exakte Namen der zu löschenden Arbeitsblätter. | optional    |

Die [OpenAPI-Spezifikation](https://apireference.aspose.cloud/cells/#/Worksheets/DeleteWorksheets) definiert eine öffentlich zugängliche Programmierschnittstelle und ermöglicht REST-Interaktionen direkt aus einem Webbrowser.

Sie können das cURL-Befehlszeilentool verwenden, um Aspose.Cells-Webdienste problemlos aufzurufen. Das folgende Beispiel zeigt, wie Aufrufe an die Cloud-API mit cURL durchgeführt werden. **Ein gültiges JWT-Token ist im `Authorization`-Header erforderlich.**

{{< tabs tabTotal="2" tabID="1" tabName1="Anforderung" tabName2="Antwort" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets?folder=Temp" \
  -X DELETE \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt_token>" \
  -d '{"FullMatchConditions":["Sheet1","Sheet2","Sheet3"]}'
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

Die Anforderung kann auch allgemeine Fehlerantworten zurückgeben, beispielsweise:

| HTTP-Status | Bedeutung                                   | Beispiel-Payload                                          |
| ----------- | ------------------------------------------- | --------------------------------------------------------- |
| 400         | Ungültige Anforderung – ungültiges JSON oder Parameter | `{"Code":400,"Message":"Ungültige Anforderungsnutzlast."}` |
| 401         | Nicht autorisiert – fehlendes oder ungültiges JWT-Token | `{"Code":401,"Message":"Authentifizierung fehlgeschlagen."}` |
| 403         | Verboten – unzureichende Berechtigungen     | `{"Code":403,"Message":"Zugriff verweigert."}`            |
| 404         | Nicht gefunden – Datei oder Arbeitsblatt existiert nicht | `{"Code":404,"Message":"Ressource nicht gefunden."}`      |
| 500         | Interner Serverfehler                       | `{"Code":500,"Message":"Ein unerwarteter Fehler ist aufgetreten."}` |

{{< /tab >}}

{{< /tabs >}}

## Cloud SDK-Familie

Die Verwendung eines SDK ist die beste Möglichkeit, die Entwicklung zu beschleunigen. Ein SDK übernimmt die Low-Level-Details, sodass Sie sich auf Ihre Projekt Aufgaben konzentrieren können. Bitte besuchen Sie das [GitHub-Repository](https://github.com/aspose-cells-cloud), um eine vollständige Liste der Aspose.Cells Cloud SDKs zu erhalten.

Die folgenden Codebeispiele zeigen, wie Aufrufe an Aspose.Cells-Webdienste mithilfe verschiedener SDKs durchgeführt werden:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleDeleteWorksheets.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_DeleteWorksheets.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_DeleteWorksheets.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_DeleteWorksheets.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_DeleteWorksheets.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_DeleteWorksheets.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_DeleteWorksheets.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_DeleteWorksheets.go" >}}

{{< /tab >}}

{{< /tabs >}}

**Siehe auch:**  
- [Einzelnes Arbeitsblatt löschen](https://docs.aspose.cloud/cells/de/worksheets/delete/)  
- [Arbeitsblatt kopieren](https://docs.aspose.cloud/cells/de/worksheets/copy/)  
- [Arbeitsblatt verschieben](https://docs.aspose.cloud/cells/de/worksheets/move/)  
---