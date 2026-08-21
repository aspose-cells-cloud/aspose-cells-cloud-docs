---
title: "Top 10-Filter in einem Excel-Arbeitsblatt anwenden (Aspose.Cells Cloud)"
ArticleTitle: "Top 10-Filter in einem Excel-Arbeitsblatt anwenden – Aspose.Cells Cloud"
second_title: "Dokument"
linktype: "docs"
url: /autofilter/add-top-10-filter/
aliases:
  [/filter-the-top-10-items-in-the-list/, /autofilter/add-a-top-10-filter/]
keywords: "Aspose.Cells, AutoFilter, Top 10-Filter, Excel-API"
description: "Erfahren Sie, wie Sie einen Top 10-AutoFilter in einem Excel-Arbeitsblatt mithilfe der Aspose.Cells Cloud REST-API anwenden. Enthält Endpunkt, Parameter, ein HTTPS-cURL-Beispiel, Authentifizierungsdetails, Fehlerbehandlung und SDK-Ausschnitte für C#, Java, Python und weitere."
weight: 65
---

Diese REST-API filtert die **Top 10**-Elemente in einer Liste.

> **Voraussetzungen**  
> • Holen Sie sich ein gültiges JWT-Token über die Aspose.Cells Cloud-Authentifizierung.  
> • Laden Sie die Excel-Arbeitsmappe in Ihren Aspose Cloud-Speicher hoch (oder geben Sie den Speicher/Ordner an, in dem sich die Datei befindet).  
> • Kennen Sie den Namen des Arbeitsblatts sowie den Zellbereich, den Sie filtern möchten.

## PutWorksheetFilterTop10 API

```http
PUT https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/autoFilter/filterTop10
```

### **Sicherheit und Authentifizierung**

Die Aspose.Cells Cloud APIs sind sicher und erfordern eine <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-Token-basierte Authentifizierung</a>.

### Anforderungsparameter

| Parametername     | Typ     | Speicherort | Erforderlich | Standardwert | Beschreibung                                                                 |
| ----------------- | ------- | ----------- | ------------ | ------------ | ---------------------------------------------------------------------------- |
| **name**          | string  | Pfad        | Ja           | —            | Der Name der Excel-Datei.                                                    |
| **sheetName**     | string  | Pfad        | Ja           | —            | Der Name des Arbeitsblatts, das die Daten enthält.                           |
| **range**         | string  | Abfrage     | Ja           | —            | Der Zellbereich, auf den der Filter angewendet wird (z. B. `A1:B10`).        |
| **fieldIndex**    | integer | Abfrage     | Ja           | —            | Nullbasierter Index der Spalte, auf die der Filter angewendet wird.          |
| **isTop**         | boolean | Abfrage     | Ja           | `true`       | `true`, um die obersten Elemente zu filtern; `false` für die untersten.      |
| **isPercent**     | boolean | Abfrage     | Nein         | `false`      | `true`, um `itemCount` als Prozentsatz zu interpretieren; `false` für eine absolute Anzahl. |
| **itemCount**     | integer | Abfrage     | Nein         | `10`         | Anzahl der Elemente, die in den Filter einbezogen werden sollen.             |
| **matchBlanks**   | boolean | Abfrage     | Nein         | `false`      | `true`, um leere Zellen in die Filterergebnisse einzubeziehen.              |
| **refresh**       | boolean | Abfrage     | Nein         | `false`      | `true`, um den Filter nach dem Anwenden zu aktualisieren.                   |
| **folder**        | string  | Abfrage     | Nein         | —            | Der Ordner im Speicher, in dem sich die Excel-Datei befindet.               |
| **storageName**   | string  | Abfrage     | Nein         | —            | Der Name des Aspose Cloud-Speichers.                                         |

### **Antwort**

```json
{
    "Status":"OK",
    "Code":200
}
```

**Typische Fehlerantworten**

```json
{
    "Code":400,
    "Message":"Bad Request – fehlende oder ungültige Parameter."
}
```

```json
{
    "Code":401,
    "Message":"Unauthorized – ungültiges oder fehlendes JWT-Token."
}
```

```json
{
    "Code":413,
    "Message":"Payload Too Large – hochgeladene Datei überschreitet die zulässige Größe."
}
```

```json
{
    "Code":500,
    "Message":"Internal Server Error – unerwarteter Serverfehler."
}
```

**HTTP-Statuscodes**

| Code | Bedeutung                   | Beschreibung                                                           |
|------|-----------------------------|------------------------------------------------------------------------|
| 200  | OK                          | Filter erfolgreich angewendet; Antwort enthält Details zum Vorgang.   |
| 400  | Bad Request                 | Fehlende oder ungültige Parameter (z. B. nicht unterstützter Dateityp). |
| 401  | Unauthorized                | Ungültiges oder fehlendes JWT-Token.                                  |
| 413  | Payload Too Large           | Hochgeladene Datei überschreitet die Größe.                           |
| 500  | Internal Server Error       | Unerwarteter Serverfehler.                                             |

## Verwendung der PutWorksheetFilterTop10 API mit SDKs

### PutWorksheetFilterTop10 API-Spezifikation

Die [OpenAPI-Spezifikation](https://apireference.aspose.cloud/cells/#/AutoFilter/PutWorksheetFilterTop10) definiert eine öffentlich zugängliche Programmierschnittstelle und ermöglicht es Ihnen, REST-Interaktionen direkt über einen Webbrowser durchzuführen.

Sie können das cURL-Befehlszeilentool nutzen, um problemlos auf die Aspose.Cells-Webdienste zuzugreifen. Im folgenden Beispiel wird gezeigt, wie die API mit cURL aufgerufen wird.

{{< tabs tabTotal="2" tabID="11" tabName11="Anforderung" tabName12="Antwort" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/autoFilter/filterTop10?range=A1:B10&fieldIndex=0&isTop=true&itemCount=10" \
  -X PUT \
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

### Verwendung der Aspose.Cells Cloud SDKs

Die Verwendung eines SDKs ist der schnellste Weg zur Entwicklung. Ein SDK übernimmt die Details der niedrigen Ebene, sodass Sie sich auf Ihr Projekt konzentrieren können. Besuchen Sie das [GitHub-Repository](https://github.com/aspose-cells-cloud), um eine vollständige Liste der Aspose.Cells Cloud SDKs zu erhalten.

Die folgenden Codebeispiele zeigen, wie Aspose.Cells-Webdienste mithilfe verschiedener SDKs aufgerufen werden:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePutWorksheetFilterTop10.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PutWorksheetFilterTop10.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PutWorksheetFilterTop10.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PutWorksheetFilterTop10.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PutWorksheetFilterTop10.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PutWorksheetFilterTop10.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PutWorksheetFilterTop10.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PutWorksheetFilterTop10.go" >}}

{{< /tab >}}

{{< /tabs >}}