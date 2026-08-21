---
title: "Excel-Arbeitsmappe entsperren – Aspose.Cells Cloud API"
second_title: "Dokument"
linktitle: "Excel-Datei entsperren"
type: docs
url: /excel-file-unprotect/
aliases:
  - /unprotect-excel-workbooks/
  - /workbook/unprotect/
keywords: "Aspose Cells, Excel-Entsperr-API, Arbeitsmapppenschutz entfernen, REST-API, Cloud-Tabellenkalkulation"
description: "Erfahren Sie, wie Sie den Schutz einer Excel-Arbeitsmappe mithilfe der Aspose.Cells Cloud REST API entfernen. Enthält Anforderungssyntax, Parameter, cURL-Beispiel und SDK-Code in mehreren Sprachen."
weight: 60
ArticleTitle: "Excel-Arbeitsmappe entsperren – Aspose.Cells Cloud API"
---

Verwenden Sie diese REST API, um den Schutz einer Excel-Arbeitsmappe zu entfernen.

## DeleteUnProtectWorkbook API

```http
DELETE https://api.aspose.cloud/v3.0/cells/{name}/protection
```

### **Sicherheit und Authentifizierung**

Die Aspose.Cells Cloud APIs sind sicher und erfordern eine <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-Token-basierte Authentifizierung</a>.

### Pfadparameter

| Parameter | Typ    | Beschreibung                                               | Erforderlich |
| --------- | ------ | ---------------------------------------------------------- | ------------ |
| **name**  | string | Name der Arbeitsmappe (einschließlich Dateierweiterung). | Ja           |

### Abfrageparameter

| Parametername | Typ    | Beschreibung                                           |
| ------------- | ------ | ------------------------------------------------------ |
| folder        | string | Pfad zum Ordner, der die ursprüngliche Arbeitsmappe enthält. |
| storageName   | string | Name des Speicherdienstes, in dem sich die Arbeitsmappe befindet. |

### Anforderungstextparameter

| Parametername | Typ                     | Beschreibung                                          |
| ------------- | ----------------------- | ----------------------------------------------------- |
| protection    | WorkbookProtectionRequest | Objekt, das die zu entfernenden Schutzeinstellungen angibt. |

#### WorkbookProtectionRequest

| Parametername   | Typ    | Beschreibung                                                                                                    |
| --------------- | ------ | --------------------------------------------------------------------------------------------------------------- |
| ProtectionType  | string | Typ des zu entfernenden Schutzes (`ALL`, `CONTENTS`, `NONE`, `OBJECTS`, `SCENARIOS`, `STRUCTURE`, `WINDOWS`). |
| Password        | string | Passwort zum Entfernen des Schutzes (optional).                                                                |

#### cURL-Beispiel

```bash
curl -X DELETE "https://api.aspose.cloud/v3.0/cells/test.xlsx/protection?folder=MyFolder&storageName=MyStorage" \
     -H "Authorization: Bearer <access_token>" \
     -H "accept: application/json" \
     -H "Content-Type: application/json" \
     -d '{ "ProtectionType": "ALL", "Password": "aspose"}'
```

#### Antwort (Erfolg)

```json
{
  "Code": 200,
  "Status": "OK"
}
```

### HTTPS-Statusfehlerantworten

| HTTP-Status | Code                | Beschreibung                                              |
| ----------- | ------------------- | --------------------------------------------------------- |
| 400         | BadRequest          | Fehlende oder ungültige Parameter.                        |
| 401         | Unauthorized        | Ungültiges oder fehlendes Zugriffstoken.                  |
| 404         | NotFound            | Angegebene Arbeitsmappe im angegebenen Ordner/Speicher nicht gefunden. |
| 500         | InternalServerError | Unerwarteter Serverfehler.                                |

## Verwenden der DeleteUnProtectWorkbook API mit SDKs

### DeleteUnProtectWorkbook API-Spezifikation

Die [OpenAPI-Spezifikation](https://apireference.aspose.cloud/cells/#/Protection/DeleteUnProtectWorkbook) definiert eine öffentlich zugängliche Programmierschnittstelle und ermöglicht REST-Interaktionen direkt aus einem Webbrowser.

Sie können das cURL-Befehlszeilentool verwenden, um Aspose.Cells-Webservices einfach aufzurufen. Das folgende Beispiel zeigt, wie mit cURL Aufrufe an die Cloud-API durchgeführt werden.

### Verwenden der Aspose.Cells Cloud SDKs

Die Verwendung eines SDK vereinfacht die Integration und reduziert den Boilerplate-Code. Besuchen Sie das [GitHub-Repository](https://github.com/aspose-cells-cloud), um eine vollständige Liste der Aspose.Cells Cloud SDKs zu erhalten.

Die folgenden Codebeispiele zeigen, wie Aspose.Cells-Webservices mithilfe verschiedener SDKs aufgerufen werden:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleDeleteUnProtectWorkbook.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_DeleteUnProtectWorkbook.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_DeleteUnProtectWorkbook.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_DeleteUnProtectWorkbook.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_DeleteUnProtectWorkbook.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_DeleteUnProtectWorkbook.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_DeleteUnProtectWorkbook.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_DeleteUnProtectWorkbook.go" >}}

{{< /tab >}}

{{< /tabs >}}