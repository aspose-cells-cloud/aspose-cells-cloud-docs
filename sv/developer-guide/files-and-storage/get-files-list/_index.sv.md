---
---
title: "Aspose.Cells Cloud API – Hämta fillista (mappinnehåll)"
description: "Hämta en lista över filer och undermappar från en specifik mapp i Aspose.Cells Cloud-lagring."
keywords:
  - Aspose.Cells
  - API
  - Get Files List
  - Cloud Storage
  - Excel
  - REST
type: docs
weight: 100
---

Operationen **Get Files List** returnerar samlingen av filer och undermappar som finns i en angiven mapp i Aspose.Cells Cloud-lagring.  
Det är huvudinmatningspunkten för att bläddra bland molnbaserade Excel-arbetsböcker, arkiv och andra stödda filtyper.

## Aspose.Cells Cloud API – Hämta fillista (mappinnehåll)

```
GET https://api.aspose.cloud/v4.0/cells/storage/folder/{path}
```

### **Säkerhet och autentisering**

Aspose.Cells Cloud API:er är säkra och kräver <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-tokenbaserad autentisering</a>.

### Begärandeparametrar

| Namn            | Plats   | Typ     | Obligatorisk | Beskrivning                                                               |
| --------------- | ------- | ------- | ------------ | ------------------------------------------------------------------------- |
| **path**        | Sökväg  | string  | Ja           | Sökväg till mappen i molnlagringen.                                      |
| **storageName** | Fråga   | string  | Nej          | Namn på den lagring som ska användas. Om utelämnas används standardlagring. |
| **pageSize**    | Fråga   | integer | Nej          | Maximalt antal objekt per sida (standard: 100).                          |
| **pageNumber**  | Fråga   | integer | Nej          | Sidnummer att hämta (börjar på 1, standard: 1).                          |

- **Value** – Array med `StorageFile`-objekt. Varje objekt innehåller:
  - `Name` – Fil- eller mappnamn.
  - `IsFolder` – `true` om objektet är en mapp.
  - `Size` – Storlek i byte (mappar rapporterar `0`).
  - `ModifiedDate` – Tidsstämpel för senaste ändring (ISO 8601).

### **Svar**

**HTTP-statuskoder**

| HTTP-kod | HTTP-status           | Beskrivning                                                             |
| -------- | --------------------- | ----------------------------------------------------------------------- |
| 200      | OK                    | Webb-API:et anropades framgångsrikt; svaret innehåller åtgärddetaljer. |
| 400      | Bad Request           | Saknade eller ogiltiga parametrar (t.ex. filtyp som inte stöds).       |
| 401      | Unauthorized          | Ogiltig eller saknad JWT-token.                                         |
| 413      | Payload Too Large     | Den uppladdade filen överskrider storleksgränsen.                       |
| 500      | Internal Server Error | Oväntat serverfel.                                                      |
|          |

## OpenAPI-specifikation

[OpenAPI-specifikationen](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Folder/GetFilesList) definierar ett offentligt tillgängligt programmeringsgränssnitt och låter dig utföra REST-interaktioner direkt från en webbläsare.

Du kan använda verktyget cURL för kommandoraden för enkelt att komma åt Aspose.Cells webbtjänster. Följande exempel visar hur du gör anrop till Cloud API med cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Begäran" tabName12="Svar" >}}

{{< tab tabNum="11" >}}

```bash
curl -X GET "https://api.aspose.cloud/v4.0/cells/storage/folder/{path}?storageName=MyStorage&pageSize=100&pageNumber=1" \
     -H "Authorization: Bearer <your_access_token>"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Value": [
    {
      "Name": "Report.xlsx",
      "IsFolder": false,
      "Size": 124578,
      "ModifiedDate": "2024-03-10T12:34:56Z"
    },
    {
      "Name": "Archives",
      "IsFolder": true,
      "Size": 0,
      "ModifiedDate": "2024-02-01T08:00:00Z"
    }
  ]
}
```

{{< /tab >}}

{{< /tabs >}}

### Använd Aspose.Cells Cloud SDK:er

Att använda ett SDK är det bästa sättet att påskynda utvecklingen. Ett SDK hanterar detaljer på låg nivå och låter dig fokusera på dina projektuppgifter. Se <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub-förrådet</a> för en komplett lista över Aspose.Cells Cloud SDK:er.

Följande kodexempel visar hur du gör anrop till Aspose.Cells webbtjänster med olika SDK:er:

---