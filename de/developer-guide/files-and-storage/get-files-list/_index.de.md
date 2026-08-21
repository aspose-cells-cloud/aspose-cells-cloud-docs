---
title: "Aspose.Cells Cloud API – Dateiliste abrufen (Ordnerinhalte)"
description: "Rufen Sie eine Liste von Dateien und Unterordnern aus einem bestimmten Ordner im Aspose.Cells Cloud-Speicher ab."
keywords:
  - Aspose.Cells
  - API
  - Dateiliste abrufen
  - Cloud-Speicher
  - Excel
  - REST
type: docs
weight: 100
---

Die **Get Files List**-Operation gibt die Sammlung von Dateien und Unterordnern zurück, die in einem angegebenen Ordner des Aspose.Cells Cloud-Speichers gespeichert sind.  
Sie ist der primäre Einstiegspunkt zum Durchsuchen cloudbasierter Excel-Arbeitsmappen, Archive und weiterer unterstützter Dateitypen.

## Aspose.Cells Cloud API – Dateiliste abrufen (Ordnerinhalte)

```
GET https://api.aspose.cloud/v4.0/cells/storage/folder/{path}
```

### **Sicherheit und Authentifizierung**

Die Aspose.Cells Cloud APIs sind sicher und erfordern eine <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-Token-basierte Authentifizierung</a>.

### Anforderungsparameter

| Name            | Position | Typ     | Erforderlich | Beschreibung                                                                 |
| --------------- | -------- | ------- | ------------ | ---------------------------------------------------------------------------- |
| **path**        | Pfad     | string  | Ja           | Pfad zum Ordner im Cloud-Speicher.                                           |
| **storageName** | Abfrage  | string  | Nein         | Name des zu verwendenden Speichers. Falls weggelassen, wird der Standardspeicher verwendet. |
| **pageSize**    | Abfrage  | integer | Nein         | Maximale Anzahl von Elementen pro Seite (Standard: 100).                    |
| **pageNumber**  | Abfrage  | integer | Nein         | Seite, die abgerufen werden soll (beginnend bei 1, Standard: 1).            |

- **Value** – Array von `StorageFile`-Objekten. Jedes Objekt enthält:
  - `Name` – Datei- oder Ordnername.
  - `IsFolder` – `true`, wenn der Eintrag ein Ordner ist.
  - `Size` – Größe in Bytes (Ordner geben `0` an).
  - `ModifiedDate` – Zeitstempel der letzten Änderung (ISO 8601).

### **Antwort**

**HTTP-Statuscodes**

| HTTP-Code | HTTP-Status           | Beschreibung                                                    |
| --------- | --------------------- | --------------------------------------------------------------- |
| 200       | OK                    | Web-API erfolgreich aufgerufen; Antwort enthält Vorgangsdetails. |
| 400       | Bad Request           | Fehlende oder ungültige Parameter (z. B. nicht unterstützter Dateityp). |
| 401       | Unauthorized          | Ungültiger oder fehlender JWT-Token.                           |
| 413       | Payload Too Large     | Die hochgeladene Datei überschreitet das Größenlimit.          |
| 500       | Internal Server Error | Unerwarteter Serverfehler.                                     |
|           |                       |                                                                 |

## OpenAPI-Spezifikation

Die [OpenAPI-Spezifikation](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Folder/GetFilesList) definiert eine öffentlich zugängliche Programmierschnittstelle und ermöglicht es Ihnen, REST-Interaktionen direkt aus einem Webbrowser heraus durchzuführen.

Sie können das cURL-Befehlszeilentool verwenden, um problemlos auf Aspose.Cells-Webservices zuzugreifen. Das folgende Beispiel zeigt, wie Sie mit cURL Aufrufe an die Cloud-API durchführen.

{{< tabs tabTotal="2" tabID="11" tabName11="Anforderung" tabName12="Antwort" >}}

{{< tab tabNum="11" >}}

```bash
curl -X GET "https://api.aspose.cloud/v4.0/cells/storage/folder/{path}?storageName=MyStorage&pageSize=100&pageNumber=1" \
     -H "Authorization: Bearer <your_access_token>"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Value": [
    {
      "Name": "Report.xlsx",
      "IsFolder": false,
      "Size": 124578,
      "ModifiedDate": "2024-03-10T12:34:56Z"
    },
    {
      "Name": "Archives",
      "IsFolder": true,
      "Size": 0,
      "ModifiedDate": "2024-02-01T08:00:00Z"
    }
  ]
}
```

{{< /tab >}}

{{< /tabs >}}

### Verwenden Sie Aspose.Cells Cloud SDKs

Die Verwendung eines SDKs ist der beste Weg, um die Entwicklung zu beschleunigen. Ein SDK verwaltet die Low-Level-Details und lässt Sie sich auf Ihre Projektaktivitäten konzentrieren. Bitte prüfen Sie das <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub-Repository</a> für eine vollständige Liste der Aspose.Cells Cloud SDKs.

Die folgenden Codebeispiele zeigen, wie Aufrufe an Aspose.Cells-Webservices mithilfe verschiedener SDKs durchgeführt werden:

---