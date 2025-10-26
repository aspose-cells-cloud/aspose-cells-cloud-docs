---
title: Ta bort fil - Excel AP
second_title: Documen
linktitle: Ta bort fil
type: docs
url: /sv/delete-file/
keywords: Delete file, Excel API, REST API, Office Cloud, Spreadsheet management, File deletion, Cloud storage, API usag
description: Lär dig hur du tar bort filer i Excel med hjälp av Aspose.Cells API. Den här guiden ger detaljerad information om slutpunkten deleteFile API, förfrågningsparametrar och svarsstruktur.
weight: 100
kwords: Ta bort fil, Excel API, REST API, Office Moln, Kalkylbladshantering, Filradering, Molnlagring, API usag
---
## **Excel API: Ta bort fil**

```
DELETE http://api.aspose.cloud/v4.0/cells/storage/file/{path}
```

### **Funktionsbeskrivning**

 De**ta bort fil** API låter användare ta bort specifika filer från molnlagring, vilket säkerställer effektiv hantering av resurser och data.

###  Begäranparametrarna för**ta bort fil** API är

| Parameternamn| Typ| Sökväg/Frågesträng/HTTP-text| Beskrivning|
|:- |:- |:- |:- |
|väg|Sträng|Väg|Sökvägen till filen som behöver raderas.|
|lagringsnamn|Sträng|Fråga|Namnet på lagringsplatsen där filen finns. Valfritt om standardlagringsplats används.|
|versions-ID|Sträng|Fråga|Versions-ID för filen som ska raderas, om tillämpligt.|

### **Svarsbeskrivning**

```json
{
Void
}
```

## OpenAPI-specifikation

 De[OpenAPI-specifikation](https://reference.aspose.cloud/cells/#/FileController/DeleteFile) definierar ett offentligt tillgängligt programmeringsgränssnitt och låter dig utföra REST-interaktioner direkt från en webbläsare.

## Excel API SDK

 Att använda ett SDK är det bästa sättet att snabba upp utvecklingen. Ett SDK hanterar detaljer på låg nivå, vilket gör att du kan fokusera på dina projektuppgifter. Vänligen kolla in[GitHub-arkiv](https://github.com/aspose-cells-cloud) för en komplett lista över Aspose.Cells Cloud SDK:er.

Följande kodexempel visar hur man anropar Aspose.Cells webbtjänster med hjälp av olika SDK:er:
