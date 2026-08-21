---
title: "Hinzufügen einer digitalen Signatur zu einer Excel-Arbeitsmappe"
ArticleTitle: "Hinzufügen einer digitalen Signatur zu einer Excel-Arbeitsmappe – Aspose.Cells Cloud API"
second_title: "Dokument"
linktype: "docs"
url: /excel-digital-signature/
aliases:
  - /protect/digital-signature/
  - /workbook/digital-signature/
keywords: "Aspose.Cells Cloud, digitale Signatur, Excel-Arbeitsmappe, REST-API, .pfx, JWT, Signatur-API"
description: "Erfahren Sie, wie Sie einer Excel-Arbeitsmappe mithilfe der Aspose.Cells Cloud REST-API (v4.0) eine digitale Signatur hinzufügen. Enthält Endpunkt, Parameter, Authentifizierung, Antwort-Schema, Fehlerbehandlung und SDK-Beispiele für mehrere Sprachen."
weight: 35
---


**Voraussetzungen:**  
Bevor Sie diesen Endpunkt aufrufen, stellen Sie sicher, dass Folgendes vorliegt:

- Ein gültiges JWT-Zugriffstoken, das über die Aspose Cloud-Authentifizierung erhalten wurde.  
- Die Ziel-Arbeitsmappe ist in Ihrem Aspose Cloud-Speicher hochgeladen.  
- Eine digitale Signaturdatei im Format `.pfx` oder `.p12` sowie deren Passwort.

Diese REST-API fügt einer Excel-Arbeitsmappe eine **digitale Signatur** hinzu.

## PostDigitalSignature API

```http
POST https://api.aspose.cloud/v4.0/cells/{name}/digitalsignature
```

### **Sicherheit und Authentifizierung**

Die Aspose.Cells Cloud-APIs sind sicher und erfordern eine <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-Token-basierte Authentifizierung</a>.

### Anforderungsparameter

| Parametername            | Typ    | Position              | Beschreibung                                               |
| ------------------------ | ------ | --------------------- | ---------------------------------------------------------- |
| **name**                 | string | `<code>path</code>`   | Der Name der Arbeitsmappe.                                 |
| **digitalsignaturefile** | string | `<code>query</code>`  | Pfad zur digitalen Signaturdatei (`.pfx` oder `.p12`).     |
| **password**             | string | `<code>query</code>`  | Passwort für die Arbeitsmappe, sofern geschützt.           |
| **folder**               | string | `<code>query</code>`  | Ordner, in dem die Arbeitsmappe gespeichert ist.           |
| **storageName**          | string | `<code>query</code>`  | Name des zu verwendenden Speicherdienstes.                 |

*Hinweis: Falls der Dateiname Sonderzeichen enthält, müssen Sie ihn vor dem Hinzufügen zur Abfragezeichenfolge URL-kodieren.*

### Fehlerbehandlung

| HTTP-Status | Bedeutung                                                  |
| ----------- | ---------------------------------------------------------- |
| 200         | Signatur erfolgreich angewendet.                           |
| 400         | Ungültige Anforderung – fehlende oder ungültige Parameter. |
| 401         | Nicht autorisiert – ungültiges oder abgelaufenes OAuth-Token. |
| 403         | Verboten – unzureichende Berechtigungen oder Zugriff verweigert. |
| 500         | Interner Serverfehler – unerwarteter Fehler.              |

### HTTP-Status-Fehlerantworten

| HTTP-Status | Code                | Beschreibung                                                    |
| ----------- | ------------------- | --------------------------------------------------------------- |
| 400         | BadRequest          | Fehlende oder ungültige Parameter.                              |
| 401         | Unauthorized        | Ungültiges oder fehlendes Zugriffstoken.                        |
| 404         | NotFound            | Angegebene Arbeitsmappe im angegebenen Ordner/Speicher nicht gefunden. |
| 500         | InternalServerError | Unerwarteter Serverfehler.                                      |


## Verwendung der PostDigitalSignature API mit SDKs

### PostDigitalSignature API-Spezifikation

Die [OpenAPI-Spezifikation](https://apireference.aspose.cloud/cells/#/Protection/PostDigitalSignature) definiert eine öffentlich zugängliche Programmierschnittstelle und ermöglicht REST-Interaktionen direkt über einen Webbrowser.

Sie können das cURL-Befehlszeilentool verwenden, um Aspose.Cells-Webdienste aufzurufen. Das folgende Beispiel zeigt eine Anfrage an die API:

{{< tabs tabTotal="2" tabID="11" tabName11="Anforderung" tabName12="Antwort" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v4.0/cells/{name}/digitalsignature?digitalsignaturefile=signature.pfx&password=IhrPasswort" \
  -X POST \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

**Antwort-Schema**  
Die API gibt ein JSON-Objekt mit den folgenden Feldern zurück:

| Feld          | Typ    | Beschreibung                                             |
| ------------- | ------ | -------------------------------------------------------- |
| `Code`        | int    | HTTP-ähnlicher Statuscode, der das Ergebnis angibt.     |
| `Status`      | string | Kurzer Text zur Beschreibung des Ergebnisses (z. B. `OK`). |
| `SignatureId` | string | Bezeichner der angewendeten digitalen Signatur (optional). |
| `Message`     | string | Zusätzliche Informationen oder Fehlerdetails (optional). |

### Verwendung der Aspose.Cells Cloud SDKs

Die Verwendung eines SDK vereinfacht die Integration und reduziert den Boilerplate-Code. Besuchen Sie das [GitHub-Repository](https://github.com/aspose-cells-cloud), um eine vollständige Liste der Aspose.Cells Cloud SDKs zu erhalten.

Die folgenden Codebeispiele zeigen, wie Aspose.Cells-Webdienste mithilfe verschiedener SDKs aufgerufen werden:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostDigitalSignature.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostDigitalSignature.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostDigitalSignature.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostDigitalSignature.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82a2de2e4189bc27ae92abf73c36b4df0" "Example_PostDigitalSignature.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostDigitalSignature.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostDigitalSignature.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostDigitalSignature.go" >}}

{{< /tab >}}

{{< /tabs >}}