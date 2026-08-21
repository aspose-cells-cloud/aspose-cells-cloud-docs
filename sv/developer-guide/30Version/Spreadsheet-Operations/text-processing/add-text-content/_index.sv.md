---
title: "Lägg till text i Excel: Infoga data effektivt med Spreadsheet Web API"
second_title: "Dokument"
linktitle: "Lägg till text"
type: docs
url: /sv/excel-add-text/
keywords: "Excel, Aspose.Cells, Lägg till text, Spreadsheet API, REST API, Office Cloud, Textinfogning, Excel API"
description: "Lägger till text i en angiven plats i ett Excel-kalkylark via Aspose.Cells Cloud API."
weight: 100
---

Lägger till textinnehåll i en angiven plats i ett kalkylark. Det kräver ett objekt som definierar den text som ska läggas till och infogningsplatsen.

## **Excel API: PostAddTextContent**

```
POST http://api.aspose.cloud/v3.0/cells/addtext
```

### **Säkerhet och autentisering**

Aspose.Cells Cloud API:er är säkra och kräver <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-tokenbaserad autentisering</a>.


### **Funktionsbeskrivning**

Denna metod säkert lägger till ny text till angivna celler och stöder flera infogningslägen samt hantering av format.

- **Lägg till text i början av valda celler**  
  Lägger till text i början av alla valda celler och säkerställer konsekvens i din datainmatning. Idealisk för att lägga till vanliga identifierare eller etiketter såsom produktkoder, kategorier eller prefix.

- **Infoga tecken före eller efter specifik text**  
  Placerar tecken före eller efter måltexten i de valda cellerna, vilket gör det enkelt att skapa strukturerat och organiserat innehåll.

- **Lägg till samma text i slutet av varje vald cell**  
  Lägger till identisk text i slutet av flera celler i en enda åtgärd, vilket förenklar datainmatning och garanterar en enhetlig utseendemässig profil.

- **Infoga text före eller efter ett angivet antal tecken**  
  Infogar text efter ett definierat antal tecken från början eller slutet av varje cell i målintervallet. Vanliga användningsfall inkluderar formatering av koder, tidsstämplar eller anpassade avgränsare.

### **Begäran parameter**

| Parameter Name   | Typ   | Plats | Beskrivning                                                                 |
| ---------------- | ----- | ----- | --------------------------------------------------------------------------- |
| addTextOptions   | Klass | Body  | Anger textinnehållet och positionen där texten ska läggas till.            |

### **Svar**

```json
{
  "Filename": "xxxxxx.pdf",
  "FileSize": xxxx,
  "FileContent": "File Content: base64_encoded_string"
}
```

**HTTP-statuskoder**

| Kod | Betydelse                   | Beskrivning                                             |
|-----|-----------------------------|---------------------------------------------------------|
| 200 | OK                          | Filtret tillämpades framgångsrikt; svaret innehåller åtgärdens detaljer. |
| 400 | Felaktig begäran            | Saknade eller ogiltiga parametrar (t.ex. filtyp som inte stöds). |
| 401 | Autentisering krävs         | Ogiltig eller saknad JWT-token. |
| 413 | Begäran är för stor         | Den uppladdade filen överskrider storleksgränsen. |
| 500 | Internt serverfel           | Oväntat serverfel. |

## Hur man använder PostAddTextContent API med SDK:er

### PostAddTextContent API-specificering

[OpenAPI-specificeringen](https://reference.aspose.cloud/cells/#/TextProcessingController/PostAddTextContent) definierar ett offentligt tillgängligt programmeringsgränssnitt och låter dig utföra REST-interaktioner direkt från en webbläsare.

### Använd Aspose.Cells Cloud SDK:er

Att använda en SDK är det mest effektiva sättet att påskynda utvecklingen. En SDK hanterar detaljer på låg nivå så att du kan fokusera på dina projektuppgifter. Se [GitHub-förrådet](https://github.com/aspose-cells-cloud) för en komplett lista över Aspose.Cells Cloud SDK:er.

Följande kodexempel visar hur man anropar Aspose.Cells webbtjänster med olika SDK:er:

{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_PostAddTextContent.cs" >}}
{{</ tab>}}
{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_PostAddTextContent.java" >}}
{{</ tab>}}
{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_PostAddTextContent.php" >}}
{{</ tab>}}
{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_PostAddTextContent.rb" >}}
{{</ tab>}}
{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_PostAddTextContent.ts" >}}
{{</ tab>}}
{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_PostAddTextContent.py" >}}
{{</ tab>}}
{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_PostAddTextContent.pl" >}}
{{</ tab>}}
{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_PostAddTextContent.go" >}}
{{</ tab>}}
{{< /tabs >}}