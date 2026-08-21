---
title: "Ta bort tecken från Excel – Aspose.Cells Cloud API (POST /cells/removecharacters)"
second_title: "Dokument"
linktitle: "Ta bort tecken"
type: docs
url: /sv/excel-remove-characters/
keywords: "ta bort tecken, Aspose.Cells, Excel API, textbearbetning, moln"
description: "Lär dig hur du tar bort tecken, teckenuppsättningar eller delsträngar från Excel-ark med Aspose.Cells Cloud API. Inkluderar begärandeschema, cURL-exempel, SDK-kod och felhantering."
weight: 100
ArticleTitle: "Ta bort tecken från Excel – Aspose.Cells Cloud API (POST /cells/removecharacters)"
---

## Ta bort tecken från Excel-webb-API

En omfattande uppsättning verktyg för att rensa textinnehåll i valda celler. API:et tar bort specifika tecken, fördefinierade teckenuppsättningar eller delsträngar, vilket säkerställer att arktexten är standardiserad och fri från oönskade symboler.

**Förutsättningar**

- Ett aktivt Aspose Cloud-konto.  
- En giltig JWT-åtkomsttoken som erhållits enligt beskrivningen i autentiseringshandboken.  
- Excel-filen måste vara uppladdad till lagring innan du anropar den här slutpunkten.  
- Stödda filformat inkluderar `.xlsx`, `.xls`, `.xlsm` och andra vanliga Excel-typer.

```http
POST https://api.aspose.cloud/v3.0/cells/removecharacters
```

### **Säkerhet och autentisering**

Aspose.Cells Cloud-API:er är säkra och kräver <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-tokenbaserad autentisering</a>.

### Funktionsbeskrivning

- **Ta bort anpassade tecken** – Ange alla tecken du vill ta bort. Ange varje tecken i fältet _Ta bort anpassade tecken_; API:et tar bort alla förekomster av dessa tecken i de valda cellerna.  
- **Ta bort teckenuppsättningar** – Välj från de fördefinierade uppsättningarna:  
  - **Icke-utskrivbara tecken** – Tar bort radbrytningar och de första 32 icke-utskrivbara ASCII-tecknen (0‑31) samt ytterligare koderna (127, 129, 141, 143, 144, 157).  
  - **Texttecken** – Tar bort alla bokstäver.  
  - **Numeriska tecken** – Tar bort alla siffror.  
  - **Symboler** – Tar bort matematiska, geometriska, tekniska, valutasymboler samt bokstavsliknande symboler som „?“, „1“ och „™“.  
  - **Skiljetecken** – Tar bort alla skiljetecken.  
- **Ta bort en delsträng** – Tar bort valfri angiven delsträng (t.ex. ett ord) från de valda cellerna.

### Begärandeparametrar

| Parameter Name          | Typ   | Plats  | Beskrivning                                                                   |
| ----------------------- | ----- | ------ | ----------------------------------------------------------------------------- |
| removeCharactersOptions | Klass | Body   | Alternativ som definierar vilka tecken, teckenuppsättningar eller delsträngar som ska tas bort. |

**Schema för `removeCharactersOptions`**

| Egenskap         | Typ     | Obligatorisk | Beskrivning                                                                                                    |
| ---------------- | ------- | ------------ | -------------------------------------------------------------------------------------------------------------- |
| Range            | sträng  | Ja           | A‑1-notation eller namngivet område som identifierar cellerna som ska bearbetas (t.ex. `"A1:C10"`).           |
| CustomCharacters | sträng  | Nej          | En sträng som innehåller varje anpassat tecken som ska tas bort (t.ex. `"@#$"`).                               |
| CharacterSet     | sträng  | Nej          | Enum-värde som anger en fördefinierad uppsättning (`"NonPrinting"`, `"Text"`, `"Numeric"`, `"Symbols"`, `"Punctuation"`). |
| Substring        | sträng  | Nej          | Den exakta delsträngen som ska tas bort (t.ex. `"USD"`).                                                       |
| IgnoreCase       | boolean | Nej        | När `true` är teckenborttagning skiftlägesokänslig.                                                            |

**Exempel på JSON-begärandetext**

```json
{
  "Range": "A1:B20",
  "CustomCharacters": "@#$",
  "CharacterSet": "NonPrinting",
  "Substring": "USD",
  "IgnoreCase": true
}
```

**Exempel på cURL-begäran**

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/removecharacters" \
     -H "Authorization: Bearer {access_token}" \
     -H "Content-Type: application/json" \
     -d '{
           "Range": "A1:B20",
           "CustomCharacters": "@#$",
           "CharacterSet": "NonPrinting",
           "Substring": "USD",
           "IgnoreCase": true
         }'
```

### **Svar**

```json
{
    "Status" : "OK",
    "Code" : 200,
    "Filename" : "[sammanslagningsfilens namn]",
    "Filesize" : [filstorlek],
    "FileContent" : "[Base64-sträng]"
}
```

**HTTP-statuskoder**

| Kod | Betydelse                   | Beskrivning                                             |
|-----|-----------------------------|---------------------------------------------------------|
| 200 | OK                          | Filter tillämpades framgångsrikt; svaret innehåller åtgärdens detaljer. |
| 400 | Felaktig begäran            | Saknade eller ogiltiga parametrar (t.ex. filtyp som inte stöds). |
| 401 | Oauktoriserad               | Ogiltig eller saknad JWT-token. |
| 413 | Begärandetext för stor      | Den uppladdade filen överskrider storleksgränsen. |
| 500 | Internt serverfel           | Oväntat serverfel. |

## Hur du använder PostRemoveCharacters-API:et med SDK:er

### PostRemoveCharacters API-specifikation

<a href="https://reference.aspose.cloud/cells/#/TextProcessingController/PostRemoveCharacters" rel="noopener noreferrer">Den fullständiga OpenAPI-specifikationen för PostRemoveCharacters-slutpunkten</a> definierar ett offentligt tillgängligt programmeringsgränssnitt och låter dig utföra REST-interaktioner direkt från en webbläsare.

### Använd Aspose.Cells Cloud SDK:er

Att använda en SDK är det bästa sättet att påskynda utvecklingen. En SDK hanterar detaljer på låg nivå och låter dig fokusera på dina projektuppgifter. Kolla in <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub-förrådet</a> för en komplett lista över Aspose.Cells Cloud SDK:er.

Följande kodexempel visar hur du gör anrop till Aspose.Cells-webbtjänster med diverse SDK:er:
---