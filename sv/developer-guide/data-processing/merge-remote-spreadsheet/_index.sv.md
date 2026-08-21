---
title: "Aspose.Cells Cloud – Sammanfoga Excel-filer i molnet | Kombinera kalkylblad via API"
second_title: "Aspose.Cells Cloud"
ArticleTitle: "Sammanfoga Excel-filer i molnet – Kombinera kalkylblad online med Aspose.Cells Cloud API"
linktitle: "Sammanfoga fjärrkalkylblad"
type: docs
url: /merge-remote-spreadsheet/
keywords: "Aspose.Cells, sammanfoga Excel, moln-API, kombinera kalkylblad"
description: "Sammanfoga Excel-arbetsböcker lagrade i molnlagring med Aspose.Cells Cloud API. Angiv utdataformat, målmapp och sammanfogningsläge i ett enda HTTPS-anrop."
weight: 100
---

Sammanfoga snabbt Excel-filer som lagras i molnet med andra kalkylblad med Aspose.Cells Cloud API, och ange utdataformatet och lagringsplatsen.

## API för sammanfogning av fjärrkalkylblad

Innan du anropar den här åtgärden, se till att du har:

- En giltig **JWT-åtkomsttoken** (se autentiseringshandboken).
- Källarbetsboken och alla filer som ska sammanfogas uppladdade till din molnlagring.
- Lämpliga behörigheter för att läsa från källmappen och skriva till målmappen.

### Webb-API

```http
PUT https://api.aspose.cloud/v4.0/cells/{name}/merge/spreadsheet
```

### **Säkerhet och autentisering**

Aspose.Cells Cloud-API:en är säkra och kräver <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-tokenbaserad autentisering</a>.

### Begärparametrar:

| Parameternamn     | Typ     | Sökväg/Frågesträng/HTTPBody | Beskrivning                                                                                                                        |
| :---------------- | :------ | :------------------------- | :--------------------------------------------------------------------------------------------------------------------------------- |
| name              | String  | Sökväg                     | Namnet på källarbetsbokens fil som ska sammanfogas.                                                                                |
| mergedSpreadsheet | String  | Frågesträng                | En kommseparerad lista med filnamn på kalkylblad som ska sammanfogas i källarbetsboken.                                            |
| folder            | String  | Frågesträng                | Mappsökvägen i molnlagring som innehåller källarbetsboken.                                                                         |
| outFormat         | String  | Frågesträng                | Önskat format för den sammanfogade utdatafilen (t.ex. `XLSX`, `PDF`, `CSV`).                                                       |
| mergeInOneSheet   | Boolean | Frågesträng                | Ställ in till `true` för att sammanfoga all källdata till ett enda kalkylblad; `false` skapar separata kalkylblad för varje fil. |
| storageName       | String  | Frågesträng                | _(Valfritt)_ Namnet på molnlagringen där källarbetsboken finns. Om utelämnas används standardlagring.                              |
| outPath           | String  | Frågesträng                | _(Valfritt)_ Mappsökvägen i molnlagringen för att spara den sammanfogade filen. Om utelämnas sparas filen i källmappen.             |
| outStorageName    | String  | Frågesträng                | Namnet på molnlagringen för att spara utdatafilen.                                                                                 |
| fontsLocation     | String  | Frågesträng                | _(Valfritt)_ Anpassad mappsökväg för typsnittsfiler som används vid konvertering till bild/PDF-format.                             |
| region            | String  | Frågesträng                | _(Valfritt)_ Lokal/region för datum-, nummer- och valutainställningar i utdatafilen (t.ex. `sv-SE`, `en-US`, `de-DE`).            |
| password          | String  | Frågesträng                | _(Valfritt)_ Lösenord som krävs för att öppna källarbetsboken om den är skyddad.                                                   |

### Svar

**Status:** `200 OK`

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

Filen kan laddas ner direkt eller sparas på den plats som anges av `outPath`.

**Detaljer för lyckat svar**

| Statuskod | Content-Type               | Beskrivning                               |
| --------- | -------------------------- | ----------------------------------------- |
| 200 OK    | `application/octet-stream` | Binär ström för den sammanfogade arbetsboksfilen. |

**HTTP-statuskoder**

| Kod | Betydelse             | Beskrivning                                                       |
| --- | --------------------- | ----------------------------------------------------------------- |
| 200 | OK                    | Filter applicerades framgångsrikt; svaret innehåller åtgärdens detaljer. |
| 400 | Felaktig förfrågan    | Saknade eller ogiltiga parametrar (t.ex. filtyp som inte stöds).  |
| 401 | Obehörig              | Ogiltig eller saknad JWT-token.                                   |
| 413 | För stor nyttolast    | Den uppladdade filen överskrider storleksgränsen.                 |
| 500 | Internt serverfel     | Oväntat serverfel.                                                |

## Var bör vi använda API:et för sammanfogning av fjärrkalkylblad?

### Dataintegration på enterprise-nivå

- **Konsolidering av rapporter från flera avdelningar** – Sammanfoga separata Excel-rapporter som lämnats in av sälj-, marknadsförings-, finans- och andra team.
- **Sammanfattning av filialdata** – Sammanfatta prestandadata från varje filial globalt.
- **Konsolidering av partnerdata** – Sammanfoga datainlämningar från flera partners till en enda arbetsbok.

### Molndokumentbearbetningsarbetsflöde

- **Molnlagringsfilbearbetning** – Sammanfoga Excel-filer som lagras direkt i AWS S3, Azure Blob eller Google Cloud Storage.
- **Datakonsolidering från flera källor** – Kombinera filer från olika molnplattformar till en enda arbetsbok.
- **Automatiserade datapipelines** – Integrera API:et i ETL-processer för att automatisera filsammanfogning.

### Dokumenthanteringsautomatisering

- **Konsolidering av versioner** – Sammanfoga olika versioner av ett projektplan- eller budgetarbetsbok.
- **Fylla i mallar med data** – Infoga datafiler i standardiserade rapportmallar.
- **Regelbunden rapportgenerering** – Automatisera veckovisa, månatliga och kvartalsvisa sammanfattningsrapporter.

### Plattformöverskridande samarbete

- **Samarbete med distansteam** – Sammanfoga arbete som lämnats in av spridda teammedlemmar.
- **Kunddatadispositionering** – Sammanfoga order- eller feedbackdata från flera kunder.
- **Sammanfattning av leverantörsinformation** – Kombinera offert- eller produktinformation från flera leverantörer.

## Varför bör du använda API:et för sammanfogning av fjärrkalkylblad?

- **Utvecklarvänlig** – Aspose.Cells Cloud tillhandahåller SDK:er för många språk, vilket minskar utvecklingstiden och erbjuder omfattande dokumentation. Jämfört med att bygga en egen lösning minskas arbetsmängden betydligt.
- **Lägre arbetskostnad** – Minskar behovet av personal som är tilldelad manuell dokumentkonsolidering.
- **Betala per användning** – Ingen förstainvestering; du betalar endast för de API-anrop du faktiskt använder.
- **Inga underhållskostnader** – Inga servrar att underhålla, ingen programvaruuppdatering och inga kompatibilitetsproblem.

## Hur man använder API:et för sammanfogning av fjärrkalkylblad med SDK:er

### API-specifikation för sammanfogning av fjärrkalkylblad

<a href="https://reference.aspose.cloud/cells/#/DataProcessingController/MergeRemoteSpreadsheet" target="_blank" rel="noopener noreferrer">API-specifikationen för sammanfogning av fjärrkalkylblad</a> beskriver REST-gränssnittet som kan anropas direkt från valfri HTTP-klient.

Du kan använda verktyget cURL för att enkelt komma åt Aspose.Cells-webbtjänster. Följande exempel visar hur man gör anrop till Cloud-API:et med cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Förfrågan" tabName12="Svar" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/MyWorkbook.xlsx/merge/spreadsheet?mergedSpreadsheet=Report1.xlsx&outFormat=XLSX&mergeInOneSheet=true" \
  -H "Authorization: Bearer {access_token}"
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

Att använda en SDK är det snabbaste sättet att utveckla, eftersom den abstraher bort detaljer på lägre nivå och låter dig sammanfoga ett kalkylblad till ett annat med en kort kodsnutt.  
Se <a href="https://github.com/aspose-cells-cloud" target="_blank" rel="noopener noreferrer">GitHub-förrådet</a> för en komplett lista över Aspose.Cells Cloud SDK:er.

Följande kodexempel visar hur man interagerar med Aspose.Cells-webbtjänster med olika SDK:er:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_MergeRemoteSpreadsheet.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_MergeRemoteSpreadsheet.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_MergeRemoteSpreadsheet.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_MergeRemoteSpreadsheet.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_MergeRemoteSpreadsheet.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_MergeRemoteSpreadsheet.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_MergeRemoteSpreadsheet.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_MergeRemoteSpreadsheet.go" >}}
{{</tab>}}
{{< /tabs >}}