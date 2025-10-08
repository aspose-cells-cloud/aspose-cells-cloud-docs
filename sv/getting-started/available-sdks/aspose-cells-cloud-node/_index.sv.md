---
title: "Aspose.Cells Cloud SDK för Node.js: Konvertera, slå samman, dela, skydda, sök, ersätt med mera"
second_title: Documen
ArticleTitle: "Aspose.Cells Cloud SDK for Node.js: Convert, merge, split, protect, search, replace, and more"
linktitle: Aspose.Cells Cloud SDK för Node.j
type: docs
url: /sv/available-sdks/aspose-cells-cloud-node/
description: "Aspose.Cells Cloud SDK för Node.js erbjuder verklig plattformsoberoende kraft: en import ger Windows-, Linux- och macOS-utvecklare samma flytande API för att skapa, konvertera, slå samman, dela, skydda och manipulera varje Excel objekt – ingen Office installation krävs och inga plattformsspecifika justeringar behövs."
weight: 30
kwords: Node.js, Node.js SDK, Excel SDK för Node.js, Cloud SDK för Node.js, REST, Diagram, Pivottabell, Tabell-/Listobjekt, Konvertera kalkylblad, PDF, CSV, Json, Markdown, Sammanfoga, Dela, Skydda, Sök, Ersätt
---
SDK:et är öppen källkod och licensierat under MIT-licensen. Du kan komma åt[Nodbibliotekets källkod för Aspose.Cells Cloud](https://github.com/aspose-cells-cloud/aspose-cells-cloud-node).

# **Hur man använder nodbiblioteket i Aspose.Cells Cloud**

Aspose.Cells Cloud SDK för Node är ett kraftfullt bibliotek som låter utvecklare manipulera och bearbeta Microsoft Excel-filer med hjälp av programmeringsspråket Node. Med detta SDK kan du skapa, redigera och konvertera Excel-dokument i molnet, utan att installera ytterligare programvara eller beroenden på din lokala dator.

I den här artikeln ska vi utforska hur man använder Aspose.Cells Cloud SDK för Node för att utföra några vanliga uppgifter, till exempel att skapa en ny Excel-arbetsbok, infoga data i celler och spara den modifierade arbetsboken i molnet.

## Komma igång

 Innan du kan börja använda Aspose.Cells Cloud SDK för Go måste du konfigurera din utvecklingsmiljö och installera nödvändiga beroenden. Se[artikeln](https://docs.aspose.cloud/cells/quickstart/) på webbplatsen Aspose för att få ditt klient-ID och din klienthemlighet.

## Så här installerar du Node-paketet för Aspose.Cells Cloud

Du kan installera Aspose.Cells Cloud SDK för Node med hjälp av npm. Nedan följer stegen för npm:

```Powershell

npm install asposecellscloud

```

## Hur man lägger till beroenden i paketkonfigurationen för Aspose.Cells Cloud

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

## Hur man använder Node-paketet för att konvertera Xlsx till andra format

- Importera Aspose.Cells Molnbibliotek
 Börja med att importera det nödvändiga paketet från Aspose.Cells Cloud NodeJS SDK till ditt projekt.
- Konfigurera API-klienten med autentiseringsuppgifter
 Autentisera din API-klient med ditt unika klient-ID och din klienthemlighet.
- Förbered konverteringsparametrar
 Definiera parametrar för konverteringsuppgiften, inklusive källfilens namn, önskat utdataformat och sökvägen till lagringsmappen.
- Kör arbetsbokskonvertering
 Anropa konverteringsprocessen med hjälp av PostConvertWorkbook-metoden och hantera svaret.

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_AvailableSDKs.ts" >}}
