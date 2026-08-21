---
title: "Daten in einem Bereich auf einem Excel-Arbeitsblatt sortieren"
second_title: "Document"
linktitle: "Sortieren"
type: docs
url: /worksheets/sort-data/
aliases: [/sort-worksheet-data/]
keywords: "Aspose.Cells Cloud, Excel-Sortier-API, Sortierung von Bereichsdaten auf Arbeitsblättern, REST-API, dataSorter"
description: "Sortieren Sie einen bestimmten Bereich in einem Excel-Arbeitsblatt mithilfe der Aspose.Cells Cloud REST-API. Enthält Endpunkt, erforderliche Parameter, Authentifizierungsschritte, Fehlerbehandlung und SDK-Beispiele."
weight: 20
---

Die REST-API sortiert Daten innerhalb eines angegebenen Bereichs in einem Excel-Arbeitsblatt.

## REST-API

```shell
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/sort
```

### Anforderungsparameter

| Parametername   | Typ    | Speicherort | Erforderlich | Beschreibung                                                      |
| --------------- | ------ | ----------- | ------------ | ----------------------------------------------------------------- |
| name            | string | Pfad        | Ja           | Der Name der Arbeitsmappe.                                        |
| sheetName       | string | Pfad        | Ja           | Der Name des Arbeitsblatts.                                       |
| cellArea        | string | Abfrage     | Ja           | Der zu sortierende Zellbereich (z. B. `A5:A10`).                 |
| dataSorter      | object | Körper      | Ja           | JSON-Objekt, das die Sortiereinstellungen definiert (siehe Schema unten). |
| folder          | string | Abfrage     | Nein         | Der Ordner, der die Arbeitsmappe enthält.                        |
| storageName     | string | Abfrage     | Nein         | Der Name des Speichers, in dem sich die Arbeitsmappe befindet.   |

**`dataSorter`-Objektschema** – Der Körper muss ein JSON-Objekt mit den folgenden Eigenschaften enthalten:

- `CaseSensitive` _(boolean, erforderlich)_ – Gibt an, ob die Sortierung zwischen Groß- und Kleinschreibung unterscheidet.
- `HasHeaders` _(boolean, erforderlich)_ – Gibt an, ob der Bereich eine Kopfzeile enthält.
- `KeyList` _(array, erforderlich)_ – Eine Sammlung von Sortierschlüsseln. Jedes Schlüsselobjekt enthält:
  - `Key` _(integer)_ – Nullbasierter Spaltenindex.
  - `SortOrder` _(string)_ – `"ascending"` (aufsteigend) oder `"descending"` (absteigend).
- `SortLeftToRight` _(boolean, erforderlich)_ – Wenn `true`, erfolgt die Sortierung von links nach rechts; andernfalls von oben nach unten.
- (Optional) `CaseOrder`, `SortLeftToRight` usw. können gemäß der OpenAPI-Spezifikation ebenfalls angegeben werden.

Die [OpenAPI-Spezifikation](https://apireference.aspose.cloud/cells/#/Worksheets/PostWorksheetRangeSort) definiert eine öffentlich zugängliche Programmierschnittstelle und ermöglicht REST-Interaktionen direkt aus einem Webbrowser.

Sie können das cURL-Befehlszeilentool verwenden, um problemlos auf Aspose.Cells-Webservices zuzugreifen. Das folgende Beispiel zeigt, wie ein Aufruf der Cloud-API mit cURL durchgeführt wird.

{{< tabs tabTotal="2" tabID="1" tabName1="Anforderung" tabName2="Antwort" >}}

{{< tab tabNum="1" >}}

```shell
curl -v "https://api.aspose.cloud/v3.0/cells/Sample_Test_Book.xls/worksheets/Sheet1/sort?cellArea=A5:A10" \
  -X POST \
  -d '{"CaseSensitive":false,"HasHeaders":false,"KeyList":[{"Key":0,"SortOrder":"descending"}],"SortLeftToRight":false}' \
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

**Fehlerbehandlung** – Die API kann Standard-HTTP-Fehlercodes zurückgeben. Typische Antworten sind:

| HTTP-Status | Code | Nachricht                                           |
| ----------- | ---- | --------------------------------------------------- |
| 400         | 400  | Ungültige Anforderung – fehlende oder ungültige Parameter. |
| 401         | 401  | Nicht autorisiert – ungültiges oder fehlendes JWT-Token.   |
| 404         | 404  | Nicht gefunden – Arbeitsmappe oder Arbeitsblatt existiert nicht. |
| 500         | 500  | Interner Serverfehler.                             |

Der Antworttext folgt bei Fehlerfällen dem Muster `{ "Code": <status>, "Message": "<description>", "Status": "Error" }`.

## Cloud SDK-Familie

Die Verwendung eines SDKs ist die schnellste Möglichkeit zur Entwicklung. Ein SDK übernimmt die Details auf niedriger Ebene, sodass Sie sich auf Ihre Projekt Aufgaben konzentrieren können. Besuchen Sie das [GitHub-Repository](https://github.com/aspose-cells-cloud), um eine vollständige Liste der Aspose.Cells Cloud SDKs zu erhalten.

Die folgenden Codebeispiele zeigen, wie Aspose.Cells-Webservices mithilfe verschiedener SDKs aufgerufen werden:

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-.NET-CellsWorksheetsPostWorksheetRangeSort.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-worksheet-SortWorksheetData-sort-worksheet-data.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Worksheet-PostWorksheetRangeSort-.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Worksheet-sort_worksheet_range-.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "SortWorkSheetData.py" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-Worksheet-SortWorksheetData-1.js" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "9d725d4678edaac53f95c5208e17783c" "Examples-Android-worksheet-SortWorksheetData-sort-worksheet-data.java" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-Worksheet-SortWorksheetData-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< gist "aspose-cells-cloud-gists" "48dd9dae5e2188a64e2284bb12b9201b" >}}

{{< /tab >}}

{{< /tabs >}}

---