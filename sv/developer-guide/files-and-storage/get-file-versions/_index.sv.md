---
title: "Aspose.Cells Cloud Get File Versions API – Snabb hämtning av filversionshistorik"
secondtitle: "Dokument"
ArticleTitle: "Excel-hantering i molnet – Snabb hämtning av filversionshistorik i Aspose.Cells Cloud"
linktitle: "Hämta filversioner"
type: docs
url: /sv/get-file-versions/
keywords: "Aspose Cells API, filversioner, kalkylarksversionering, molnlagrings-API, REST, Excel-filhistorik"
description: "Få en komplett lista över versionshistorik för valfritt Excel-filark lagrat i Aspose.Cells Cloud. Stödjer val av lagring, autentisering och detaljerade felkoder."
weight: 100
---

Hämta en komplett lista över versionsposter för ett specifikt kalkylark lagrat i Aspose.Cells Cloud. Den här slutpunkten möjliggör utvecklare att spåra ändringar, granska modifieringar och implementera versionshanteringsarbetsflöden direkt från molnlagringen.

**GetFileVersions**-API:et returnerar alla versionsposter för ett angivet kalkylark lagrat i Aspose.Cells Cloud. Det hjälper dig att behålla en komplett ändringshistorik för varje fil.

## **Excel-API: Hämta filversioner**

### Web API

```
GET https://api.aspose.cloud/v4.0/cells/storage/version/{path}
```

### **Säkerhet och autentisering**

Aspose.Cells Cloud API:er är säkra och kräver <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-tokenbaserad autentisering</a>.

### Begärandeparametrarna för **GetFileVersions**-API:et är

| Parameter namn | Typ    | Plats  | Beskrivning                                                                                   |
| -------------- | ------ | ------ | --------------------------------------------------------------------------------------------- |
| `path`         | Sträng | Sökväg | **Obligatoriskt.** Fullständig sökväg till den fil vars versioner ska hämtas.                 |
| `storageName`  | Sträng | Fråga  | Valfritt. Namnet på den lagring som innehåller filen. Om utelämnas används standardlagringen. |

### **Svar**

```json
{
  "Name": "FileVersions",
  "Description": [
    "Innehåller en lista över filversioner för det angivna dokumentet."
  ],
  "Type": "Class",
  "IsAbstract": false,
  "Properties": [
    {
      "Name": "Value",
      "Description": ["En samling med detaljerad information om filversioner."],
      "Nullable": true,
      "ReadOnly": false,
      "IsInherit": false,
      "DataType": {
        "Identifier": "Container",
        "Reference": "FileVersion",
        "ElementDataType": {
          "Identifier": "Class",
          "Reference": "FileVersion",
          "Name": "class:fileversion"
        },
        "Name": "container"
      }
    }
  ]
}
```

Vid framgång returnerar API:et **HTTP 200 OK** med ett JSON-svarsinnehåll som innehåller `Value`-arrayen med filversionsobjekt, enligt ovan.

**HTTP-statuskoder**

| Kod | Betydelse             | Beskrivning                                                       |
| --- | --------------------- | ----------------------------------------------------------------- |
| 200 | OK                    | Filter applicerades framgångsrikt; svaret innehåller åtgärdens detaljer. |
| 400 | Felaktig begäran      | Saknade eller ogiltiga parametrar (t.ex. filtyp som inte stöds). |
| 401 | Ej auktoriserad       | Ogiltig eller saknad JWT-token.                                   |
| 413 | Payload för stor      | Den uppladdade filen överskrider storleksgränsen.                |
| 500 | Internt serverfel     | Oväntat serverfel.                                                |

## OpenAPI-specifikation

[OpenAPI-specifikationen](https://reference.aspose.cloud/cells/#/StorageController/GetFileVersions) tillhandahåller ett omfattande programmeringsgränssnitt för att utföra REST-interaktioner direkt från en webbläsare.

Du kan använda kommandoradsverktyget cURL för enkelt att komma åt Aspose.Cells webbtjänster. Följande exempel visar hur man gör anrop till moln-API:et med cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Begäran" tabName12="Svar" >}}

{{< tab tabNum="11" >}}

```bash
curl -X GET "https://api.aspose.cloud/v4.0/cells/storage/version/MinMapp/MinFil.xlsx" \
     -H "Authorization: Bearer {access_token}" \
     -H "Accept: application/json"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Value": [
    {
      "VersionId": "1",
      "IsLatest": false,
      "ModifiedDate": "2024-01-15T12:34:56Z",
      "Size": 10240
    },
    {
      "VersionId": "2",
      "IsLatest": true,
      "ModifiedDate": "2024-03-01T08:22:10Z",
      "Size": 10300
    }
  ]
}
```

{{< /tab >}}

{{< /tabs >}}

### Använd Aspose.Cells Cloud SDK:er

Att använda ett SDK förenklar utvecklingen genom att abstrahera bort lågnivåkomplexitet, vilket tillåter utvecklare att fokusera på kärnfunktioner.Utforska [GitHub-lagringsplatsen](https://github.com/aspose-cells-cloud) för en komplett lista över Aspose.Cells Cloud SDK:er.

Följande kodexempel illustrerar hur man interagerar med Aspose.Cells webbtjänster i olika programmeringsspråk:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_GetFileVersions.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_GetFileVersions.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_GetFileVersions.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_GetFileVersions.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_GetFileVersions.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_GetFileVersions.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_GetFileVersions.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_GetFileVersions.go" >}}
{{</tab>}}
{{< /tabs >}}