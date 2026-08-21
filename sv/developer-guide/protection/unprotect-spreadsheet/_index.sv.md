---
title: "Aspose.Cells Cloud Excel-Web-API för att ta bort skydd – Ta programmvis bort öppnings- och ändringslösenord"
second_title: "Dokument"
ArticleTitle: "Ta bort Excel-skydd – Lås upp öppnings- och ändringslösenord omedelbart"
linktitle: "Ta bort skydd från kalkylark"
type: docs
url: /sv/unprotect-spreadsheet/
keywords: "ta bort skydd, kalkylark, Aspose.Cells, API, Excel, borttagning av lösenord"
description: "Ta bort öppnings- och ändringslösenord från Excel-filer programmässigt med Aspose.Cells Cloud API för att ta bort skydd från kalkylark. Stöder .xlsx/.xls, OAuth2-autentisering och batchbehandling."
weight: 100
---

API:et för att ta bort skydd från kalkylark tar bort både öppnings- och ändringslösenordsskydd från Excel-filer med ett enda anrop. Det är idealiskt för datapipler, dokumenthanteringssystem och migreringsarbetsflöden.

## **API för att ta bort skydd från kalkylark**

### **Webb-API**

```http
PUT https://api.aspose.cloud/v4.0/cells/unprotection/spreadsheet
```

### **Säkerhet och autentisering**

Aspose.Cells Cloud-API:er är säkra och kräver <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-token-baserad autentisering</a>.

```bash
-H "Authorization: Bearer {access_token}"
```

### **Parametrar för begäran**

| Parametername  | Typ    | Plats    | Beskrivning                                                                         |
| -------------- | ------ | -------- | ----------------------------------------------------------------------------------- |
| Spreadsheet    | Fil    | FormData | Den Excel-fil som ska avskyddas.                                                    |
| password       | Sträng | Fråga    | Lösenordet som skyddar filen mot öppning.                                           |
| modifyPassword | Sträng | Fråga    | Lösenordet som krävs för att ändra i filen (valfritt om endast ett öppningslösenord är inställt). |
| outPath        | Sträng | Fråga    | (Valfritt) Mappsökväg där det avskyddade arbetshäftet kommer att sparas.            |
| outStorageName | Sträng | Fråga    | (Valfritt) Namn på lagringsutrymmet där utdatafilen ska skrivas.                    |
| region         | Sträng | Fråga    | (Valfritt) Inställningar för kalkylarksregion.                                     |

### **Svar**

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

Ett lyckat svar returnerar den avskyddade filen som en ström. Filen kan sparas på den plats som anges av `outPath`/`outStorageName` eller hämtas direkt från svaret.

**HTTP-statuskoder**

| Kod | Betydelse             | Beskrivning                                                       |
| --- | --------------------- | ----------------------------------------------------------------- |
| 200 | OK                    | Skydd har tagits bort; svaret innehåller information om åtgärden. |
| 400 | Felaktig begäran      | Saknade eller ogiltiga parametrar (t.ex. filtyp som inte stöds).  |
| 401 | Inte auktoriserad     | Ogiltig eller saknad JWT-token.                                   |
| 413 | För stor nyttolast    | Den uppladdade filen överskrider storleksgränsen.                 |
| 500 | Internt serverfel     | Oväntat serverfel.                                                |

## När bör du använda API:et för att ta bort skydd från kalkylark?

- **Återställ åtkomst till låsta arbetshäften** – Ta snabbt bort glömda öppnings- eller ändringslösenord utan manuellt ingripande.
- **Automatisera massupplåsning** – Bearbeta stora mängder filer i data-migrerings- eller arkiveringsprojekt.
- **Integrera med befintliga arbetsflöden** – Kombinera med lagrings- eller konverterings-API:er för att skapa slut-till-slut-pipelines (t.ex. ladda upp → ta bort skydd → konvertera till PDF).
- **Upprätthåll datasäkerhet** – Åtgärden sker på serversidan, vilket håller originalfilerna säkra medan den avskyddade versionen lagras i ditt molnlagringsutrymme.

## Hur du använder API:et för att ta bort skydd från kalkylark med SDK:er

### OpenAPI-specifikation

[OpenAPI-specifikationen för API:et för att ta bort skydd från kalkylark](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Protection/ProtectSpreadsheet) tillhandahåller ett offentligt tillgängligt programmeringsgränssnitt för att underlätta direkta REST-interaktioner från en webbläsare.

Du kan använda kommandoradsverktyget cURL för enkelt att komma åt Aspose.Cells-webbtjänster. Följande exempel visar hur du gör anrop till Cloud-API:et med cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Begäran" tabName12="Svar" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/unprotection/spreadsheet?password=OldPass&modifyPassword=ModPass" \
     -H "Authorization: Bearer {access_token}" \
     -F "Spreadsheet=@myfile.xlsx"
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

Att använda ett SDK förenklar anropet genom att hantera autentisering, begäranstruktion och svarsparssning. SDK:erna finns tillgängliga för många språk och innehåller färdiga metoder för att ta bort skydd från kalkylark.

Följande kodexempel illustrerar hur du anropar API:et för att ta bort skydd från kalkylark med olika SDK:er:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_UnprotectSpreadsheet.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_UnprotectSpreadsheet.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_UnprotectSpreadsheet.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_UnprotectSpreadsheet.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_UnprotectSpreadsheet.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_UnprotectSpreadsheet.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_UnprotectSpreadsheet.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_UnprotectSpreadsheet.go" >}}
{{</tab>}}
{{< /tabs >}}