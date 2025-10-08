---
title: Flytta fil
second_title: Documen
linktitle: Flytta fil
type: docs
url: /sv/move-file/
keywords: Move file, Aspose.Cells API, File Management, Excel API, REST API, Cloud Storage, Spreadsheet Manipulatio
description: Lär dig hur du använder MoveFile API för att hantera filer i molnlagring Aspose.Cells
weight: 100
kwords: Excel, Office Moln, REST API, Kalkylblad, PDF, CSV, Json, Markdown, Flytta fil, Filhantering, Molnlagring
---
## **Excel API: Flytta fil**

```
PUT http://api.aspose.cloud/v4.0/cells/storage/file/move/{srcPath}
```

### **Funktionsbeskrivning**

 De**flyttaFil** Med API kan du flytta en fil från en plats till en annan inom Aspose.Cells-molnlagringen. Detta är särskilt användbart för att organisera filer och hantera lagring effektivt.

###  Begäranparametrarna för**flyttaFil** API är

| Parameternamn| Typ| Sökväg/Frågesträng/HTTP-text| Beskrivning|
|---------------|--|------------------------|--------------------------------------|
| srcPath| Sträng| Väg| Källsökvägen för filen som ska flyttas.|
| destPath| Sträng| Fråga| Målsökvägen dit filen ska flyttas.|
| srcLagringsnamn| Sträng| Fråga| Källlagringsnamnet om tillämpligt.|
| destStorageName| Sträng| Fråga|Namnet på destinationslagringen, om tillämpligt.|
| versions-ID| Sträng| Fråga| Filens versions-ID, om tillämpligt.|

### **Svarsbeskrivning**

```json
{
Void
}
```

## OpenAPI-specifikation

 De[OpenAPI-specifikation](https://reference.aspose.cloud/cells/#/FileController/MoveFile) definierar ett offentligt tillgängligt programmeringsgränssnitt och låter dig utföra REST-interaktioner direkt från en webbläsare.

## Excel API SDK

 Att använda ett SDK är det bästa sättet att snabba upp utvecklingen. Ett SDK tar hand om detaljer på låg nivå och låter dig fokusera på dina projektuppgifter. Vänligen kolla in[GitHub-arkiv](https://github.com/aspose-cells-cloud) för en komplett lista över Aspose.Cells Cloud SDK:er.

Följande kodexempel visar hur man anropar Aspose.Cells webbtjänster med hjälp av olika SDK:er:
