---
title: "Duplikate entfernen"
ArticleTitle: "Duplikate entfernen – Aspose.Cells Cloud API"
second_title: "Dokument"
linktype: "docs"
url: /cells/remove/duplicates
aliases: []
keywords: "Aspose.Cells, Duplikate entfernen, API"
description: "Entfernt doppelte Werte in einem Arbeitsblatt, einem Bereich oder einer Tabelle."
weight: 1000
---

## Das Entfernen von Duplikaten mit Aspose.Cells Cloud-Webdiensten

Entfernt doppelte Werte im Arbeitsblatt, im Bereich oder in der Tabelle. Diese Methode durchsucht den Zielbereich nach Zeilen mit identischen Werten in den angegebenen Spalten, die überprüft werden sollen. Bei jeder Gruppe von Duplikaten werden alle Vorkommen bis auf das erste entfernt. Der Vergleich erfolgt in der Regel unterscheidend zwischen Groß- und Kleinschreibung und prüft den exakten Zellwert.

### Web-API-Endpunkt

```http
PUT https://api.aspose.cloud/v4.0/cells/remove/duplicates
```

### **Sicherheit und Authentifizierung**

Die Aspose.Cells Cloud-APIs sind sicher und erfordern eine <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-Token-basierte Authentifizierung</a>.

### Anforderungsparameter

| Parametername   | Typ    | Pfad/Abfragezeichenfolge/HTTP-Body | Beschreibung |
|-----------------|--------|------------------------------------|--------------|
| Spreadsheet     | Datei  | FormData                           | Laden Sie die Tabellendatei hoch. |
| worksheet       | String | Abfrage                            | Der Name des Arbeitsblatts. (optional) |
| range           | String | Abfrage                            | Der Name des Bereichs, aus dem Duplikate entfernt werden sollen. (optional) |
| table           | String | Abfrage                            | Der Name der Tabelle, aus der Duplikate entfernt werden sollen. (optional) |
| outPath         | String | Abfrage                            | (Optional) Der Ordnerpfad, in dem die Arbeitsmappe gespeichert ist. Standardwert ist null. |
| outStorageName  | String | Abfrage                            | Name des Speichers für die Ausgabedatei. |
| region          | String | Abfrage                            | Regionale/lokale Einstellung der Tabellendatei (z. B. `de-DE`, `fr-FR`). Beeinflusst die Zahlenformatierung, Datumsauswertung und länderspezifisches Verhalten. |
| password        | String | Abfrage                            | Das Passwort zum Öffnen der Tabellendatei. |

### Anforderungstextparameter

| Parametername | Typ | Beschreibung |
| ------------- | --- | ------------ |
| [TBD] | [TBD] | [TBD] |

### **Antwort**

```json
{
  "File": "Binärstream der resultierenden Tabellendatei (z. B. .xlsx)"
}
```

**HTTP-Antwortstatuscodes**

| Code | Bedeutung | Beschreibung |
|------|-----------|--------------|
| 200 | OK | Die resultierende Tabellendatei mit entfernten Duplikaten wird als Dateistream zurückgegeben. |
| 400 | Bad Request | Ungültige Anforderungsparameter oder falsch formatierte URL. |
| 401 | Unauthorized | Authentifizierung fehlgeschlagen oder keine Anmeldeinformationen bereitgestellt. |
| 413 | Payload Too Large | Die hochgeladene Datei überschreitet das zulässige Dateigrößenlimit. |
| 500 | Internal Server Error | In der Tabellendatei ist beim Abrufen von Daten oder einem anderen serverseitigen Fehler ein Problem aufgetreten. |

## Verwendung des Entfernens von Duplikaten mit SDKs

### Spezifikation für das Entfernen von Duplikaten

Die [API-Spezifikation zum Entfernen von Duplikaten](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/{Transform}/{RemoveDuplicates}) definiert eine öffentlich zugängliche Programmierschnittstelle und ermöglicht REST-Interaktionen direkt aus einem Webbrowser.

Sie können das cURL-Befehlszeilentool nutzen, um einfach auf Aspose.Cells-Webdienste zuzugreifen. Im folgenden Beispiel wird gezeigt, wie Aufrufe an die Cloud-API mit cURL durchgeführt werden.

{< tabs tabTotal="2" tabID="1" tabName1="Anforderung" tabName2="Antwort" >}
{< tab tabNum="1" >}
```bash
# Verwenden Sie HTTPS für eine sichere Verbindung
curl -v "https://api.aspose.cloud/v4.0/cells/remove/duplicates?worksheet=Tabelle1&range=A1:C10&table=MeineTabelle&outPath=ausgabe%2Fordner&outStorageName=MeinSpeicher&region=de-DE&password=MeinPasswort" \
  -X PUT \
  -H "Content-Type: multipart/form-data" \
  -H "Accept: application/octet-stream" \
  -H "Authorization: Bearer <jwt token>" \
  -F 'Spreadsheet=@beispiel.xlsx'
```
{< /tab >}
{< tab tabNum="2" >}
```json
{
  "File": "Binärstream der resultierenden Tabellendatei (z. B. .xlsx)"
}
```
{< /tab >}
{< /tabs >}

### Verwendung der Aspose Cells Cloud SDKs

Die Verwendung eines SDKs ist die schnellste Möglichkeit, die Entwicklung zu beschleunigen. Ein SDK abstractiert Low-Level-Details, sodass Sie sich auf Ihre Projekt Aufgaben konzentrieren können. Weitere Informationen finden Sie im <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub-Repository</a> für eine vollständige Liste der Aspose.Cells Cloud SDKs.

Die folgenden Codebeispiele zeigen, wie Aspose Cells Cloud-Webdienste mithilfe verschiedener SDKs aufgerufen werden:

```csharp
// SDK-Beispielcode für C#
var config = new Configuration
{
    AccessToken = "<jwt token>"
};
var apiInstance = new TransformApi(config);
var file = File.ReadAllBytes("example.xlsx");
var result = apiInstance.RemoveDuplicates(
    file,
    worksheet: "Sheet1",
    range: "A1:C10",
    table: "MyTable",
    outPath: "output/folder",
    outStorageName: "MyStorage",
    region: "en-US",
    password: "MyPassword"
);
File.WriteAllBytes("result.xlsx", result);
```

```java
// SDK-Beispielcode für Java
ApiClient client = new ApiClient();
client.setAccessToken("<jwt token>");
TransformApi api = new TransformApi(client);
byte[] file = Files.readAllBytes(Paths.get("example.xlsx"));
byte[] result = api.removeDuplicates(
    file,
    "Sheet1",
    "A1:C10",
    "MyTable",
    "output/folder",
    "MyStorage",
    "en-US",
    "MyPassword"
);
Files.write(Paths.get("result.xlsx"), result);
```

```python
# SDK-Beispielcode für Python
import asposecellscloud
from asposecellscloud.rest import ApiException

configuration = asposecellscloud.Configuration()
configuration.access_token = "<jwt token>"
api_instance = asposecellscloud.TransformApi(asposecellscloud.ApiClient(configuration))

with open('example.xlsx', 'rb') as f:
    file_bytes = f.read()

try:
    result = api_instance.remove_duplicates(
        file=file_bytes,
        worksheet='Sheet1',
        range='A1:C10',
        table='MyTable',
        out_path='output/folder',
        out_storage_name='MyStorage',
        region='en-US',
        password='MyPassword'
    )
    with open('result.xlsx', 'wb') as out_f:
        out_f.write(result)
except ApiException as e:
    print("Exception when calling TransformApi->remove_duplicates: %s\\n" % e)
```

`[TBD]`
---