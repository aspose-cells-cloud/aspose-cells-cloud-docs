---
---
title: "Aspose.Cells Cloud – Delete File API"
second_title: "Dokument"
ArticleTitle: "Aspose.Cells Cloud – Delete File API"
linktitle: "Ta bort fil"
type: docs
url: /sv/delete-file/
keywords: "Aspose Cells, Delete File API, Excel molnlagring, REST API, filhantering"
description: "Ta bort en Excel-fil från Aspose.Cells Cloud-lagring med REST-baserade Delete File API. Inkluderar endpoint, parametrar, autentisering och exempelkod."
weight: 100
---

**deleteFile**-API:et tar bort den angivna filen från molnlagringen och hjälper dig att effektivt hantera resurser och data.

## **Excel API: Ta bort fil**

### Web API

```http
DELETE https://api.aspose.cloud/v4.0/cells/storage/file/{path}
```

### **Säkerhet och autentisering**

Aspose.Cells Cloud API:er är säkra och kräver <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-tokenbaserad autentisering</a>.

```bash
-H "Authorization: Bearer {access_token}"
```

### Begärparametrar

| Parameternamn  | Typ    | Plats  | Beskrivning                                                                                      |
| :------------- | :----- | :----- | :----------------------------------------------------------------------------------------------- |
| `path`         | string | Sökväg | Den URL-kodade sökvägen till den fil som ska tas bort.                                          |
| `storageName`  | string | Fråga  | Namnet på lagringen där filen finns. Utelämna om standardlagring används.                       |
| `versionId`    | string | Fråga  | Identifikator för en specifik filversion som ska tas bort. Om utelämnas tas den senaste versionen bort. |

### Svarsbeskrivning

En lyckad begäran returnerar **HTTP 200** med en tom svarsbody. Inget JSON-innehåll returneras.

```json
{}
```

**HTTP-statuskoder**

| Kod | Betydelse             | Beskrivning                                                      |
| ---- | --------------------- | ---------------------------------------------------------------- |
| 200  | OK                    | Filter tillämpades framgångsrikt; svaret innehåller åtgärdens detaljer. |
| 400  | Felaktig begäran      | Saknade eller ogiltiga parametrar (t.ex. filtyp som inte stöds). |
| 401  | Autentisering krävs   | Ogiltig eller saknad JWT-token.                                  |
| 413  | För stor nyttolast    | Den uppladdade filen överskrider storleksgränsen.                |
| 500  | Internt serverfel     | Oväntat serverfel.                                               |

## OpenAPI-specifikation

[OpenAPI-specifikationen](https://reference.aspose.cloud/cells/#/FileController/DeleteFile) definierar ett offentligt tillgängligt programmeringsgränssnitt och låter dig utföra REST-interaktioner direkt från en webbläsare.

Du kan använda verktyget cURL för att enkelt komma åt Aspose.Cells webbtjänster. Följande exempel visar hur du gör anrop till Cloud API med cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Begäran" tabName12="Svar" >}}

{{< tab tabNum="11" >}}

```bash
curl -X DELETE "https://api.aspose.cloud/v4.0/cells/storage/file/Example.xlsx?storageName=MyStorage" \
     -H "Authorization: Bearer DIN_ACCESS_TOKEN" \
     -H "Accept: application/json"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```
{
}
```

{{< /tab >}}

{{< /tabs >}}

### Använd Aspose.Cells Cloud SDK:n

Att använda ett SDK är det bästa sättet att påskynda utvecklingen. Ett SDK hanterar detaljer på lågnivå, så att du kan fokusera på dina projekttal. Kontrollera [GitHub-förrådet](https://github.com/aspose-cells-cloud) för en komplett lista över Aspose.Cells Cloud SDK:n.

Följande kodexempel visar hur man gör anrop till Aspose.Cells webbtjänster med olika SDK:er.

---