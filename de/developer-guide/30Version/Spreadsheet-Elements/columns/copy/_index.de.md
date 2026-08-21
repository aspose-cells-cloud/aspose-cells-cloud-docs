---
title: "Spalten in einem Excel-Arbeitsblatt kopieren"
second_title: "Dokument"
linktitle: "Kopieren"
type: docs
url: /de/columns/copy/
aliases:
  [/de/copy-columns-in-excel-worksheet/, /de/copy-columns-in-an-excel-worksheet/]
keywords: "Aspose.Cells, Spalten kopieren, Excel-API, REST, Cloud SDK, cURL, C#, Java, Python, Ruby, Node.js, Go, Perl"
description: "Erfahren Sie, wie Sie eine oder mehrere Spalten in einem Excel-Arbeitsblatt mithilfe der Aspose.Cells Cloud REST API (v3.0) kopieren. Enthält die Anforderungssyntax, erforderliche Parameter, Authentifizierungsdetails, Fehlerbehandlung und SDK-Beispiele in C#, Java, Python, Ruby, Node.js, Go, Perl und weiteren."
articleTitle: "Spalten in einem Excel-Arbeitsblatt mithilfe der Aspose.Cells Cloud API kopieren"
weight: 30
---

Diese REST API kopiert **Spalten** in einem Excel-Arbeitsblatt. Die **Spalten kopieren**-Operation ermöglicht es Ihnen, eine einzelne Spalte oder einen Bereich von Spalten zu duplizieren und die Kopie an einer angegebenen Position innerhalb desselben Arbeitsblatts einzufügen. Verwenden Sie diesen Endpunkt, um Spalten effizient bei der Arbeit mit großen Tabellenkalkulationen zu kopieren. Weitere Informationen zu verwandten Vorgängen finden Sie unter [Spalte hinzufügen](/de/columns/add/) und [Spalte ausblenden](/de/columns/hide/).

## Sicherheit und Authentifizierung  
Die Aspose.Cells Cloud APIs sind sicher und erfordern eine [JWT-Token-basierte Authentifizierung](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/).

## REST API

```bash
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/columns/copy
```

### Anforderungsparameter

| Parametername              | Typ     | Ort    | Beschreibung                                                                                      |
| -------------------------- | ------- | ------ | ------------------------------------------------------------------------------------------------- |
| **name**                   | string  | path   | Der Name der Arbeitsmappe.                                                                        |
| **sheetName**              | string  | path   | Der Name des Arbeitsblatts.                                                                       |
| **sourceColumnIndex**      | integer | query  | 0-basierter Index der zu kopierenden Spalte.                                                      |
| **destinationColumnIndex** | integer | query  | 0-basierter Index, an dem die kopierte(n) Spalte(n) eingefügt werden sollen.                     |
| **columnNumber**           | integer | query  | Anzahl der aufeinanderfolgenden zu kopierenden Spalten.                                           |
| **worksheet**              | string  | query  | _Optional_: Arbeitsblattbezeichner, der verwendet wird, wenn der Name des Arbeitsblatts vom Pfad abweicht. |
| **folder**                 | string  | query  | Pfad zum Ordner, der die Arbeitsmappe im Aspose Cloud-Speicher enthält.                           |

Die [OpenAPI-Spezifikation](https://apireference.aspose.cloud/cells/#/Cells/PostCopyWorksheetColumns) definiert den vollständigen Vertrag für diesen Vorgang.

### cURL-Beispiel

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/cells/columns/copy?sourceColumnIndex=1&destinationColumnIndex=12&columnNumber=10" \
     -H "Authorization: Bearer $ASPOSE_TOKEN" \
     -H "accept: application/json"
```

### Antwort

```json
{
  "Code": 200,
  "Status": "OK"
}
```

## Fehlerbehandlung

Die API gibt Standard-HTTP-Statuscodes mit einer JSON-Nutzdatenstruktur zurück, die die Fehlerbeschreibung enthält.

| Statuscode | Bedeutung                                        | Beispiel-JSON-Body                                                  |
| ---------- | ------------------------------------------------ | ------------------------------------------------------------------- |
| **400**    | Ungültige Anforderung – ungültige Parameter     | `{ "Code": 400, "Message": "Ungültiger Spaltenindex." }`            |
| **401**    | Nicht autorisiert – fehlendes oder ungültiges Token | `{ "Code": 401, "Message": "Zugriffstoken ist ungültig oder abgelaufen." }` |
| **404**    | Nicht gefunden – Arbeitsmappe oder Arbeitsblatt existiert nicht | `{ "Code": 404, "Message": "Arbeitsmappe nicht gefunden." }` |
| **500**    | Interner Serverfehler – unerwarteter Zustand    | `{ "Code": 500, "Message": "Ein unerwarteter Fehler ist aufgetreten." }` |

> **Wie Sie Fehler beheben:** Stellen Sie sicher, dass der Zugriffstoken aktuell ist, die Namen von Arbeitsmappe und Arbeitsblatt korrekt sind und `sourceColumnIndex`, `destinationColumnIndex` sowie `columnNumber` innerhalb des Spaltenbereichs des Arbeitsblatts liegen.

## Cloud SDK-Familie

Die Verwendung eines SDKs ist die beste Möglichkeit, die Entwicklung zu beschleunigen. Ein SDK übernimmt die Low-Level-Details, sodass Sie sich auf die Aufgaben Ihres Projekts konzentrieren können. Besuchen Sie das [GitHub-Repository](https://github.com/aspose-cells-cloud), um eine vollständige Liste der Aspose.Cells Cloud SDKs anzuzeigen.

Die folgenden Codebeispiele zeigen, wie Aufrufe an Aspose.Cells-Webservices mithilfe verschiedener SDKs durchgeführt werden:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostCopyWorksheetColumns.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostCopyWorksheetColumns.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostCopyWorksheetColumns.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostCopyWorksheetColumns.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostCopyWorksheetColumns.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostCopyWorksheetColumns.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostCopyWorksheetColumns.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostCopyWorksheetColumns.go" >}}

{{< /tab >}}

{{< /tabs >}}

<script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@type": "FAQPage",
  "mainEntity": [
    {
      "@type": "Question",
      "name": "Wie erfolgt die Authentifizierung beim Aufruf der „Spalten kopieren“-API?",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "Holen Sie sich einen OAuth2-Zugriffstoken von Aspose Cloud mithilfe Ihrer Client-ID und Ihres Geheimnisses und fügen Sie ihn in den Anforderungsheader als `Authorization: Bearer <access_token>` ein."
      }
    },
    {
      "@type": "Question",
      "name": "Was ist der Unterschied zwischen `sourceColumnIndex` und `destinationColumnIndex`?",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "`sourceColumnIndex` ist der 0-basierte Index der Spalte, die Sie kopieren möchten. `destinationColumnIndex` ist der 0-basierte Index, an dem die kopierte(n) Spalte(n) eingefügt werden sollen."
      }
    },
    {
      "@type": "Question",
      "name": "Welche Antwort erhalte ich, wenn der Kopiervorgang fehlschlägt?",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "Die API gibt einen Statuscode ungleich 200 zurück (z. B. 400 für eine ungültige Anforderung, 401 für nicht autorisiert). Der Antworttext enthält ein JSON-Objekt mit den Feldern `Code` und `Message`, das die Fehlerbeschreibung enthält."
      }
    }
  ]
}
</script>
---