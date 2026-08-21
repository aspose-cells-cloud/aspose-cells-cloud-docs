---
title: "Hämta en specifik dokumentegenskap"
second_title: "Dokument"
linktitle: "Hämta"
type: docs
url: /document-properties/get/
aliases: [/get-a-particular-document-property/]
keywords: "Aspose.Cells, molntjänst, hämta dokumentegenskap, Excel-metadata, REST GET, SDK-exempel"
description: "Hämta en namngiven dokumentegenskap (t.ex. författare, titel) från en Excel-fil med Aspose.Cells Cloud REST API. Innehåller cURL-exempel, SDK-utdrag och svarsschema."
weight: 20
---

Denna REST API läser en dokumentegenskap med namn.

## REST API

```bash
GET https://api.aspose.cloud/v3.0/cells/{name}/documentproperties/{propertyName}
```

### Parametrar för begäran

| ParameterNamn   | Typ    | Plats  | Beskrivning                                      |
| --------------- | ------ | ------ | ------------------------------------------------ |
| name            | string | path   | Namnet på Excel-filen.                           |
| propertyName    | string | path   | Namnet på den dokumentegenskap som ska hämtas.   |
| folder          | string | query  | Mappen som innehåller filen (valfritt).          |
| storageName     | string | query  | Lagringsnamnet (valfritt).                       |

[OpenAPI-specifikationen](https://apireference.aspose.cloud/cells/#/Properties/GetDocumentProperty) definierar ett offentligt tillgängligt programmeringsgränssnitt och låter dig utföra REST-interaktioner direkt från en webbläsare.

Du kan använda **cURL kommandoradsverktyget** för enkelt att komma åt Aspose.Cells webbtjänster. Följande exempel visar hur man gör anrop till molntjänsten med cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Begäran" tabName12="Svar" >}}

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

### Detaljer för svar

JSON-objektet som returneras av API:et innehåller följande fält:

| Fält                            | Typ     | Beskrivning                                                   |
| ------------------------------- | ------- | ------------------------------------------------------------- |
| **DocumentProperty.Name**       | string  | Namnet på egenskapen (t.ex. `Author`).                        |
| **DocumentProperty.Value**      | string  | Värdet för egenskapen. Kan vara tomt om inte angivet.         |
| **DocumentProperty.BuiltIn**    | boolean | Anger om egenskapen är en inbyggd Excel-egenskap.             |
| **DocumentProperty.link.Href**  | string  | Relativ URL till egenskapsresursen.                            |
| **DocumentProperty.link.Rel**   | string  | Relations typ, vanligtvis `self`.                             |
| **DocumentProperty.link.Title** | string  | Mänsklig läsbar titel (kan vara `null`).                      |
| **DocumentProperty.link.Type**  | string  | MIME-typ för den länkade resursen (kan vara `null`).          |
| **Code**                        | integer | HTTP-statuskod som returnerats av tjänsten.                   |
| **Status**                      | string  | Textuell beskrivning av statusen (t.ex. `OK`).                |

### Felaktiga svar

| HTTP-status | Kod                    | Beskrivning                                         |
| ----------- | ---------------------- | --------------------------------------------------- |
| 400         | `InvalidParameter`     | En eller flera begäransparametrar är ogiltiga.     |
| 401         | `AuthenticationFailed` | Saknas eller ogiltigt JWT-token.                   |
| 404         | `PropertyNotFound`     | Den angivna dokumentegenskapen finns inte.         |
| 500         | `InternalError`        | Ett oväntat fel uppstod på servern.                 |

Ett typiskt felmeddelande ser ut så här:

```json
{
  "Code": 404,
  "Status": "Property not found"
}
```

## Molnsdk-familj

Att använda en sdk är det bästa sättet att påskynda utvecklingen. En sdk hanterar detaljer på låg nivå så att du kan fokusera på dina projektuppgifter. Kontrollera [GitHub-lagringsplatsen](https://github.com/aspose-cells-cloud) för en komplett lista över Aspose.Cells Cloud SDK:n.

Följande kodexempel visar hur man gör anrop till Aspose.Cells webbtjänster med olika SDK:n:

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

### Terminologi

| Term                  | Definition                                                                                          |
| --------------------- | --------------------------------------------------------------------------------------------------- |
| **Document Property** | En bit metadata kopplad till en Excel-arbetsbok (t.ex. författare, titel, skapat).                |
| **Metadata**          | Generellt uttryck för data som beskriver annan data; i detta sammanhang avses dokumentegenskaper. |
| **Custom Property**   | En användardefinierad egenskap som inte ingår i den inbyggda uppsättningen.                        |

### Vanliga frågor

**Fråga:** _Hur kan jag hämta författaregenskapen för en Excel-fil som lagras i Aspose Cloud?_  
**Svar:** Skicka en GET-begäran till `https://api.aspose.cloud/v3.0/cells/{fileName}/documentproperties/author` med ett giltigt Bearer-token. SVaret JSON innehåller `DocumentProperty.Name = "Author"` och dess `Value`.

**Fråga:** _Vilket fel returneras om den begärda egenskapen inte finns?_  
**Svar:** API:et returnerar HTTP 404 med ett JSON-svar innehållande `Code: 404` och `Status: "Property not found"`.

**Fråga:** _Måste jag ange `storageName` när filen finns i standardlagringen?_  
**Svar:** Nej. Parametern `storageName` är valfri; utelämna den för att använda standardlagringen som konfigurerats för ditt konto.

---