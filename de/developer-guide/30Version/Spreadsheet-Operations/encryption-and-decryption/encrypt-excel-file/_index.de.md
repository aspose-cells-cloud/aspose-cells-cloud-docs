---
title: "Verschlüsseln einer Excel-Arbeitsmappe mit der Aspose.Cells Cloud API – Schnelle cURL- und SDK-Beispiele"
second_title: "Dokument"
linktitle: "Excel-Datei verschlüsseln"
type: docs
url: /de/excel-file-encrypt/
aliases: [  /de/encrypt-excel-workbooks/ , /de/workbook/encrypt/ ]
keywords: "Aspose Cells Arbeitsmappe verschlüsseln, Excel-Verschlüsselungs-API, REST API, cURL, .NET, Java, Python, PHP, Ruby, Node.js, Go, Perl"
description: "Erfahren Sie, wie Sie eine Excel-Arbeitsmappe mit der Aspose.Cells Cloud REST API (v3.0) verschlüsseln. Enthält cURL-Befehl, SDK-Codebeispiele (C#, Java, Python, …), erforderliche Parameter und Fehlerbehandlung."
weight: 20
ArticleTitle: "Excel-Arbeitsmappe mit Aspose.Cells Cloud API verschlüsseln – cURL- und SDK-Beispiele"
---

Diese REST API verschlüsselt eine Excel-**Arbeitsmappe**.

**Voraussetzungen:** Sie müssen über ein gültiges JWT-Token verfügen und die Arbeitsmappe zuvor in einem Speicherort hochgeladen haben, bevor Sie diesen Endpunkt aufrufen.

## PostEncryptDocument API

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/encryption
```

### **Sicherheit und Authentifizierung**

Die Aspose.Cells Cloud APIs sind sicher und erfordern eine <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-Token-basierte Authentifizierung</a>.

### **Abfrageparameter**

| Parametername     | Typ    | Erforderlich | Beschreibung                                      |
| ----------------- | ------ | ------------ | ------------------------------------------------- |
| folder            | string | ✗            | Pfad des Ordners mit der ursprünglichen Arbeitsmappe. |
| storageName       | string | ✗            | Name des zu verwendenden Speichers.              |

### **Parameter im Anforderungstext**

| Parametername | Typ                         | Erforderlich | Beschreibung                               |
| ------------- | --------------------------- | ------------ | ------------------------------------------ |
| encryption    | WorkbookEncryptionRequest   | ✓            | Verschlüsselungseinstellungen für die Arbeitsmappe. |

#### **WorkbookEncryptionRequest**

| Parametername   | Typ     | Erforderlich | Beschreibung                                                                                      |
| --------------- | ------- | ------------ | ------------------------------------------------------------------------------------------------- |
| EncryptionType  | string  | ✓            | Verschlüsselungsalgorithmus. Siehe die nachfolgende Tabelle für unterstützte Werte und deren Bedeutung. |
| KeyLength       | integer | ✗            | Länge des Verschlüsselungsschlüssels in Bit (wird für `XOR` und `Compatible` ignoriert).         |
| Password        | string  | ✓            | Passwort, das für die Verschlüsselung verwendet wird.                                            |

#### **Werte für EncryptionType**

| Wert                              | Beschreibung                                           |
| --------------------------------- | ------------------------------------------------------ |
| `XOR`                             | Einfacher XOR-Algorithmus (veraltet, niedrige Sicherheit). |
| `Compatible`                      | Excel 97‑2003-kompatible Verschlüsselung (40‑Bit).    |
| `EnhancedCryptographicProviderV1` | AES‑128 mit SHA‑1-Hash.                               |
| `StrongCryptographicProvider`     | AES‑256 mit SHA‑512-Hash (stärkste Verschlüsselung).  |

### Antwort

```json
{
  "Status":"OK",
  "Code":200
}
```

**HTTP-Statuscodes**

| Code | Bedeutung                 | Beschreibung                                                                 |
|------|---------------------------|------------------------------------------------------------------------------|
| 200  | OK                        | Filter erfolgreich angewendet; Antwort enthält Details zum Vorgang.         |
| 400  | Bad Request               | Fehlende oder ungültige Parameter (z. B. nicht unterstützter Dateityp).     |
| 401  | Unauthorized              | Ungültiges oder fehlendes JWT-Token.                                        |
| 413  | Payload Too Large         | Die hochgeladene Datei überschreitet das Größenlimit.                       |
| 500  | Internal Server Error     | Unerwarteter Serverfehler.                                                  |

## Verwenden der PostEncryptDocument API mit SDKs

### PostEncryptDocument API-Spezifikation

Die <a href="https://apireference.aspose.cloud/cells/#/Workbook/PostEncryptDocument" rel="noopener noreferrer">OpenAPI-Spezifikation</a> definiert eine öffentlich zugängliche Programmierschnittstelle und ermöglicht REST-Interaktionen direkt aus einem Webbrowser.

Sie können das **cURL**-Befehlszeilentool verwenden, um problemlos auf die Aspose.Cells-Webdienste zuzugreifen. Im folgenden Beispiel wird gezeigt, wie ein Aufruf der Cloud-API mit cURL erfolgt.

{{< tabs tabTotal="2" tabID="1" tabName1="Anforderung" tabName2="Antwort" >}}

{{< tab tabNum="1" >}}

```bash
# Verschlüsseln der Arbeitsmappe "test.xlsx" mit dem XOR-Algorithmus (128‑Bit-Schlüssel) und dem Passwort "mateen".
curl -X POST "https://api.aspose.cloud/v3.0/cells/test.xlsx/encryption" \
     -H "accept: application/json" \
     -H "Content-Type: application/json" \
     -H "Authorization: Bearer <access_token>" \
     -d '{ "EncryptionType": "XOR", "KeyLength": 128, "Password": "mateen"}'
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Code": "200",
  "Status": "OK"
}
```

**Mögliche Fehlerantworten**

| HTTP-Status | Code                | Nachricht                                           |
| ----------- | ------------------- | --------------------------------------------------- |
| 400         | BadRequest          | Fehlende oder ungültige Parameter.                 |
| 401         | Unauthorized        | Authentifizierungstoken fehlt oder ist ungültig.   |
| 403         | Forbidden           | Unzureichende Berechtigungen für den Zugriff auf den Speicher. |
| 500         | InternalServerError | Unerwarteter Serverfehler.                         |

{{< /tab >}}

{{< /tabs >}}

### Verwenden der Aspose.Cells Cloud SDKs

Die Verwendung eines SDKs ist der beste Weg, die Entwicklungszeit zu verkürzen. Ein SDK übernimmt die Low-Level-Details, sodass Sie sich auf die Aufgaben Ihres Projekts konzentrieren können. Ein vollständiges Listing der Aspose.Cells Cloud SDKs finden Sie im <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub-Repository</a>.

Die folgenden Codebeispiele zeigen, wie Aspose.Cells-Webdienste mit verschiedenen SDKs aufgerufen werden:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostEncryptWorkbook.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostEncryptWorkbook.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostEncryptWorkbook.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostEncryptWorkbook.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostEncryptWorkbook.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostEncryptWorkbook.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostEncryptWorkbook.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostEncryptWorkbook.go" >}}

{{< /tab >}}

{{< /tabs >}}