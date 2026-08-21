---
title: "Exportera tabell – Aspose.Cells Cloud API | Konvertera Excel till PDF, PNG, CSV"
second_title: "Dokument"
ArticleTitle: "Så här exporterar du en extern kalkylarkstabell till ett annat format: Steg-för-steg-guide"
linktitle: "Exportera tabell till angivet format"
type: docs
url: /sv/export-table-as-format/
keywords: "Aspose.Cells, Exportera tabell, Excel till PDF, moln-API, REST"
description: "Exportera en extern Excel-tabell till PDF, PNG, CSV, JSON eller andra format med Aspose.Cells Cloud API. Säker HTTPS-slutpunkt med JWT-autentisering och SDK-exempel."
weight: 100
---

Exportera en molnlagrad kalkylarkstabell (Excel) till en fil i ett annat format.

## **Exportera tabell som format-API**

### Web-API

```http
GET https://api.aspose.cloud/v4.0/cells/{name}/worksheets/{worksheet}/tables/{tableName}
```

### **Säkerhet och autentisering**

Aspose.Cells Cloud-API:er är säkra och kräver <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-tokenbaserad autentisering</a>.

```bash
-H "Authorization: Bearer {access_token}"
```

### **Förfrågningsparametrar:**

| Parametername | Typ   | Path/Query String/HTTPBody | Beskrivning                                                                                                                                       |
| :------------- | :----- | :------------------------- | :------------------------------------------------------------------------------------------------------------------------------------------------ |
| name           | String | Path                       | **Obligatoriskt.** Namnet på arbetsbokens fil som ska hämtas.                                                                                      |
| worksheet      | String | Path                       | Namn på kalkylbladet.                                                                                                                            |
| tableName      | String | Path                       | Namn på tabellen.                                                                                                                                |
| format         | String | Query                      | **Obligatoriskt.** Önskat utdataformat (t.ex. "png", "pdf", "svg").                                                                              |
| folder         | String | Query                      | Valfritt. Mappsökvägen dit arbetsboken är lagrad. Standard är `null`.                                                                        |
| storageName    | String | Query                      | Valfritt. Namnet på lagringen om du använder anpassad molnlagring. Använd standardlagring om utelämnas.                                                  |
| outPath        | String | Query                      | Valfritt. Mappsökvägen för utdatalagring. Standard är `null`.                                                                                  |
| outStorageName | String | Query                      | Valfritt. Namn på utdatalagringslagring.                                                                                                        |
| fontsLocation  | String | Query                      | Valfritt. Plats för anpassade typsnitt.                                                                                                              |
| region         | String | Query                      | Valfritt. Kalkylarksregion/språkinställning (t.ex. `sv-SE`, `en-US`, `fr-FR`). Påverkar nummerformatering, datumtolkning och språkspecifikt beteende. |
| password       | String | Query                      | Valfritt. Lösenord för att öppna kalkylarksfilen.                                                                                              |

### **Svar**

```json
[
  {
    "Name": "ResponseFile",
    "DataType": {
      "Identifier": "File",
      "Reference": "Stream"
    }
  }
]
```

**HTTP-statuskoder**

| Kod | Betydelse               | Beskrivning                                                       |
| ---- | --------------------- | ----------------------------------------------------------------- |
| 200  | OK                    | Filter tillämpades framgångsrikt; svaret innehåller åtgärdsdetaljer. |
| 400  | Felaktig förfrågan           | Saknade eller ogiltiga parametrar (t.ex. filtyp som inte stöds).      |
| 401  | Obehörig          | Ogiltig eller saknad JWT-token.                                     |
| 413  | För stor nyttolast     | Uppladdad fil överskrider storleksgränsen.                                 |
| 500  | Internt serverfel | Oväntat serverfel.                                          |

## **Var bör du använda API:et för export av tabell till ett annat format?**

- **Migrering av äldre system**: Konvertera tusentals äldre XLS-filer till XLSX för moderna system.
- **Arkiveringsstandardisering**: Normalisera olika kalkylarksformat (XLS, XLSM, ODS, CSV) till ett enda format för arkivering.
- **Interoperabilitet med kontorsprogramvarupaket**: Konvertera Excel-filer till format som är kompatibla med LibreOffice, Google Sheets eller Apple Numbers.
- **Normalisering av datakällor**: Konvertera olika kalkylarksformat till CSV eller JSON för databasinläsning.
- **Webbpublicering**: Konvertera finansiella modeller till HTML för visning på webben.

## **Varför bör du använda API:et för export av tabell till ett annat format?**

- **Utvecklarvänligt**: Aspose.Cells Cloud erbjuder SDK-bibliotek i flera språk, vilket möjliggör snabb utveckling, samt tillhandahåller omfattande dokumentation. Jämfört med att bygga egna lösningar för diagramrendering minskas utvecklingsarbetet avsevärt.
- **Lägre arbetskostnader**: Minskar behovet av att tilldela personal till dokumentkonsolidering.
- **Betala per användning**: Inga förhandsinvesteringar; du betalar endast för API-anrop som faktiskt används.
- **Inga underhållskostnader**: Du behöver inte underhålla servrar, uppdatera programvara eller hantera kompatibilitetsproblem.
- **API:et returnerar endast råtabelldata utan någon arbetsboksformatering.**

## **Hur använder man API:et för export av kalkylarkstabell som format med SDK:er?**

### Exportera tabell som format-API-specifikation

<a href="https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Conversion/ExportTableAsFormat" target="_blank" rel="noopener noreferrer">API-specifikationen för Export Table as Format</a> definierar ett offentligt tillgängligt programmeringsgränssnitt och låter dig utföra REST-interaktioner direkt från en webbläsare.

Du kan använda kommandoradsverktyget cURL för enkelt att komma åt Aspose.Cells-webbtjänster. Följande exempel visar hur man gör anrop till moln-API:et med cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Förfrågan" tabName12="Svar" >}}

{{< tab tabNum="11" >}}

```bash
curl -X GET "https://api.aspose.cloud/v4.0/cells/MyWorkbook.xlsx/worksheets/Sheet1/tables/Table1?format=pdf" \
     -H "Authorization: Bearer {access_token}" \
     -H "Accept: application/octet-stream"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```
{
  "type": "FileContentResult",
  "fileContents": "byte[] (Base64-kodad)",
  "contentType": "MIME-typ",
  "fileDownloadName": "valfritt filnamn"
}
```

{{< /tab >}}

{{< /tabs >}}

### Använd Aspose.Cells Cloud SDK:er

Att använda SDK är det snabbaste sättet att utveckla, eftersom den döljer de lågnivådetaljer som krävs, så att du kan exportera en kalkylarkstabell till en fil i ett visst format med kort kod. Se <a href="https://github.com/aspose-cells-cloud" target="_blank" rel="noopener noreferrer">GitHub-förrådet</a> för en fullständig lista över Aspose.Cells Cloud SDK:er.

Följande kodexempel visar hur man gör anrop till Aspose.Cells-webbtjänster med olika SDK:er:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_ExportTableAsFormat.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_ExportTableAsFormat.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_ExportTableAsFormat.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_ExportTableAsFormat.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_ExportTableAsFormat.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_ExportTableAsFormat.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_ExportTableAsFormat.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_ExportTableAsFormat.go" >}}
{{</tab>}}
{{< /tabs >}}