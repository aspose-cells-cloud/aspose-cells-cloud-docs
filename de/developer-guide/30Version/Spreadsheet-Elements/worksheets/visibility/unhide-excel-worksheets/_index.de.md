---
title: "Excel-Arbeitsblatt anzeigen"
second_title: "Dokument"
linktitle: "Anzeigen"
type: docs
url: /de/worksheets/unhide/
aliases: [  /de/unhide-excel-worksheets/ ]
keywords: "Aspose.Cells, Arbeitsblatt anzeigen, Excel-API, Cloud-Tabellenkalkulation, REST, Sichtbarkeit des Arbeitsblatts, Excel-Arbeitsmappe"
description: "Erfahren Sie, wie Sie die Aspose.Cells Cloud REST API verwenden, um ein Arbeitsblatt in einer Excel-Arbeitsmappe wieder anzuzeigen. Enthält Anforderungsdetails, cURL-Beispiele und SDK-Codeausschnitte für mehrere Programmiersprachen."
weight: 60
---

Diese REST API stellt einen Endpunkt bereit, um ein **Arbeitsblatt in einer Excel-Arbeitsmappe wieder anzuzeigen**.

**Voraussetzungen**  
Bevor Sie diesen Vorgang aufrufen, müssen Sie Folgendes erfüllt haben:

* Ein gültiges Aspose Cloud-Zugriffstoken (JWT) im `Authorization`-Header.  
* Die Arbeitsmappe muss an einem unterstützten Speicherort gespeichert sein, den Sie mit den Abfrageparametern `folder` und `storageName` angeben.  
* Die Arbeitsmappe muss in einem Format vorliegen, das von Aspose.Cells unterstützt wird (z. B. `.xls`, `.xlsx`, `.xlsm`).  

## REST API

```bash
PUT https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/visible
```

### **Anforderungsparameter**

| Parametername | Typ     | Position | Beschreibung                                |
| ------------- | ------- | -------- | ------------------------------------------- |
| name          | string  | path     | Name des Dokuments.                         |
| sheetName     | string  | path     | Name des Arbeitsblatts.                     |
| isVisible     | boolean | query    | Neuer Wert für die Sichtbarkeit des Arbeitsblatts (`true`). |
| folder        | string  | query    | Der Dokumentenordner.                       |
| storageName   | string  | query    | Name des Speichers.                         |

Die [OpenAPI-Spezifikation](https://apireference.aspose.cloud/cells/#/Worksheets/PutChangeVisibilityWorksheet) definiert eine öffentlich zugängliche Programmierschnittstelle, mit der Sie REST-Interaktionen direkt aus einem Webbrowser durchführen können.

Sie können das cURL-Befehlszeilentool verwenden, um Aspose.Cells-Webservices einfach aufzurufen. Das folgende Beispiel zeigt, wie eine Anforderung mit cURL gestellt wird.

{{< tabs tabTotal="2" tabID="1" tabName1="Anforderung" tabName2="Antwort" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Sample_Test_Book.xls/worksheets/Sheet1/visible?isVisible=true" \
-X PUT \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"   # ersetzen Sie <jwt token> durch Ihr Zugriffstoken
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

**Mögliche Antwortcodes**

| HTTP-Code | Bedeutung                                         | Beispiel-Body (sofern zutreffend)                           |
|-----------|---------------------------------------------------|--------------------------------------------------------------|
| 200       | Sichtbarkeit des Arbeitsblatts erfolgreich aktualisiert | `{ "Code": 200, "Status": "OK" }`                           |
| 400       | Ungültige Anforderung – fehlende oder ungültige Parameter | `{ "Code": 400, "Message": "Ungültige Anforderungsparameter." }` |
| 401       | Nicht autorisiert – fehlendes oder ungültiges JWT-Token | `{ "Code": 401, "Message": "Authentifizierung fehlgeschlagen." }` |
| 404       | Nicht gefunden – Arbeitsmappe oder Arbeitsblatt existiert nicht | `{ "Code": 404, "Message": "Datei oder Arbeitsblatt nicht gefunden." }` |
| 500       | Interner Serverfehler                             | `{ "Code": 500, "Message": "Ein unerwarteter Fehler ist aufgetreten." }` |

{{< /tab >}}

{{< /tabs >}}

## Cloud SDK-Familie

Die Verwendung eines SDKs ist der schnellste Weg zur Entwicklung. Ein SDK übernimmt die Low-Level-Details, sodass Sie sich auf Ihr Projekt konzentrieren können. Eine vollständige Liste der Aspose.Cells Cloud SDKs finden Sie im [GitHub-Repository](https://github.com/aspose-cells-cloud).

Die folgenden Codebeispiele zeigen, wie Aspose.Cells-Webservices mithilfe verschiedener SDKs aufgerufen werden:

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Perl" tabName8="Android" tabName9="Objective C" tabName10="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNET-CSharp-Worksheet-UnhideWorksheet-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-worksheet-UnhideWorksheet-unhide-worksheets.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Worksheet-PutChangeVisibilityWorksheet-.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Worksheet-change_worksheet_visibility-.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "UnhideExcelWorksheets.py" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-Worksheet-UnhideWorksheet-1.js" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-Worksheet-UnhideWorksheet-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "9d725d4678edaac53f95c5208e17783c" "Examples-Android-worksheet-UnhideWorksheet-unhide-worksheets.java" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< gist "aspose-cells-cloud-gists" "e30ac521e9cdb174baa702a743be16ae" >}}

{{< /tab >}}

{{< /tabs >}}