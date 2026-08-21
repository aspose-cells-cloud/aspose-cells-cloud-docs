---
title: "Hinzufügen eines Symbolfilters zu einem Excel-Arbeitsblatt"
second_title: "Dokument"
linktitle: "Symbolfilter hinzufügen"
type: docs
url: /de/autofilter/add-icon-filter/
aliases: [  /de/add-an-icon-filter/ , /de/autofilter/add-an-icon-filter/ ]
keywords: "Aspose.Cells Cloud, Excel, Symbolfilter, AutoFilter, REST-API"
description: "Erfahren Sie, wie Sie mithilfe der Aspose.Cells Cloud REST-API einen Symbolfilter zu einem Excel-Arbeitsblatt hinzufügen – inklusive detaillierter Anforderungsinformationen, cURL-Beispiel, SDK-Codebeispielen und Fehlerbehandlung."
weight: 65
ArticleTitle: "Hinzufügen eines Symbolfilters zu einem Excel-Arbeitsblatt – Aspose.Cells Cloud-Dokumentation"
---

## REST-API

Diese REST-API fügt mithilfe der **Aspose.Cells Cloud REST-API** einen **Symbolfilter** zu einem Excel-Arbeitsblatt hinzu.

**Hintergrund:** Ein Symbolfilter wendet eine visuelle Symbolsammlung auf Zellen basierend auf deren Werten an, sodass Daten trends schnell visuell analysiert werden können. Gängige Anwendungsfälle sind die Hervorhebung von Leistungsmetriken, Statusanzeigen oder die Kategorisierung von Werten mithilfe von Ampelsymbolen direkt innerhalb von Excel-Arbeitsblättern.


```bash
PUT https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/autoFilter/iconFilter
```

### **Sicherheit und Authentifizierung**

Die Aspose.Cells Cloud-APIs sind sicher und erfordern eine <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-Token-basierte Authentifizierung</a>.


### Anforderungsparameter:

| Parametername   | Typ     | Position | Beschreibung |
|-----------------|---------|----------|-------------|
| name            | string  | Path     | Der Name der Arbeitsmappe. |
| sheetName       | string  | Path     | Der Name des Arbeitsblatts. |
| range           | string  | Query    | Der Zellbereich (z. B. `A1:B1`), auf den der Filter angewendet werden soll. |
| fieldIndex      | integer | Query    | Der nullbasierte Index der Spalte, auf die sich der Filter bezieht. |
| iconSetType     | string  | Query    | Die zu verwendende Symbolsammlung. Zulässige Werte: `Arrows3`, `ArrowsGray3`, `Flags3`, `Signs3`, `Symbols3`, `Symbols32`, `TrafficLights31`, `TrafficLights32`, `Arrows4`, `ArrowsGray4`, `Rating4`, `RedToBlack4`, `TrafficLights4`, `Arrows5`, `ArrowsGray5`, `Quarters5`, `Rating5`, `Stars3`, `Boxes5`, `Triangles3`, `None`, `CustomSet`, `Smilies3`, `ColorSmilies3`. |
| iconId          | integer | Query    | Die Kennung des spezifischen Symbols innerhalb der ausgewählten Symbolsammlung. |
| matchBlanks     | boolean | Query    | Gibt an, ob leere Zellen eingeschlossen werden sollen (`true` oder `false`). |
| refresh         | boolean | Query    | Gibt an, ob der Filter nach dem Anwenden aktualisiert werden soll (`true` oder `false`). |
| folder          | string  | Query    | Der Ordner, der die ursprüngliche Arbeitsmappe enthält. |
| storageName     | string  | Query    | Der Name des Speichers, in dem sich die Arbeitsmappe befindet. |

### **Antwort**

```json
{
    "Status":"OK",
    "Code":200
}
```

**HTTP-Statuscodes**

| Code | Bedeutung                 | Beschreibung |
|------|---------------------------|-------------|
| 200  | OK                        | Filter wurde erfolgreich angewendet; die Antwort enthält Details zum Vorgang. |
| 400  | Bad Request               | Fehlende oder ungültige Parameter (z. B. nicht unterstützter Dateityp). |
| 401  | Unauthorized              | Ungültiges oder fehlendes JWT-Token. |
| 413  | Payload Too Large         | Die hochgeladene Datei überschreitet das Größenlimit. |
| 500  | Internal Server Error     | Unerwarteter Serverfehler. |

## Verwendung der PutWorksheetIconFilter-API mit SDKs

### PutWorksheetIconFilter-API-Spezifikation

Die [OpenAPI-Spezifikation](https://apireference.aspose.cloud/cells/#/AutoFilter/PutWorksheetIconFilter) definiert eine öffentlich zugängliche Programmierschnittstelle und ermöglicht REST-Interaktionen direkt aus einem Webbrowser.

Sie können das cURL-Befehlszeilentool nutzen, um problemlos auf Aspose.Cells-Webdienste zuzugreifen. Im folgenden Beispiel wird gezeigt, wie ein Aufruf an die Cloud-API mit cURL erfolgt.

{{< tabs tabTotal="2" tabID="11" tabName11="Anforderung" tabName12="Antwort" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/autoFilter/iconFilter?range=A1:B1&fieldindex=0&iconsettype=ArrowsGray3&iconid=1" \
  -X PUT \
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

Mögliche Antwortstatuscodes:

| Code | Beschreibung |
|------|-------------|
| 200  | Filter erfolgreich angewendet. |
| 400  | Bad Request – fehlende oder ungültige Parameter. |
| 401  | Unauthorized – ungültiges oder fehlendes Authentifizierungstoken. |
| 404  | Arbeitsmappe, Arbeitsblatt oder angegebener Bereich nicht gefunden. |
| 500  | Internal Server Error. |
{{< /tab >}}

{{< /tabs >}}

### Verwendung von Aspose.Cells Cloud SDKs

Die Verwendung eines SDKs ist die beste Möglichkeit, die Entwicklung zu beschleunigen. Ein SDK übernimmt die Details der unteren Schichten, sodass Sie sich auf Ihre Projektziele konzentrieren können. Eine vollständige Liste der Aspose.Cells Cloud SDKs finden Sie im [GitHub-Repository](https://github.com/aspose-cells-cloud).

Die folgenden Codebeispiele zeigen, wie Aspose.Cells-Webdienste mithilfe verschiedener SDKs aufgerufen werden:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePutWorksheetIconFilter.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PutWorksheetIconFilter.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PutWorksheetIconFilter.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PutWorksheetIconFilter.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PutWorksheetIconFilter.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PutWorksheetIconFilter.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PutWorksheetIconFilter.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PutWorksheetIconFilter.go" >}}

{{< /tab >}}

{{< /tabs >}}

Weitere Informationen zu anderen AutoFilter-Funktionen finden Sie in der Dokumentation zu **[Farbfilter hinzufügen](/autofilter/add-color-filter/)**, **[Datumsfilter hinzufügen](/autofilter/add-date-filter/)** und **[AutoFilter löschen](/autofilter/clear-autofilter/)**.