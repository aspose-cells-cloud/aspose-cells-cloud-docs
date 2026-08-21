---
title: "Aspose.Cells Cloud-kalkylbladssplittrare Web API – dela Excel-arbetsbok i flera filer i 30+ format"
second_title: "Dokument"
ArticleTitle: "Dela Excel-fil i molnet för att separera filer & exportera till 30+ format"
linktitle: "Dela fjärrkalkylblad i molnet"
type: docs
url: /split-remote-spreadsheet/
keywords: "Aspose.Cells Cloud, dela Excel-arbetsbok, kalkylbladssplittrare, moln-API, exportera till PDF, exportera till CSV, exportera till JSON, flera formatexport, kalkylbladsbehandling i molnet"
description: "Använd Aspose.Cells Cloud API för att dela en Excel-arbetsbok som lagras i molnlagring i separata kalkylblad och exportera varje del till över 30 format såsom PDF, CSV, JSON, XLSX, HTML, ODS och XPS."
weight: 100
---

Dela upp en stor Excel-arbetsbok som lagras i molnet i separata filer per kalkylblad och exportera varje del till över 30 utdataformat såsom PDF, CSV, JSON, ODS och XPS med Aspose.Cells Cloud.

## **Split Remote Spreadsheet API**

### Web API

```http
PUT https://api.aspose.cloud/v4.0/cells/{name}/split/spreadsheet
```

### **Säkerhet och autentisering**

Aspose.Cells Cloud APIs är säkra och kräver <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-tokenbaserad autentisering</a>.

### **Begäran parametrar:**

| Parameter Name | Typ     | Path/Query String/HTTP Body | Beskrivning                                                                                                                       |
| :------------- | :------ | :-------------------------- | :-------------------------------------------------------------------------------------------------------------------------------- |
| name           | String  | Path                        | Namnet på arbetsboksfilen (t.ex. `data.xlsx`) som ska delas, placerad i den angivna mappen i molnlagring.                          |
| folder         | String  | Query                       | Sökvägen till molnlagringsmappen där källarbetsboken lagras.                                                                      |
| from           | Integer | Query                       | Startindex för kalkylblad (0-baserat) för delningsåtgärden. Exempel: `0` anger det första kalkylbladet.                            |
| to             | Integer | Query                       | Slutindex för kalkylblad (0-baserat) för delningsåtgärden. Exempel: `2` delar kalkylbladen 0, 1 och 2.                             |
| outFormat      | String  | Query                       | Utdatafilformat för de delade filerna. Stödda format inkluderar `XLSX`, `PDF`, `CSV`, `JSON`, `HTML` och 30+ andra.                |
| storageName    | String  | Query                       | _(Valfritt)_ Namnet på molnlagringen där källarbetsboken finns. Om utelämnas används standardmolnlagringen.                        |
| outPath        | String  | Query                       | _(Valfritt)_ Målmappens sökväg i molnet där de delade filerna sparas. Om utelämnas sparas filerna i källmappen.                    |
| outStorageName | String  | Query                       | Namnet på molnlagringen där de utdata-delade filerna kommer att lagras.                                                            |
| fontsLocation  | String  | Query                       | _(Valfritt)_ Anger en anpassad mapp i molnet som innehåller typsnittsfiler för korrekt textrendering i PDF/bildutdata.            |
| region         | String  | Query                       | _(Valfritt)_ Anger språkinställningen för formatering av tal, datum och valuta i utdatafilerna (t.ex. `"sv-SE"`, `"en-US"`, `"de-DE"`). |
| password       | String  | Query                       | _(Valfritt)_ Om källarbetsboken är lösenordsskyddad, ange lösenordet för att öppna filen.                                          |

## **Svar**

```json
[
  {
    "Name": "ResponseFile",
    "DataType": {
      "Identifier": "File",
      "Reference": "Stream",
      "Name": "file"
    }
  }
]
```

Filen kan laddas ner direkt från eller sparas till den plats som anges av `outPath`.

**Detaljerad lyckad respons**

| Statuskod | Content‑Type               | Beskrivning                                  |
| --------- | -------------------------- | -------------------------------------------- |
| 200 OK    | `application/octet-stream` | Binär ström av den sammanslagna arbetsboksfilen. |

**HTTP-statuskoder**

| Kod | Betydelse               | Beskrivning                                                       |
| --- | ----------------------- | ----------------------------------------------------------------- |
| 200 | OK                      | Filter tillämpades framgångsrikt; svaret innehåller åtgärdens detaljer. |
| 400 | Bad Request             | Saknade eller ogiltiga parametrar (t.ex. filtyp som inte stöds).  |
| 401 | Unauthorized            | Ogiltig eller saknad JWT-token.                                   |
| 413 | Payload Too Large       | Den uppladdade filen överskrider storleksgränsen.                 |
| 500 | Internal Server Error   | Oväntat serverfel.                                                |

## Var bör vi använda Split Remote Spreadsheet API?

- **Avdelningsdatafördelning**: Dela en enhetlig arbetsbok som innehåller data från flera avdelningar i avdelningsspecifika filer.
- **Regional rapportfördelning**: Dela nationella försäljningsrapporter i separata regionala rapportfiler enligt region.
- **Kunddataskyddsfördelning**: Dela en arbetsbok som innehåller känslig information i en dedikerad kundvy-fil.
- **Periodisk rapportdelning**: Dela automatiskt sammanfattande rapporter i veckovisa eller dagliga rapporter månadsvis.
- **Fördelning i flera format**: Dela en enda Excel-fil i flera formatversioner såsom PDF, CSV, JSON, etc., samtidigt.
- **Mallbaserad delning**: Dela datafiler i standardiserade utdatafiler baserat på fördefinierade mallar.
- **Datkälla förbearbetning**: Dela Excel-filen i en standardiserad CSV-fil innan data laddas in i databasen.
- **API-förberedelse av data**: Dela stora datamängder i mindre chunkar lämpliga för API-överföring.
- **Mikrotjänstdatabefordran**: Dela den centrala datafilen i separata datafiler som krävs av varje mikrotjänst.

## Varför bör du använda Split Remote Spreadsheet API?

- **Utvecklarvänligt**: Aspose.Cells Cloud erbjuder SDK-bibliotek i flera språk, vilket möjliggör snabb utveckling och följs med omfattande dokumentation. Jämfört med att bygga egna lösningar för diagramrendering minskar detta avsevärt utvecklingsarbetet.
- **Lägre arbetskostnader**: Minskar behovet av tjänster dedikerade till dokumentkonsolidering.
- **Betala per användning**: Inget förstainvestering; du betalar endast för API-anrop som faktiskt används.
- **Inga underhållskostnader**: Inget behov av att underhålla servrar, uppdatera programvara eller hantera kompatibilitetsproblem.
- **Bevarar avancerad Excel-formatering** i allmänt tillgängligt PDF-format.

## Hur man använder Split Remote Spreadsheet API med SDK:er

### Split Remote Spreadsheet API-specifikation

[Split Remote Spreadsheet API-specifikationen](https://reference.aspose.cloud/cells/#/DataProcessingController/SplitRemoteSpreadsheet) definierar ett offentligt tillgängligt programmeringsgränssnitt och möjliggör REST-interaktioner direkt från en webbläsare.

Du kan använda verktyget cURL för kommandoraden för enkelt att komma åt Aspose.Cells webbtjänster. Följande exempel visar hur man gör anrop till moln-API:et med cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Begäran" tabName12="Svar" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/Report.xlsx/split/spreadsheet?folder=Input&outFormat=PDF&from=0&to=2" \
     -H "Authorization: Bearer {access_token}" \
     -H "Accept: application/json"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```
{
  "type": "FileContentResult",
  "fileContents": "byte[] (Base64-kodad)",
  "contentType": "MIME-typ",
  "fileDownloadName": "valfritt filnamn"
}
```

{{< /tab >}}

{{< /tabs >}}

### Använd Aspose.Cells Cloud SDK:er

Att använda ett SDK är det snabbaste sättet att utveckla, eftersom det abstraherar bort detaljerna på låg nivå och låter dig dela upp kalkylbladet i molnet i separata filer med kort kod.  
Kolla in [GitHub-lagringsplatsen](https://github.com/aspose-cells-cloud) för en komplett lista över Aspose.Cells Cloud SDK:er.  
Följande kodexempel visar hur man gör anrop till Aspose.Cells webbtjänster med olika SDK:er:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_SplitFileInRemote.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_SplitFileInRemote.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_SplitFileInRemote.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_SplitFileInRemote.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_SplitFileInRemote.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_SplitFileInRemote.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_SplitFileInRemote.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_SplitFileInRemote.go" >}}
{{</tab>}}
{{< /tabs >}}