---
title: "Mehrere Zeilen zu einem Excel-Arbeitsblatt hinzufügen"
ArticleTitle: "Mehrere Zeilen zu einem Excel-Arbeitsblatt mit der Aspose.Cells Cloud API hinzufügen"
second_title: "Dokument"
linktype: "Rows"
type: docs
url: /rows/add/rows/
keywords: "Aspose.Cells Cloud, Zeilen einfügen, Excel-Arbeitsblatt, REST API, SDK, mehrere Zeilen hinzufügen"
description: "Erfahren Sie, wie Sie die Aspose.Cells Cloud REST API verwenden, um mehrere Zeilen in ein Excel-Arbeitsblatt einzufügen. Dieser Leitfaden behandelt den Endpunkt, die Anforderungsparameter, Beispiels cURL-Befehle und SDK-Nutzungsbeispiele."
weight: 20
---

Diese REST API fügt mehrere neue Zeilen zu einem Excel-Arbeitsblatt hinzu.

## PutInsertWorksheetRows API

```http
PUT http://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/rows
```

### **Sicherheit und Authentifizierung**

Die Aspose.Cells Cloud APIs sind sicher und erfordern eine <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-Token-basierte Authentifizierung</a>.

### **Anforderungsparameter**

| Parametername   | Typ     | Position | Beschreibung                                                         |
| --------------- | ------- | -------- | -------------------------------------------------------------------- |
| name            | string  | path     | Der Name der Arbeitsmappe.                                           |
| sheetName       | string  | path     | Der Name des Arbeitsblatts.                                          |
| startrow        | integer | query    | Der Index der ersten einzufügenden Zeile (**0-basiert**).            |
| totalRows       | integer | query    | Die Anzahl der einzufügenden Zeilen.                                 |
| updateReference | boolean | query    | Gibt an, ob Zellverweise nach dem Einfügen aktualisiert werden sollen (`true` oder `false`). |
| folder          | string  | query    | Der Ordner, der das Dokument enthält.                                |
| storageName     | string  | query    | Der Speichername.                                                    |

**Voraussetzungen**  
Die Arbeitsmappe muss bereits im angegebenen Speicher (oder Ordner) vorhanden sein, bevor dieser Vorgang aufgerufen wird.

**Authentifizierung**  
Die API erfordert ein gültiges JWT-Token. Fügen Sie es in den `Authorization`-Header ein, wie im folgenden cURL-Beispiel gezeigt.

Die [OpenAPI-Spezifikation](https://apireference.aspose.cloud/cells/#/Cells/PutInsertWorksheetRows) definiert eine öffentlich zugängliche Programmierschnittstelle und ermöglicht es Ihnen, REST-Interaktionen direkt aus einem Webbrowser durchzuführen.

Sie können das cURL-Befehlszeilentool verwenden, um problemlos auf Aspose.Cells-Webdienste zuzugreifen. Das folgende Beispiel zeigt, wie die Cloud-API mit cURL aufgerufen wird.

{{< tabs tabTotal="2" tabID="1" tabName1="Anforderung" tabName2="Antwort" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/cells/rows?startrow=1&totalRows=11&updateReference=true" \
  -X PUT \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

> **Hinweis:** Dieser `PUT`-Vorgang erfordert keinen Anforderungstext; ein leeres JSON-Objekt (`{}`) kann gesendet werden, wenn die Client-Bibliothek einen Payload erzwingt.

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

*Mögliche Antwortcodes*  

- **200 OK** – Zeilen erfolgreich eingefügt.  
- **400 Bad Request** – Ungültige Parameter (z. B. negativer Zeilenindex).  
- **401 Unauthorized** – Fehlendes oder ungültiges JWT-Token.  
- **404 Not Found** – Die angegebene Arbeitsmappe oder das angegebene Arbeitsblatt ist nicht vorhanden.  
- **500 Internal Server Error** – Unerwarteter Serverfehler.

{{< /tab >}}

{{< /tabs >}}

Weitere Vorgänge zu Zeilen finden Sie auf den folgenden Seiten: **Zeilen löschen**, **Zeilen abrufen** und **Zeilen kopieren**.

## Cloud SDK-Familie

Die Verwendung eines SDK ist die schnellste Möglichkeit zur Entwicklung. Ein SDK übernimmt Low-Level-Details, sodass Sie sich auf Ihr Projekt konzentrieren können. Überprüfen Sie das [GitHub-Repository](https://github.com/aspose-cells-cloud) für eine vollständige Liste der Aspose.Cells Cloud SDKs.

Die folgenden Codebeispiele zeigen, wie Aspose.Cells-Webdienste mithilfe verschiedener SDKs aufgerufen werden:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePutInsertWorksheetRows.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PutInsertWorksheetRows.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PutInsertWorksheetRows.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PutInsertWorksheetRows.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2b4189bc27ae92abf73c36b4df0" "Example_PutInsertWorksheetRows.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PutInsertWorksheetRows.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PutInsertWorksheetRows.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PutInsertWorksheetRows.go" >}}

{{< /tab >}}

{{< /tabs >}}