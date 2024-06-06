---
title: Aspose.Cells Cloud SDK för Per
second_title: Aspose.Cells Cloud Documen
type: docs
url: /sv/available-sdks/aspose-cells-cloud-perl/
description: Aspose.Cells Cloud stöder Excel för att skapa, konvertera, sammanfoga, dela, skydda, inre objektoperation och så vidare
weight: 30
kwords: Excel, Office Cloud, REST API, Spreadsheet, PDF, CSV, Json, Markdwon, Perl
---
 SDK:n är öppen källkod och licensierad under MIT-licensen. Du kan komma åt Perl-bibliotekets källkod för Aspose.Cells Cloud[här](https://github.com/aspose-cells-cloud/aspose-cells-cloud-perl).


# **Hur man använder Perl-biblioteket i Aspose.Cells Cloud**

Aspose.Cells Cloud SDK för Perl är ett kraftfullt bibliotek som tillåter utvecklare att manipulera och bearbeta Microsoft Excel filer med hjälp av programmeringsspråket Perl. Med denna SDK kan du skapa, redigera och konvertera Excel dokument i molnet, utan att installera ytterligare programvara eller beroenden på din lokala dator.

I den här artikeln kommer vi att utforska hur du använder Aspose.Cells Cloud SDK för Perl för att utföra några vanliga uppgifter, som att skapa en ny Excel arbetsbok, infoga data i celler och spara den modifierade arbetsboken i molnet.

## Komma igång

 Innan du kan börja använda Aspose.Cells Cloud SDK för Go måste du konfigurera din utvecklingsmiljö och installera nödvändiga beroenden. Hänvisa till[artikeln](https://docs.aspose.cloud/cells/quickstart/) på webbplatsen Aspose för att få ditt klient-ID och klienthemlighet.

## Så här installerar du paketet Perl för Aspose.Cells Cloud

Du kan installera Aspose.Cells Cloud SDK för Perl med kommandot nedan:

```Powershell

perl -MCPAN -e shell

install AsposeCellsCloud::CellsApi

```

## Hur man använder Perl-paketet för att konvertera Xlsx till PDF

- Importera Aspose.Cells Molnbibliotek
 Börja med att importera det nödvändiga paketet från Aspose.Cells Cloud Perl SDK till ditt projekt.
- Konfigurera API klient med inloggningsuppgifter
 Autentisera din API-klient med ditt unika klient-ID och klienthemlighet.
- Förbered konverteringsparametrar
 Definiera parametrar för konverteringsuppgiften, inklusive källfilens namn, önskat utdataformat och lagringsmappens sökväg.
- Utför arbetsbokkonvertering
 Anropa konverteringsprocessen med PostConvertWorkbook-metoden och hantera svaret.

```Perl
use lib 'lib';
use strict;
use warnings;
use File::Slurp;
use MIME::Base64;
use AsposeCellsCloud::CellsApi;

my $config = AsposeCellsCloud::Configuration->new( client_id => $ENV{'CellsCloudClientId'}, client_secret => $ENV{'CellsCloudClientSecret'});
my $instance = AsposeCellsCloud::CellsApi->new(AsposeCellsCloud::ApiClient->new( $config));

my $remoteFolder = 'TestData/In';
  
my $localName = 'Book1.xlsx';
my $remoteName = 'Book1.xlsx';

my $upload_file_request = AsposeCellsCloud::Request::UploadFileRequest->new( 'UploadFiles'=>{ $localName => $localName  }  ,'path'=>$remoteFolder . '/' . $remoteName );
 
my $format = 'csv';

my $mapFiles = {};           

 $mapFiles->{$localName}= "TestData/".$localName ;

my $request = AsposeCellsCloud::Request::PutConvertWorkbookRequest->new();
$request->{file} =  $mapFiles;
$request->{format} =  $format;
$instance->put_convert_workbook(request=> $request);
```
