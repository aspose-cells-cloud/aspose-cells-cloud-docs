---
title: Aspose.Cells Cloud SDK för Ne
second_title: Aspose.Cells Cloud Documen
type: docs
url: /sv/available-sdks/aspose-cells-cloud-net/
description: Aspose.Cells Molnet stöder Excel för att skapa, konvertera, sammanfoga, dela, skydda, hantera interna objekt och så vidare.
weight: 30
kwords: Excel, Office Moln, REST API, Kalkylblad, PDF, CSV, Json, Markdown, Nät
---
 SDK:et är öppen källkod och licensierat under MIT-licensen. Du kan komma åt Net-bibliotekets källkod för Aspose.Cells Cloud.[här](https://github.com/aspose-cells-cloud/aspose-cells-cloud-dotnet).

# **Hur man använder nätbiblioteket i Aspose.Cells Cloud**

Aspose.Cells Cloud SDK för Net är ett kraftfullt bibliotek som låter utvecklare manipulera och bearbeta Microsoft Excel-filer med hjälp av programmeringsspråket Net. Med detta SDK kan du skapa, redigera och konvertera Excel-dokument i molnet, utan att installera ytterligare programvara eller beroenden på din lokala dator.

I den här artikeln ska vi utforska hur man använder Aspose.Cells Cloud SDK for Net för att utföra några vanliga uppgifter, som att skapa en ny Excel-arbetsbok, infoga data i celler och spara den modifierade arbetsboken i molnet.

## Komma igång

 Innan du kan börja använda Aspose.Cells Cloud SDK för Go måste du konfigurera din utvecklingsmiljö och installera nödvändiga beroenden. Se[artikeln](https://docs.aspose.cloud/cells/quickstart/) på webbplatsen Aspose för att få ditt klient-ID och din klienthemlighet.

## Hur man installerar Net-paketet för Aspose.Cells Cloud

Du kan installera Aspose.Cells Cloud SDK for Net med hjälp av nuget. Nedan följer stegen för nuget:

```nuget

Install-Package Aspose.Cells-Cloud

```

Du kan även installera Aspose.Cells Cloud SDK for Net med hjälp av dotnet. Nedan följer stegen för dotnet:

```powershell

dotnet add package Aspose.Cells-Cloud

```

## Hur man använder Net-paketet för att konvertera Xlsx till PDF

- Importera Aspose.Cells Molnbibliotek
 Börja med att importera det nödvändiga paketet från Aspose.Cells Cloud DotNet SDK till ditt projekt.
- Konfigurera API-klienten med autentiseringsuppgifter
 Autentisera din API-klient med ditt unika klient-ID och din klienthemlighet.
- Förbered konverteringsparametrar
 Definiera parametrar för konverteringsuppgiften, inklusive källfilens namn, önskat utdataformat och sökvägen till lagringsmappen.
- Kör arbetsbokskonvertering
 Anropa konverteringsprocessen med hjälp av PostConvertWorkbook-metoden och hantera svaret.

### **Exempelkod**

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example_AvailableSDKs.cs" >}}
