---
title: "Aspose.Cells Trim Content API – Ta bort blanksteg och radbrytningar från Excel"
second_title: "Dokument"
linktitle: "Trim Content"
type: docs
url: /spreadsheet-trim-content/
keywords: "Aspose.Cells, Trim Content API, rensa Excel-data, ta bort blanksteg i Excel, ta bort radbrytningar, rensa kalkylbladsdata"
description: "Använd Aspose.Cells Cloud PostTrimContent API för att automatiskt rensa extra blanksteg, radbrytningar och oönskade tecken från Excel-celler. Lär dig om slutpunkten, begäranformat, exempelkod och felhantering."
weight: 100
---

## **Excel Web API: PostTrimContent**

**PostTrimContent**-API:et bearbetar och trimmar innehåll i ett angivet intervall i ett kalkylblad. Det tar bort extra blanksteg, radbrytningar och andra onödiga tecken från innehållet i markerade celler, vilket gör det användbart för att rensa inmatningsdata och säkerställa konsekvent kalkylbladsformatering.

```http
POST https://api.aspose.cloud/v3.0/cells/trimcontent
```

### **Säkerhet och autentisering**

Aspose.Cells Cloud API:er är säkra och kräver <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-tokenbaserad autentisering</a>.


### **Funktionsbeskrivning**

- **Effektivitet** – Trimmar innehåll endast inom det angivna intervallet, vilket sparar tid och resurser genom att undvika onödiga operationer på hela kalkylbladet.
- **Flexibilitet** – Låter användaren definiera exakt vilket cellintervall som ska bearbetas, vilket möjliggör anpassning till olika dataset och krav.
- **Dataskydd** – Tar bort extra blanksteg och radbrytningar, vilket hjälper till att upprätthålla konsekvent och pålitlig data för analys och rapportering.
- **Användarvänlighet** – Enkel integration med minimal konfiguration, lämplig för både utvecklare och slutanvändare.

### **Begärparametrar**

| Parameternamn      | Typ   | Plats    | Beskrivning                                                                 |
| ------------------ | ----- | -------- | --------------------------------------------------------------------------- |
| trimContentOptions | Klass | Body     | Alternativ som anger hur innehållet ska trimmas (t.ex. målintervall, trim-läge). |

### **Svar**

```json
{
    "Status" : "OK",
    "Code" : 200,
    "Filename" : "[sammanslagningsfilnamn]",
    "Filesize" : [filstorlek],
    "FileContent" : "[Base64-sträng]"
}
```

**HTTP-statuskoder**

| Kod | Betydelse                   | Beskrivning                                         |
|-----|-----------------------------|-----------------------------------------------------|
| 200 | OK                          | Filter tillämpades framgångsrikt; svaret innehåller åtgärdens detaljer. |
| 400 | Ogiltig förfrågan           | Saknas eller ogiltiga parametrar (t.ex. filtyp som inte stöds). |
| 401 | Otillåten                   | Ogiltig eller saknad JWT-token. |
| 413 | För stor nyttolast          | Den uppladdade filen överskrider storleksgränsen. |
| 500 | Internt serverfel           | Oväntat serverfel. |

## Hur man använder PostRemoveCharacters API med SDK:er

### PostRemoveCharacters API-specifikation


[OpenAPI-specifikationen](https://reference.aspose.cloud/cells/#/TextProcessingController/PostTrimContent) definierar ett offentligt tillgängligt programmeringsgränssnitt och låter dig utföra REST-interaktioner direkt från en webbläsare.

### Använd Aspose.Cells Cloud SDK:er

Att använda en SDK är det bästa sättet att påskynda utvecklingen. En SDK hanterar detaljer på lågnivå, så att du kan fokusera på dina projektuppgifter. Se [GitHub-förrådet](https://github.com/aspose-cells-cloud) för en komplett lista över Aspose.Cells Cloud SDK:er.

Följande kodexempel visar hur man anropar Aspose.Cells webbtjänster med olika SDK:er:

{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_PostTrimContent.cs" >}}
{{</ tab>}}
{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_PostTrimContent.java" >}}
{{</ tab>}}
{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_PostTrimContent.php" >}}
{{</ tab>}}
{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_PostTrimContent.rb" >}}
{{</ tab>}}
{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_PostTrimContent.ts" >}}
{{</ tab>}}
{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_PostTrimContent.py" >}}
{{</ tab>}}
{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_PostTrimContent.pl" >}}
{{</ tab>}}
{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_PostTrimContent.go" >}}
{{</ tab>}}
{{< /tabs >}}

**Senast uppdaterad: 2026-03-30**