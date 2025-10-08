---
title: Aspose.Cells Molnwebb API - Sammanfoga ett kalkylblad med ett annat.
second_title: Aspose.Cells Cloud"
ArticleTitle: Merge one spreadsheet into anothe
linktitle: Sammanfoga fjärrkalkylblad
type: docs
url: /sv/merge-remote-spreadsheet/
keywords: Merge spreadsheets, cloud storage, Aspose.Cells Cloud Web API, spreadsheet merging, XLSX, CSV, PD
description: Kombinera en kalkylbladsfil som lagras i en molnlagring med ett annat kalkylblad, så kan du ange format och plats för datautdata.
weight: 100
kwords: Excel, Office Moln, REST API, Kalkylblad, PDF, CSV, JSON, Markdown, sammanfoga tomma celler, molnbearbetning
---
Kombinera en kalkylbladsfil som lagras i en molnlagring med ett annat kalkylblad, så kan du ange format och plats för datautdata.

## **Sammanfoga fjärrkalkylblad API**

```http
PUT http://api.aspose.cloud/v4.0/cells/{name}/merge/spreadsheet
```

### **Begäranparametrar:**

| Parameternamn| Typ| Sökväg/Frågesträng/HTTP-kropp| Beskrivning|
|:- |:- |:- |:- |
|namn|Sträng|Väg|Namnet på den arbetsboksfil som ska sammanfogas.|
|sammanslaget kalkylblad|Sträng|Fråga|Listan över kalkylarksfiler som ska sammanfogas.|
|mapp|Sträng|Fråga|Mappsökvägen där arbetsboken lagras.|
|utformat|Sträng|Fråga|Utdatafilformatet (t.ex. XLSX, PDF).|
|sammanfogaIEttSheet|Booleansk|Fråga|Om all data ska kombineras till ett enda kalkylblad.|
|lagringsnamn|Sträng|Fråga|(Valfritt) Namnet på lagringsplatsen om anpassad molnlagring används. Standardlagring används om den utelämnas.|
|utväg|Sträng|Fråga|(Valfritt) Mappsökvägen för den sammanfogade arbetsboken. Standardvärdet är null.|
|outStorageName|Sträng|Fråga|Namnet på lagringsplatsen för utdatafilen.|
|teckensnittPlats|Sträng|Fråga|Anpassad teckensnittsplacering.|
|område|Sträng|Fråga|Inställningen för kalkylbladets region.|
|lösenord|Sträng|Fråga|Lösenordet för att komma åt kalkylbladsfilen.|

### **Svar**

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

### Felkoder

- **400 Felaktig begäran**Ogiltig Apose.Cells Cloud API URI.
- **401 Obehörig**Ogiltig åtkomsttoken. Eller ogiltigt klient-ID och hemlighet.
- **404 Hittades inte**Kalkylbladsfilen är inte tillgänglig.
- **500 Serverfel**Kalkylbladet har stött på ett fel vid hämtning av beräkningsdata.

## Var ska vi använda Merge Remote Spreadsheet API?

- När du behöver sammanfoga flera datafiler i molnlagring.


## Varför ska du använda Merge Remote Spreadsheet API?

- Molnlagringsfiler behöver inte laddas ner och kan sammanfogas direkt i molnet.
- Utvecklingen kan snabbt slutföras via det befintliga SDK:t.

## Så här använder du kalkylbladet Merge Remote API med SDK:er

### Sammanfoga fjärrkalkylblad API Specifikation

 De[Sammanfoga fjärrkalkylblad API Specifikation](https://reference.aspose.cloud/cells/#/DataProcessingController/MergeRemoteSpreadsheet) tillhandahåller ett offentligt tillgängligt programmeringsgränssnitt för att utföra REST-interaktioner direkt från en webbläsare.

## Excel API SDK

### Använd Aspose.Cells Cloud SDK:er

Att använda SDK:t är det snabbaste sättet att utveckla, eftersom det abstraherar bort detaljer på låg nivå, vilket gör att du kan sammanfoga ett kalkylblad med ett annat kalkylblad med kort kod.
 Vänligen kolla in[GitHub-arkiv](https://github.com/aspose-cells-cloud) för en komplett lista över Aspose.Cells Cloud SDK:er.
Följande kodexempel visar hur man interagerar med Aspose.Cells-webbtjänster med hjälp av olika SDK:er:

{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_MergeRemoteSpreadsheet.cs" >}}
{{< /tab >}}
{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_MergeRemoteSpreadsheet.java" >}}
{{< /tab >}}
{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_MergeRemoteSpreadsheet.php" >}}
{{< /tab >}}
{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_MergeRemoteSpreadsheet.rb" >}}
{{< /tab >}}
{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_MergeRemoteSpreadsheet.ts" >}}
{{< /tab >}}
{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_MergeRemoteSpreadsheet.py" >}}
{{< /tab >}}
{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_MergeRemoteSpreadsheet.pl" >}}
{{< /tab >}}
{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_MergeRemoteSpreadsheet.go" >}}
{{< /tab >}}
{{< /tabs >}}
