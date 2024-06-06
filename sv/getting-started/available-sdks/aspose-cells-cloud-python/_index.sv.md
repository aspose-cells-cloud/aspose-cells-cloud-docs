---
title: Aspose.Cells Cloud SDK för Pytho
second_title: Aspose.Cells Cloud Documen
type: docs
url: /sv/available-sdks/aspose-cells-cloud-python/
description: Aspose.Cells Cloud stöder Excel för att skapa, konvertera, sammanfoga, dela, skydda, inre objektoperation och så vidare
weight: 30
kwords: Excel, Office Cloud, REST API, Spreadsheet, PDF, CSV, Json, Markdwon, Python
---
 SDK:n är öppen källkod och licensierad under MIT-licensen. Du kan komma åt Python-bibliotekets källkod för Aspose.Cells Cloud[här](https://github.com/aspose-cells-cloud/aspose-cells-cloud-python).

# **Hur man använder Aspose.Cells Cloud SDK för Python**

Aspose.Cells Cloud SDK för Python är ett kraftfullt bibliotek som tillåter utvecklare att manipulera och bearbeta Microsoft Excel filer med hjälp av programmeringsspråket Python. Med denna SDK kan du skapa, redigera och konvertera Excel dokument i molnet, utan att installera ytterligare programvara eller beroenden på din lokala dator.

I den här artikeln kommer vi att utforska hur du använder Aspose.Cells Cloud SDK för Python för att utföra några vanliga uppgifter, som att skapa en ny Excel arbetsbok, infoga data i celler och spara den modifierade arbetsboken i molnet.

## Komma igång

 Innan du kan börja använda Aspose.Cells Cloud SDK för Go måste du konfigurera din utvecklingsmiljö och installera nödvändiga beroenden. Hänvisa till[artikeln](https://docs.aspose.cloud/cells/quickstart/) på webbplatsen Aspose för att få ditt klient-ID och klienthemlighet.

## Så här installerar du paketet Python för Aspose.Cells Cloud

Du kan installera Aspose.Cells Cloud SDK för Python med kommandot nedan:

```bash

    pip3 install AsposeCellsCloud
  
 ```

## Hur man använder Python-paketet för att konvertera Xlsx till PDF

- Importera Aspose.Cells Molnbibliotek
 Börja med att importera det nödvändiga paketet från Aspose.Cells Cloud Python SDK till ditt projekt.
- Konfigurera API klient med inloggningsuppgifter
 Autentisera din API-klient med ditt unika klient-ID och klienthemlighet.
- Förbered konverteringsparametrar
 Definiera parametrar för konverteringsuppgiften, inklusive källfilens namn, önskat utdataformat och lagringsmappens sökväg.
- Utför arbetsbokkonvertering
 Anropa konverteringsprocessen med PostConvertWorkbook-metoden och hantera svaret.

```python
import os
import sys
from asposecellscloud.apis.cells_api import CellsApi
from asposecellscloud.models import *
from asposecellscloud.requests import *

api  = CellsApi(os.getenv('CellsCloudClientId'),os.getenv('CellsCloudClientSecret'),"v3.0",os.getenv('CellsCloudApiBaseUrl'))
remote_folder = 'TestData/In'

local_name = 'Book1.xlsx'
remote_name = 'Book1.xlsx'

format = 'csv'

mapFiles = { 
    local_name: os.path.dirname(os.path.realpath(__file__)) + "/../TestData/" +local_name             
}
mapFiles = { 
    local_name:  local_name             
}
request =  UploadFileRequest( mapFiles, remote_folder + '/' + remote_name,storage_name= '')
api.upload_file(request)
 
request =  PutConvertWorkbookRequest( mapFiles,format= format)
api.put_convert_workbook(request)

```
