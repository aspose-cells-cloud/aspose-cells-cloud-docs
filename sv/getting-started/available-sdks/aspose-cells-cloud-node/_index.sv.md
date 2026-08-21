---
title: "Aspose.Cells Cloud SDK för Node.js: Konvertera, sammanfoga, dela, skydda, söka, ersätta och mer."
second_title: "Dokument"
ArticleTitle: "Aspose.Cells Cloud SDK för Node.js: Konvertera, sammanfoga, dela, skydda, söka, ersätta och mer."
linktitle: "Aspose.Cells Cloud SDK för Node.js"
type: docs
url: /available-sdks/aspose-cells-cloud-node/
description: "Aspose.Cells Cloud SDK för Node.js erbjuder verklig plattformsoberoende kraft: en enda import ger Windows-, Linux- och macOS-utvecklare samma flytande API för att skapa, konvertera, sammanfoga, dela, skydda och manipulera alla Excel-objekt – ingen Office-installation krävs och inga plattformsspecifika justeringar behövs."
weight: 30
kwords: Node.js, Node.js SDK, Excel SDK för Node.js, Cloud SDK för Node.js, REST, Diagram, Pivot-tabell, Tabell-/listobjekt, Konvertera kalkylark, PDF, CSV, JSON, Markdown, Sammanfoga, Dela, Skydda, Söka, Ersätta
---

SDK:t är öppen källkod och licensierat under MIT-licensen. Du kan nå Node-bibliotekets källkod för Aspose.Cells Cloud [här](https://github.com/aspose-cells-cloud/aspose-cells-cloud-node).

# **Hur man använder Node-biblioteket för Aspose.Cells Cloud**

Aspose.Cells Cloud SDK för Node är ett kraftfullt bibliotek som låter utvecklare manipulera och bearbeta Microsoft Excel-filer med hjälp av programmeringsspråket Node. Med detta SDK kan du skapa, redigera och konvertera Excel-dokument i molnet utan att behöva installera ytterligare programvara eller beroenden på din lokala maskin.

I denna artikel kommer vi att undersöka hur man använder Aspose.Cells Cloud SDK för Node för att utföra några vanliga uppgifter, såsom att skapa ett nytt Excel-arbetsbok, infoga data i celler och spara den modifierade arbetsboken i molnet.

## Kom igång

Innan du börjar använda Aspose.Cells Cloud SDK för Go måste du ställa in din utvecklingsmiljö och installera nödvändiga beroenden. Se [den här artikeln](https://docs.aspose.cloud/cells/quickstart/) på Asposes webbplats för att få ditt klient-ID och klienthemlighet.

## Hur man installerar Node-paketet för Aspose.Cells Cloud

Du kan installera Aspose.Cells Cloud SDK för Node med hjälp av npm. Här är stegen för npm:

```Powershell

npm install asposecellscloud

```

## Hur man lägger till beroenden i paketkonfigurationen för Aspose.Cells Cloud

Node-konfigurationsfil: package.json

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

## Hur man använder Node-paketet för att konvertera Xlsx till andra format

- Importera Aspose.Cells Cloud-biblioteket  
  Börja med att importera det nödvändiga paketet från Aspose.Cells Cloud NodeJS SDK till ditt projekt.
- Konfigurera API-klienten med inloggningsuppgifter  
  Autentisera din API-klient med ditt unika klient-ID och klienthemlighet.
- Förbered konverteringsparametrar  
  Definiera parametrar för konverteringsuppgiften, inklusive källfilens namn, önskat utdataformat och lagringsmappens sökväg.
- Kör arbetsbokskonvertering  
  Anropa konverteringsprocessen med metoden PostConvertWorkbook och hantera svaret.

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_AvailableSDKs.ts" >}}