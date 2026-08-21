---
title: "Object Exists API – Kontrollera fil- eller mappnärvaro i Aspose.Cells Cloud"
second_title: "Dokument"
ArticleTitle: "Object Exists API – Verifiera fil- eller mappnärvaro i Aspose.Cells Cloud"
linktitle: "Object Exists"
type: docs
url: /object-exists/
keywords: "Aspose.Cells, molnlagring, objekt finns, filnärvaro, mappnärvaro, API"
description: "Använd Object Exists API för snabbt att verifiera om en fil eller mapp finns i Aspose.Cells Cloud-lagring. Stöder valfritt lagringsnamn och versions-ID, samt fungerar med versionshanterade objekt."
weight: 100
---

**Object Exists API** låter utvecklare avgöra om en specifik fil eller mapp finns i Aspose.Cells Cloud-lagring. API:t returnerar en enkel Boolean-värde som anger om objektet finns samt om sökvägen pekar på en mapp.

## **Excel API: Object Exists**

### Webb-API

```http
GET https://api.aspose.cloud/v5.0/cells/storage/exist/{path}
```

_`{path}`_ är den fullständiga sökvägen till filen eller mappen i lagringen.

### **Säkerhet och autentisering**

Aspose.Cells Cloud-API:er är säkra och kräver <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-tokenbaserad autentisering</a>.

### Begäranparametrar

| Parametername   | Typ    | Plats   | Obligatoriskt | Beskrivning                                                       |
| --------------- | ------ | ------- | ------------- | ----------------------------------------------------------------- |
| `path`          | string | Sökväg  | Ja            | Fullständig sökväg till filen eller mappen.                       |
| `storageName`   | string | Fråga   | Nej           | Namn på lagringen; standardvärde är primär lagring om utelämnas.   |
| `versionId`     | string | Fråga   | Nej           | Specifikt versions-ID för filen (om versionshantering är aktiverat). |

**HTTP-statuskoder**

| HTTP-kod | HTTP-status            | Beskrivning                                                        |
| -------- | ---------------------- | ------------------------------------------------------------------ |
| 200      | OK                     | Webb-API:t anropades framgångsrikt; svaren innehåller åtgärdens detaljer. |
| 400      | Felaktig begäran       | Saknade eller ogiltiga parametrar (t.ex. filtyp som inte stöds).   |
| 401      | Oautentiserad          | Ogiltig eller saknad JWT-token.                                    |
| 413      | Payload för stor       | Den uppladdade filen överskrider storleksgränsen.                  |
| 500      | Internt serverfel      | Oväntat serverfel.                                                 |

### **Svar**

Ett framgångsrikt anrop returnerar ett JSON-svar med två egenskaper:

```json
{
  "Exists": true,
  "IsFolder": false
}
```

- **Exists** – `true` om filen eller mappen finns; annars `false`.
- **IsFolder** – `true` om sökvägen pekar på en mapp; `false` för en fil.

## OpenAPI-specifikation

[OpenAPI-specifikationen](https://reference.aspose.cloud/cells/#/StorageController/ObjectExists) definierar ett offentligt tillgängligt programmeringsgränssnitt och möjliggör REST-interaktioner direkt från en webbläsare.

Du kan använda kommandoradsverktyget cURL för enkelt att komma åt Aspose.Cells webbtjänster. Följande exempel visar hur man gör anrop till Cloud API med cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Begäran" tabName12="Svar" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/storage/exist/myFolder/subFolder" \
     -H "Authorization: Bearer {access_token}" \
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

Att använda ett SDK är det bästa sättet att påskynda utvecklingen. Ett SDK hanterar detaljer på lågnivå och låter dig fokusera på dina projektuppgifter. Kolla in [GitHub-förrådet](https://github.com/aspose-cells-cloud) för en komplett lista över Aspose.Cells Cloud SDK:n.

Följande kodexempel visar hur man gör anrop till Aspose.Cells webbtjänster med olika SDK:n. Om en Gist inte laddas visas ett statiskt exempel nedanför varje flik.

---