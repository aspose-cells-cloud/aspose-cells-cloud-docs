---
title: Ta bort alla OLE-objekt i ett Excel-ark
description: Lär dig hur du tar bort alla OLE-objekt från ett Excel-ark med Aspose.Cells Cloud REST API (v3.0). Innehåller endpoint, parametrar, exempel på begäran/svar, SDK-fragment, autentisering, felhantering och vanliga frågor.
keywords: Aspose.Cells Cloud, ta bort OLE-objekt, Excel API, REST API, rensa OLE i kalkylark, moln-SDK
api_version: v3.0
last_updated: 2024-11-01
weight: 60
---

# Ta bort alla OLE-objekt i ett Excel-ark

**OleObjects – Clear** tar bort **alla** OLE-objekt (Object Linking and Embedding) från ett angivet kalkylark utan att påverka celldata. Denna åtgärd är användbar för att rensa äldre kalkylark eller förbereda en arbetsbok för vidare distribution.

---

## Förutsättningar

- En giltig **Aspose Cloud JWT-åtkomsttoken** (OAuth 2.0).  
- Målarbetsboken måste lagras i Aspose Cloud-lagring (eller så måste du ange `folder`/`storageName` där den finns).  
- API-version **v3.0** eller högre.  

> **Obs!** Åtgärden är *idempotent* – om den anropas när inga OLE-objekt finns kvar returneras ändå `200 OK`.

---

## HTTP-begäran

```
DELETE https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/oleobjects
```

### Sökvägsparametrar

| Namn         | Typ    | Obligatorisk | Beskrivning                     |
|--------------|--------|--------------|---------------------------------|
| `name`       | string | ✔️           | Namnet på arbetsbokens fil.     |
| `sheetName`  | string | ✔️           | Namnet på kalkylarket.          |

### Frågeparametrar

| Namn          | Typ    | Obligatorisk | Beskrivning                              |
|---------------|--------|--------------|------------------------------------------|
| `folder`      | string | valfritt     | Mapp där arbetsboken finns.              |
| `storageName` | string | valfritt     | Lagringsnamn där arbetsboken ligger.     |

**Rubriker**

| Rubrik              | Värde                         |
|---------------------|------------------------------|
| `Authorization`     | `Bearer <jwt token>` |
| `Accept`            | `application/json` |
| `Content-Type`      | `application/json` |

---

## Exempel på begäran (cURL)

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Embedded_OleObject_Sample_Book1.xlsx/worksheets/Sheet1/oleobjects?folder=Samples&storageName=MyStorage" \
     -X DELETE \
     -H "Authorization: Bearer <jwt token>" \
     -H "Accept: application/json" \
     -H "Content-Type: application/json"
```

*Ersätt `<jwt token>` med en giltig åtkomsttoken och justera `folder`/`storageName` enligt behov.*

---

## Lyckat svar

```json
{
  "Code": 200,
  "Status": "OK"
}
```

**HTTP-statuskoder**

| Kod | Betydelse                | Beskrivning                                                  |
|-----|--------------------------|--------------------------------------------------------------|
| 200 | OK                       | Åtgärden utfördes korrekt; svaret innehåller åtgärdsinformation. |
| 400 | Bad Request              | Saknade eller ogiltiga parametrar (t.ex. filtyp som inte stöds). |
| 401 | Unauthorized             | Ogiltig eller saknad JWT-token.                              |
| 413 | Payload Too Large        | Den uppladdade filen överskrider storleksgränsen.            |
| 500 | Internal Server Error    | Oväntat serverfel.                                           |
---

## SDK-exempel

Följande kodfragment visar hur du anropar **DeleteWorksheetOleObjects** med de officiella Aspose.Cells Cloud SDK:erna. Ersätt platshållarvärden (`<YOUR_TOKEN>`, `<FILE_NAME>` etc.) med dina egna uppgifter.

| Språk      | Exempel |
|------------|---------|
| **C#** | <details><summary>Visa C#-exempel</summary>```csharp\nusing Aspose.Cells.Cloud.SDK.Api;\nusing Aspose.Cells.Cloud.SDK.Model;\n\nvar config = new Configuration { AccessToken = "<YOUR_TOKEN>", BasePath = "https://api.aspose.cloud" };\nvar api = new OleObjectsApi(config);\napi.DeleteWorksheetOleObjects(name: "Sample.xlsx", sheetName: "Sheet1", folder: "Samples", storageName: null);\n```</details> |
| **Java** | <details><summary>Visa Java-exempel</summary>```java\nimport com.aspose.cells.cloud.api.OleObjectsApi;\nimport com.aspose.cells.cloud.client.ApiClient;\nimport com.aspose.cells.cloud.client.Configuration;\n\nConfiguration config = new Configuration();\nconfig.setAccessToken("<YOUR_TOKEN>");\nconfig.setBasePath("https://api.aspose.cloud");\nOleObjectsApi api = new OleObjectsApi(new ApiClient(config));\napi.deleteWorksheetOleObjects("Sample.xlsx", "Sheet1", "Samples", null);\n```</details> |
| **Python** | <details><summary>Visa Python-exempel</summary>```python\nfrom asposecellscloud import ApiClient, Configuration, OleObjectsApi\n\nconfig = Configuration()\nconfig.access_token = '<YOUR_TOKEN>'\nconfig.host = 'https://api.aspose.cloud'\nclient = ApiClient(configuration=config)\napi = OleObjectsApi(client)\napi.delete_worksheet_ole_objects(name='Sample.xlsx', sheet_name='Sheet1', folder='Samples')\n```</details> |
| **Node.js** | <details><summary>Visa Node.js-exempel</summary>```javascript\nconst { OleObjectsApi, Configuration } = require('asposecellscloud');\n\nlet config = new Configuration({ accessToken: '<YOUR_TOKEN>', basePath: 'https://api.aspose.cloud' });\nlet api = new OleObjectsApi(config);\napi.deleteWorksheetOleObjects('Sample.xlsx', 'Sheet1', { folder: 'Samples' })\n  .then(() => console.log('Alla OLE-objekt borttagna'))\n  .catch(err => console.error(err));\n```</details> |
| **Go** | <details><summary>Visa Go-exempel</summary>```go\npackage main\nimport (\n    "context"\n    "github.com/aspose-cells-cloud/aspose-cells-cloud-go/v3"\n)\n\nfunc main() {\n    cfg := asposecellscloud.NewConfiguration()\n    cfg.AccessToken = "<YOUR_TOKEN>"\n    cfg.Host = "https://api.aspose.cloud"\n    api := asposecellscloud.NewOleObjectsApi(cfg)\n    _, err := api.DeleteWorksheetOleObjects(context.Background(), "Sample.xlsx", "Sheet1", map[string]interface{}{ "folder": "Samples" })\n    if err != nil { panic(err) }\n    println("Alla OLE-objekt borttagna")\n}\n```</details> |

*Fullständiga källkodsfilerna för alla stödda språk finns i [Aspose.Cells Cloud GitHub-lagringsplatsen](https://github.com/aspose-cells-cloud).*

---

## Fel & hantering

- **Idempotens** – Att ta bort OLE-objekt i ett kalkylark som redan är fritt från sådana returnerar fortfarande `200 OK`.  
- **Token-utgång** – Om du får `401 Unauthorized` ska du skaffa en ny JWT-token och försöka igen.  
- **Ogiltigt kalkylarksnamn** – Se till att kalkylarksnamnet matchar det exakta skiftläget i arbetsboken; annars returneras `400 Bad Request`.  

Implementera återförsökslogik med exponentiell backoff för tillfälliga `500`-fel.

---

## Vanliga frågor

**Q1: Måste jag ange parametrarna `folder` och `storageName`?**  
**A:** Nej. Om de utelämnas antar Aspose Cloud standardlagring och rotmapp.

**Q2: Kan jag ta bort OLE-objekt från en specifik cell?**  
**A:** Endpoint:en tar bort **alla** OLE-objekt i kalkylarket. För att ta bort ett enskilt objekt använd åtgärden *Ta bort ett specifikt OLE-objekt*.

**Q3: Vad händer om arbetsboken är låst för redigering?**  
**A:** API:et returnerar `400 Bad Request` med ett meddelande om att filen är låst. Se till att filen inte är öppnad någon annanstans innan du anropar endpoint:en.

**Q4: Finns det en gräns för arbetsbokens storlek?**  
**A:** Tjänsten följer de allmänna Aspose Cloud-filstorleksbegränsningarna (för närvarande upp till 2 GB per fil). Större filer kan behöva delas upp eller bearbetas i delar.

---

## Bästa praxis

- **Prestanda** – Använd `async`- eller `defer`-attributen när du laddar tredjepartsskript på din dokumentationswebbplats för att minska sidans ursprungliga lästid.  
- **Säkerhet** – Lägg till `rel="noopener noreferrer"` till alla externa länkar som öppnas i en ny flik.  
- **Tillgänglighet** – Dekorativa ikoner (t.ex. nedåtpil i sidofält) bör ha `alt=""` och `role="presentation"` för att uppfylla WCAG AA-kraven.  
- **Konsekvens** – Använd ISO‑8601-datumformat (`ÅÅÅÅ‑MM‑DD`) för att undvika kodningsproblem.  

---

## Relaterade åtgärder

- **Lägg till OLE-objekt** – `POST /cells/{name}/worksheets/{sheetName}/oleobjects`  
- **Ta bort ett specifikt OLE-objekt** – `DELETE /cells/{name}/worksheets/{sheetName}/oleobjects/{oleObjectIndex}`  

Använd navigeringslänkarna längst ner på sidan för att växla mellan relaterade API-åtgärder.

---
---