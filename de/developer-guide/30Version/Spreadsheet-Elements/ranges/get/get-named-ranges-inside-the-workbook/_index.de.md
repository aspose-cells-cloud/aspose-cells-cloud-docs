---
title: "Benannte Bereiche in einer Excel-Arbeitsmappe abrufen"
second_title: "Dokument"
linktitle: "Name"
type: docs
url: /de/ranges/get/name/
aliases: [  /de/get-named-ranges-inside-the-workbook/ ]
keywords: "benannte Bereiche, Excel, Aspose.Cells, Cloud-API, Arbeitsblätter"
description: "Rufen Sie benannte Bereiche aus einer Excel-Arbeitsmappe mithilfe der Aspose.Cells Cloud REST-API ab. Enthält Anforderungsdetails, Beispiel-cURL-Befehle und SDK-Beispiele für mehrere Programmiersprachen."
ArticleTitle: "Benannte Bereiche in einer Excel-Arbeitsmappe abrufen – Aspose.Cells Cloud API"
weight: 10
---

Diese REST-API gibt Informationen zu benannten Bereichen zurück, die in Arbeitsblättern definiert sind.

**Hintergrund** – Ein *benannter Bereich* ist eine benutzerdefinierte Kennung, die auf eine bestimmte Zelle oder Zellgruppe in einem Arbeitsblatt verweist. Benannte Bereiche vereinfachen die Formelerstellung, verbessern die Lesbarkeit und ermöglichen programmgesteuerten Zugriff auf häufig verwendete Bereiche einer Arbeitsmappe.

**Voraussetzungen** – Der Zugriff auf die Aspose.Cells Cloud API erfordert ein gültiges JWT-Access-Token. Holen Sie sich das Token durch Authentifizierung mit Ihrer Aspose-Cloud-Client-ID und Ihrem Clientgeheimnis über den OAuth 2.0-Token-Endpunkt. Binden Sie das Token in den Header `Authorization: Bearer <jwt token>` jeder Anforderung ein.

## GetNamedRanges API

```http
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/ranges
```

### **Sicherheit und Authentifizierung**

Die Aspose.Cells Cloud APIs sind sicher und erfordern <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-Token-basierte Authentifizierung</a>.

### Anforderungsparameter

| Parametername   | Typ    | Standort       | Beschreibung                                      |
| --------------- | ------ | -------------- | ------------------------------------------------- |
| name            | string | Pfad           | Der Name der Excel-Datei.                         |
| folder          | string | Abfragezeichenfolge | Der Ordner, der das Dokument enthält.         |
| storageName     | string | Abfragezeichenfolge | Der Speichername, in dem sich das Dokument befindet. |

**HTTP-Statuscodes**

| Code | Bedeutung                   | Beschreibung                                      |
|------|-----------------------------|---------------------------------------------------|
| 200  | OK                          | Filter erfolgreich angewendet; Antwort enthält Details zum Vorgang. |
| 400  | Bad Request                 | Fehlende oder ungültige Parameter (z. B. nicht unterstützter Dateityp). |
| 401  | Unauthorized                | Ungültiges oder fehlendes JWT-Token.             |
| 413  | Payload Too Large           | Die hochgeladene Datei überschreitet das Größenlimit. |
| 500  | Internal Server Error       | Unerwarteter Serverfehler.                        |

Die [OpenAPI-Spezifikation](https://apireference.aspose.cloud/cells/#/Worksheets/GetNamedRanges) definiert eine öffentlich zugängliche Programmierschnittstelle, mit der Sie REST-Interaktionen direkt aus einem Webbrowser heraus durchführen können.

Sie können das cURL-Befehlszeilentool verwenden, um Aspose.Cells-Webdienste aufzurufen. Das folgende Beispiel zeigt, wie Sie benannte Bereiche mit cURL abrufen.

{{< tabs tabTotal="2" tabID="1" tabName1="Anforderung" tabName2="Antwort" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/ranges" \
  -X GET \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Ranges": {
    "RangeList": [
      {
        "ColumnCount": 7,
        "ColumnWidth": 8.428571428571429,
        "FirstColumn": 1,
        "FirstRow": 9,
        "Name": "data",
        "RefersTo": "=Sheet1!$B$10:$H$10",
        "RowCount": 1,
        "RowHeight": 15,
        "Worksheet": "Sheet1"
      }
    ]
  },
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

**Antwortmodell**

| Feld            | Typ     | Beschreibung                                           |
|-----------------|---------|--------------------------------------------------------|
| `ColumnCount`   | integer | Anzahl der Spalten im Bereich.                         |
| `ColumnWidth`   | number  | Breite jeder Spalte (in Punkten).                      |
| `FirstColumn`   | integer | Nullbasierter Index der ersten Spalte im Bereich.     |
| `FirstRow`      | integer | Nullbasierter Index der ersten Zeile im Bereich.      |
| `Name`          | string  | Der benutzerdefinierte Name des Bereichs.             |
| `RefersTo`      | string  | Eine Formel, die die Zellreferenz definiert (z. B. `=Sheet1!$B$10:$H$10`). |
| `RowCount`      | integer | Anzahl der Zeilen im Bereich.                          |
| `RowHeight`     | number  | Höhe jeder Zeile (in Punkten).                         |
| `Worksheet`     | string  | Name des Arbeitsblatts, das den Bereich enthält.      |

## Cloud SDK-Familie

Die Verwendung eines SDKs ist der schnellste Weg, diese Funktionalität zu integrieren. SDKs übernehmen die Low-Level-Details, sodass Sie sich auf Ihre Geschäftslogik konzentrieren können. Eine vollständige Liste der Aspose.Cells Cloud SDKs finden Sie im [GitHub-Repository](https://github.com/aspose-cells-cloud).

Die folgenden Codebeispiele zeigen, wie Aspose.Cells-Webdienste mithilfe verschiedener SDKs aufgerufen werden:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetNamedRanges.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetNamedRanges.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetNamedRanges.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetNamedRanges.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_GetNamedRanges.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetNamedRanges.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetNamedRanges.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetNamedRanges.go" >}}

{{< /tab >}}

{{< /tabs >}}