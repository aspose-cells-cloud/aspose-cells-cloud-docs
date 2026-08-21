---
title: "Überprüfen, ob ein Speicher vorhanden ist – Aspose.Cells Cloud API (v4.0)"
second_title: "Dokument"
ArticleTitle: "Cloud-basiertes Excel-Dateimanagement – Überprüfung der Speichervorhandenheit"
linktype: "storage-exists"
type: docs
url: /de/storage-exists/
keywords: "Aspose.Cells, Speicher vorhanden, Cloud-Speicher-API, REST, Excel"
description: "Überprüfen Sie die Vorhandenheit eines Speichercontainers in Aspose.Cells Cloud. Erfahren Sie mehr über den Endpunkt GET /v4.0/cells/storage/{storageName}/exist, die erforderlichen Parameter, das Antwortformat und erhalten Sie SDK-Beispiele in C#, Java, Python und weiteren Sprachen."
weight: 100
---

Die `storageExists`-API überprüft, ob ein angegebener Speicher im Aspose.Cells-Cloud-Dienst vorhanden ist. Diese Funktion ist entscheidend, um sicherzustellen, dass alle Vorgänge, die vom Speicher abhängen, fehlerfrei ausgeführt werden können.
**Zusammenfassung** – Mit dem `storageExists`-Endpunkt können Sie bestätigen, ob ein bestimmter Speichercontainer in Aspose.Cells Cloud verfügbar ist. Nutzen Sie dies vor dateibezogenen Vorgängen, um Laufzeitfehler zu vermeiden.

## Überprüfung der Speichervorhandenheit (storageExists)

### Web-API

```
GET https://api.aspose.cloud/v4.0/cells/storage/{storageName}/exist
```

### **Sicherheit und Authentifizierung**

Die Aspose.Cells Cloud-APIs sind sicher und erfordern eine <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-Token-basierte Authentifizierung</a>.

### Anforderungsparameter

| Parametername | Typ    | Ort    | Beschreibung                                           |
| ------------- | ------ | ------ | ------------------------------------------------------ |
| storageName   | String | Pfad   | Der Name des Speichers, dessen Vorhandensein geprüft werden soll. |

### **Antwort**

```json
{
  "Name": "StorageExist",
  "Description": ["Gibt an, ob der angegebene Speicher vorhanden ist."],
  "Type": "Class",
  "IsAbstract": false,
  "Properties": [
    {
      "Name": "Exists",
      "Description": [
        "Gibt an, ob der Speicher vorhanden ist.",
        "Diese Eigenschaft gibt true zurück, wenn der Speicher vorhanden ist; andernfalls wird false zurückgegeben."
      ],
      "Nullable": true,
      "ReadOnly": false,
      "IsInherit": false,
      "DataType": {
        "Identifier": "Boolean",
        "Name": "boolean"
      }
    }
  ]
}
```

**HTTP-Statuscodes**

| Code | Bedeutung             | Beschreibung                                                    |
| ---- | --------------------- | --------------------------------------------------------------- |
| 200  | OK                    | Filter erfolgreich angewendet; Antwort enthält Vorgangsdetails. |
| 400  | Ungültige Anforderung | Fehlende oder ungültige Parameter (z. B. nicht unterstützter Dateityp). |
| 401  | Nicht autorisiert     | Ungültiges oder fehlendes JWT-Token.                           |
| 413  | Anforderung zu groß   | Die hochgeladene Datei überschreitet die Größenbeschränkung.  |
| 500  | Interner Serverfehler | Unerwarteter Serverfehler.                                     |

## Wie verwendet man die Storage-Exists-API mit SDKs?

### OpenAPI-Spezifikation

Die <a href="https://reference.aspose.cloud/cells/#/StorageController/StorageExists" rel="nofollow noopener noreferrer">OpenAPI-Spezifikation</a> definiert eine öffentlich zugängliche Programmierschnittstelle, die es Entwicklern ermöglicht, direkt über einen Webbrowser nahtlos mit der REST-API zu interagieren.

Sie können das cURL-Befehlszeilentool nutzen, um Aspose.Cells-Webservices einfach aufzurufen. Das folgende Beispiel zeigt, wie Sie mit cURL Aufrufe an die Cloud-API durchführen.

{{< tabs tabTotal="2" tabID="11" tabName11="Anforderung" tabName12="Antwort" >}}

{{< tab tabNum="11" >}}

```bash
curl -X GET "https://api.aspose.cloud/v4.0/cells/storage/{storageName}/exist" \
     -H "Authorization: Bearer {access_token}"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Exists": true
}
```

{{< /tab >}}

{{< /tabs >}}

### Verwendung der Aspose.Cells Cloud SDKs

Die Verwendung eines SDKs ist der effizienteste Weg, um die Entwicklung zu beschleunigen. Ein SDK abstractiert die implementierungsspezifischen Details auf niedriger Ebene, sodass Entwickler sich auf ihre Projekt Aufgaben konzentrieren können. Eine vollständige Liste der verfügbaren Aspose.Cells Cloud SDKs finden Sie im <a href="https://github.com/aspose-cells-cloud" rel="nofollow noopener noreferrer">GitHub-Repository</a>.

Die folgenden Codebeispiele zeigen, wie Sie mit verschiedenen SDKs API-Aufrufe an Aspose.Cells-Webservices durchführen:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_StorageExists.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_StorageExists.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_StorageExists.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_StorageExists.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_StorageExists.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_StorageExists.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_StorageExists.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_StorageExists.go" >}}
{{</tab>}}
{{< /tabs >}}