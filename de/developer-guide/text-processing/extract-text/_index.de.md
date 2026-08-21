---
title: "Aspose.Cells Cloud Web API – Text extrahieren"
second_title: "Aspose.Cells Cloud – Online Short‑Code"
linktitle: "Text extrahieren"
type: docs
url: /de/extract-text/
keywords: "Aspose.Cells Cloud, Text extrahieren, Excel API, Zelltextextraktion, REST API"
description: "Extrahieren Sie Teilzeichenfolgen, Zahlen oder Zeichen aus Excel-Zellen mithilfe der Aspose.Cells Cloud API. Unterstützt Text extrahieren vor/nach einem Muster, positionsbasierte Extraktion und direkte Ausgabe in einen neuen Bereich."
weight: 100
ArticleTitle: "Aspose.Cells Cloud Extract Text API-Dokumentation"
---

Extrahiert Teilzeichenfolgen, Zeichen oder Zahlen aus einer Zelle einer Tabellendatei in eine andere Zelle und eliminiert so die Notwendigkeit komplexer FINDEN-, MIN-, LINKS- oder RECHTS-Formeln.

## **ExtractText API**

```http
PUT https://api.aspose.cloud/v4.0/cells/content/extract/text
```

### **Sicherheit und Authentifizierung**

Die Aspose.Cells Cloud APIs sind sicher und erfordern eine <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-Token-basierte Authentifizierung</a>.

```bash
-H "Authorization: Bearer {access_token}"
```

### Die Anforderungsparameter der **extractText** API sind

| Parametername    | Typ     | Position           | Beschreibung                                                                                                                     |
| ---------------- | ------- | ------------------ | ------------------------------------------------------------------------------------------------------------------------------- |
| Spreadsheet      | Datei   | FormData           | Hochladen der Tabellendatei.                                                                                                    |
| extractTextType  | String  | Query              | Enum, der den Extraktionsmodus angibt. Zulässige Werte: `Before`, `After`, `BeforePosition`, `AfterPosition`.                 |
| beforeText       | String  | Query              | Text, der **vor** der zu extrahierenden Teilzeichenfolge stehen muss. Wird verwendet, wenn `extractTextType=Before`.           |
| afterText        | String  | Query              | Text, der **nach** der zu extrahierenden Teilzeichenfolge stehen muss. Wird verwendet, wenn `extractTextType=After`.            |
| beforePosition   | Integer | Query              | Anzahl der Zeichen, die von der linken Seite der Zelle zurückgegeben werden sollen. Wird verwendet, wenn `extractTextType=BeforePosition`. |
| afterPosition    | Integer | Query              | Anzahl der Zeichen, die von der rechten Seite der Zelle zurückgegeben werden sollen. Wird verwendet, wenn `extractTextType=AfterPosition`. |
| outPositionRange | String  | Query              | Der Zielbereich (z. B. `Tabelle1!A1`), in den der extrahierte Text geschrieben wird.                                            |
| worksheet        | String  | Query              | Name des Arbeitsblatts, das die Quellzelle enthält.                                                                            |
| range            | String  | Query              | Die Quellzelle oder der Quellbereich (z. B. `A1`).                                                                              |
| outPath          | String  | Query _(Optional)_ | Ordnerpfad im Speicher, in dem die resultierende Arbeitsmappe gespeichert wird. Falls weggelassen, wird das Ergebnis im Antworttext zurückgegeben. |
| outStorageName   | String  | Query              | Name des für die Ausgabedatei zu verwendenden Speichers.                                                                        |
| region           | String  | Query              | Regionseinstellung der Tabellendatei (z. B. `US`, `EU`).                                                                        |
| password         | String  | Query              | Passwort zum Öffnen einer geschützten Arbeitsmappe.                                                                             |

**Beispiel-cURL-Anforderung**

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/content/extract/text?extractTextType=Before&beforeText=Total&outPositionRange=Sheet1!B1&worksheet=Sheet1&range=A1" \
     -H "Authorization: Bearer {access_token}" \
     -F "Spreadsheet=@Sample.xlsx"
```

### **Antwort**

Wenn die Anforderung erfolgreich ist, gibt die API eine JSON-Payload zurück, die den extrahierten Text und die Adresse der Zelle enthält, in die er geschrieben wurde:

```json
[
  {
    "Name": "ResponseFile",
    "DataType": {
      "Identifier": "File",
      "Reference": "Stream"
    }
  }
]
```

Falls der Parameter `outPath` angegeben wurde, enthält die Antwort nur eine Statusnachricht; die Arbeitsmappe wird an die angegebene Stelle geschrieben.

**Beispiel-Antwort, wenn `outPath` weggelassen wurde**

```json
{
  "Code": 200,
  "Status":"OK"
}
```

### Fehlercodes

- **200 OK** – Extraktion erfolgreich abgeschlossen.  
- **202 Accepted** – Anforderung zur asynchronen Verarbeitung akzeptiert.  
- **400 Bad Request** – Ungültige Aspose.Cells Cloud API-URI oder fehlende erforderliche Parameter.  
- **401 Unauthorized** – Ungültiges Zugriffstoken, Client-ID oder Client-Geheimnis.  
- **404 Not Found** – Die angegebene Tabellendatei ist nicht zugänglich.  
- **500 Server Error** – Beim Verarbeiten der Arbeitsmappe ist ein unerwarteter Fehler aufgetreten.

## OpenAPI-Spezifikation

Die [OpenAPI-Spezifikation](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/TextProcessing/ExtractText) definiert eine öffentlich zugängliche Programmierschnittstelle und ermöglicht es Ihnen, REST-Interaktionen direkt aus einem Webbrowser heraus durchzuführen.

### Verwendung der Aspose.Cells Cloud SDKs

Die Verwendung eines SDKs ist der beste Weg, die Entwicklung zu beschleunigen. Das SDK übernimmt die zugrunde liegenden Details, sodass Sie die Funktion **Text extrahieren** für Zellen mit minimalem Codeaufwand implementieren können. Eine vollständige Liste der Aspose.Cells Cloud SDKs finden Sie im [GitHub-Repository](https://github.com/aspose-cells-cloud).

Die folgenden Codebeispiele zeigen, wie Aufrufe an Aspose.Cells-Webservices mithilfe verschiedener SDKs durchgeführt werden:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{<tab tabNum="1" >}}

```csharp
// C#-Beispiel – Text extrahieren (Code zur Kürze ausgelassen)
```

{{</tab>}}

{{<tab tabNum="2" >}}

```java
// Java-Beispiel – Text extrahieren (Code zur Kürze ausgelassen)
```

{{</tab>}}

{{<tab tabNum="3" >}}

```php
// PHP-Beispiel – Text extrahieren (Code zur Kürze ausgelassen)
```

{{</tab>}}

{{<tab tabNum="4" >}}

```ruby
# Ruby-Beispiel – Text extrahieren (Code zur Kürze ausgelassen)
```

{{</tab>}}

{{<tab tabNum="5" >}}

```javascript
// Node.js-Beispiel – Text extrahieren (Code zur Kürze ausgelassen)
```

{{</tab>}}

{{<tab tabNum="6" >}}

```python
# Python-Beispiel – Text extrahieren (Code zur Kürze ausgelassen)
```

{{</tab>}}

{{<tab tabNum="7" >}}

```perl
# Perl-Beispiel – Text extrahieren (Code zur Kürze ausgelassen)
```

{{</tab>}}

{{<tab tabNum="8" >}}

```go
// Go-Beispiel – Text extrahieren (Code zur Kürze ausgelassen)
```

{{</tab>}}

{{< /tabs >}}