---
title: "Aspose.Cells Cloud SDK för PHP: Konvertera, slå samman, dela, skydda, sök, ersätt med mera"
second_title: Documen
ArticleTitle: "Aspose.Cells Cloud SDK for PHP: Convert, merge, split, protect, search, replace, and more"
linktitle: Aspose.Cells Cloud SDK för PH
type: docs
url: /sv/available-sdks/aspose-cells-cloud-php/
description: "Aspose.Cells Cloud SDK för PHP erbjuder verklig plattformsoberoende kraft: en import ger Windows-, Linux- och macOS-utvecklare samma flytande API för att skapa, konvertera, slå samman, dela, skydda och manipulera alla Excel-objekt – ingen Office-installation krävs och inga plattformsspecifika justeringar behövs."
weight: 30
kwords: PHP SDK, Excel SDK för PHP, Cloud SDK för PHP, REST, Diagram, Pivottabell, Tabell-/listobjekt, Konvertera kalkylblad, PDF, CSV, Json, Markdown, Sammanfoga, Dela, Skydda, Sök, Ersätt
---
SDK:et är öppen källkod och licensierat under MIT-licensen. Du kan komma åt[PHP-bibliotekets källkod för Aspose.Cells Cloud](https://github.com/aspose-cells-cloud/aspose-cells-cloud-php).

# **Hur man använder Aspose.Cells Cloud SDK för PHP**

Aspose.Cells Cloud SDK för PHP är ett kraftfullt bibliotek som låter utvecklare manipulera och bearbeta Microsoft Excel-filer med programmeringsspråket Go. Med detta SDK kan du skapa, redigera och konvertera Excel-dokument i molnet, utan att installera ytterligare programvara eller beroenden på din lokala dator.

den här artikeln ska vi utforska hur man använder Aspose.Cells Cloud SDK för PHP för att utföra några vanliga uppgifter, till exempel att skapa en ny Excel-arbetsbok, infoga data i celler och spara den modifierade arbetsboken i molnet.

## Komma igång

 Innan du kan börja använda Aspose.Cells Cloud SDK för Go måste du konfigurera din utvecklingsmiljö och installera nödvändiga beroenden. Se[artikeln](https://docs.aspose.cloud/cells/quickstart/) på webbplatsen Aspose för att få ditt klient-ID och din klienthemlighet.

## Så här installerar du PHP-paketet för Aspose.Cells Cloud

Du kan installera Aspose.Cells Cloud SDK för PHP. Nedan följer stegen:

- Lägg till Aspose.Cells Cloud som ett beroende till din `composer.json`-fil:

   ```json
   {
       "require": {
           "aspose/cells-cloud": "^24.3"
       }
   }
   ```

- Kör Composer-uppdateringen för att installera SDK:n:

   ```bash

   composer install

   ```

- Inkludera Composers autoloader i din PHP-kod:

   ```php

   require 'vendor/autoload.php';

   ```

## Hur man använder PHP-paketet för att konvertera Xlsx till andra format

- Importera Aspose.Cells Molnbibliotek
 Börja med att importera det nödvändiga paketet från Aspose.Cells Cloud PHP SDK till ditt projekt.
- Konfigurera API-klienten med autentiseringsuppgifter
 Autentisera din API-klient med ditt unika klient-ID och din klienthemlighet.
- Förbered konverteringsparametrar
 Definiera parametrar för konverteringsuppgiften, inklusive källfilens namn, önskat utdataformat och sökvägen till lagringsmappen.
- Kör arbetsbokskonvertering
 Anropa konverteringsprocessen med hjälp av PostConvertWorkbook-metoden och hantera svaret.

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_AvailableSDKs.php" >}}
