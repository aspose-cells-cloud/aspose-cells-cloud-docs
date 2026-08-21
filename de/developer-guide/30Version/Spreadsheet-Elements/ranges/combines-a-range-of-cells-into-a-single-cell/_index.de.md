---
title: "Aspose.Cells Cloud API – Zellbereich zusammenführen"
second_title: "Dokument"
linktitle: "Zusammenführen"
type: docs
url: /de/ranges/merge/
aliases: [  /de/combines-a-range-of-cells-into-a-single-cell/ ]
keywords: "Aspose.Cells, Zellen zusammenführen, Excel-API, REST, Cloud-SDK"
description: "Führen Sie einen Zellbereich mithilfe der Aspose.Cells Cloud REST API in einer einzigen Zelle zusammen. Erfahren Sie mehr über das Anfrageformat, die Parameter und SDK-Beispiele für C#, Java, Python und mehr."
weight: 20
---

Diese REST API führt einen Zellbereich in einer einzigen Zelle auf einem Excel-Arbeitsblatt zusammen.

**Übersicht** – Beim Zusammenführen eines Bereichs werden die ausgewählten Zellen zu einer einzigen Zelle verschmolzen, wobei der Wert der oberen linken Zelle beibehalten und die übrigen verworfen werden. Verwenden Sie diesen Vorgang, wenn Sie eine Kopfzeile erstellen möchten, die mehrere Spalten oder Zeilen überspannt, oder wenn Sie das Layout eines Arbeitsblatts vereinfachen möchten.

## REST API

```bash
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/ranges/merge
```

### **Anfrageparameter**

| Parametername   | Typ    | Ort    | Beschreibung                                         |
| --------------- | ------ | ------ | ---------------------------------------------------- |
| **name**        | string | path   | Name der Arbeitsmappe.                               |
| **sheetName**   | string | path   | Name des Arbeitsblatts.                             |
| **range**       | object | body   | Bereichsobjekt, das die zusammenzuführenden Zellen angibt. |
| **folder**      | string | query  | Ordner, in dem die Arbeitsmappe gespeichert ist.    |
| **storageName** | string | query  | Name des Speichers.                                  |

#### Schema des Anfragetexts

Das **Range**-Objekt muss die folgenden Felder enthalten (alle anderen sind optional):

| Eigenschaft     | Typ     | Erforderlich | Beschreibung                                         |
| --------------- | ------- | ------------ | ---------------------------------------------------- |
| **FirstRow**    | integer | Ja           | Nullbasierter Index der ersten Zeile im Bereich.    |
| **FirstColumn** | integer | Ja           | Nullbasierter Index der ersten Spalte im Bereich.   |
| **RowCount**    | integer | Ja           | Anzahl der im Bereich einzuschließenden Zeilen.      |
| **ColumnCount** | integer | Ja           | Anzahl der im Bereich einzuschließenden Spalten.     |
| **Name**        | string  | Nein         |OPTIONALER Name für den Bereich.                      |
| **RefersTo**    | string  | Nein         | Eine Formel, auf die der Bereich verweist.           |
| **Worksheet**   | string  | Nein         | Name des Arbeitsblatts (sofern unterschiedlich vom Pfadparameter). |
| **RowHeight**   | number  | Nein         | Höhe der Zeilen im Bereich (Pixel).                  |
| **ColumnWidth** | number  | Nein         | Breite der Spalten im Bereich (Pixel).               |

Sie können das cURL-Befehlszeilentool verwenden, um einfach auf die Aspose.Cells-Webdienste zuzugreifen. Das folgende Beispiel zeigt, wie ein Aufruf an die Cloud API mit cURL durchgeführt wird.

{{< tabs tabTotal="2" tabID="1" tabName1="Anfrage" tabName2="Antwort" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/ranges/merge" \
  -X POST \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>" \
  -d '{
        "FirstRow": 9,
        "FirstColumn": 0,
        "RowCount": 1,
        "ColumnCount": 7
      }'
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

#### Antwortdetails

| HTTP-Status                   | Beschreibung                                            | Beispiel-JSON                                          |
| ----------------------------- | ------------------------------------------------------- | ------------------------------------------------------ |
| **200 OK**                    | Der Bereich wurde erfolgreich zusammengeführt.         | `{ "Code": 200, "Status": "OK" }`                      |
| **400 Bad Request**           | Ungültige Bereichsparameter (z. B. Indices außerhalb des gültigen Bereichs). | `{ "Code": 400, "Message": "Ungültiger Bereich." }`   |
| **401 Unauthorized**          | Fehlendes oder ungültiges JWT-Token.                   | `{ "Code": 401, "Message": "Authentifizierung fehlgeschlagen." }` |
| **404 Not Found**             | Arbeitsmappe oder Arbeitsblatt nicht gefunden.         | `{ "Code": 404, "Message": "Ressource nicht gefunden." }` |
| **500 Internal Server Error** | Unerwarteter Serverfehler.                             | `{ "Code": 500, "Message": "Interner Serverfehler." }` |

## Cloud SDK-Familie

Die Verwendung eines SDKs ist der beste Weg, die Entwicklung zu beschleunigen. Ein SDK übernimmt die Details der unteren Schicht, sodass Sie sich auf Ihre Projekt Aufgaben konzentrieren können. Besuchen Sie das [GitHub-Repository](https://github.com/aspose-cells-cloud), um eine vollständige Liste der Aspose.Cells Cloud SDKs zu erhalten.

Die folgenden Codebeispiele zeigen, wie Aspose.Cells-Webdienste mithilfe verschiedener SDKs aufgerufen werden:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostWorksheetCellsRangeMerge.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostWorksheetCellsRangeMerge.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostWorksheetCellsRangeMerge.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostWorksheetCellsRangeMerge.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostWorksheetCellsRangeMerge.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostWorksheetCellsRangeMerge.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostWorksheetCellsRangeMerge.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostWorksheetCellsRangeMerge.go" >}}

{{< /tab >}}

{{< /tabs >}}

---