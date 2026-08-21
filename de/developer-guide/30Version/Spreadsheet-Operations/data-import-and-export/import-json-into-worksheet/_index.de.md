---
title: "JSON-Daten in Excel importieren"
second_title: "Dokument"
linktitle: "JSON importieren"
type: docs
url: /import-json-data-into-excel/
aliases: [/import/json/]
keywords: "Aspose.Cells Cloud, JSON-Import, Excel-API, REST-JSON-Import, SDK-Beispiele"
description: "Erfahren Sie, wie Sie JSON-Daten mithilfe der Aspose.Cells Cloud REST-API in ein Excel-Arbeitsblatt importieren. Enthält Endpunktdetails, Anforderungs-/Antwortbeispiele und SDK-Code für .NET, Java und Python."
weight: 40
---

Diese REST-API **importiert JSON-Daten** in ein Excel-Arbeitsblatt.

## REST-API

```bash
POST https://api.aspose.cloud/v3.0/cells/{name}/importjson
```
### **Sicherheit und Authentifizierung**

Die Aspose.Cells Cloud-APIs sind sicher und erfordern eine <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-Token-basierte Authentifizierung</a>.

### **Anforderungsparameter**

| Parametername         | Position     | Typ    | Beschreibung                                                                                         |
| --------------------- | ------------ | ------ | ---------------------------------------------------------------------------------------------------- |
| name                  | Pfad         | string | Der Name der Arbeitsmappe.                                                                           |
| importJsonRequest     | HTTP-Body    | class  | Die Anforderungsnutzdaten, die Details zum JSON-Import enthalten.                                   |
| password              | Abfragezeichenfolge | string | Passwort zum Öffnen der Arbeitsmappe (falls geschützt).                                             |
| folder                | Abfragezeichenfolge | string | Der Ordner, der die ursprüngliche Arbeitsmappe enthält.                                            |
| storageName           | Abfragezeichenfolge | string | Der Name des Speichers, in dem sich die Arbeitsmappe befindet.                                     |
| outPath               | Abfragezeichenfolge | string | Pfad für die Ausgabedatei nach dem Import. Falls weggelassen, wird die aktualisierte Arbeitsmappe in der Antwort zurückgegeben. |
| outStorageName        | Abfragezeichenfolge | string | Speichername für die Ausgabedatei.                                                                  |
| checkExcelRestriction | Abfragezeichenfolge | string | Kennzeichen, ob Excel-spezifische Einschränkungen erzwungen werden sollen (true/false).             |

### **Beispiel für Anforderungstext**

```json
{
  "JsonFileSource": {
    "FilePath": "string"
  },
  "ImportPosition": {
    "SheetName": "string",
    "RowIndex": 0,
    "ColumnIndex": 0
  },
  "JsonContent": "string"
}
```

### Antwort

Eine erfolgreiche Anforderung gibt **HTTP 200** mit einem JSON-Payload zurück, der folgendermaßen aussieht:

```json
{
  "Code": 200,
  "Status": "OK"
}
```

Mögliche Statuscodes:

| Code | Bedeutung                                      |
| ---- | ---------------------------------------------- |
| 200  | Import erfolgreich                             |
| 400  | Ungültige Anforderung – fehlende oder ungültige Daten |
| 401  | Nicht autorisiert – ungültiges oder fehlendes Token |
| 500  | Interner Serverfehler                          |


## Verwendung der PostWorkbookImportJson-API mit SDKs

### PostWorkbookImportJson-API-Spezifikation

Die [OpenAPI-Spezifikation](https://reference.aspose.cloud/cells/#/DataProcessing/PostWorkbookImportJson) definiert eine öffentlich zugängliche Programmierschnittstelle und ermöglicht REST-Interaktionen direkt über einen Webbrowser.

### Verwendung der Aspose.Cells Cloud SDKs

Die Verwendung eines SDKs ist die effizienteste Methode, um die Entwicklung zu beschleunigen. SDKs übernehmen die Details auf niedriger Ebene, sodass Sie sich auf Ihre Geschäftslogik konzentrieren können. Eine vollständige Liste der Aspose.Cells Cloud SDKs finden Sie im [GitHub-Repository](https://github.com/aspose-cells-cloud).

Die folgenden Codebeispiele zeigen, wie Aspose.Cells-Webservices mithilfe verschiedener SDKs aufgerufen werden:

---