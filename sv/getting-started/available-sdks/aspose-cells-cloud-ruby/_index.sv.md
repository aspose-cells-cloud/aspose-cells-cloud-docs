---
title: Aspose.Cells Cloud SDK för Rub
second_title: Aspose.Cells Cloud Documen
type: docs
url: /sv/available-sdks/aspose-cells-cloud-ruby/
description: Aspose.Cells Cloud stöder Excel för att skapa, konvertera, sammanfoga, dela, skydda, inre objektoperation och så vidare
weight: 30
kwords: Excel, Office Cloud, REST API, Spreadsheet, PDF, CSV, Json, Markdwon, Ruby
---
 SDK:n är öppen källkod och licensierad under MIT-licensen. Du kan komma åt Ruby-bibliotekets källkod för Aspose.Cells Cloud[här](https://github.com/aspose-cells-cloud/aspose-cells-cloud-ruby).

# **Hur man använder Aspose.Cells Cloud SDK för Ruby**

Aspose.Cells Cloud SDK för Ruby är ett kraftfullt bibliotek som tillåter utvecklare att manipulera och bearbeta Microsoft Excel filer med hjälp av Rubys programmeringsspråk. Med denna SDK kan du skapa, redigera och konvertera Excel dokument i molnet, utan att installera ytterligare programvara eller beroenden på din lokala dator.

I den här artikeln kommer vi att utforska hur du använder Aspose.Cells Cloud SDK för Ruby för att utföra några vanliga uppgifter, som att skapa en ny Excel-arbetsbok, infoga data i celler och spara den modifierade arbetsboken i molnet.

## Komma igång

 Innan du kan börja använda Aspose.Cells Cloud SDK för Go måste du konfigurera din utvecklingsmiljö och installera nödvändiga beroenden. Hänvisa till[artikeln](https://docs.aspose.cloud/cells/quickstart/) på webbplatsen Aspose för att få ditt klient-ID och klienthemlighet.

## Hur man installerar Ruby-paketet för Aspose.Cells Cloud

Du kan installera Aspose.Cells Cloud SDK för Ruby genom kommandot nedan:

```bash

    gem install aspose_cells_cloud
  
 ```

## Hur man använder Ruby-paketet för att konvertera Xlsx till PDF

- Importera Aspose.Cells Molnbibliotek
 Börja med att importera det nödvändiga paketet från Aspose.Cells Cloud Python SDK till ditt projekt.
- Konfigurera API klient med inloggningsuppgifter
 Autentisera din API-klient med ditt unika klient-ID och klienthemlighet.
- Förbered konverteringsparametrar
 Definiera parametrar för konverteringsuppgiften, inklusive källfilens namn, önskat utdataformat och lagringsmappens sökväg.
- Utför arbetsbokkonvertering
 Anropa konverteringsprocessen med PostConvertWorkbook-metoden och hantera svaret.

```Ruby
require 'openssl'
require 'bundler'
require 'aspose_cells_cloud'

@instance = AsposeCellsCloud::CellsApi.new(ENV['CellsCloudClientId'], ENV['CellsCloudClientSecret'],'v3.0',ENV['CellsCloudApiBaseUrl'])

remote_folder = 'TestData/In'

local_name = 'Book1.xlsx'
remote_name = 'Book1.xlsx'

format = "csv"

    
mapFiles = { }   
mapFiles = { }               
mapFiles[local_name] = ::File.open(File.expand_path("TestData/"+local_name),"r")  
 
uploadrequest = AsposeCellsCloud::UploadFileRequest.new( { :UploadFiles=>mapFiles,:path=>remote_folder })
@instance.upload_file(uploadrequest)
mapFiles[local_name]= ::File.open(File.expand_path("TestData/"+local_name),"r")
request =   AsposeCellsCloud::PutConvertWorkbookRequest.new(:File=>mapFiles,:format=>format);
@instance.put_convert_workbook(request);


```
