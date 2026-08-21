---
title: "Wertebereich in einem Excel-Arbeitsblatt festlegen"
second_title: "Dokument"
linktitle: "Werte festlegen"
type: docs
url: /ranges/update/values/
aliases: [/set-range-value-in-excel-worksheet/]
keywords: "Aspose.Cells, Excel-API, Wertebereich festlegen, REST-API, Cloud-SDK, Arbeitsblatt aktualisieren"
description: "Erfahren Sie, wie Sie einen Zell- oder Bereichswert in einer Excel-Arbeitsmappe mithilfe der Aspose.Cells Cloud REST API (v3.0) festlegen. Enthält Endpunkt, Parameter, cURL-Beispiel, SDK-Codebeispiele und Fehlerbehandlung."
weight: 72
ArticleTitle: "Wertebereich in einem Excel-Arbeitsblatt festlegen – Aspose.Cells Cloud API"
---

Nutzen Sie diese REST API, um einen Wert im angegebenen Bereich festzulegen. Bei geeigneter Gegebenheit wird der Wert in einen anderen Datentyp konvertiert und das Zahlenformat der Zelle zurückgesetzt.

**Voraussetzungen**  
- Ein gültiger Aspose Cloud-Account.  
- Ein JWT-Token mit dem Bereich `Cells.ReadWrite`.  
- Die Arbeitsmappe muss bereits in den Ziel-Speicherort hochgeladen worden sein.

## PostWorksheetCellsRangeValue API

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/ranges/value
```

Die Anfrageparameter sind:

| Parametername  | Typ     | Ort      | Beschreibung                                               |
|----------------|---------|----------|------------------------------------------------------------|
| name           | string  | path     | Name der Arbeitsmappe                                      |
| sheetName      | string  | path     | Name des Arbeitsblatts                                     |
| value          | string  | query    | Eingabewert                                                |
| range          | object  | body     | Bereichsobjekt im Arbeitsblatt                             |
| isConverted    | boolean | query    | Gibt an, ob der Eingabewert konvertiert werden soll       |
| setStyle       | boolean | query    | Gibt an, ob das Format auf die Zielzellen angewendet werden soll |
| folder         | string  | query    | Ordner der Arbeitsmappe                                    |
| storageName    | string  | query    | Name des Speichers                                         |

**Beispiel für das `range`-Objekt**, das im Anfragetext gesendet werden kann:

```json
{
  "range": {
    "FirstRow": 0,
    "FirstColumn": 0,
    "RowCount": 1,
    "ColumnCount": 1
  }
}
```

Die [OpenAPI-Spezifikation](https://apireference.aspose.cloud/cells/#/Ranges/PostWorksheetCellsRangeValue) definiert eine öffentlich zugängliche Programmierschnittstelle und ermöglicht REST-Interaktionen direkt aus einem Webbrowser.

Sie können das cURL-Befehlszeilentool verwenden, um problemlos auf Aspose.Cells-Webdienste zuzugreifen. Das folgende Beispiel zeigt, wie die Cloud-API mit cURL aufgerufen wird. **Geben Sie ein gültiges JWT-Token im Header `Authorization` an.**

{{< tabs tabTotal="2" tabID="1" tabName1="Anfrage" tabName2="Antwort" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/ranges/value?value=25&isConverted=false&setStyle=false" \
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

**Antworthschema**

| Feld    | Typ     | Beschreibung                                             |
|---------|---------|----------------------------------------------------------|
| Code    | integer | HTTP-Statuscode des Vorgangs.                            |
| Status  | string  | Kurze Beschreibung des Ergebnisses (z. B. „OK“).        |
| Message | string  | Detaillierte Fehlermeldung bei fehlgeschlagenen Anfragen (optional). |
| Result  | object  | Zusätzliche Daten für erfolgreiche Aufrufe (optional).  |

**Mögliche HTTP-Statuscodes**

- **200 OK** – Der Bereichswert wurde erfolgreich festgelegt.  
- **400 Bad Request** – Ungültige Parameter oder fehlerhafter Anfragetext.  
- **401 Unauthorized** – Fehlendes oder ungültiges JWT-Token.  
- **403 Forbidden** – Unzureichende Berechtigungen für den angeforderten Vorgang.  
- **404 Not Found** – Die angegebene Arbeitsmappe, das Arbeitsblatt oder der Bereich existiert nicht.  
- **500 Internal Server Error** – Unerwarteter Serverfehler.

*Beispiel für eine Fehlerantwort bei „400 Bad Request“:*

```json
{
  "Code": 400,
  "Status": "Bad Request",
  "Message": "Das Objekt 'range' fehlen erforderliche Felder."
}
```

## Cloud SDK-Familie

Die Verwendung eines SDKs ist die beste Möglichkeit, die Entwicklungszeit zu verkürzen. Ein SDK übernimmt die Low-Level-Details und ermöglicht es Ihnen, sich auf Ihre Projekt Aufgaben zu konzentrieren. Besuchen Sie das [GitHub-Repository](https://github.com/aspose-cells-cloud), um eine vollständige Liste der Aspose.Cells Cloud SDKs zu erhalten.

Die folgenden Codebeispiele zeigen, wie Aufrufe an Aspose.Cells-Webdienste mit verschiedenen SDKs durchgeführt werden:

{{< tabs tabTotal="9" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Swift" tabName8="Perl" tabName9="Go" >}}

{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNET-CSharp-Cells-SetRangeValueWorksheet-1.cs" >}}
{{< /tab >}}

{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-cells-SetRangeValueWorksheet-1.java" >}}
{{< /tab >}}

{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Cells-PostSetCellRangeValue-.php" >}}
{{< /tab >}}

{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Cells-set_cell_range_value-.rb" >}}
{{< /tab >}}

{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-Cells-SetRangeValueWorksheet-1.js" >}}
{{< /tab >}}

{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "SetRangeValueInExcelWorksheet.py" >}}
{{< /tab >}}

{{< tab tabNum="7" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-Cells-SetRangeValueWorksheet-1.pl" >}}
{{< /tab >}}

{{< tab tabNum="9" >}}
{{< gist "aspose-cells-cloud-gists" "7dc9243752ac8a0e5d9c0f211a029cd9" >}}
{{< /tab >}}

{{< /tabs >}}