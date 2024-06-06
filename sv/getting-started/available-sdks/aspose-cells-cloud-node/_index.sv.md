---
title: Aspose.Cells Cloud SDK för Nod
second_title: Aspose.Cells Cloud Documen
type: docs
url: /sv/available-sdks/aspose-cells-cloud-node/
description: Aspose.Cells Cloud stöder Excel för att skapa, konvertera, sammanfoga, dela, skydda, inre objektoperation och så vidare
weight: 30
kwords: Excel, Office Cloud, REST API, Spreadsheet, PDF, CSV, Json, Markdwon, Node
---
 SDK:n är öppen källkod och licensierad under MIT-licensen. Du kan komma åt nodbibliotekets källkod för Aspose.Cells Cloud[här](https://github.com/aspose-cells-cloud/aspose-cells-cloud-node).


# **Hur man använder Node-biblioteket i Aspose.Cells Cloud**

Aspose.Cells Cloud SDK för Node är ett kraftfullt bibliotek som gör det möjligt för utvecklare att manipulera och bearbeta Microsoft Excel-filer med hjälp av Node-programmeringsspråket. Med denna SDK kan du skapa, redigera och konvertera Excel dokument i molnet, utan att installera ytterligare programvara eller beroenden på din lokala dator.


den här artikeln kommer vi att utforska hur du använder Aspose.Cells Cloud SDK för Node för att utföra några vanliga uppgifter, som att skapa en ny Excel-arbetsbok, infoga data i celler och spara den modifierade arbetsboken i molnet.

## Komma igång

 Innan du kan börja använda Aspose.Cells Cloud SDK för Go måste du konfigurera din utvecklingsmiljö och installera nödvändiga beroenden. Hänvisa till[artikeln](https://docs.aspose.cloud/cells/quickstart/) på webbplatsen Aspose för att få ditt klient-ID och klienthemlighet.

## Så här installerar du Node-paketet för Aspose.Cells Cloud

Du kan installera Aspose.Cells Cloud SDK för Node med npm. Nedan följer stegen för npm:


```Powershell

npm install asposecellscloud

```

## Hur man lägger till beroenden i paketkonfiguration för Aspose.Cells Cloud

nodkonfigurationsfil: package.json

```Node

{
    "requires": true,
    "lockfileVersion": 1,
    "dependencies": {
        "@types/jest": "^26.0.24",
        "@types/request": "^2.48.7",
        "asposecellscloud": "24.4",
        "axios": "^1.5.1",
        "JSON": "^1.0.0",
        "mocha": "^10.2.0",
        "request": "^2.88.2",
        "request-debug": "^0.2.0"
    }
}

```

## Hur man använder Node-paketet för att konvertera Xlsx till PDF

- Importera Aspose.Cells Molnbibliotek
 Börja med att importera det nödvändiga paketet från Aspose.Cells Cloud NodeJS SDK till ditt projekt.
- Konfigurera API klient med inloggningsuppgifter
 Autentisera din API-klient med ditt unika klient-ID och klienthemlighet.
- Förbered konverteringsparametrar
 Definiera parametrar för konverteringsuppgiften, inklusive källfilens namn, önskat utdataformat och lagringsmappens sökväg.
- Utför arbetsbokkonvertering
 Anropa konverteringsprocessen med PostConvertWorkbook-metoden och hantera svaret.

```javascript
var fs = require('fs');
var path = require('path');
const _ = require('asposecellscloud');

const cellsApi = new CellsApi(process.env.CellsCloudClientId, process.env.CellsCloudClientSecret,"v3.0",process.env.CellsCloudApiBaseUrl);

var remoteFolder = "TestData/In"
  
var localName = "Book1.xlsx"
var remoteName = "Book1.xlsx"

var localNameRequest = new  model.UploadFileRequest();
localNameRequest.uploadFiles ={localName:fs.createReadStream(localPath  + localName)};
localNameRequest.path = remoteFolder + "/" + remoteName ;
localNameRequest.storageName ="";
cellsApi.uploadFile(localNameRequest );
 
var format = "csv"

var mapFiles = {};           

 mapFiles[localName]= fs.createReadStream(localPath  +localName) ;

var request = new model.PutConvertWorkbookRequest();
request.file =  mapFiles;
request.format =  format;
return cellsApi.putConvertWorkbook(request).then((result) => {
    expect(result.response.statusCode).to.equal(200);
});
```
