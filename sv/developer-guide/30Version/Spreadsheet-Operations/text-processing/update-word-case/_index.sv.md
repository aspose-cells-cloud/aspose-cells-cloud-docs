---
title: "Aspose.Cells – API för att uppdatera textstil"
second_title: "Dokument"
linktype: "Textstil"
type: docs
url: /sv/post-update-word-case/
keywords: "Aspose.Cells, API för att uppdatera textstil, konvertering av textstil, Excel, CSV, Google Sheets, REST API"
description: "Konvertera textstil i Excel-, CSV- eller Google Sheets-filer med Aspose.Cells Cloud:s API för att uppdatera textstil. Stöder versaler, gemener, versalstart i varje ord och versalisering av första bokstaven."
weight: 100
ArticleTitle: "Aspose.Cells – Dokumentation för API för att uppdatera textstil"
---

**API-version:** 3.0

Att hantera inkonsekvent textstil i kalkylblad (Excel, Google Sheets, CSV) kan vara irriterande, särskilt med stora dataset. **PostUpdateWordCase-webb-API:t** automatiserar konvertering av textstil och säkerställer rent och standardiserat data med minimal insats.


## **Excel-webb-API – API för att uppdatera textstil**

```http
POST https://api.aspose.cloud/v3.0/cells/updatewordcase
```
### **Säkerhet och autentisering**

Aspose.Cells Cloud-API:er är säkra och kräver <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-tokenbaserad autentisering</a>.

### **Funktionsbeskrivning**

PostUpdateWordCase-webb-API:et löser det vanliga problemet med inkonsekvent textstil i kalkylblad, vilket kan påverka dataanalys och bearbetning avsevärt. Detta API automatiserar konvertering av textstil så att dina data blir rena, standardiserade och redo för vidare bearbetning eller analys.

- **Automatiserad konvertering av textstil**
  - **Versaler till gemener** – Konvertera alla versaler till gemener.
  - **Gemener till versaler** – Konvertera alla gemener till versaler.
  - **Versalisera första bokstaven** – Versalisera första bokstaven i varje ord.
  - **Titelstil (Title Case)** – Konvertera text till titelstil, där första bokstaven i varje viktigt ord versaliseras.

- **Stöd för flera format** – API:t fungerar med ett brett utbud av kalkylbladsformat, inklusive Excel, OpenOffice, JSON, CSV och andra. Denna mångsidighet gör det lämpligt för diverse datahanteringsbehov.

### **Begärandeparametrar**

| Parameternamn      | Typ    | Plats          | Beskrivning                                                                                                                |
| ------------------ | ------ | -------------- | -------------------------------------------------------------------------------------------------------------------------- |
| `wordCaseOptions`  | objekt | Begärandetext  | Alternativ som definierar önskad textstilstransformation, t.ex. källomfång, måltextstil och ytterligare inställningar.   |

**Schemat för `wordCaseOptions`**

```json
{
  "Range": "A1:B10", // Omfång i Excel-stil som ska bearbetas (obligatoriskt)
  "CaseType": "Upper", // Enum: Upper, Lower, Capitalize, Title (obligatoriskt)
  "IgnoreBlank": true // Booleskt värde, valfritt – när true lämnas tomma celler oförändrade
}
```

**Exempel på begärandetext**

```json
{
  "Range": "A1:B10",
  "CaseType": "Upper",
  "IgnoreBlank": true
}
```

- **Range** – Cellomfång som textstilsomvandlingen ska tillämpas på (t.ex. `A1:C5`).
- **CaseType** – Typ av textstilsomvandling. Tillåtna värden är `Upper`, `Lower`, `Capitalize` och `Title`.
- **IgnoreBlank** – Om `true` ignoreras tomma celler; standardvärdet är `false`.

### **Svar**

```json
{
    "Status" : "OK",
    "Code" : 200,
    "Filename" : "[sammanfogat filnamn]",
    "Filesize" : [filstorlek],
    "FileContent" : "[Base64-sträng]"
}
```

- **Filename** – Namn på den bearbetade filen.
- **FileSize** – Storlek på filen i byte.
- **FileContent** – Base64-kodat innehåll i den omvandlade filen.

**HTTP-statuskoder**

| Kod | Betydelse                   | Beskrivning                                     |
|-----|-----------------------------|-------------------------------------------------|
| 200 | OK                          | Filter applicerades framgångsrikt; svaret innehåller åtgärdsdetaljer. |
| 400 | Felaktig begäran            | Saknade eller ogiltiga parametrar (t.ex. filtyp som inte stöds). |
| 401 | Oautentiserad               | Ogiltig eller saknad JWT-token. |
| 413 | För stor nyttolast          | Den uppladdade filen överskrider storleksgränsen. |
| 500 | Internt serverfel           | Oväntat serverfel. |

## Hur man använder PostUpdateWordCase-API:t med SDK:er

### PostUpdateWordCase-API-specifikation

<a href="https://reference.aspose.cloud/cells/#/TextProcessingController/PostUpdateWordCase" target="_blank" rel="noopener noreferrer">OpenAPI-specifikationen</a> definierar ett offentligt tillgängligt programmeringsgränssnitt och gör det möjligt att utföra REST-interaktioner direkt från en webbläsare.

### Använd Aspose.Cells Cloud SDK:er

Att använda en SDK är det bästa sättet att snabba upp utvecklingen. En SDK hanterar detaljer på låg nivå och låter dig fokusera på dina projektoppgifter. Se <a href="https://github.com/aspose-cells-cloud" target="_blank" rel="noopener noreferrer">GitHub-förrådet</a> för en komplett lista över Aspose.Cells Cloud SDK:er.

Följande kodexempel visar hur man anropar Aspose.Cells-webbtjänster med olika SDK:er:

{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_PostUpdateWordCase.cs" >}}
{{</ tab>}}
{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_PostUpdateWordCase.java" >}}
{{</ tab>}}
{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_PostUpdateWordCase.php" >}}
{{</ tab>}}
{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_PostUpdateWordCase.rb" >}}
{{</ tab>}}
{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_PostUpdateWordCase.ts" >}}
{{</ tab>}}
{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_PostUpdateWordCase.py" >}}
{{</ tab>}}
{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_PostUpdateWordCase.pl" >}}
{{</ tab>}}
{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_PostUpdateWordCase.go" >}}
{{</ tab>}}
{{</ tabs >}}
---