---
title: "Aspose.Cells Cloud PHP SDK – Konvertera, sammanfoga, dela, skydda Excel-filer"  
second_title: "Dokument"  
ArticleTitle: "Aspose.Cells Cloud PHP SDK – Konvertera, sammanfoga, dela, skydda Excel-filer"  
linktitle: "Aspose.Cells Cloud PHP SDK"  
type: docs  
url: /sv/available-sdks/aspose-cells-cloud-php/
description: "Ladda ner Aspose.Cells Cloud PHP SDK (v24.3). Lär dig hur du installerar via Composer, autentiserar, konverterar XLSX till PDF/CSV, sammanfogar arbetsböcker, skyddar ark med mera – allt utan att installera Office."  
keywords: "Aspose.Cells, moln, PHP, SDK, Excel, konvertera, sammanfoga, dela, skydda"  
weight: 30  
---  

SDK:et är öppen källkod och licensierat under MIT-licensen. Du kan nå källkoden för PHP-biblioteket för Aspose.Cells Cloud <a href="https://github.com/aspose-cells-cloud/aspose-cells-cloud-php" target="_blank" rel="noopener noreferrer">här</a>.

# **Hur man använder Aspose.Cells Cloud SDK för PHP**

Aspose.Cells Cloud SDK för PHP är ett kraftfullt bibliotek som låter utvecklare manipulera och bearbeta Microsoft Excel-filer med **PHP-programmeringsspråket**. Med detta SDK kan du skapa, redigera och konvertera Excel-dokument i molnet, utan att behöva installera ytterligare programvara eller beroenden på din lokala maskin.

I detta artikel kommer vi att undersöka hur man använder Aspose.Cells Cloud SDK för PHP för att utföra några vanliga uppgifter, såsom att skapa en ny Excel-arbetsbok, infoga data i celler och spara den modifierade arbetsboken i molnet.

## Komma igång

Innan du börjar använda Aspose.Cells Cloud SDK för **PHP**, måste du konfigurera din utvecklingsmiljö och installera nödvändiga beroenden. Se <a href="https://docs.aspose.cloud/cells/quickstart/" target="_blank" rel="noopener noreferrer">artikeln</a> på Asposes webbplats för att erhålla ditt klient-ID och klienthemlighet.

**Förutsättningar**

- PHP 7.4 eller senare  
- Composer installerat på din utvecklingsmaskin  
- Giltigt Aspose Cloud klient-ID och klienthemlighet  
- Åtkomst till en Aspose Cloud-lagringsplats (standard eller anpassad)  

## Hur man installerar PHP-paketet för Aspose.Cells Cloud

Du kan installera Aspose.Cells Cloud SDK för PHP. Nedan finns stegen:

- Lägg till Aspose.Cells Cloud som ett beroende i din `composer.json`-fil:

   ```json
   {
       "require": {
           "aspose/cells-cloud": "^24.3"
       }
   }
   ```

- Kör Composer-uptimering för att installera SDK:et:

   ```bash
   composer install
   ```

- Inkludera Composers autoloader i din PHP-kod:

   ```php
   require 'vendor/autoload.php';
   ```

## Hur man använder PHP-paketet för att konvertera Xlsx till andra format

- Importera Aspose.Cells Cloud-biblioteket  
  Börja med att importera det nödvändiga paketet från Aspose.Cells Cloud PHP SDK till ditt projekt.

- Konfigurera API-klienten med autentiseringsuppgifter  
  Autentisera din API-klient med ditt unika klient-ID och klienthemlighet.

- Förbered konverteringsparametrar  
  Definiera parametrar för konverteringsuppgiften, inklusive källfilens namn, önskat utdataformat och lagringsmappens sökväg.

- Kör arbetsbokskonvertering  
  Anropa konverteringsprocessen med metoden `PostConvertWorkbook` och hantera svaret.

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_AvailableSDKs.php" >}}

### API-referens för `PostConvertWorkbook`

| Parameter      | Beskrivning                                   | Typ    | Krävs |
|----------------|-----------------------------------------------|--------|-------|
| `file`         | Namn på käll-Excel-filen (t.ex. `sample.xlsx`). | string | Ja    |
| `format`       | Önskat utdataformat (`pdf`, `csv`, `png`, etc.). | string | Ja    |
| `storage`      | Lagringsnamn eller mappsökväg där källfilen finns. | string | Nej   |
| `outPath`      | Valfri sökväg för att spara den konverterade filen direkt i lagringen. | string | Nej   |

**HTTP-metod:** POST  
**Endpoint:** `/cells/convert/{format}`  

**Exempel på svar (JSON)**  

```json
{
  "status": "OK",
  "url": "https://api.aspose.cloud/v3.0/cells/convert/output.pdf"
}
```

**Statuskoder**

- `200` – Konvertering lyckades.  
- `400` – Felaktig begäran (parametrar saknas eller är ogiltiga).  
- `401` – Autentisering misslyckades.  
- `500` – Serverfel.  
---