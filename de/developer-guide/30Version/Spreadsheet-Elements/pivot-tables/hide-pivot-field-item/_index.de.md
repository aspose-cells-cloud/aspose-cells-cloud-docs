---
title: "Pivot-Feldelement in einer Pivot-Tabelle ausblenden"
second_title: "Dokument"
linktitle: Ausblenden
type: docs
url: /de/pivot-tables/hide-pivot-field-item/
aliases: [  /de/hide-pivot-field-item/ ]
keywords: "Aspose.Cells, Pivot-Feldelement ausblenden, PivotTable API, REST API, Cloud-SDK"
description: "Erfahren Sie, wie Sie ein Pivot-Feldelement in einer Pivot-Tabelle mit der Aspose.Cells Cloud REST API ausblenden. Enthält Anforderungsdetails, cURL-Beispiel und SDK-Code-Snippets für mehrere Sprachen."
weight: 110
ArticleTitle: "Pivot-Feldelement in einer Pivot-Tabelle ausblenden – Aspose.Cells Cloud API-Anleitung"
---

Bevor Sie die API aufrufen, stellen Sie sicher, dass Folgendes vorliegt:

* Ein gültiges **JWT-Access-Token** (erhältlich über den Aspose Cloud-Authentifizierungsworkflow).  
* Die Ziel-Workbook wurde in Ihren Aspose Cloud-Speicher hochgeladen.  
* Das Arbeitsblatt und die Pivot-Tabelle sind bereits erstellt.

Diese Voraussetzungen verhindern Authentifizierungsfehler sowie „Ressource nicht gefunden“-Antworten. Die folgenden Schritte beschreiben die erforderliche Einrichtung vor dem Aufruf der API.

Diese REST-API blendet ein Pivot-Feldelement in einer Pivot-Tabelle aus.

## PostPivotTableFieldHideItem API

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/pivottables/{pivotTableIndex}/PivotField/Hide
```

### **Sicherheit und Authentifizierung**

Die Aspose.Cells Cloud APIs sind sicher und erfordern eine <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-Token-basierte Authentifizierung</a>.

### **Anforderungsparameter**

| Parametername   | Typ     | Ort      | Beschreibung                                                                                     |
| --------------- | ------- | -------- | ------------------------------------------------------------------------------------------------ |
| name            | string  | path     | Name der Excel-Datei.                                                                            |
| sheetName       | string  | path     | Arbeitsblatt, das die Pivot-Tabelle enthält.                                                    |
| pivotTableIndex | integer | path     | Index der Pivot-Tabelle innerhalb des Arbeitsblatts.                                             |
| pivotFieldType  | string  | query    | Typ des Pivot-Felds (Zeile, Spalte, Seite, Daten usw.).                                         |
| fieldIndex      | integer | query    | Nullbasierter Index des zu ändernden Pivot-Felds.                                               |
| itemIndex       | integer | query    | Index des spezifischen Elements innerhalb des Felds, das ausgeblendet werden soll.             |
| isHide          | boolean | query    | Auf **true** setzen, um das Element auszublenden; **false**, um es anzuzeigen.                 |
| needReCalculate | boolean | query    | Gibt an, ob die Pivot-Tabelle nach der Änderung neu berechnet werden soll. Standard: **false**. |
| folder          | string  | query    | Ordnerpfad, in dem die Workbook gespeichert ist.                                                |
| storageName     | string  | query    | Name des Speicherdiensts.                                                                        |

**Kurzreferenz der erforderlichen Query-Parameter**

- **pivotFieldType** – Typ des Felds (z. B. `Row`).  
- **fieldIndex** – nullbasierter Index des zu ändernden Felds.  
- **itemIndex** – nullbasierter Index des auszublendenden/anzuzeigenden Elements.  
- **isHide** – `true` zum Ausblenden, `false` zum Anzeigen.  
- **needReCalculate** – optional, Standardwert `false`.

Die [OpenAPI-Spezifikation](https://apireference.aspose.cloud/cells/#/PivotTables/PostPivotTableFieldHideItem) definiert eine öffentlich zugängliche Programmierschnittstelle und ermöglicht es Ihnen, REST-Interaktionen direkt aus einem Webbrowser durchzuführen.

Sie können das cURL-Befehlszeilentool verwenden, um problemlos auf Aspose.Cells-Webservices zuzugreifen. Das folgende Beispiel zeigt, wie die API mit cURL aufgerufen wird.

{{< tabs tabTotal="2" tabID="1" tabName1="Anforderung" tabName2="Antwort" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/pivottables/0/PivotField/Hide?pivotFieldType=Row&fieldIndex=0&itemIndex=1&isHide=true&needReCalculate=true" \
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

**Antwortdetails**

| Statuscode | Beschreibung                                                           |
| ---------- | ---------------------------------------------------------------------- |
| 200        | Das Element wurde erfolgreich ausgeblendet.                           |
| 400        | Ungültige Anforderung – fehlende oder ungültige Parameter.            |
| 401        | Nicht autorisiert – ungültiges oder fehlendes JWT-Token.              |
| 500        | Serverfehler – der Vorgang konnte nicht abgeschlossen werden.         |

**Hinweis:** Wenn der übergebene `fieldIndex` oder `itemIndex` außerhalb des gültigen Bereichs liegt, gibt die API eine **400 Bad Request**-Antwort zurück.

## Cloud SDK-Familie

Die Verwendung eines SDKs ist die schnellste Methode zur Entwicklung gegenüber der API. SDKs übernehmen die Low-Level-Details, sodass Sie sich auf Ihre Geschäftslogik konzentrieren können. Besuchen Sie das [GitHub-Repository](https://github.com/aspose-cells-cloud), um eine vollständige Liste der Aspose.Cells Cloud SDKs zu erhalten.

Die folgenden Codebeispiele zeigen, wie ein Pivot-Feldelement mithilfe verschiedener SDKs ausgeblendet wird.

{{< tabs tabTotal="2" tabID="4" tabName1="C#" tabName2="Go" >}}

{{< tab tabNum="1" >}}

```csharp
public void Run_PivotTable_NeedReCalculate()
{
    // Bereiten Sie die Workbook und das Arbeitsblatt vor
    url = @"https://api.aspose.cloud/v3.0/storage/file/Temp/V17.02.00_01.xlsx";
    using (HttpWebResponse response = _helper.CallDelete(url, string.Empty, contentType))
    {
        Assert.AreEqual(response.StatusCode, HttpStatusCode.OK);
    }

    // Laden Sie die Workbook hoch
    url = @"https://api.aspose.cloud/v3.0/cells/V17.02.00_01.xlsx?folder=Temp";
    using (HttpWebResponse response = _helper.CallPut(url, string.Empty, contentType))
    {
        Assert.AreEqual(response.StatusCode, HttpStatusCode.OK);
    }

    // Erstellen Sie das Arbeitsblatt, das die Pivot-Tabelle enthalten soll
    url = @"https://api.aspose.cloud/v3.0/cells/V17.02.00_01.xlsx/worksheets/PivotSheet?folder=Temp";
    using (HttpWebResponse response = _helper.CallPut(url, string.Empty, contentType))
    {
        Assert.AreEqual(response.StatusCode, HttpStatusCode.OK);
    }

    // Erstellen Sie ein zweites Arbeitsblatt mit Beispieldaten
    url = @"https://api.aspose.cloud/v3.0/cells/V17.02.00_01.xlsx/worksheets/Sheet2?folder=Temp";
    using (HttpWebResponse response = _helper.CallPut(url, string.Empty, contentType))
    {
        Assert.AreEqual(response.StatusCode, HttpStatusCode.OK);
    }

    // Importieren Sie Beispieldaten in Sheet2
    url = @"https://api.aspose.cloud/v3.0/cells/V17.02.00_01.xlsx/importdata?folder=Temp";
    data = "{ \"BatchData\":[{...}] }"; // Aus Gründen der Kürze gekürzt
    using (HttpWebResponse response = _helper.CallPost(url, data, contentType))
    {
        Assert.AreEqual(response.StatusCode, HttpStatusCode.OK);
    }

    // Fügen Sie eine Pivot-Tabelle zu PivotSheet hinzu
    url = @"https://api.aspose.cloud/v3.0/cells/V17.02.00_01.xlsx/worksheets/PivotSheet/pivottables?folder=Temp";
    data = "{\"Name\":\"TestPivot\",\"SourceData\":\"=Sheet2!A1:E8\",\"DestCellName\":\"C1\",\"UseSameSource\":true,\"PivotFieldRows\":[0,1],\"PivotFieldColumns\":[2],\"PivotFieldData\":[3,4]}";
    using (HttpWebResponse response = _helper.CallPut(url, data, contentType))
    {
        Assert.AreEqual(response.StatusCode, HttpStatusCode.OK);
    }

    // Blenden Sie ein bestimmtes Zeilenfeldelement aus
    url = @"https://api.aspose.cloud/v3.0/cells/V17.02.00_01.xlsx/worksheets/PivotSheet/pivottables/0/PivotField/Hide?pivotFieldType=Row&fieldIndex=0&itemIndex=1&isHide=true&needReCalculate=true&folder=Temp";
    using (HttpWebResponse response = _helper.CallPost(url, string.Empty, contentType))
    {
        Assert.AreEqual(response.StatusCode, HttpStatusCode.OK);
    }
}
```

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "a0bec26a8274b9f7cb514015843a214e" >}}

{{< /tab >}}

{{< /tabs >}}

**Hinweis:** Die SDK-Beispiele setzen voraus, dass Sie die Authentifizierung (JWT-Token) bereits konfiguriert haben und sich die Workbook im angegebenen Speicherordner befindet. Passen Sie die Parameter `folder` und `storageName` je nach Ihrer Umgebung entsprechend an.