---
title: "Gruppera kolumner – Aspise.Cells Molntjänst-API-dokumentation"
description: "Gruppera kolumner i ett kalkylblad i Excel med Aspose.Cells Cloud REST API (v3.0). Innehåller begäran syntax, parametrar, cURL- och SDK-exempel samt svarsinformation."
keywords: "Aspose.Cells, gruppera kolumner, Excel-API, REST, moln-SDK"
weight: 60
type: docs
aliases:
  - /group-columns-in-an-excel-worksheet/
  - /group-columns-in-excel-worksheet/
---

# Gruppera kolumner i ett Excel-kalkylblad

**API-version:** v3.0  
**Åtgärd:** `PostGroupWorksheetColumns` – Gruppera kolumner i ett kalkylblad.

---

## Översikt

Detta REST API låter dig gruppera ett intervall av kolumner i ett kalkylblad. Grupperade kolumner kan visas eller döljas, vilket möjliggör skapandet av collapsebara sektioner, liknande de i Microsoft Excel.

---

## Förutsättningar

- En giltig **JWT-åtkomsttoken** som hämtats från Aspose Cloud:s autentiseringstjänst.  
- Arbetshandboken måste lagras på en plats som Aspose.Cells Cloud har tillgång till (standardlagring eller ett anpassat lagringsnamn).  
- Nödvändig SDK-version (om en SDK används): den senaste utgåvan som stöder API-version **v3.0**.  

---

## Autentisering

Alla begäranden kräver **Bearer token**-autentisering.

```http
Authorization: Bearer <access_token>
```

För detaljer om hur du hämtar en token, se [JWT-autentiseringsguide](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/).

---

## HTTP-begäran

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/columns/group
```

| Parameter | Plats | Krävs | Beskrivning |
|-----------|-------|-------|-------------|
| `name` | Sökväg | Ja | Arbetshandbokens filnamn (t.ex. `test.xlsx`). |
| `sheetName` | Sökväg | Ja | Kalkylbladet som innehåller de kolumner som ska grupperas. |
| `firstIndex` | Frågeparameter | Ja | Nollbaserat index för den första kolumnen som ska ingå i gruppen. |
| `lastIndex` | Frågeparameter | Ja | Nollbaserat index för den sista kolumnen som ska ingå i gruppen. |
| `hide` | Frågeparameter | Nej | Om `true` döljs de grupperade kolumnerna; annars förblir de synliga. |
| `folder` | Frågeparameter | Nej | Sökväg till mappen som innehåller arbetshandboken. |
| `storageName` | Frågeparameter | Nej | Namn på lagringstjänsten där filen finns. |

---

## Exempel på begäran (cURL)

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/cells/columns/group?firstIndex=1&lastIndex=2&hide=true" \
     -H "accept: application/json" \
     -H "Authorization: Bearer <access_token>"
```

> **Obs:** Begäran använder **HTTPS** för att säkerställa krypterad kommunikation.

---

## Svar

### Lyckad (200)

| Fält | Typ | Beskrivning |
|------|-----|-------------|
| `Code` | heltal | HTTP-statuskod (`200`). |
| `Status` | sträng | Textuell status för åtgärden (`OK`). |

**Exempel**

```json
{
  "Code": 200,
  "Status": "OK"
}
```

### Fel (t.ex. 400 Bad Request)

| Fält | Typ | Beskrivning |
|------|-----|-------------|
| `Code` | heltal | HTTP-statuskod (`400`, `401`, `404`, `500`, …). |
| `Status` | sträng | Textuell status (`Error`). |
| `ErrorMessage` | sträng | Människoläsbar beskrivning av problemet. |
| `ErrorCode` | sträng | Programmatiskt identifieringsnamn för felet. |

**Exempel – Bad Request**

```json
{
  "Code": 400,
  "Status": "Error",
  "ErrorMessage": "Ogiltigt kolumnindex.",
  "ErrorCode": "InvalidParameter"
}
```

---

## SDK-exempel

Följande kodsnuttar visar hur man anropar operationen **Gruppera kolumner i kalkylblad** med de SDK:er som stöds.

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostGroupWorksheetColumns.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostGroupWorksheetColumns.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostGroupWorksheetColumns.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostGroupWorksheetColumns.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostGroupWorksheetColumns.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostGroupWorksheetColumns.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostGroupWorksheetColumns.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostGroupWorksheetColumns.go" >}}

{{< /tab >}}

{{< /tabs >}}

---

## Anmärkningar

- **Grupperingsbeteende:** API:t skapar en kolumngrupp som kan expanderas eller kollapsas i Excel. Om `hide=true` sätts kollapsas gruppen omedelbart.  
- **Nollbaserad indexerings:** Både `firstIndex` och `lastIndex` börjar på **0**; den första kolumnen i ett kalkylblad har index 0.  
- **Lagringsöverväganden:** Om arbetshandboken finns i en icke-standardlagring måste du ange både `folder` och `storageName` som frågeparametrar.  

---

## Se även

- [Autentisering – JWT-tokenbaserad](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/)  
- [OpenAPI-specifikation för Gruppera kolumner i kalkylblad](https://apireference.aspose.cloud/cells/#/Cells/PostGroupWorksheetColumns)  
- [Aspose.Cells Cloud SDK:er (GitHub)](https://github.com/aspose-cells-cloud)  
- [Gruppera rader i ett Excel-kalkylblad](/rows/group/)  

---

> *Illustration:* ![Skärmbild som visar grupperade kolumner i ett Excel-kalkylblad](./images/group-columns.png){: .img-fluid alt="Skärmbild som visar grupperade kolumner i ett Excel-kalkylblad" }

*Ovanstående platsinnehålls-bild bör ersättas med en faktisk skärmbild som visar det visuella resultatet av att gruppera kolumner.*