---
title: "Aspose.Cells Cloud ersätter Web API – uppdatera text i fjärrkalkylark"
secondtitle: "Dokument"
ArticleTitle: "Sök och ersätt text i fjärrkalkylark med Aspose.Cells Cloud API"
linktitle: "Ersätt innehåll i fjärrkalkylark"
type: docs
url: /replace-content-in-remote-worksheet/
keywords: "Aspose.Cells, ersätt text, fjärrkalkylark, Excel-API, molnarkalkylark, sök och ersätt, REST API"
description: "Ersätt text i ett specifikt kalkylark i en Excel-fil som lagras i Aspose Cloud. Stöder lösenordsskyddade arbetsböcker, regionskänslig sökning och massuppdateringar."
weight: 100
---

Ersätt angiven text i ett specifikt kalkylark i fjärr-Excel-filer. Uppdatera innehåll i målgrupperade kalkylarksblad effektivt med Aspose.Cells:s API för sökning och ersättning för exakt redigering av kalkylark.

## **Ersätt innehåll i fjärrkalkylark API**

### **Webb-API**

```http
PUT https://api.aspose.cloud/v4.0/cells/{name}/worksheets/{worksheet}/replace/content
```

### **Säkerhet och autentisering**

Aspose.Cells Cloud API:er är säkra och kräver <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-tokenbaserad autentisering</a>.

```bash
-H "Authorization: Bearer {access_token}"
```

### **Begäran parametrar**

| Parameternamn | Typ   | Sökväg/Frågesträng/HTTPBody | Beskrivning                                                                                                                                                                     |
| :------------ | :---- | :-------------------------- | :------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| name          | String | Sökväg                      | Namnet på arbetsboksfilen som är lagrad i molnlagringen och ska ändras (t.ex. `"sales_report.xlsx"`, `"budget_2024.xls"`).                                                    |
| worksheet     | String | Sökväg                      | Namnet på det specifika kalkylarksblad där sök-och-ersätt-åtgärden ska utföras (t.ex. `"Q1_Sales"`, `"Sheet1"`).                                                              |
| searchText    | String | Frågesträng                 | Den textsträng som ska sökas efter i det angivna kalkylarksbladet. Sökningen gäller alla celler i kalkylarksbladet om inte ytterligare begränsas.                             |
| replaceText   | String | Frågesträng                 | Den textsträng som kommer att ersätta alla förekomster av `searchText` som hittas i det angivna kalkylarksbladet.                                                               |
| folder        | String | Frågesträng                 | Sökvägen till mappen i molnlagringen där källarbetsboken finns (t.ex. `"/reports/monthly/"`, `"/finance/"`).                                                                  |
| storageName   | String | Frågesträng                 | _(Valfritt)_ Namnet på den anpassade molnlagringen (t.ex. `"CorporateS3"`, `"AzureArchive"`). Om utelämnas används standardmolnlagringen för ditt konto.                         |
| region        | String | Frågesträng                 | _(Valfritt)_ Anger lokal för texthantering, vilket kan påverka teckenkodning och språkspecifik sökbeteende i kalkylarksbladet (t.ex. `"en-GB"`, `"es-ES"`).                     |
| password      | String | Frågesträng                 | _(Valfritt)_ Om arbetsboken är lösenordsskyddad, ange lösenordet för att öppna och ändra filen.                                                                                 |

**Exempel på begäran (cURL)**  

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/sales_report.xlsx/worksheets/Sheet1/replace/content?searchText=OldValue&replaceText=NewValue&folder=/reports" \
     -H "Authorization: Bearer {access_token}"
```

### **Svar**

```json
{
  "Code": 200,
  "Status": "OK"
}
```

### **Felkoder**

| Kod | Beskrivning                       | När det inträffar                                                 |
|-----|-----------------------------------|-------------------------------------------------------------------|
| 400 | Felaktig begäran (Bad Request)    | Begäran-URI:n är felaktig eller obligatoriska parametrar saknas. |
| 401 | Inte auktoriserad (Unauthorized)  | Åtkomsttoken saknas, är ogiltig eller klientuppgifterna är felaktiga. |
| 404 | Hittades inte (Not Found)         | Det angivna arbetsboken eller kalkylarksbladet kunde inte hittas. |
| 500 | Internt serverfel (Internal Server Error) | Ett oväntat fel inträffade vid bearbetning av begäran.         |

## Var bör vi använda API:et för att ersätta innehåll i kalkylark i fjärrkalkylark?

- **Batch-uppdatering av molnfiler**: Ändra innehållet i flera Excel-filer som är lagrade i molnlagringar som AWS S3 och Azure Blob.
- **Dynamisk ifyllnad av molnmallar**: Batch-fyll i dynamiskt data i rapportmallar som lagras i molnet.
- **Filsynkronisering över regioner**: Synkronisera innehållskonsistensen i Excel-filer i molnlagring över olika geografiska regioner.

## Varför bör du använda API:et för att ersätta innehåll i kalkylark i fjärrkalkylark?

- **Utvecklarvänlig**: Aspose.Cells Cloud erbjuder SDK-bibliotek i flera språk, vilket möjliggör snabb utveckling och kommer med omfattande dokumentation. Jämfört med att bygga egna lösningar för diagramgenerering minskas utvecklingsarbetet markant.
- **Lägre arbetskostnad**: Minskar behovet av personal som är dedikerad till dokumentkonsolidering.
- **Betala per användning**: Inget förstakostnadskrav; du betalar endast för de API-anrop som faktiskt används.
- **Inga underhållskostnader**: Ingen behov av att underhålla servrar, uppdatera programvara eller hantera kompatibilitetsproblem.

## Hur använder man API:et för att ersätta innehåll i kalkylark i fjärrkalkylark med SDK:er

### OpenAPI-specifikation

[OpenAPI-specifikationen](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Search/ReplaceContentInRemoteRange) definierar ett offentligt tillgängligt programmeringsgränssnitt och gör det möjligt att utföra REST-interaktioner direkt från en webbläsare.

### Använd Aspose.Cells Cloud SDK:er

Att använda SDK är det bästa sättet att påskynda utvecklingen. SDK hanterar underliggande detaljer, så att du enkelt kan implementera ersättning av kalkylarksinnehåll i Excel-filer med minimal kod.  
Kontrollera [GitHub-förrådet](https://github.com/aspose-cells-cloud) för en fullständig lista över Aspose.Cells Cloud SDK:er.

Följande kodexempel illustrerar hur du interagerar med Aspose.Cells-webbtjänster med olika SDK:er:  
---