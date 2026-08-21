---
title: "Aspose.Cells Cloud Excel-lösenordskydds webb-API – Automatisera öppnings- och ändringslösenord för kryptering"
secondtitle: "Utvecklarguide för Excel-skydd"
articletitle: "Excel-lösenordskyddverktyg – Ställ in öppnings- och ändringslösenord – Säkra dina kalkylark"
linktitle: "Säkra kalkylark"
type: docs
url: /sv/protect-spreadsheet/
keywords: "Aspose.Cells, Excel-lösenordskydd, API, öppningslösenord, ändringslösenord, molnlagring, kalkylarksäkerhet"
description: "Säkra Excel-filer programmatiskt med Aspose.Cells Cloud. Ställ in både öppnings- och ändringslösenord via ett enda API-anrop. Stödjer .xlsx, .xls och molnlagring. Testa gratis."
weight: 100
---

Automatisera Excel-lösenordskydd i stor skala med vårt utvecklar-API – tillämpa både öppnings- och ändringslösenord programmatiskt. Idealiskt för företagsworkflower och kompatibelt med .xlsx och äldre format. Få dokumentation och börja din gratis integration idag.

## **API för kalkylarksskydd**

### **Webb-API**

```http
PUT https://api.aspose.cloud/v4.0/cells/protection/spreadsheet
```

### **Säkerhet och autentisering**

Aspose.Cells Cloud API:er är säkra och kräver <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-tokenbaserad autentisering</a>.

```bash
-H "Authorization: Bearer {access_token}"
```

### **Parametrar för begäran:**

| Parameternamn     | Typ    | Sökväg/Frågesträng/HTTPBody | Beskrivning                                                                                                                                  |
| :---------------- | :----- | :-------------------------- | :------------------------------------------------------------------------------------------------------------------------------------------- |
| Spreadsheet       | Fil    | FormData                    | Excel-kalkylarkfilen som ska laddas upp och skyddas med lösenordskryptering.                                                                |
| openPassword      | Sträng | Frågesträng                 | Lösenordet som krävs för att öppna (dekryptera) det skyddade kalkylarket.                                                                   |
| modifyPassword    | Sträng | Frågesträng                 | Lösenordet som krävs för att aktivera redigering eller ändring av kalkylarkets innehåll.                                                   |
| outPath           | Sträng | Frågesträng                 | (Valfritt) Anger utdatamappens sökväg där det skyddade arbetsboken sparas. Om den inte anges returneras filen i svaret.                     |
| outStorageName    | Sträng | Frågesträng                 | Namnet på molnlagringen som används för att lagra den skyddade utdatafilen.                                                                 |
| region            | Sträng | Frågesträng                 | Anger regionala/kulturella inställningar (t.ex. datumformat, nummerformatering) som tillämpas på kalkylarket under bearbetning.            |

**Autentisering**  
Alla anrop till API:et för kalkylarksskydd kräver en giltig OAuth 2.0-access-token. Inkludera token i `Authorization`-headern:

```http
Authorization: Bearer {access_token}
```

Token måste erhållas från Aspose Cloud:s autentiseringsslutpunkt och måste inkludera **Cells**-omfattningen.

## **Svar**

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

**HTTP-statuskoder**

| Kod | Betydelse             | Beskrivning                                                       |
| --- | --------------------- | ----------------------------------------------------------------- |
| 200 | OK                    | Filter tillämpades framgångsrikt; svaret innehåller åtgärdens detaljer. |
| 400 | Felaktig begäran      | Saknade eller ogiltiga parametrar (t.ex. filtyp som inte stöds). |
| 401 | Obehörig              | Ogiltig eller saknad JWT-token.                                   |
| 413 | För stor nyttolast    | Den uppladdade filen överskrider storleksgränsen.                 |
| 500 | Internt serverfel     | Oväntat serverfel.                                                |

## Var bör vi använda API:et för kalkylarksskydd?

- **Säkra känslig finansiell data** – Skydda Excel-filer som innehåller budgetar, fakturor eller löneinformation med öppnings- och ändringslösenord för att förhindra obehörig åtkomst eller redigering.
- **Dela konfidentiella rapporter på ett säkert sätt** – Se till att endast auktoriserade mottagare kan se eller ändra affärs-, revisions- eller efterlevnadsrapporter vid distribution internt eller externt.
- **Automatisera dokument säkerhet i workflower** – Integrera API:et i företagssystem (t.ex. ERP, CRM) för att automatiskt lösenordskydda genererade kalkylark före lagring eller e-postleverans.
- **Tvinga fram skrivskyddad åtkomst** – Tillåt användare att öppna rapporter för visning medan ändringar begränsas genom att använda ett separat ändringslösenord – idealiskt för mallar eller färdiga dataset.
- **Uppfylla regleringskrav** – Hjälpa till att uppfylla GDPR, HIPAA eller SOX-krav genom att kryptera känslig kalkylarksdata i vila och i transit via automatiskt skydd.

## Varför bör du använda API:et för kalkylarksskydd?

- **Utvecklarvänligt** – Aspose.Cells Cloud erbjuder SDK-bibliotek i flera språk, vilket möjliggör snabb utveckling, och levereras med omfattande dokumentation. Jämfört med att bygga egna lösningar minskas utvecklingsarbetet avsevärt.
- **Minskar behovet av personal** – Automatiserar dokumentkonsolidering och säkerhet, vilket minskar behovet av dedikerad personal.
- **Betala per användning** – Inga förvalskostnader; du betalar endast för de API-anrop du faktiskt använder.
- **Inga underhållskostnader** – Inga servrar att underhålla, ingen mjukvaruuppdatering och inga kompatibilitetsproblem.
- **Bevarar all original Excel-formatering** vid tillämpning av lösenordskydd, vilket säkerställer att det skyddade arbetsboken ser exakt ut som källfilen.

## Hur man använder API:et för kalkylarksskydd med SDK:er

### OpenAPI-specifikation

[API-specifikation för kalkylarksskydd](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Protection/ProtectSpreadsheet) tillhandahåller ett offentligt tillgängligt programmeringsgränssnitt för att underlätta direkt REST-interaktion från en webbläsare.

Du kan använda kommandoradsverktyget cURL för enkelt att komma åt Aspose.Cells-webbtjänster. Följande exempel visar hur man gör anrop till moln-API:et med cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Begäran" tabName12="Svar" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/protection/spreadsheet?openPassword=MyOpenPwd&modifyPassword=MyModifyPwd" \
     -H "Authorization: Bearer {access_token}" \
     -F "Spreadsheet=@/path/to/workbook.xlsx"
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

Att använda SDK är det bästa sättet att påskynda utvecklingen. SDK:en hanterar underliggande detaljer, så att du enkelt kan implementera kalkylarksSkyddsfunktion med minimal kod. Kolla in <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub-förrådet</a> för en komplett lista över Aspose.Cells Cloud SDK:er.

Följande kodexempel illustrerar hur man interagerar med Aspose.Cells-webbtjänster med olika SDK:er:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_ProtectSpreadsheet.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_ProtectSpreadsheet.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_ProtectSpreadsheet.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_ProtectSpreadsheet.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_ProtectSpreadsheet.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_ProtectSpreadsheet.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_ProtectSpreadsheet.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_ProtectSpreadsheet.go" >}}
{{</tab>}}
{{< /tabs >}}
---