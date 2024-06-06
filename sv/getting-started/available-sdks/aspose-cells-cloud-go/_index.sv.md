---
title: Aspose.Cells Cloud SDK för G
second_title: Aspose.Cells Cloud Documen
type: docs
url: /sv/available-sdks/aspose-cells-cloud-go/
description: Aspose.Cells Cloud SDK for Go ger starkt plattformsoberoende stöd för Go-utvecklare, vilket gör det enkelt att integrera och använda för Windows, Linux eller macOS. Den stöder Excel för att skapa, konvertera, sammanfoga, dela, skydda, inre objektoperation och så vidare
weight: 30
kwords: Go, Excel, Office Cloud, REST API, diagram, pivottabell, tabell, kalkylblad, PDF, CSV, Json, Markdown
---
 SDK:n är öppen källkod och licensierad under MIT-licensen. Du kan komma åt Go-bibliotekets källkod för Aspose.Cells Cloud[här](https://github.com/aspose-cells-cloud/aspose-cells-cloud-go).

# **Hur man använder Go-biblioteket i Aspose.Cells Cloud**

Aspose.Cells Cloud SDK för Go är ett kraftfullt bibliotek som gör det möjligt för utvecklare att manipulera och bearbeta Microsoft Excel filer med hjälp av programmeringsspråket Go. Med denna SDK kan du skapa, redigera och konvertera Excel dokument i molnet, utan att installera ytterligare programvara eller beroenden på din lokala dator.

den här artikeln kommer vi att utforska hur du använder Aspose.Cells Cloud SDK för Go för att utföra några vanliga uppgifter, som att skapa en ny Excel-arbetsbok, infoga data i celler och spara den modifierade arbetsboken i molnet.

## **Komma igång**

 Innan du kan börja använda Aspose.Cells Cloud SDK för Go måste du konfigurera din utvecklingsmiljö och installera nödvändiga beroenden. Hänvisa till[artikeln](https://docs.aspose.cloud/cells/quickstart/) på webbplatsen Aspose för att få ditt klient-ID och klienthemlighet.

## Så här installerar du Go-paketet för Aspose.Cells Cloud

Du kan installera Aspose.Cells Cloud SDK för Go med kommandot `go get`. Öppna din terminal eller kommandotolk och kör följande kommando:

```bash
go get -u github.com/aspose-cells-cloud/aspose-cells-cloud-go
```

Detta kommer att ladda ner och installera den senaste versionen av SDK till din Go-arbetsyta.


## Så här importerar du Go-biblioteket till ditt projekt


```golang
package main

import (
	asposecellscloud "github.com/aspose-cells-cloud/aspose-cells-cloud-go"
)
```

## Hur man använder Go-paketet för att konvertera Xlsx till PDF

- Importera Aspose.Cells Molnbibliotek
Börja med att importera det nödvändiga paketet från Aspose.Cells Cloud Go SDK till ditt projekt.
- Konfigurera API klient med inloggningsuppgifter
 Autentisera din API-klient med ditt unika klient-ID och klienthemlighet.
- Förbered konverteringsparametrar
 Definiera parametrar för konverteringsuppgiften, inklusive källfilens namn, önskat utdataformat och lagringsmappens sökväg.
- Utför arbetsbokkonvertering
 Anropa konverteringsprocessen med PostConvertWorkbook-metoden och hantera svaret.

### **Exempelkod**

```golang
package main

import (
	"os"
	asposecellscloud "github.com/aspose-cells-cloud/aspose-cells-cloud-go"
)
func main() {
	instance := asposecellscloud.NewCellsApiService(os.Getenv("ProductClientId"), os.Getenv("ProductClientSecret"), "https://api.aspose.cloud", "v3.0")
    remoteFolder := "TestData/In"

    localName := "Book1.xlsx"
    remoteName := "Book1.xlsx"

    format := "pdf"

    var mapFiles map[string]string       
    mapFiles = make(map[string]string)
    mapFiles[localName]=  localName 

    request := new (asposecellscloud.PutConvertWorkbookRequest)
    request.File =         mapFiles    
    request.Format =         format    
    _, httpResponse, err := instance.PutConvertWorkbook(request)
    if err != nil {
      print(err)
    } else if httpResponse.StatusCode < 200 || httpResponse.StatusCode > 299 {
      print("Test fail")
    }
}

```
