---
title: "Aspose.Cells Cloud Flyttmapp-API – Snabbt flytta mappar i molnet"
secondtitle: "Dokument"
ArticleTitle: "Molnbaserad Excel-filhantering – Snabbt flytta mappar i molnet"
linktitle: "Flyttmapp"
type: docs
url: /sv/move-folder/
keywords: "Aspose.Cells, Flyttmapp, Molnlagring, Excel-API"
description: "Lär dig hur du flyttar mappar i Aspose.Cells Cloud-lagring via REST-baserade Flyttmapp-API:et. Inkluderar slutpunkt, parametrar, exempel på cURL, felkoder och SDK-exempel för C#, Java, Python med mera."
weight: 100
---

Detta API flyttar en mapp från en plats till en annan inom Aspose.Cells Cloud-lagring. Det hjälper till att organisera filer och hantera molnlagring effektivt.

## **Excel-API: Flyttmapp**

### Web API

```http
PUT https://api.aspose.cloud/v4.0/cells/storage/folder/move/{srcPath}
```

**Exempel på cURL-förfrågan**

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/storage/folder/move/FolderA?destPath=FolderB" \
     -H "Authorization: Bearer {access_token}"
```

### **Säkerhet och autentisering**

Aspose.Cells Cloud-API:er är säkra och kräver <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-tokenbaserad autentisering</a>.

### Begäranparametrarna för **moveFolder**-API:et är

| Parameter Name  | Type   | Location | Description                                                       |
| --------------- | ------ | -------- | ----------------------------------------------------------------- |
| srcPath         | string | Path     | Den fullständiga sökvägen till mappen som ska flyttas, t.ex. `FolderA/`. |
| destPath        | string | Query    | Målsökvägen dit mappen ska flyttas, t.ex. `FolderB/`.            |
| srcStorageName  | string | Query    | (Valfritt) Namn på källlagring.                                   |
| destStorageName | string | Query    | (Valfritt) Namn på mållagring.                                    |

**Parameterbeskrivning**

- **srcPath** – obligatoriskt. Källmappens sökväg.
- **destPath** – obligatoriskt. Målmappens sökväg.
- **srcStorageName** – valfritt. Identifierare för källlagring.
- **destStorageName** – valfritt. Identifierare för mållagring.

### **Svar**

Vid lyckad åtgärd returnerar API:et en tom svarskropp med HTTP-statuskod **200 OK**. Fel returneras som JSON-objekt som innehåller ett fält `error`.

**HTTP-statuskoder**

| HTTP Code | HTTP Status           | Description                                                       |
| --------- | --------------------- | ----------------------------------------------------------------- |
| 200       | OK                    | Web-API:et anropades utan problem; svaret innehåller åtgärd detaljer. |
| 400       | Bad Request           | Saknade eller ogiltiga parametrar (t.ex. filtyp som inte stöds). |
| 401       | Unauthorized          | Ogiltig eller saknad JWT-token.                                   |
| 413       | Payload Too Large     | Den uppladdade filen överskrider storleksgränsen.                 |
| 500       | Internal Server Error | Oväntat serverfel.                                                |

## OpenAPI-specifikation

[OpenAPI-specifikationen](https://reference.aspose.cloud/cells/#/FolderController/MoveFolder) definierar ett offentligt tillgängligt programmeringsgränssnitt och låter dig utföra REST-interaktioner direkt från en webbläsare.

Du kan använda verktyget cURL för kommandoraden för enkelt att komma åt Aspose.Cells webbtjänster. Följande exempel visar hur du gör anrop till Cloud-API:et med cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Förfrågan" tabName12="Svar" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/storage/folder/move/{srcPath}?destPath={destPath}" \
     -H "Authorization: Bearer {access_token}"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{}
```

{{< /tab >}}

{{< /tabs >}}

Att använda ett SDK är det bästa sättet att snabba upp utvecklingen. Ett SDK hanterar detaljer på lågnivå och låter dig fokusera på dina projektuppgifter. Kolla in [GitHub-repositoriet](https://github.com/aspose-cells-cloud) för en komplett lista över Aspose.Cells Cloud SDK:er.

Följande kodexempel visar hur man gör anrop till Aspose.Cells webbtjänster med olika SDK:er:

---