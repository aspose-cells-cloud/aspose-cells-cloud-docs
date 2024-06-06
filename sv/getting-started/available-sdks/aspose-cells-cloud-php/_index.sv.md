---
title: Aspose.Cells Cloud SDK för PH
second_title: Aspose.Cells Cloud Documen
type: docs
url: /sv/available-sdks/aspose-cells-cloud-php/
description: Aspose.Cells Cloud stöder Excel för att skapa, konvertera, sammanfoga, dela, skydda, inre objektoperation och så vidare
weight: 30
kwords: Excel, Office Cloud, REST API, Spreadsheet, PDF, CSV, Json, Markdwon, PHP
---
 SDK:n är öppen källkod och licensierad under MIT-licensen. Du kan komma åt PHP-bibliotekets källkod för Aspose.Cells Cloud[här](https://github.com/aspose-cells-cloud/aspose-cells-cloud-php).

# **Hur man använder Aspose.Cells Cloud SDK för PHP**

Aspose.Cells Cloud SDK för PHP är ett kraftfullt bibliotek som tillåter utvecklare att manipulera och bearbeta Microsoft Excel filer med hjälp av programmeringsspråket Go. Med denna SDK kan du skapa, redigera och konvertera Excel dokument i molnet, utan att installera ytterligare programvara eller beroenden på din lokala dator.

I den här artikeln kommer vi att utforska hur du använder Aspose.Cells Cloud SDK för PHP för att utföra några vanliga uppgifter, som att skapa en ny Excel arbetsbok, infoga data i celler och spara den modifierade arbetsboken i molnet.

## Komma igång

 Innan du kan börja använda Aspose.Cells Cloud SDK för Go måste du konfigurera din utvecklingsmiljö och installera nödvändiga beroenden. Hänvisa till[artikeln](https://docs.aspose.cloud/cells/quickstart/) på webbplatsen Aspose för att få ditt klient-ID och klienthemlighet.

## Så här installerar du paketet PHP för Aspose.Cells Cloud

Du kan installera Aspose.Cells Cloud SDK för PHP. Nedan följer stegen:

- Lägg till Aspose.Cells Cloud som ett beroende till din `composer.json`-fil:

   ```json
   {
       "require": {
           "aspose/cells-cloud": "^24.3"
       }
   }
   ```

- Kör Composer update för att installera SDK:n:

   ```bash

   composer install

   ```

- Inkludera Composers autoloader i din PHP-kod:

   ```php

   require 'vendor/autoload.php';

   ```

## Hur man använder PHP-paketet för att konvertera Xlsx till PDF

- Importera Aspose.Cells Molnbibliotek
 Börja med att importera det nödvändiga paketet från Aspose.Cells Cloud PHP SDK till ditt projekt.
- Konfigurera API klient med inloggningsuppgifter
 Autentisera din API-klient med ditt unika klient-ID och klienthemlighet.
- Förbered konverteringsparametrar
 Definiera parametrar för konverteringsuppgiften, inklusive källfilens namn, önskat utdataformat och lagringsmappens sökväg.
- Utför arbetsbokkonvertering
 Anropa konverteringsprocessen med PostConvertWorkbook-metoden och hantera svaret.

```PHP
<?php
require_once('vendor\autoload.php');
use \Aspose\Cells\Cloud\Api\CellsApi;
use \Aspose\Cells\Cloud\Request\PutConvertWorkbookRequest;

$cellsApi = new CellsApi(getenv("CellsCloudClientId"),getenv("CellsCloudClientSecret"),"v3.0",getenv("CellsCloudApiBaseUrl"));

$remoteFolder = "TestData/In";

$localName = "Book1.xlsx";
$remoteName = "Book1.xlsx";

$format = "csv";

$mapFiles = array ();
$mapFiles[$localName] = CellsApiTestBase::getfullfilename($localName);
CellsApiTestBase::ready(  $this->instance,$localName ,$remoteFolder . "/" . $remoteName ,  "");
 
$request = new PutConvertWorkbookRequest();
$request->setFile( $mapFiles);
$request->setFormat( $format);
$$cellsApi->putConvertWorkbook($request);
```
