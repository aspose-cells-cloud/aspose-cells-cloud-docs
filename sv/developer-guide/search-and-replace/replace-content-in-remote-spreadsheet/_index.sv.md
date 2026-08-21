---
title: "Aspose.Cells Cloud ersätter webb-API – uppdatera text i fjärrdokument"
second_title: "Dokument"
ArticleTitle: "Massuppdatering av text i moln-Excel-filer – Find & Replace-API"
linktitle: "Ersätt innehåll i fjärrdokument"
type: docs
url: /sv/replace-content-in-remote-spreadsheet/
keywords: "Aspose.Cells Cloud, ersätt innehåll, fjärrdokument, find and replace API, moln-Excel, massuppdatering av text"
description: "Använd Aspose.Cells Cloud Find & Replace API för att massuppdatera text i fjärr-Excel-arbetsböcker. Säkert HTTPS-slutpunkt, OAuth2-autentisering och redo-användbara SDK-exempel för snabb integration."
weight: 100
---

Utför massuppdatering av text i flera Excel-filer som lagras i molnet. Hitta och uppdatera specifika textsträngar effektivt med Aspose.Cells Find & Replace API för molndokument.


## **Ersätt innehåll i fjärrdokument-API**

### **Webb-API**

```http
PUT https://api.aspose.cloud/v4.0/cells/{name}/replace/content
```

### **Säkerhet och autentisering**

Aspose.Cells Cloud-API:er är säkra och kräver <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-tokenbaserad autentisering</a>.

```bash
-H "Authorization: Bearer {access_token}"
```

### Begärningsparametrar

| Parameternamn   | Typ    | Plats  | Beskrivning                                                                                                                                              |
| --------------- | ------ | ------ | --------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **name**        | String | Path   | Namnet på arbetsbokens fil som lagras i molnlagring och ska modifieras (t.ex. `"rapport.xlsx"`).                                                          |
| **searchText**  | String | Query  | Strängen som ska hittas i hela arbetsboken. Sökningen är skiftlägeskänslig och gäller alla kalkylblad om inte begränsad av andra parametrar.               |
| **replaceText** | String | Query  | Strängen som kommer att ersätta varje förekomst av `searchText`.                                                                                         |
| **folder**      | String | Query  | Sökvägen till mappen i molnlagring som innehåller källarbetsboken (t.ex. `"/documents/quarterly/"`).                                                     |
| **storageName** | String | Query  | _(Valfritt)_ Namnet på en anpassad molnlagring (t.ex. `"MyS3Bucket"`). Om utelämnas används standardlagringen som konfigurerats för kontot.              |
| **region**      | String | Query  | _(Valfritt)_ Språkidentifierare som kan påverka teckenkodning och språkspecifik sökbeteende (t.ex. `"sv-SE"`).                                           |
| **password**    | String | Query  | _(Valfritt)_ Lösenord för att öppna en skyddad arbetsbok.                                                                                                |

### Svar

Ett typiskt lyckat svar returnerar statusen för åtgärden och antalet utförda ersättningar:

```json
{
  "Code": 200,
  "Status": "OK"
}
```

### Felkoder

- **400 Bad Request** – Ogiltig Aspose.Cells Cloud API-URI.
- **401 Unauthorized** – Saknar eller ogiltig OAuth 2.0-access_token.
- **404 Not Found** – Den angivna dokumentfilen kunde inte nås.
- **500 Server Error** – Ett oväntat serverproblem uppstod vid bearbetning av begäran.

## När ska du använda API:et för att ersätta innehåll i fjärrdokument?

- **Batch-molnfiluppdatering** – Ändra innehållet i flera Excel-filer som lagras i molnlagring såsom AWS S3 eller Azure Blob.
- **Dynamisk fyllning av molnmallar** – Fyll i rapportmallar som lagras i molnet med uppdaterad data.
- **Filsynkronisering mellan regioner** – Se till att Excel-filer är konsekventa över olika geografiska lagringsregioner.

## Varför använda API:et för att ersätta innehåll i fjärrdokument?

- **Utvecklarvänligt** – Aspose.Cells Cloud tillhandahåller SDK-bibliotek för många programmeringsspråk, vilket minskar utvecklingsinsatsen jämfört med att bygga en egen lösning.
- **Lägre arbetskostnader** – Eliminerar behovet av dedicated personal för manuell sammansättning av dokument.
- **Betala per användning** – Inget förstakostnadskrav; du betalar endast för de API-anrop du faktiskt gör.
- **Inga underhållskostnader** – Inga servrar att hantera, ingen mjukvaruuppdatering och inga kompatibilitetsproblem.
- **Bevarar all cellformatering, formler och diagram** – Åtgärden bevarar originalarbetsbokens layout och beräkningar efter textersättning.

## Hur du använder API:et för att ersätta innehåll i fjärrdokument med SDK:er

### OpenAPI-specifikation

[OpenAPI-specifikationen](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Search/ReplaceContentInRemoteRange) definierar ett offentligt tillgängligt programmeringsgränssnitt och låter dig utföra REST-interaktioner direkt från en webbläsare.

### Använd Aspose.Cells Cloud SDK:er

Att använda SDK är det bästa sättet att påskynda utvecklingen. SDK hanterar de underliggande detaljerna, så att du bara behöver implementera ersättning av innehåll i dokument med minimal kod. Kolla in [GitHub-repositoriet](https://github.com/aspose-cells-cloud) för en komplett lista över Aspose.Cells Cloud SDK:er.

Följande kodexempel visar hur du gör anrop till Aspose.Cells-webbtjänster med olika SDK:er:


---