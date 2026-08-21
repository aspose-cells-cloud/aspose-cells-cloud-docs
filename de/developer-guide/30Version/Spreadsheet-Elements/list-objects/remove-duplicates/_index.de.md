---
title: "Doppelte Zeilen aus einer ListObject entfernen – Aspose.Cells Cloud API-Dokumentation"
second_title: "Dokument"
linktitle: "Doppelte entfernen"
type: docs
keywords: "doppelte entfernen, listobject, aspose.cells cloud api, excel, rest"
url: /de/list-objects/remove-duplicates/
description: "Erfahren Sie, wie Sie doppelte Zeilen aus einem ListObject in einem Excel-Arbeitsblatt mithilfe der Aspose.Cells Cloud REST API entfernen. Enthält Endpunkt, Parameter, Authentifizierung sowie Beispielanfragen und -antworten."
weight: 20
---

Diese REST API entfernt doppelte Zeilen aus einem **ListObject** in einem Excel-Arbeitsblatt.

## REST API

```bash
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/listobjects/{listObjectIndex}/RemoveDuplicates
```

### **Anforderungsparameter**

| Parametername       | Typ     | Ort     | Beschreibung                                           |
| ------------------- | ------- | ------- | ------------------------------------------------------ |
| **name**            | String  | Pfad    | Der Name der Excel-Datei.                              |
| **sheetName**       | String  | Pfad    | Der Name des Arbeitsblatts, das das ListObject enthält. |
| **listObjectIndex** | Integer | Pfad    | Der nullbasierte Index des zu verarbeitenden ListObjects. |
| **folder**          | String  | Abfrage | (Optional) Der Ordnerpfad, in dem die Datei gespeichert ist. |
| **storageName**     | String  | Abfrage | (Optional) Der Name des Speicherdienstes.             |

### Beispielanfrage (cURL)

{{< tabs tabTotal="2" tabID="1" tabName1="Anfrage" tabName2="Antwort" >}}
{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/listobjects/{listObjectIndex}/RemoveDuplicates" \
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
  "Status": "OK",
  "DuplicateRowsRemoved": 12,
  "Message": "Doppelte Zeilen wurden erfolgreich entfernt."
}
```

{{< /tab >}}
{{< /tabs >}}

### Antwort

Im Erfolgsfall gibt der Dienst ein JSON-Objekt zurück, das dem obigen Beispiel ähnelt. Die Felder sind:

- **Code** – HTTP-Statuscode (`200` bei Erfolg).
- **Status** – Textuelle Beschreibung des Status.
- **DuplicateRowsRemoved** – Anzahl der entfernten Zeilen.
- **Message** – Zusätzliche Informationen zum Vorgang.

**HTTP-Statuscodes**

| Code | Bedeutung                   | Beschreibung                                               |
|------|-----------------------------|------------------------------------------------------------|
| 200  | OK                          | Filter erfolgreich angewendet; Antwort enthält Vorgangsdetails. |
| 400  | Bad Request                 | Fehlende oder ungültige Parameter (z. B. nicht unterstützter Dateityp). |
| 401  | Unauthorized                | Ungültiger oder fehlender JWT-Token.                      |
| 413  | Payload Too Large           | Die hochgeladene Datei überschreitet das Größenlimit.     |
| 500  | Internal Server Error       | Unerwarteter Serverfehler.                                |
## Cloud SDK-Familie

Die Verwendung eines SDKs ist der beste Weg, die Entwicklungszeit zu verkürzen. Ein SDK übernimmt die Details auf niedriger Ebene, sodass Sie sich auf die Aufgaben Ihres Projekts konzentrieren können. Bitte prüfen Sie das GitHub-Repository für eine vollständige Liste der Aspose.Cells Cloud SDKs.

Die folgenden Codebeispiele zeigen, wie Aspose.Cells-Webservices mithilfe verschiedener SDKs aufgerufen werden:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostWorksheetListObjectRemoveDuplicates.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostWorksheetListObjectRemoveDuplicates.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostWorksheetListObjectRemoveDuplicates.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostWorksheetListObjectRemoveDuplicates.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostWorksheetListObjectRemoveDuplicates.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostWorksheetListObjectRemoveDuplicates.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostWorksheetListObjectRemoveDuplicates.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostWorksheetListObjectRemoveDuplicates.go" >}}

{{< /tab >}}

{{< /tabs >}}