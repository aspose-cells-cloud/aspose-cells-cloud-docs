---
title: Aspose.Cells Cloud Web API - Sammanfoga matchande kalkylbladsfiler till en fil i en fjärrmapp
second_title: Documen
ArticleTitle: Merge matching spreadsheet files into a file in a remote Folder
linktitle: Sammanfoga kalkylblad i fjärrmapp
type: docs
url: /sv/merge-spreadsheets-in-remote-folder/
keywords: Merge spreadsheets, cloud storage, Excel API, remote processing, spreadsheet formats, REST AP
description: Kombinera kalkylbladsfilerna som lagras i molnlagringen till en fil, och filformatet stöder 30 format för utdata, till exempel PDF, Csv, Json och andra vanliga format.
weight: 100
kwords: Excel, Office Moln, REST API, Kalkylblad, PDF, CSV, JSON, Markdown, Sammanfoga kalkylblad, Molnbehandling, Fjärrhantering av filer
---
Sammanfoga matchande kalkylbladsfiler till filer i fjärrmappar. Utdatafilformatet stöder fler än 30 format som PDF, Csv, Json och andra vanliga format.


## **Sammanfoga kalkylblad i fjärrmapp API**

```http
PUT http://api.aspose.cloud/v4.0/cells/merge/remote-spreadsheets
```

### **Begäranparametrar:**

| Parameternamn| Typ| Sökväg/Frågesträng/HTTP-kropp| Beskrivning|
|:- |:- |:- |:- |
| mapp| Sträng| Fråga|Mappen där de sammanfogade filerna kommer att lagras.|
| fileMatchExpression| Sträng| Fråga| Uttryck för att matcha filer för sammanslagning.|
| utformat| Sträng| Fråga| Önskat utdatafilformat.|
| sammanfogaIEttSheet| Booleansk| Fråga| Anger om all data ska kombineras till ett enda kalkylblad.|
| lagringsnamn| Sträng| Fråga| (Valfritt) Namnet på den anpassade molnlagringen; standardlagring används som standard om den utelämnas.|
| utväg| Sträng| Fråga| (Valfritt) Mappsökvägen för att lagra arbetsboken; standardvärdet är null.|
|outStorageName| Sträng| Fråga| Namnet på lagringsplatsen för utdatafilen.|
| teckensnittPlats| Sträng| Fråga| Anger anpassade teckensnitt.|
| område| Sträng| Fråga| Ställer in kalkylbladsregionen.|
| lösenord| Sträng| Fråga| Lösenordet för att öppna kalkylbladsfilen.|

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

### Felkoder

- **400 Felaktig begäran**Ogiltig Apose.Cells Cloud API URI.
- **401 Obehörig**Ogiltig åtkomsttoken. Eller ogiltigt klient-ID och hemlighet.
- **404 Hittades inte**Kalkylbladsfilen är inte tillgänglig.
- **500 Serverfel**Kalkylbladet har stött på ett fel vid hämtning av beräkningsdata.

## Var ska vi använda det sammanfogade kalkylbladet i fjärrmappen API?

När du behöver sammanfoga flera datafiler kan du använda API.

## Varför ska du använda Sammanfoga kalkylblad i fjärrmappen API?

- Molnlagringsfiler behöver inte laddas ner och kan sammanfogas direkt i molnet.
- Batchsammanfoga flera kalkylbladsfiler, stöd för matchande uttryck.
- Utvecklingen kan snabbt slutföras via det befintliga SDK:t.

## Hur man använder det sammanfogade kalkylbladet i fjärrmapp API med SDK:er

### Sammanfoga kalkylblad i fjärrmapp API Specifikation

 De[Sammanfoga kalkylblad i fjärrmapp API Specifikation](https://reference.aspose.cloud/cells/#/DataProcessingController/MergeSpreadsheetsInRemoteFolder) tillhandahåller ett offentligt tillgängligt programmeringsgränssnitt som möjliggör REST-interaktioner direkt från en webbläsare.

### Använd Aspose.Cells Cloud SDK:er

Att använda SDK:t är det snabbaste sättet att utveckla, eftersom det abstraherar detaljer på låg nivå, vilket gör att du kan sammanfoga matchande kalkylbladsfiler till filer i fjärrmappar med kort kod.
 Vänligen kolla in[GitHub-arkiv](https://github.com/aspose-cells-cloud) för en komplett lista över Aspose.Cells Cloud SDK:er.

Följande kodexempel illustrerar hur man interagerar med Aspose.Cells-webbtjänster med hjälp av olika SDK:er:
{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_MergeSpreadsheetsInRemoteFolder.cs" >}}
{{< /tab >}}
{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_MergeSpreadsheetsInRemoteFolder.java" >}}
{{< /tab >}}
{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_MergeSpreadsheetsInRemoteFolder.php" >}}
{{< /tab >}}
{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_MergeSpreadsheetsInRemoteFolder.rb" >}}
{{< /tab >}}
{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_MergeSpreadsheetsInRemoteFolder.ts" >}}
{{< /tab >}}
{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_MergeSpreadsheetsInRemoteFolder.py" >}}
{{< /tab >}}
{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_MergeSpreadsheetsInRemoteFolder.pl" >}}
{{< /tab >}}
{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_MergeSpreadsheetsInRemoteFolder.go" >}}
{{< /tab >}}
{{< /tabs >}}
