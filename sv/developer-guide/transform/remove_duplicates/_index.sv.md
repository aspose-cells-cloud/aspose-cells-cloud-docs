---
title: "Ta bort dubbletter"
ArticleTitle: "Ta bort dubbletter – Aspose.Cells Cloud API"
second_title: "Dokument"
linktitle: "Ta bort dubbletter"
type: docs
url: /sv/cells/remove/duplicates
aliases: []
keywords: "Aspose.Cells, Ta bort dubbletter, API"
description: "Tar bort dubblettvärden i ett kalkylblad, ett område eller en tabell."
weight: 1000
---

## Ta bort dubbletter med Aspose.Cells Cloud Webbtjänster

Tar bort dubblettvärden i kalkylbladet, området eller tabellen. Denna metod skannar målomfånget efter rader med identiska värden i de angivna kolumner som ska kontrolleras. För varje uppsättning dubbletter tas alla förekomster bort utom den första. Jämförelsen är typiskt skiftlägeskänslig och matchar det exakta cellvärdet.

### Web API-slutpunkt

```http
PUT https://api.aspose.cloud/v4.0/cells/remove/duplicates
```

### **Säkerhet och autentisering**

Aspose.Cells Cloud API:er är säkra och kräver <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-tokenbaserad autentisering</a>.

### Begärparametrar

| Parameternamn | Typ   | Sökväg/Frågesträng/HTTP-nyttolast | Beskrivning |
|---------------|-------|-----------------------------------|-------------|
| Spreadsheet   | Fil   | FormData                          | Ladda upp kalkylarkfil. |
| worksheet     | Sträng | Fråga                             | Kalkylbladets namn. (valfritt) |
| range         | Sträng | Fråga                             | Namn på det område där dubbletter ska tas bort. (valfritt) |
| table         | Sträng | Fråga                             | Namn på den tabell där dubbletter ska tas bort. (valfritt) |
| outPath       | Sträng | Fråga                             | (Valfritt) Mappens sökväg där arbetsboken lagras. Standard är null. |
| outStorageName| Sträng | Fråga                             | Lagringsnamn för utdatafilen. |
| region        | Sträng | Fråga                             | Inställning för region/språk för kalkylarket (t.ex. `sv-SE`, `en-US`, `fr-FR`). Påverkar formatering av tal, tolkning av datum och språkspecifik beteende. |
| password      | Sträng | Fråga                             | Lösenord för att öppna kalkylarkfilen. |

### Begäran: Nyttolastparameter

| Parameternamn | Typ | Beskrivning |
| ------------- | --- | ----------- |
| [TBD] | [TBD] | [TBD] |

### **Svar**

```json
{
  "File": "binär ström av det resulterande kalkylarket (t.ex. .xlsx)"
}
```

**Svarsstatuskoder**

| Kod | Betydelse | Beskrivning |
|-----|-----------|-------------|
| 200 | OK | Det resulterande kalkylarket med dubbletter borttagna returneras som en filström. |
| 400 | Felaktig begäran | Ogiltiga begärparametrar eller felaktig URL. |
| 401 | Inte auktoriserad | Autentiseringen har misslyckats eller inga inloggningsuppgifter har angetts. |
| 413 | Nyttolast för stor | Den uppladdade filen överskrider den tillåtna storleksgränsen. |
| 500 | Internt serverfel | Kalkylarket stötte på ett fel vid hämtning av data eller ett annat serverseitfel. |

## Hur man använder Ta bort dubbletter med SDK:er

### Specificering av Ta bort dubbletter

[API-specificering för Ta bort dubbletter](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/{Transform}/{RemoveDuplicates}) definierar ett offentligt tillgängligt programmeringsgränssnitt och låter dig utföra REST-interaktioner direkt från en webbläsare.

Du kan använda kommandoradsverktyget cURL för enkelt att komma åt Aspose.Cells-webbtjänster. Följande exempel visar hur man gör anrop till Cloud API med cURL.

{< tabs tabTotal="2" tabID="1" tabName1="Begäran" tabName2="Svar" >}
{< tab tabNum="1" >}
```bash
# Använd HTTPS för en säker anslutning
curl -v "https://api.aspose.cloud/v4.0/cells/remove/duplicates?worksheet=Blad1&range=A1:C10&table=MinTabell&outPath=output%2Fmapp&outStorageName=MinLagring&region=sv-SE&password=MittLösenord" \
  -X PUT \
  -H "Content-Type: multipart/form-data" \
  -H "Accept: application/octet-stream" \
  -H "Authorization: Bearer <jwt token>" \
  -F 'Spreadsheet=@exempel.xlsx'
```
{< /tab >}
{< tab tabNum="2" >}
```json
{
  "File": "binär ström av det resulterande kalkylarket (t.ex. .xlsx)"
}
```
{< /tab >}
{< /tabs >}

### Använd Aspose Cells Cloud SDK:er

Att använda en SDK är det snabbaste sättet att påskynda utvecklingen. En SDK abstraher bort detaljer på lägre nivå och låter dig fokusera på dina projektuppgifter. Se <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub-förrådet</a> för en komplett lista över Aspose.Cells Cloud SDK:er.

Följande kodexempel visar hur man anropar Aspose Cells Cloud-webbtjänster med olika SDK:er:

```csharp
// Kodexempel för C# med SDK
var config = new Configuration
{
    AccessToken = "<jwt token>"
};
var apiInstance = new TransformApi(config);
var file = File.ReadAllBytes("example.xlsx");
var result = apiInstance.RemoveDuplicates(
    file,
    worksheet: "Sheet1",
    range: "A1:C10",
    table: "MyTable",
    outPath: "output/folder",
    outStorageName: "MyStorage",
    region: "en-US",
    password: "MyPassword"
);
File.WriteAllBytes("result.xlsx", result);
```

```java
// Kodexempel för Java med SDK
ApiClient client = new ApiClient();
client.setAccessToken("<jwt token>");
TransformApi api = new TransformApi(client);
byte[] file = Files.readAllBytes(Paths.get("example.xlsx"));
byte[] result = api.removeDuplicates(
    file,
    "Sheet1",
    "A1:C10",
    "MyTable",
    "output/folder",
    "MyStorage",
    "en-US",
    "MyPassword"
);
Files.write(Paths.get("result.xlsx"), result);
```

```python
# Kodexempel för Python med SDK
import asposecellscloud
from asposecellscloud.rest import ApiException

configuration = asposecellscloud.Configuration()
configuration.access_token = "<jwt token>"
api_instance = asposecellscloud.TransformApi(asposecellscloud.ApiClient(configuration))

with open('example.xlsx', 'rb') as f:
    file_bytes = f.read()

try:
    result = api_instance.remove_duplicates(
        file=file_bytes,
        worksheet='Sheet1',
        range='A1:C10',
        table='MyTable',
        out_path='output/folder',
        out_storage_name='MyStorage',
        region='en-US',
        password='MyPassword'
    )
    with open('result.xlsx', 'wb') as out_f:
        out_f.write(result)
except ApiException as e:
    print("Undantag vid anrop till TransformApi->remove_duplicates: %s\\n" % e)
```

`[TBD]`
---