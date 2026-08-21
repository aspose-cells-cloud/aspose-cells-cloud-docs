---
title: "Aspose.Cells Cloud File Copy API – Ett gränssnitt för snabb kopiering och batchåtgärder av Excel-filer i molnet"
second_title: "Dokument"
ArticleTitle: "Excel-filhantering i molnet – Detaljerad förklaring av Aspose.Cells Copy File API:s batchkopieringsfunktion"
linktitle: "Kopiera fil"
type: docs
url: /copy-file/
keywords: "Aspose.Cells, CopyFile API, kopiera Excel-fil, molnlagring, REST API"
description: "Lär dig hur du använder Aspose.Cells Cloud CopyFile API för att effektivt duplicera Excel-filer och hantera dem mellan olika lagringsplatser."
weight: 100
---

**copyFile**-API:t tillåter användare att duplicera en Excel-fil från en angiven källsökväg till en målsökväg, med stöd för olika lagringsalternativ.

## **Excel API: Kopiera fil**

### Web API

```http
PUT https://api.aspose.cloud/v4.0/cells/storage/file/copy/{srcPath}
```

### **Säkerhet och autentisering**

Aspose.Cells Cloud API:er är säkra och kräver <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-tokenbaserad autentisering</a>.

### Begärandeparametrarna för **copyFile**-API:t är

| Parameternamn    | Typ    | Path/Query String/HTTPBody | Beskrivning                                      |
| ---------------- | ------ | -------------------------- | ------------------------------------------------ |
| srcPath          | String | Path                       | Källsökvägen för filen som ska kopieras.         |
| destPath         | String | Query                      | Målsökvägen där filen ska sparas.                |
| srcStorageName   | String | Query                      | Namnet på källlagringen.                         |
| destStorageName  | String | Query                      | Namnet på mållagringen.                          |
| versionId        | String | Query                      | Valfritt versions-ID för filen som ska kopieras. |

### **Svar**

Åtgärden returnerar ingen innehållsdata vid lyckad körning. Typiska HTTP-statuskoder är:

**HTTP-statuskoder**

| Kod | Betydelse             | Beskrivning                                                         |
| --- | --------------------- | ------------------------------------------------------------------- |
| 200 | OK                    | Filtrering lyckades; svaret innehåller åtgärdsinformation.         |
| 400 | Bad Request           | Saknade eller ogiltiga parametrar (t.ex. filtyp som inte stöds).   |
| 401 | Unauthorized          | Ogiltig eller saknad JWT-token.                                    |
| 413 | Payload Too Large     | Den uppladdade filen överskrider storleksgränsen.                  |
| 500 | Internal Server Error | Oväntat serverfel.                                                 |

## Hur används Copy File API med SDK:er?

### API-specificering för Copy File

[API-specificeringen för Copy File](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/File/CopyFile) tillhandahåller ett offentligt tillgängligt programmeringsgränssnitt för att utföra REST-interaktioner direkt från en webbläsare.

Du kan använda verktyget cURL för att enkelt komma åt Aspose.Cells webbtjänster. Följande exempel visar hur man gör anrop till moln-API:t med cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Begäran" tabName12="Svar" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/storage/file/copy/MyFolder/Source.xlsx?destPath=MyFolder/Dest.xlsx&srcStorageName=MyStorage&destStorageName=MyStorage" \
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

### Använd Aspose.Cells Cloud SDK:er

Att använda SDK är det snabbaste sättet att utveckla, eftersom den abstraher bort detaljer på låg nivå och låter dig konvertera kalkylbladstabelldata till en bild med minimal kod. Ta en titt på [GitHub-förrådet](https://github.com/aspose-cells-cloud) för en komplett lista över Aspose.Cells Cloud SDK:er.

Följande kodexempel visar hur man anropar Aspose.Cells webbtjänster med olika SDK:er:

---