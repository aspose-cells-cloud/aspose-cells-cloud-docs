---
title: "Aspose.Cells Cloud Ersättningswebb-API – Uppdatera text i fjärr-Excel-omfattning"
secondtitle: "Dokument"
ArtikelTitel: "Bulk-ersättning av text i omfattningar i moln-Excel-filer – Sök-och-ersätt-API"
linktitle: "Ersätt innehåll i fjärr-omfattning"
type: docs
url: /replace-content-in-remote-range/
keywords: "ersätt text i fjärr-Excel-omfattning, Aspose.Cells Cloud API, sök och ersätt Excel, redigera moln-kalkylark, uppdatera fjärr-Excel-filer"
description: "Använd Aspose.Cells Cloud för att söka och ersätta text i en specifik omfattning i en fjärr-Excel-fil. Stödjer autentisering, felhantering och SDK:er för flera språk."
weight: 100
---

Utför bulk-textersättning över fjärr-Excel-filer lagrade i molnet. Sök och uppdatera specifika textsträngar i utvalda omfattningar effektivt med Aspose.Cells Sök-och-ersätt-API.

## **Ersätt innehåll i fjärr-omfattning – API**

### Webb-API

```
PUT https://api.aspose.cloud/v4.0/cells/{name}/worksheets/{worksheet}/ranges/{cellArea}/replace/content
```

### **Säkerhet och autentisering**

Aspose.Cells Cloud-API:er är säkra och kräver <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-tokenbaserad autentisering</a>.

```bash
-H "Authorization: Bearer {access_token}"
```

### **Parameter för begäran**

| Parameternamn   | Typ    | Sökväg/Frågesträng/HTTP-kropp | Beskrivning                                                                                                                                            |
| :-------------- | :----- | :---------------------------- | :----------------------------------------------------------------------------------------------------------------------------------------------------- |
| name            | String | Sökväg                        | Namnet på arbetsboken som finns lagrad i molnlagringen och som ska modifieras (t.ex. `"rapport.xlsx"`).                                               |
| searchText      | String | Frågesträng                   | Den textsträng som ska sökas efter i det angivna kalkylbladet och den angivna cellomfattningen. Stöder exakt textmatchning.                          |
| replaceText     | String | Frågesträng                   | Den textsträng som kommer att ersätta alla förekomster av `searchText` i den angivna omfattningen.                                                    |
| worksheet       | String | Sökväg                        | Namnet på det kalkylblad där sök-och-ersätt-åtgärden ska utföras.                                                                                     |
| cellArea        | String | Sökväg                        | Den specifika cellomfattningen (t.ex. `"A1:D20"`) där textsökning och ersättning ska ske.                                                             |
| folder          | String | Frågesträng                   | Sökvägen till molnlagringsmappen där källarbetsboken finns.                                                                                           |
| storageName     | String | Frågesträng                   | _(Valfritt)_ Namnet på den molnlagring där arbetsboken finns. Om utelämnas används standardmolnlagringen.                                             |
| region          | String | Frågesträng                   | _(Valfritt)_ Ställer in lokalt språk för texthantering, vilket kan påverka skiftlägeskänslighet och teckenkodning i sökningar (t.ex. `"sv-SE"`, `"en-US"`). |
| password        | String | Frågesträng                   | _(Valfritt)_ Om arbetsboken är lösenordsskyddad, ange lösenordet för att öppna och modifiera filen.                                                   |

### **Svar**

```json
{
  "Name": "CellsCloudResponse",
  "Type": "Class",
  "Properties": [
    {
      "Name": "Code",
      "DataType": {
        "Identifier": "Integer"
      }
    },
    {
      "Name": "Status",
      "DataType": {
        "Identifier": "String"
      }
    }
  ]
}
```

Ett lyckat anrop returnerar följande konkreta JSON-svar:

```json
{
  "Code": 200,
  "Status": "OK"
}
```


### Felkoder

| Kod | Meddelande   | När det inträffar                                       |
| --- | ------------ | ------------------------------------------------------- |
| 400 | Bad Request  | Begäran URI eller parametrar är felaktigt formaterade. |
| 401 | Unauthorized | Saknar eller har ogiltig autentiseringstoken.          |
| 404 | Not Found    | Den angivna arbetsboken kan inte hittas eller nås.     |
| 500 | Server Error | Ett internt serverfel uppstod vid bearbetning av arbetsboken. |

## Var bör vi använda API:et för att ersätta innehåll i omfattning i fjärr-Excel-ark?

- **Batch-uppdatering av moln-filer**: Modifiera innehållet i flera Excel-filer lagrade i molnlagringar som AWS S3 och Azure Blob.
- **Dynamisk ifyllnad av moln-mallar**: Batch-fyll i dynamiskt data för rapportmallar lagrade i molnet.
- **Filöverensstämmelse över regioner**: Säkerställ konsistent innehåll i Excel-filer i molnlagring över olika geografiska regioner.

## Varför bör du använda API:et för att ersätta innehåll i omfattning i fjärr-Excel-ark?

- **Utvecklarvänlig**: Aspose.Cells Cloud erbjuder SDK-bibliotek för flera språk, vilket möjliggör snabb utveckling och omfattande dokumentation. Jämfört med att bygga egna lösningar minskas utvecklingsarbetet avsevärt.
- **Lägre arbetskostnader**: Minskar behovet av speciella roller för dokumentkonsolidering.
- **Betala per användning**: Inget förstakostnadskrav – du betalar endast för de API-anrop som faktiskt används.
- **Inga underhållskostnader**: Inget behov av att underhålla servrar, uppdatera mjukvara eller hantera kompatibilitetsproblem.
- **Bevarar komplex Excel-formatering** i ett universellt tillgängligt PDF-format.

## Hur används API:et för att ersätta innehåll i omfattning i fjärr-Excel-ark med SDK:er?

### OpenAPI-specifikation

[OpenAPI-specifikationen](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Search/ReplaceContentInRemoteRange) definierar ett offentligt tillgängligt programmeringsgränssnitt och låter dig utföra REST-interaktioner direkt från en webbläsare.

### Använd Aspose.Cells Cloud SDK:er

Att använda SDK är det bästa sättet att påskynda utvecklingen. SDK:et hanterar underliggande detaljer, så att du enkelt kan implementera ersättning av innehåll i kalkylark med minimal kod. Kontrollera [GitHub-lagret](https://github.com/aspose-cells-cloud) för en komplett lista över Aspose.Cells Cloud SDK:er.

Följande kodexempel visar hur man gör anrop till Aspose.Cells-webbtjänster med diverse SDK:er:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}

```csharp
```

{{</tab>}}
{{<tab tabNum="2" >}}

```java
```

{{</tab>}}
{{<tab tabNum="3" >}}

```php
```

{{</tab>}}
{{<tab tabNum="4" >}}

```ruby
```

{{</tab>}}
{{<tab tabNum="5" >}}

```javascript
```

{{</tab>}}
{{<tab tabNum="6" >}}

```python
```

{{</tab>}}
{{<tab tabNum="7" >}}

```perl
```

{{</tab>}}
{{<tab tabNum="8" >}}

```go
```

{{</tab>}}
{{< /tabs >}}