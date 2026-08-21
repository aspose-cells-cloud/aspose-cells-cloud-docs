---
title: "Zeilen in einem Excel-Arbeitsblatt ausblenden"
second_title: "Dokument"
linktitle: "Ausblenden"
type: docs
url: /rows/hide/
aliases: [/hide-rows-in-excel-worksheet/]
keywords: "Zeilen ausblenden, Aspose.Cells Cloud, Excel-API, REST, SDK"
description: "Erfahren Sie, wie Sie eine oder mehrere Zeilen in einem Excel-Arbeitsblatt mithilfe der Aspose.Cells Cloud REST-API ausblenden. Enthält cURL-Beispiel, SDK-Snippets, Parameter, Authentifizierung, Antwortdetails und Fehlerbehandlung."
weight: 40
ArticleTitle: "Zeilen in Excel-Arbeitsblatt mit Aspose.Cells Cloud API ausblenden"
---

Diese REST-API blendet Zeilen in einem Excel-Arbeitsblatt aus.

**Voraussetzungen:** Ein gültiges JWT-Bearer-Token, das vom Aspose Cloud OAuth-Endpunkt abgerufen wurde; die Arbeitsmappe ist im Aspose Cloud-Speicher gespeichert; sowie der Name des Arbeitsblatts, das die auszublendenden Zeilen enthält. Die API funktioniert mit Excel-Dateien in den Formaten XLS, XLSX und weiteren unterstützten Formaten.

## PostHideWorksheetRows API

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/rows/hide
```

### **Sicherheit und Authentifizierung**

Die Aspose.Cells Cloud APIs sind sicher und erfordern eine <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-Token-basierte Authentifizierung</a>.

### Anforderungsparameter

| Parameter       | Typ     | Position | Beschreibung                                                           |
| --------------- | ------- | -------- | ---------------------------------------------------------------------- |
| **name**        | string  | path     | Der Name der Arbeitsmappen-Datei.                                      |
| **sheetName**   | string  | path     | Der Name des Arbeitsblatts, das die auszublendenden Zeilen enthält.   |
| **startrow**    | integer | query    | Nullbasierter Index der ersten auszublendenden Zeile.                 |
| **totalRows**   | integer | query    | Die Anzahl aufeinanderfolgender Zeilen, die ab **startrow** ausgeblendet werden sollen. |
| **folder**      | string  | query    | Der Ordner im Speicher, in dem sich die Arbeitsmappe befindet.        |
| **storageName** | string  | query    | Der Name des Speicherdienstes.                                         |

Die [OpenAPI-Spezifikation](https://apireference.aspose.cloud/cells/#/Cells/PostHideWorksheetRows) stellt eine öffentlich zugängliche Programmierschnittstelle bereit, mit der Sie REST-Interaktionen direkt aus einem Webbrowser heraus durchführen können.

Sie können das Kommandozeilentool **cURL** verwenden, um Aspose.Cells-Webdienste aufzurufen. Die API erfordert ein JWT-Bearer-Token, das vom Aspose Cloud OAuth-Endpunkt abgerufen wurde; dieses muss im `Authorization`-Header übermittelt werden. Das folgende Beispiel zeigt, wie eine Zeile mit cURL ausgeblendet wird.

{{< tabs tabTotal="2" tabID="1" tabName1="Anforderung" tabName2="Antwort" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/cells/rows/hide?startrow=1&totalRows=1" \
  -X POST \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

**HTTP-Statuscodes der Antwort**

| Code | Beschreibung                             |
|------|------------------------------------------|
| 200  | Erfolg – Zeilen ausgeblendet              |
| 400  | Ungültige Anforderung – ungültige Parameter |
| 401  | Nicht autorisiert – fehlendes oder ungültiges JWT |
| 404  | Nicht gefunden – Arbeitsmappe oder Arbeitsblatt existiert nicht |
| 500  | Serverfehler – interner Verarbeitungsfehler |

Ein erfolgreicher Aufruf gibt ein JSON-Objekt zurück, das die Felder `Code` und `Status` enthält. Im Fehlerfall enthält die Antwort zusätzliche Felder wie `Message` sowie entsprechende HTTP-Statuscodes (z. B. 400, 401, 404, 500).

**Hinweise:** Stellen Sie sicher, dass der Wert von `startrow` innerhalb des Zeilenbereichs des Arbeitsblatts liegt; andernfalls gibt die API einen Fehler mit Statuscode 400 zurück. Zeilenindizes sind nullbasiert, d. h. `startrow=0` bezieht sich auf die erste Zeile.

## Cloud SDK-Familie

Die Verwendung eines SDKs ist die schnellste Möglichkeit, diese Funktionalität in Ihre Anwendung zu integrieren. SDKs übernehmen die Details auf niedriger Ebene, sodass Sie sich auf Ihre Geschäftslogik konzentrieren können. Eine vollständige Liste der Aspose.Cells Cloud SDKs finden Sie im [GitHub-Repository](https://github.com/aspose-cells-cloud).

Die folgenden Codebeispiele zeigen, wie Zeilen mithilfe verschiedener SDKs ausgeblendet werden. (Die Beispieldateinamen beziehen sich aus historischen Gründen auf „Unhide“, der Code innerhalb jedes Gists führt jedoch die **Hide**-Operation aus.)

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostUnhideWorksheetRows.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostUnhideWorksheetRows.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostUnhideWorksheetRows.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostUnhideWorksheetRows.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostUnhideWorksheetRows.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostUnhideWorksheetRows.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostUnhideWorksheetRows.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostUnhideWorksheetRows.go" >}}

{{< /tab >}}

{{< /tabs >}}