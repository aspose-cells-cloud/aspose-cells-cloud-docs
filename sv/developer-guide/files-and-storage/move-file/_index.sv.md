---
title: "Aspose.Cells Cloud Move File API – Gränssnitt för snabb filflytt i molnet"
second_title: "Dokument"
ArticleTitle: "Effektiv molnbaserad Excel-filhanteringslösning – Gränssnitt för snabb filflytt i molnet"
linktitle: "Flytta fil"
type: docs
url: /sv/move-file/
keywords: "Aspose.Cells, Move File API, Molnlagring, Excel API, Filhantering"
description: "Hur man flyttar filer mellan mappar i Aspose.Cells Cloud-lagring med v4.0:s Move File API – slutpunkt, parametrar, exempel och SDK-länkar."
weight: 100
---

**moveFile**-API:et flyttar en fil från en plats till en annan inom Aspose.Cells Cloud-lagring. Det hjälper dig att organisera filer och hantera lagring effektivt.

## **Excel API: Flytta fil**

### Webb-API

```bash
PUT https://api.aspose.cloud/v4.0/cells/storage/file/move/{srcPath}
```

### **Säkerhet och autentisering**

Aspose.Cells Cloud API:er är säkra och kräver <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-token-baserad autentisering</a>.

```bash
-H "Authorization: Bearer {access_token}"
```

### Begäranparametrar för **moveFile**-API:et är

| Parameter Name  | Typ    | Sökväg/Frågesträng/HTTP-body | Beskrivning                                         |
| --------------- | ------ | ---------------------------- | --------------------------------------------------- |
| srcPath         | String | Sökväg                       | Källsökvägen för filen som ska flyttas.             |
| destPath        | String | Frågesträng                  | Målsökvägen dit filen ska flyttas.                  |
| srcStorageName  | String | Frågesträng                  | Källlagringsnamnet, om tillämpligt.                |
| destStorageName | String | Frågesträng                  | Mållagringsnamnet, om tillämpligt.                 |
| versionId       | String | Frågesträng                  | Filens versions-ID, om tillämpligt.                |

### **Svar**

Ett lyckat anrop returnerar **HTTP 200 OK** med en tom JSON-body.

```json
{}
```

**HTTP-statuskoder**

| HTTP-kod | HTTP-status           | Beskrivning                                                        |
| -------- | --------------------- | ------------------------------------------------------------------ |
| 200      | OK                    | Webb-API:et anropades utan problem; svaret innehåller åtgärdens detaljer. |
| 400      | Ogiltig begäran       | Saknade eller ogiltiga parametrar (t.ex. filtyp som inte stöds).  |
| 401      | Oautentiserad         | Ogiltig eller saknad JWT-token.                                    |
| 413      | För stor nyttolast    | Den uppladdade filen överskrider storleksgränsen.                  |
| 500      | Internt serverfel     | Oväntat serverfel.                                                 |

## OpenAPI-specifikation

[OpenAPI-specifikationen](https://reference.aspose.cloud/cells/#/FileController/MoveFile) definierar ett offentligt tillgängligt programmeringsgränssnitt och gör det möjligt att utföra REST-interaktioner direkt från en webbläsare.

Du kan använda verktyget cURL för kommandoraden för enkelt att komma åt Aspose.Cells-webbtjänster. Följande exempel visar hur man gör anrop till moln-API:et med cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Begäran" tabName12="Svar" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/storage/file/move/{srcPath}?destPath={destPath}" \
     -H "Authorization: Bearer {access_token}"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{}
```

{{< /tab >}}

{{< /tabs >}}

Att använda ett SDK är det bästa sättet att påskynda utvecklingen. Ett SDK hanterar detaljer på lågnivå och låter dig fokusera på dina projektuppgifter. Kolla in [GitHub-lagringsplatsen](https://github.com/aspose-cells-cloud) för en fullständig lista över Aspose.Cells Cloud SDK:er.

Följande kodexempel visar hur man gör anrop till Aspose.Cells-webbtjänster med olika SDK:er:

---