---
title: "Spezifische Dokumenteigenschaft abrufen"
second_title: "Dokument"
linktitle: "Abrufen"
type: docs
url: /document-properties/get/
aliases: [/get-a-particular-document-property/]
keywords: "Aspose.Cells, Cloud API, Dokumenteigenschaft abrufen, Excel-Metadaten, REST GET, SDK-Beispiele"
description: "Rufen Sie eine benannte Dokumenteigenschaft (z. B. Autor, Titel) aus einer Excel-Datei mithilfe der Aspose.Cells Cloud REST API ab. Enthält cURL-Beispiel, SDK-Snippets und Antwort-Schema."
weight: 20
---

Diese REST API liest eine Dokumenteigenschaft anhand ihres Namens.

## REST API

```bash
GET https://api.aspose.cloud/v3.0/cells/{name}/documentproperties/{propertyName}
```

### Anforderungsparameter

| Parametername      | Typ    | Speicherort | Beschreibung                                        |
| ------------------ | ------ | ----------- | --------------------------------------------------- |
| name               | string | path        | Der Name der Excel-Datei.                           |
| propertyName       | string | path        | Der Name der abzurufenden Dokumenteigenschaft.     |
| folder             | string | query       | Der Ordner, der die Datei enthält (optional).      |
| storageName        | string | query       | Der Speichername (optional).                       |

Die [OpenAPI-Spezifikation](https://apireference.aspose.cloud/cells/#/Properties/GetDocumentProperty) definiert eine öffentlich zugängliche Programmierschnittstelle und ermöglicht Ihnen REST-Interaktionen direkt aus einem Webbrowser.

Sie können das **cURL-Befehlszeilentool** verwenden, um problemlos auf die Aspose.Cells-Webdienste zuzugreifen. Das folgende Beispiel zeigt, wie mithilfe von cURL Aufrufe an die Cloud-API durchgeführt werden.

{{< tabs tabTotal="2" tabID="11" tabName11="Anforderung" tabName12="Antwort" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/documentproperties/author" \
  -X GET \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "DocumentProperty": {
    "Name": "Author",
    "Value": "",
    "BuiltIn": "True",
    "link": {
      "Href": "/test.xlsx/documentproperties/Author",
      "Rel": "self",
      "Title": null,
      "Type": null
    }
  },
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

### Antwortdetails

Das von der API zurückgegebene JSON-Objekt enthält die folgenden Felder:

| Feld                                | Typ     | Beschreibung                                                         |
| ----------------------------------- | ------- | -------------------------------------------------------------------- |
| **DocumentProperty.Name**           | string  | Der Name der Eigenschaft (z. B. `Author`).                           |
| **DocumentProperty.Value**          | string  | Der Wert der Eigenschaft. Kann leer sein, wenn nicht gesetzt.       |
| **DocumentProperty.BuiltIn**        | boolean | Gibt an, ob es sich um eine integrierte Excel-Eigenschaft handelt. |
| **DocumentProperty.link.Href**      | string  | Relative URL zur Ressource der Eigenschaft.                          |
| **DocumentProperty.link.Rel**       | string  | Beziehungstyp, gewöhnlich `self`.                                   |
| **DocumentProperty.link.Title**     | string  | Menschlich lesbare Überschrift (kann `null` sein).                   |
| **DocumentProperty.link.Type**      | string  | MIME-Typ der verknüpften Ressource (kann `null` sein).               |
| **Code**                            | integer | Von dem Dienst zurückgegebener HTTP-Statuscode.                     |
| **Status**                          | string  | Textuelle Beschreibung des Status (z. B. `OK`).                     |

### Fehlerantworten

| HTTP-Status | Code                   | Beschreibung                                             |
| ----------- | ---------------------- | -------------------------------------------------------- |
| 400         | `InvalidParameter`     | Mindestens ein Anforderungsparameter ist ungültig.      |
| 401         | `AuthenticationFailed` | Fehlender oder ungültiger JWT-Token.                    |
| 404         | `PropertyNotFound`     | Die angegebene Dokumenteigenschaft existiert nicht.     |
| 500         | `InternalError`        | Auf dem Server ist ein unerwarteter Fehler aufgetreten. |

Ein typischer Fehlerkörper sieht wie folgt aus:

```json
{
  "Code": 404,
  "Status": "Property not found"
}
```

## Cloud SDK-Familie

Die Verwendung eines SDKs ist die beste Möglichkeit, die Entwicklung zu beschleunigen. Ein SDK übernimmt die Low-Level-Details, sodass Sie sich auf die Aufgaben Ihres Projekts konzentrieren können. Besuchen Sie das [GitHub-Repository](https://github.com/aspose-cells-cloud), um eine vollständige Liste der Aspose.Cells Cloud SDKs zu erhalten.

Die folgenden Codebeispiele zeigen, wie Aufrufe an die Aspose.Cells-Webdienste mithilfe verschiedener SDKs durchgeführt werden:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetDocumentProperty.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetDocumentProperty.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetDocumentProperty.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetDocumentProperty.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_GetDocumentProperty.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetDocumentProperty.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetDocumentProperty.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetDocumentProperty.go" >}}

{{< /tab >}}

{{< /tabs >}}

### Terminologie

| Begriff                  | Definition                                                                                      |
| ------------------------ | ----------------------------------------------------------------------------------------------- |
| **Dokumenteigenschaft**  | Ein Metadatenelement, das mit einer Excel-Arbeitsmappe verknüpft ist (z. B. Autor, Titel, Erstelldatum). |
| **Metadaten**            | Allgemeiner Begriff für Daten, die andere Daten beschreiben; hier bezieht es sich auf Dokumenteigenschaften. |
| **Benutzerdefinierte Eigenschaft** | Eine benutzerdefinierte Eigenschaft, die nicht im integrierten Satz enthalten ist.             |

### Häufig gestellte Fragen (FAQ)

**Q:** _Wie kann ich die Autor-Eigenschaft einer Excel-Datei abrufen, die in Aspose Cloud gespeichert ist?_  
**A:** Senden Sie eine GET-Anforderung an `https://api.aspose.cloud/v3.0/cells/{fileName}/documentproperties/author` mit einem gültigen Bearer-Token. Die JSON-Antwort enthält `DocumentProperty.Name = "Author"` sowie dessen `Value`.

**Q:** _Welcher Fehler wird zurückgegeben, wenn die angeforderte Eigenschaft nicht existiert?_  
**A:** Die API gibt HTTP 404 zurück, wobei der JSON-Körper `Code: 404` und `Status: "Property not found"` enthält.

**Q:** _Muss ich `storageName` angeben, wenn sich die Datei im Standardspeicher befindet?_  
**A:** Nein. Der Abfrageparameter `storageName` ist optional; lassen Sie ihn weg, um den für Ihr Konto konfigurierten Standardspeicher zu verwenden.

---