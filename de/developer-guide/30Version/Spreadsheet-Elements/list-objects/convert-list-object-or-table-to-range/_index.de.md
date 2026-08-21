---
title: "Listobjekt in Bereich konvertieren – Aspose.Cells Cloud API"
ArticleTitle: "Listobjekt mit Aspose.Cells Cloud API in Bereich konvertieren"
second_title: "Dokument"
linktitle: "Konvertierung"
type: docs
url: /list-objects/to-range/
aliases:
  - /convert-list-object-or-table-to-range/
  - /tables/to-range/
keywords: "Aspose Cells API, Listobjekt in Bereich konvertieren, Excel REST API"
description: "Erfahren Sie, wie Sie ein Excel-ListObject (Tabelle) mithilfe der Aspose.Cells Cloud REST API in einen Bereich konvertieren. Enthält Anforderungssyntax, Parameter, Beispiel-cURL, Antwortschema, Authentifizierungsdetails, Fehlercodes und SDK-Beispiele."
weight: 30
---

Diese REST API konvertiert ein **ListObject (Tabelle)** innerhalb eines Excel-Arbeitsblatts in einen **Bereich**.

**Voraussetzungen:**  
Bevor Sie den Endpunkt aufrufen, stellen Sie sicher, dass die Arbeitsmappe in Ihrem Aspose Cloud-Speicher hochgeladen wurde, das Arbeitsblatt das Ziel-ListObject enthält und Sie ein unterstütztes Dateiformat verwenden (z. B. .xlsx, .xlsm).

## REST API

**Authentifizierung**  
Um diesen Vorgang aufzurufen, müssen Sie ein gültiges JWT-Token im `Authorization`-Header übergeben. Holen Sie sich das Token, indem Sie eine POST-Anfrage an den OAuth 2.0-Tokenendpunkt mit Ihrer Client-ID und Ihrem Clientgeheimnis senden. Das Token muss den `Cells.ReadWrite`-Geltungsbereich enthalten und ist für die vom Tokendienst zurückgegebene Gültigkeitsdauer gültig.

```bash
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/listobjects/{listObjectIndex}/ConvertToRange
```

### **Sicherheit und Authentifizierung**

Die Aspose.Cells Cloud APIs sind sicher und erfordern eine <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-Token-basierte Authentifizierung</a>.

### Anforderungsparameter

| Name                | Typ     | Ort     | Erforderlich | Standard | Beschreibung                                                |
| ------------------- | ------- | ------- | ------------ | -------- | ----------------------------------------------------------- |
| **name**            | string  | path    | Ja           | –        | Der Name der Excel-Datei.                                   |
| **sheetName**       | string  | path    | Ja           | –        | Der Name des Arbeitsblatts, das das ListObject enthält.   |
| **listObjectIndex** | integer | path    | Ja           | –        | Nullbasierter Index des zu konvertierenden ListObjects (Tabelle). |
| **folder**          | string  | query   | Nein         | –        | Ordnerpfad, in dem die Datei gespeichert ist.              |
| **storageName**     | string  | query   | Nein         | –        | Name des Speicherdiensts.                                   |

> **Hinweis:** Dieser Vorgang funktioniert nur mit modernen Excel-Formaten wie **.xlsx** und **.xlsm**. Das ListObject darf nicht geschützt sein. Weitere Informationen zu ListObjects finden Sie in der [ListObjects-Übersicht](/list-objects/). Details zum Arbeiten mit Bereichen finden Sie in der [Dokumentation zu Bereichen](/ranges/).

### cURL-Beispiel (Anforderung)

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/listobjects/0/ConvertToRange" \
  -X POST \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <your-jwt-token>"
```

{{< /tab >}}

#### Antwortschema

Die API gibt eine Antwort mit dem Status **200 OK** zurück, die Details des neu erstellten Bereichs enthält.

```json
{
  "Code": 200,
  "Status": "OK",
  "RangeName": "A1:C10",
  "Address": "Sheet1!A1:C10",
  "FirstRow": 0,
  "FirstColumn": 0,
  "RowCount": 10,
  "ColumnCount": 3
}
```

| Feld            | Typ     | Beschreibung                                         |
| --------------- | ------- | ---------------------------------------------------- |
| **Code**        | integer | HTTP-ähnlicher Statuscode (200 bedeutet Erfolg).    |
| **Status**      | string  | Textuelle Statusmeldung.                             |
| **RangeName**   | string  | Dem erstellten Bereich zugewiesener Name.            |
| **Address**     | string  | Vollständige Adresse des Bereichs inkl. Blattname.   |
| **FirstRow**    | integer | Nullbasierter Index der ersten Zeile im Bereich.     |
| **FirstColumn** | integer | Nullbasierter Index der ersten Spalte im Bereich.    |
| **RowCount**    | integer | Anzahl der Zeilen im Bereich.                        |
| **ColumnCount** | integer | Anzahl der Spalten im Bereich.                       |

**HTTP-Statuscodes**

| Code | Bedeutung                   | Beschreibung                                           |
|------|-----------------------------|--------------------------------------------------------|
| 200  | OK                          | Filter erfolgreich angewendet; Antwort enthält Details des Vorgangs. |
| 400  | Bad Request                 | Fehlende oder ungültige Parameter (z. B. nicht unterstützter Dateityp). |
| 401  | Unauthorized                | Ungültiges oder fehlendes JWT-Token.                  |
| 413  | Payload Too Large           | Hochgeladene Datei überschreitet die Größenbeschränkung. |
| 500  | Internal Server Error       | Unerwarteter Serverfehler.                             |

**Fehler-Antwortschema (Beispiel):**

```json
{
  "Code": 400,
  "Message": "Invalid listObjectIndex. Index must be between 0 and 5."
}
```

{{< tab tabNum="12" >}}

```json
{
  "Code": 200,
  "Status": "OK",
  "RangeName": "A1:C10",
  "Address": "Sheet1!A1:C10",
  "FirstRow": 0,
  "FirstColumn": 0,
  "RowCount": 10,
  "ColumnCount": 3
}
```

{{< /tab >}}

{{< /tabs >}}

## Cloud SDK-Familie

Die Verwendung eines SDKs ist der beste Weg, die Entwicklungsgeschwindigkeit zu erhöhen. Ein SDK übernimmt die Details auf unterster Ebene, sodass Sie sich auf Ihre Projektaufgaben konzentrieren können. Besuchen Sie das [GitHub-Repository](https://github.com/aspose-cells-cloud), um eine vollständige Liste der Aspose.Cells Cloud SDKs zu erhalten.

Die folgenden Codebeispiele zeigen, wie Aufrufe an Aspose.Cells-Webdienste mit verschiedenen SDKs durchgeführt werden:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostWorksheetListObjectConvertToRange.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostWorksheetListObjectConvertToRange.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostWorksheetListObjectConvertToRange.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostWorksheetListObjectConvertToRange.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostWorksheetListObjectConvertToRange.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostWorksheetListObjectConvertToRange.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostWorksheetListObjectConvertToRange.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostWorksheetListObjectConvertToRange.go" >}}

{{< /tab >}}

{{< /tabs >}}