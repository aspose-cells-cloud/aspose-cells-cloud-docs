---
title: "Ein List-Objekt in einem Excel-Arbeitsblatt aktualisieren"
ArticleTitle: "Ein List-Objekt in einem Excel-Arbeitsblatt aktualisieren – Aspose.Cells Cloud API-Dokumentation"
second_title: "Dokument"
linktitle: "Aktualisieren"
type: docs
url: /list-objects/update/
aliases:
  - /update-a-list-object-or-table-inside-the-worksheet/
  - /tables/update/
keywords: "Aspose.Cells, ListObject, Tabelle aktualisieren, Excel-API, REST, Cloud SDK, List-Objekt aktualisieren, Excel-Arbeitsblatt, Tabelle"
description: "Erfahren Sie, wie Sie eine Excel-Tabelle mithilfe der Aspose.Cells Cloud API (v3.0) aktualisieren können. Enthält Endpunkt, Parameter, Beispiel-cURL, Fehlercodes und SDK-Beispiele."
weight: 20
---

Diese REST API aktualisiert die Eigenschaften eines **List-Objekts** (Tabelle) in einem Excel-Arbeitsblatt.

## Sicherheit und Authentifizierung

Die Aspose.Cells Cloud APIs sind sicher und erfordern eine [JWT-Token-basierte Authentifizierung](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/).

## Schema des Anforderungstexts

Das DTO `listObject` enthält die folgenden Felder. Nur die Felder, die Sie ändern möchten, sind im Anforderungstext erforderlich.

| Feld                                           | Typ                | Erforderlich | Beschreibung                                                               |
| ----------------------------------------------- | ------------------ | ------------ | -------------------------------------------------------------------------- |
| **DisplayName**                                 | Zeichenkette (string) | optional     | Der für die Tabelle angezeigte Name.                                       |
| **StartRow** / **StartColumn**                  | Ganzzahl (integer)  | optional     | Nullbasierten Index der ersten Zeile/Spalte der Tabelle.                  |
| **EndRow** / **EndColumn**                      | Ganzzahl (integer)  | optional     | Nullbasierten Index der letzten Zeile/Spalte der Tabelle.                 |
| **Range**                                       | Zeichenkette (string) | optional     | A1-Stil-Adresse, die den Tabellenbereich definiert (z. B. `A1:D10`).       |
| **ShowHeaderRow**                               | Boolean (boolean)   | optional     | `true`, um die Kopfzeile anzuzeigen.                                       |
| **ShowTotals**                                  | Boolean (boolean)   | optional     | `true`, um die Gesamtzeile anzuzeigen.                                     |
| **TableStyleName**                              | Zeichenkette (string) | optional     | Name des anzuwendenden integrierten Tabellenstils.                        |
| **TableStyleType**                              | Zeichenkette (string) | optional     | Stilart (`TableStyleLight`, `TableStyleMedium`, usw.).                     |
| **ListColumns**                                 | Array von Objekten  | optional     | Sammlung von Spaltendefinitionen (`Name`, `TotalsCalculation`).            |
| **Sorter**, **AutoFilter**, **ShowTableStyle…** | Objekt             | optional     | Erweiterte Formatierungs- und Filteroptionen (siehe vollständiges DTO in der OpenAPI-Spezifikation). |

### Minimales Beispiel für Nutzdaten

```json
{
  "DisplayName": "SalesData",
  "Range": "A1:E20",
  "ShowHeaderRow": true,
  "ShowTotals": false
}
```

## REST API

```bash
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/listobjects/{listObjectIndex}
```

### **Anforderungsparameter**

| Parametername       | Typ    | Speicherort | Beschreibung                                |
| ------------------- | ------ | ----------- | ------------------------------------------- |
| **name**            | Zeichenkette (string) | Pfad        | Name des Dokuments.                         |
| **sheetName**       | Zeichenkette (string) | Pfad        | Name des Arbeitsblatts.                     |
| **listObjectIndex** | Ganzzahl (integer)  | Pfad        | Index des zu aktualisierenden List-Objekts. |
| **listObject**      | Objekt | Körper (body) | ListObject-DTO im Anforderungstext.         |
| **folder**          | Zeichenkette (string) | Abfrage     | Ordner, der das Dokument enthält.           |
| **storageName**     | Zeichenkette (string) | Abfrage     | Name des Speichers.                         |

Die [OpenAPI-Spezifikation](https://apireference.aspose.cloud/cells/#/ListObjects/PostWorksheetListObject) definiert eine öffentlich zugängliche Programmierschnittstelle und ermöglicht es Ihnen, REST-Interaktionen direkt aus einem Webbrowser durchzuführen.

### Anforderung

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet7/listobjects/0" \
  -X POST \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>" \
  -d '{
    "DisplayName": "SalesData",
    "Range": "A1:E20",
    "ShowHeaderRow": true,
    "ShowTotals": false,
    "ListColumns": [
      { "Name": "Product", "TotalsCalculation": "None" },
      { "Name": "Quantity", "TotalsCalculation": "Sum" },
      { "Name": "Price", "TotalsCalculation": "Average" }
    ]
  }'
```

{{< /tab >}}

### Antwort

{{< tab tabNum="12" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

Die erfolgreiche Antwort enthält die folgenden Felder:

| Feld   | Typ    | Beschreibung                                          |
| ------ | ------ | ----------------------------------------------------- |
| Code   | Ganzzahl (integer) | HTTP-Statuscode (200 bei Erfolg).         |
| Status | Zeichenkette (string) | Textuelle Beschreibung des Status.     |
| UpdatedObject *(optional)* | Objekt | Die aktualisierte `ListObject`-Darstellung, die die geänderten Eigenschaften enthält. |

{{< /tab >}}

{{< /tabs >}}

## Fehlerantworten

| HTTP-Code | Beschreibung                                                                 | Beispiel-Nutzdaten                                     |
| --------- | ---------------------------------------------------------------------------- | ------------------------------------------------------ |
| **400**   | Ungültige Anforderung – fehlende erforderliche Felder oder ungültiges JSON. | `{ "Code": 400, "Message": "Invalid request body." }`  |
| **401**   | Nicht autorisiert – JWT-Token fehlt oder ist ungültig.                      | `{ "Code": 401, "Message": "Authentication failed." }` |
| **404**   | Nicht gefunden – die angegebene Arbeitsmappe, das Arbeitsblatt oder List-Objekt existiert nicht. | `{ "Code": 404, "Message": "Resource not found." }`    |
| **500**   | Interner Serverfehler – unerwarteter Zustand auf Serverseite.               | `{ "Code": 500, "Message": "Server error." }`          |

## FAQ

<details>  
<summary>Wie aktualisiere ich ein List-Objekt mithilfe der Aspose.Cells Cloud API?</summary>

Verwenden Sie den Endpunkt `POST /cells/{name}/worksheets/{sheetName}/listobjects/{listObjectIndex}`. Fügen Sie einen JSON-Text mit den Eigenschaften hinzu, die Sie ändern möchten (z. B. `DisplayName`, `ShowHeaderRow`). Authentifizieren Sie sich mit einem JWT-Token im `Authorization`-Header.

</details>

<details>  
<summary>Welche Antwort erhalte ich nach einer erfolgreichen Aktualisierung?</summary>

Es wird ein JSON-Objekt mit `Code: 200` und `Status: "OK"` zurückgegeben. Bei einem Fehler enthält die Antwort den entsprechenden HTTP-Statuscode und ein `Error`-Objekt mit einer Beschreibung des Problems.

</details>

<details>  
<summary>Kann ich nur eine Teilmenge der List-Objekteigenschaften aktualisieren?</summary>

Ja. Geben Sie im Anforderungstext nur die Felder an, die Sie ändern möchten; alle weggelassenen Felder bleiben unverändert.

</details>

## Verwandte Dokumentation

- [Ein List-Objekt hinzufügen](https://docs.aspose.cloud/cells/list-objects/add/)
- [List-Objekt abrufen](https://docs.aspose.cloud/cells/list-objects/get/)
- [List-Objekt löschen](https://docs.aspose.cloud/cells/list-objects/delete/)

## Cloud SDK-Familie

Die Verwendung eines SDKs ist der beste Weg, um die Entwicklung zu beschleunigen. Ein SDK übernimmt die Details auf unterster Ebene, sodass Sie sich auf Ihre Projekt Aufgaben konzentrieren können. Besuchen Sie das [GitHub-Repository](https://github.com/aspose-cells-cloud), um eine vollständige Liste der Aspose.Cells Cloud SDKs zu erhalten.

Die folgenden Codebeispiele zeigen, wie Aspose.Cells-Webdienste mithilfe verschiedener SDKs aufgerufen werden:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostWorksheetListObject.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostWorksheetListObject.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostWorksheetListObject.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostWorksheetListObject.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2b4189bc27ae92abf73c36b4df0" "Example_PostWorksheetListObject.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostWorksheetListObject.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostWorksheetListObject.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostWorksheetListObject.go" >}}

{{< /tab >}}

{{< /tabs >}}
---