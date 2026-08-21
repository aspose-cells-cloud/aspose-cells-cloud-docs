---
title: "Aspose.Cells Cloud Web API – Extrahera text"
second_title: "Aspose.Cells Cloud – Online kortkod"
linktitle: "Extrahera text"
type: docs
url: /sv/extract-text/
keywords: "Aspose.Cells Cloud, extrahera text, Excel API, celltextextraktion, REST API"
description: "Extrahera delsträngar, siffror eller tecken från Excel-cellerna med Aspose.Cells Cloud API. Stöder text före/efter, positionbaserad extraktion och direkt utmatning till ett nytt intervall."
weight: 100
ArticleTitle: "Aspose.Cells Cloud Extract Text API-dokumentation"
---

Extraherar delsträngar, tecken eller siffror från en kalkylbladscell till en annan cell, vilket eliminierar behovet av komplexa FIND-, MIN-, LEFT- eller RIGHT-formler.

## **ExtractText API**

```http
PUT https://api.aspose.cloud/v4.0/cells/content/extract/text
```

### **Säkerhet och autentisering**

Aspose.Cells Cloud API:er är säkra och kräver <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-tokenbaserad autentisering</a>.

```bash
-H "Authorization: Bearer {access_token}"
```

### **Requestparametrar för API:t extractText**

| Parameternamn    | Typ     | Plats              | Beskrivning                                                                                                                     |
| ---------------- | ------- | ------------------ | ------------------------------------------------------------------------------------------------------------------------------- |
| Spreadsheet      | Fil     | FormData           | Ladda upp kalkylbladsfilen.                                                                                                     |
| extractTextType  | Sträng  | Frågeparameter     | Enum som anger extraktionsläge. Tillåtna värden: `Before`, `After`, `BeforePosition`, `AfterPosition`.                       |
| beforeText       | Sträng  | Frågeparameter     | Text som måste förekomma **före** den extraherade delsträngen. Används när `extractTextType=Before`.                                   |
| afterText        | Sträng  | Frågeparameter     | Text som måste förekomma **efter** den extraherade delsträngen. Används när `extractTextType=After`.                                     |
| beforePosition   | Heltal  | Frågeparameter     | Antal tecken som ska returneras från vänster sida av cellen. Används när `extractTextType=BeforePosition`.                      |
| afterPosition    | Heltal  | Frågeparameter     | Antal tecken som ska returneras från höger sida av cellen. Används när `extractTextType=AfterPosition`.                      |
| outPositionRange | Sträng  | Frågeparameter     | Målintervall (t.ex. `Sheet1!A1`) dit det extraherade texten skrivs.                                                  |
| worksheet        | Sträng  | Frågeparameter     | Namn på kalkylbladet som innehåller källcellen.                                                                            |
| range            | Sträng  | Frågeparameter     | Källcellen eller intervallet (t.ex. `A1`).                                                                                          |
| outPath          | Sträng  | Frågeparameter _(Valfritt)_ | Mappväg i lagringen dit den resulterande arbetsboken sparas. Om utelämnad returneras resultatet i svarskroppen. |
| outStorageName   | Sträng  | Frågeparameter     | Namn på lagringen som ska användas för utdatafilen.                                                                                 |
| region           | Sträng  | Frågeparameter     | Inställning för kalkylbladsregion (t.ex. `US`, `EU`).                                                                                  |
| password         | Sträng  | Frågeparameter     | Lösenord för att öppna en skyddad arbetsbok.                                                                                      |

**Exempel på cURL-förfrågan**

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/content/extract/text?extractTextType=Before&beforeText=Total&outPositionRange=Sheet1!B1&worksheet=Sheet1&range=A1" \
     -H "Authorization: Bearer {access_token}" \
     -F "Spreadsheet=@Sample.xlsx"
```

### **Svar**

När förfrågan lyckas returnerar API:et en JSON-payload som innehåller det extraherade textinnehållet samt adressen till den cell dit det skrevs:

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

Om parametern `outPath` anges innehåller svaret endast ett statusmeddelande; arbetsboken skrivs till den angivna platsen.

**Exempel på svar när `outPath` inte anges**

```json
{
  "Code": 200,
  "Status":"OK"
}
```

### Felkoder

- **200 OK** – Extraktionen slutfördes framgångsrikt.  
- **202 Accepted** – Förfrågan godkänd för asynkron bearbetning.  
- **400 Bad Request** – Ogiltig URI för Aspose.Cells Cloud API eller saknade obligatoriska parametrar.  
- **401 Unauthorized** – Ogiltig åtkomsttoken, klient-ID eller klienthemlighet.  
- **404 Not Found** – Den angivna kalkylbladsfilen kan inte nås.  
- **500 Server Error** – Ett oväntat fel inträffade vid bearbetning av arbetsboken.

## OpenAPI-specifikation

[OpenAPI-specifikationen](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/TextProcessing/ExtractText) definierar ett offentligt tillgängligt programmeringsgränssnitt och låter dig utföra REST-interaktioner direkt från en webbläsare.

### Använd Aspose.Cells Cloud SDK:er

Att använda SDK är det bästa sättet att snabba upp utvecklingen. SDK:en hanterar de underliggande detaljerna, så att du helt enkelt kan implementera **Extrahera text** för celler med minimal kod. Kontrollera [GitHub-repositoriet](https://github.com/aspose-cells-cloud) för en komplett lista över Aspose.Cells Cloud SDK:er.

Följande kodexempel visar hur man gör anrop till Aspose.Cells-webbtjänster med diverse SDK:er:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{<tab tabNum="1" >}}

```csharp
// C#-exempel – extrahera text (kod utelämnad för korthet)
```

{{</tab>}}

{{<tab tabNum="2" >}}

```java
// Java-exempel – extrahera text (kod utelämnad för korthet)
```

{{</tab>}}

{{<tab tabNum="3" >}}

```php
// PHP-exempel – extrahera text (kod utelämnad för korthet)
```

{{</tab>}}

{{<tab tabNum="4" >}}

```ruby
# Ruby-exempel – extrahera text (kod utelämnad för korthet)
```

{{</tab>}}

{{<tab tabNum="5" >}}

```javascript
// Node.js-exempel – extrahera text (kod utelämnad för korthet)
```

{{</tab>}}

{{<tab tabNum="6" >}}

```python
# Python-exempel – extrahera text (kod utelämnad för korthet)
```

{{</tab>}}

{{<tab tabNum="7" >}}

```perl
# Perl-exempel – extrahera text (kod utelämnad för korthet)
```

{{</tab>}}

{{<tab tabNum="8" >}}

```go
// Go-exempel – extrahera text (kod utelämnad för korthet)
```

{{</tab>}}

{{< /tabs >}}