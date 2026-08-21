---
title: "Excel zu SQL"
second_title: "Dokument"
linktitle: "Excel zu SQL"
type: docs
url: /de/convert-excel-file-to-sql-file/
keywords: "Aspose.Cells, Excel zu SQL, Cloud-API, Tabellenkalkulationsumwandlung, REST"
description: "Verwenden Sie die Aspose.Cells Cloud REST-API, um Excel-Tabellenkalkulationsdateien in SQL-Dateien zu konvertieren. Unterstützt mehrere SDKs und Programmiersprachen für eine nahtlose Integration in Ihre Anwendungen."
weight: 100
ArticleTitle: "Excel zu SQL konvertieren – Aspose.Cells Cloud API"
---

Diese REST-API wandelt eine Tabellenkalkulationsdatei in ein SQL-Format um.

**Voraussetzungen**  
Um diesen Endpunkt nutzen zu können, benötigen Sie ein gültiges JWT-Token, das gemäß der Anleitung in der <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-Token-basierten Authentifizierung</a> erzeugt wurde. Die API unterstützt Excel-Dateien bis zu den in der Service-Dokumentation definierten Größenbeschränkungen und kann passwortgeschützte Arbeitsmappen verarbeiten, sofern der Abfrageparameter `password` übergeben wird.

## PostConvertWorkbookToSQL API

```http
POST https://api.aspose.cloud/v3.0/cells/convert/sql
```

### **Sicherheit und Authentifizierung**

Die Aspose.Cells Cloud APIs sind sicher und erfordern <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-Token-basierte Authentifizierung</a>.

### **Abfrageparameter**

| Parametername         | Typ    | Beschreibung                                                                             |
| --------------------- | ------ | --------------------------------------------------------------------------------------- |
| password              | string | Passwort zum Öffnen der Excel-Datei.                                                    |
| storageName           | string | Name des Speichers, in dem die Datei gespeichert ist.                                   |
| checkExcelRestriction | bool   | Gibt an, ob Excel-Dateibeschränkungen überprüft werden sollen, wenn zellbezogene Objekte geändert werden. |

### **Parameter im Anforderungstext**

| Parametername | Typ       | Beschreibung                                                                   |
| ------------- | --------- | ------------------------------------------------------------------------------ |
| datafile      | data file | Die zu konvertierende Tabellenkalkulationsdatei, als erster Teil der Anfrage. |

### Antwort

Die API gibt ein **FileInfo**-Objekt zurück, das die erzeugte SQL-Datei enthält.

| Feld            | Typ    | Beschreibung                                |
| --------------- | ------ | ------------------------------------------- |
| **Filename**    | string | Name der SQL-Datei (z. B. `example.sql`).  |
| **FileSize**    | int    | Größe der Datei in Bytes.                   |
| **FileContent** | string | Inhalt der SQL-Datei in Base64-Kodierung.   |

[FileInfo](/cells/file-info/)

**HTTP-Statuscodes**

| Code | Bedeutung                   | Beschreibung                                      |
|------|-----------------------------|--------------------------------------------------|
| 200  | OK                          | Filter erfolgreich angewendet; Antwort enthält Details zum Vorgang. |
| 400  | Bad Request                 | Fehlende oder ungültige Parameter (z. B. nicht unterstützter Dateityp). |
| 401  | Unauthorized                | Ungültiges oder fehlendes JWT-Token.            |
| 413  | Payload Too Large           | Die hochgeladene Datei überschreitet das Größenlimit. |
| 500  | Internal Server Error       | Unerwarteter Serverfehler.                      |

## Verwendung der PostConvertWorkbookToSQL API mit SDKs

### Spezifikation der PostConvertWorkbookToSQL API

Die <a href="https://reference.aspose.cloud/cells/#/Conversion/PostConvertWorkbookToSQL" rel="noopener noreferrer">OpenAPI-Spezifikation</a> definiert eine öffentlich zugängliche Programmierschnittstelle und ermöglicht REST-Interaktionen direkt aus einem Webbrowser.

Sie können das Kommandozeilentool **cURL** verwenden, um Aspose.Cells-Webservices einfach aufzurufen. Das folgende Beispiel zeigt, wie Aufrufe an die Cloud-API mit cURL erfolgen:

{{< tabs tabTotal="2" tabID="11" tabName11="Anforderung" tabName12="Antwort" >}}

{{< tab tabNum="11" >}}

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/convert/sql" \
     -H "accept: multipart/form-data" \
     -H "Content-Type: multipart/form-data" \
     -H "x-aspose-client: curl" \
     -d '{"File":{}}'
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Filename": "example.sql",
  "FileSize": 1024,
  "FileContent": "base64_encoded_string"
}
```

{{< /tab >}}

{{< /tabs >}}

### Verwendung der Aspose.Cells Cloud SDKs

Die Verwendung eines SDKs ist die beste Möglichkeit, die Entwicklung zu beschleunigen. Ein SDK übernimmt die Low-Level-Details, sodass Sie sich auf die Aufgaben Ihres Projekts konzentrieren können. Eine vollständige Liste der Aspose.Cells Cloud SDKs finden Sie im <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub-Repository</a>.

Die folgenden Codebeispiele zeigen, wie Aspose.Cells-Webservices mit verschiedenen SDKs aufgerufen werden:
{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example_PostConvertWorkbookToSQL.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostConvertWorkbookToSQL.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostConvertWorkbookToSQL.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostConvertWorkbookToSQL.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostConvertWorkbookToSQL.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostConvertWorkbookToSQL.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostConvertWorkbookToSQL.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostConvertWorkbookToSQL.go" >}}

{{< /tab >}}

{{< /tabs >}}

## Weitere APIs, die diese Funktion implementieren

- **[POST /cells/{name}/saveAs](https://apireference.aspose.cloud/cells/#/SaveAs/PostDocumentSaveAs)** – Speichert eine Arbeitsmappe in einem anderen Format und speichert das Ergebnis im angegebenen Speicher.

- **[PUT /cells/convert](https://apireference.aspose.cloud/cells/#/Workbook/PutConvertWorkBook)** – Wandelt eine Arbeitsmappe in ein anderes Format mit optionalen Einstellungen um und gibt das Ergebnis in der Antwort zurück.

- **[GET /cells/{name}](https://apireference.aspose.cloud/cells/#/Workbook/GetWorkBook)** – Ruft eine Arbeitsmappe mit optionalen Umwandlungseinstellungen ab.

**Hinweise**  
- Bei der Umwandlung passwortgeschützter Excel-Dateien stellen Sie sicher, dass der Abfrageparameter `password` übergeben wird; andernfalls schlägt die Umwandlung mit einem 400-Fehler fehl.  
- Der Dienst gibt den SQL-Dateiinhalt als Base64-kodierten String zurück; dekodieren Sie ihn vor dem Speichern in einer `.sql`-Datei.  

**Beispieldateien**  
Laden Sie eine Beispiel-Excel-Arbeitsmappe [hier](https://example.com/sample.xlsx) und ein vorgeneriertes SQL-Ergebnis [hier](https://example.com/sample.sql) herunter, um die API schnell zu testen.