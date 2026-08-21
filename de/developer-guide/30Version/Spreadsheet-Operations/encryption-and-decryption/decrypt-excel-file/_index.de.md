---
title: "Entschlüsseln einer Excel-Arbeitsmappe"
second_title: "Dokument"
linktitle: "Entschlüsseln einer Excel-Datei"
type: docs
url: /excel-file-decrypt/
aliases: [/decrypt-excel-workbooks/, /workbook/decrypt/]
keywords: "Aspose.Cells, Excel-Entschlüsselung, REST-API, Cloud-SDK"
description: "Erfahren Sie, wie Sie eine Excel-Arbeitsmappe mithilfe der Aspose.Cells Cloud REST-API entschlüsseln können. Enthält erforderliche Parameter, ein cURL-Beispiel, SDK-Codebeispiele und Details zur Fehlerbehandlung."
ArticleTitle: "So entschlüsseln Sie eine Excel-Arbeitsmappe mithilfe der Aspose.Cells Cloud-API"
weight: 50
---

**Voraussetzungen**

- Ein gültiges JWT-Zugriffstoken.
- Die Arbeitsmappe muss in den Aspose Cloud-Speicher hochgeladen sein, und ihr Pfad muss im Abfrageparameter `folder` angegeben werden.

## DeleteDecryptWorkbook API

```http
DELETE https://api.aspose.cloud/v3.0/cells/{name}/encryption
```

### **Sicherheit und Authentifizierung**

Die Aspose.Cells Cloud-APIs sind sicher und erfordern eine <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-Token-basierte Authentifizierung</a>.

### Abfrageparameter

| Parametername    | Typ    | Beschreibung                                           |
| ---------------- | ------ | ------------------------------------------------------ |
| folder           | string | Pfad des Ordners mit der ursprünglichen Arbeitsmappe.  |
| storageName      | string | Name des Speichers, in dem sich die Arbeitsmappe befindet. |

### Parameter des Anforderungstextes

| Parametername | Typ                      | Beschreibung                                  |
| ------------- | ------------------------ | --------------------------------------------- |
| encryption    | WorkbookEncryptionRequest | Verschlüsselungseinstellungen für die Entschlüsselung. |

### WorkbookEncryptionRequest

| Parametername   | Typ     | Beschreibung                                                                                                 |
| --------------- | ------- | ------------------------------------------------------------------------------------------------------------ |
| EncryptionType  | string  | Verschlüsselungsalgorithmus (`XOR`, `Compatible`, `EnhancedCryptographicProviderV1`, `StrongCryptographicProvider`). |
| KeyLength       | integer | Länge des Verschlüsselungsschlüssels in Bits.                                                                |
| Password        | string  | Passwort, das für die Entschlüsselung verwendet wird.                                                       |

### Antwort

```json
{
  "Status": "OK",
  "Code": 200
}
```

**Beispiel für Fehlerantworten**

```json
{
  "Code": "400",
  "Message": "Ungültige Anforderungsparameter."
}
```

```json
{
  "Code": "401",
  "Message": "Authentifizierung fehlgeschlagen. Ungültiges oder fehlendes JWT-Token."
}
```

```json
{
  "Code": "413",
  "Message": "Nutzlast zu groß. Die hochgeladene Datei überschreitet die zulässige Größe."
}
```

```json
{
  "Code": "500",
  "Message": "Interner Serverfehler. Bitte versuchen Sie es später erneut."
}
```

**HTTP-Statuscodes**

| Code | Bedeutung                    | Beschreibung                                             |
| ---- | ---------------------------- | -------------------------------------------------------- |
| 200  | OK                           | Filter erfolgreich angewendet; Antwort enthält Details zum Vorgang. |
| 400  | Bad Request                  | Fehlende oder ungültige Parameter (z. B. nicht unterstützter Dateityp). |
| 401  | Unauthorized                 | Ungültiges oder fehlendes JWT-Token.                     |
| 413  | Payload Too Large            | Die hochgeladene Datei überschreitet das Größenlimit.    |
| 500  | Internal Server Error        | Unerwarteter Serverfehler.                               |

## So verwenden Sie die DeleteDecryptWorkbook API mit SDKs

### DeleteDecryptWorkbook API-Spezifikation

Die [OpenAPI-Spezifikation](https://apireference.aspose.cloud/cells/#/Workbook/DeleteDecryptWorkbook) definiert eine öffentlich zugängliche Programmierschnittstelle und ermöglicht REST-Interaktionen direkt aus einem Webbrowser.

Sie können **cURL** verwenden, um problemlos auf die Aspose.Cells-Webdienste zuzugreifen. Das folgende Beispiel zeigt, wie die Cloud-API mit cURL aufgerufen wird.

{{< tabs tabTotal="2" tabID="1" tabName1="Anforderung" tabName2="Antwort" >}}

{{< tab tabNum="1" >}}

```bash
curl -X DELETE "https://api.aspose.cloud/v3.0/cells/test.xlsx/encryption" \
     -H "accept: application/json" \
     -H "Content-Type: application/json" \
     -H "Authorization: Bearer <access_token>" \
     -d '{ "EncryptionType": "XOR", "KeyLength": 1280, "Password": "aspose"}'
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Code": "200",
  "Status": "OK"
}
```

{{< /tab >}}

### Verwendung der Aspose.Cells Cloud SDKs

Die Verwendung eines SDKs ist der beste Weg, um die Entwicklung zu beschleunigen. Ein SDK übernimmt die Details auf unterster Ebene, sodass Sie sich auf Ihre Projektaufgaben konzentrieren können. Eine vollständige Liste der Aspose.Cells Cloud SDKs finden Sie im [GitHub-Repository](https://github.com/aspose-cells-cloud).

Die folgenden Codebeispiele zeigen, wie Aspose.Cells-Webdienste mithilfe verschiedener SDKs aufgerufen werden:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleDeleteDecryptWorkbook.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_DeleteDecryptWorkbook.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_DeleteDecryptWorkbook.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_DeleteDecryptWorkbook.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_DeleteDecryptWorkbook.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_DeleteDecryptWorkbook.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_DeleteDecryptWorkbook.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_DeleteDecryptWorkbook.go" >}}

{{< /tab >}}

{{< /tabs >}}