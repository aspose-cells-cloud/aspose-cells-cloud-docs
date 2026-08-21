---
title: "Ein Listenobjekt (Tabelle) zu einem Excel-Arbeitsblatt hinzufügen"
second_title: "Dokument"
linktitle: "Hinzufügen"
type: docs
url: /de/list-objects/add/
aliases: [  /de/add-a-list-object-or-table-inside-the-worksheet/ , /de/tables/add/ ]
keywords: "Aspose.Cells Cloud, Excel-API, Listenobjekt, Tabelle, REST-API, Arbeitsblatt"
description: "Erfahren Sie, wie Sie mit der Aspose.Cells Cloud REST-API ein Listenobjekt (Excel-Tabelle) zu einem Arbeitsblatt hinzufügen. Enthält Endpunkt, Parameter, Authentifizierungsschritte, cURL-Beispiel und SDK-Codebeispiele."
weight: 10
ArticleTitle: "Ein Listenobjekt (Tabelle) zu einem Excel-Arbeitsblatt hinzufügen – Aspose.Cells Cloud-Dokumentation"
---

Diese REST-API fügt ein **Listenobjekt (Tabelle)** zu einem Excel-Arbeitsblatt hinzu.

Bevor Sie diesen Endpunkt verwenden, stellen Sie sicher, dass Sie über ein gültiges JWT-Token verfügen, die Arbeitsmappe in einer unterstützten Cloud-Speicherlösung gespeichert ist und das Arbeitsblatt vorhanden ist.

## REST-API

```bash
PUT https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/listobjects
```

### Anforderungsparameter

| Parametername   | Typ     | Ort    | Beschreibung                                                              |
| --------------- | ------- | ------ | ------------------------------------------------------------------------- |
| **name**        | string  | path   | Dateiname der Arbeitsmappe.                                               |
| **sheetName**   | string  | path   | Name des Arbeitsblatts.                                                   |
| **startRow**    | integer | query  | Nullbasierter Index der ersten Zeile des Tabellenbereichs.               |
| **startColumn** | integer | query  | Nullbasierter Index der ersten Spalte des Tabellenbereichs.              |
| **endRow**      | integer | query  | Nullbasierter Index der letzten Zeile des Tabellenbereichs.              |
| **endColumn**   | integer | query  | Nullbasierter Index der letzten Spalte des Tabellenbereichs.             |
| **hasHeaders**  | boolean | query  | `true`, wenn die erste Zeile Spaltenüberschriften enthält, andernfalls `false`. |
| **listObject**  | object  | body   | Definition des Listenobjekts (siehe **Schema des Anforderungstextes**).  |
| **folder**      | string  | query  | Ordner, der die Arbeitsmappe enthält.                                     |
| **storageName** | string  | query  | Name des Speichers.                                                       |

### Schema des Anforderungstextes

Das **listObject**-Objekt beschreibt die zu erstellende Tabelle. Es werden nur die gängigsten Eigenschaften angezeigt; die vollständige Liste finden Sie in der OpenAPI-Spezifikation.

```json
{
  "displayName": "MeineTabelle",
  "showTotals": false,
  "style": "TableStyleMedium2"
}
```

### Beispielanforderung (cURL)

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/listobjects?startRow=1&startColumn=1&endRow=10&endColumn=12&hasHeaders=true" \
  -X PUT \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>" \
  -d '{
        "displayName": "MeineTabelle",
        "showTotals": false,
        "style": "TableStyleMedium2"
      }'
```

### Beispielantwort

```json
{
  "Code": 200,
  "Status": "OK"
}
```

### Fehlercodes

| HTTP-Status | Grund                 | Beschreibung                                        |
| ----------- | --------------------- | --------------------------------------------------- |
| **400**     | Bad Request           | Ungültige Bereichsparameter oder fehlerhafter JSON-Text. |
| **401**     | Unauthorized          | Fehlendes oder abgelaufenes JWT-Token.             |
| **404**     | Not Found             | Angegebene Arbeitsmappe oder Arbeitsblatt existiert nicht. |
| **500**     | Internal Server Error | Unerwarteter Serverfehler.                         |

**Beispiel für eine 400-Antwort**

```json
{
  "Code": 400,
  "Status": "Bad Request",
  "Message": "Ungültige Bereichsparameter."
}
```

**Beispiel für eine 401-Antwort**

```json
{
  "Code": 401,
  "Status": "Unauthorized",
  "Message": "Authentifizierungstoken fehlt oder ist abgelaufen."
}
```

Die [OpenAPI-Spezifikation](https://apireference.aspose.cloud/cells/#/ListObjects/PutWorksheetListObject) enthält die vollständige Spezifikation für diesen Vorgang.

## Cloud SDK-Familie

Die Verwendung eines SDK ist die beste Möglichkeit, die Entwicklungsgeschwindigkeit zu erhöhen. Ein SDK übernimmt die Details auf unterster Ebene und ermöglicht es Ihnen, sich auf Ihre Projektanforderungen zu konzentrieren. Besuchen Sie das [GitHub-Repository](https://github.com/aspose-cells-cloud), um eine vollständige Liste der Aspose.Cells Cloud SDKs anzuzeigen.

Die folgenden Codebeispiele zeigen, wie Aufrufe an Aspose.Cells-Webdienste mithilfe verschiedener SDKs durchgeführt werden:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePutWorksheetListObject.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PutWorksheetListObject.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PutWorksheetListObject.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PutWorksheetListObject.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PutWorksheetListObject.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PutWorksheetListObject.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PutWorksheetListObject.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PutWorksheetListObject.go" >}}

{{< /tab >}}

{{< /tabs >}}
---