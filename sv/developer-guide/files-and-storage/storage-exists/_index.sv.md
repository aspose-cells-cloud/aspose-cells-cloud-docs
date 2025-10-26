---
title: Lagring finns
second_title: Documen
linktitle: Lagring finns
type: docs
url: /sv/storage-exists/
keywords: Excel API, Storage Exists, REST API, Office Cloud, Cloud Storage, Excel Worksheet, Check Storage, Data Management, API Integratio
description: Lär dig hur du kontrollerar om det finns lagring med hjälp av Aspose.Cells REST API. Den här guiden innehåller detaljerad information om API-slutpunkter, förfrågningsparametrar och svarsbeskrivningar.
weight: 100
kwords: Excel, Office Moln, REST API, Kalkylblad, PDF, CSV, JSON, Markdown, Matcha alla tomma celler i ett Excel-kalkylblad
---
## **Excel API: Lagring finns**

```
GET http://api.aspose.cloud/v4.0/cells/storage/{storageName}/exist
```

### **Funktionsbeskrivning**

 De**lagringExisterar**API kontrollerar om en angiven lagring finns i molntjänsten Aspose.Cells. Denna funktion är avgörande för att säkerställa att alla operationer som är beroende av lagring kan fortsätta utan fel.

###  Begäranparametrarna för**lagringExisterar** API är

| Parameternamn| Typ| Sökväg/Frågesträng/HTTP-kropp| Beskrivning|
|:- |:- |:- |:- |
|lagringsnamn|Sträng|Väg|Namnet på lagringsutrymmet som ska kontrolleras.|

### **Svarsbeskrivning**

```json
{
  "Name": "StorageExist",
  "Description": [
    "Indicates whether the specified storage exists."
  ],
  "Type": "Class",
  "IsAbstract": false,
  "Properties": [
    {
      "Name": "Exists",
      "Description": [
        "Indicates if the storage exists.",
        "This property returns true if the storage is present; otherwise, it returns false."
      ],
      "Nullable": true,
      "ReadOnly": false,
      "IsInherit": false,
      "DataType": {
        "Identifier": "Boolean",
        "Name": "boolean"
      }
    }
  ]
}
```

## OpenAPI-specifikation

 De[OpenAPI-specifikation](https://reference.aspose.cloud/cells/#/StorageController/StorageExists) definierar ett offentligt tillgängligt programmeringsgränssnitt, vilket gör det möjligt för utvecklare att sömlöst interagera med REST API direkt från en webbläsare.

## Excel API SDK

 Att använda ett SDK är det mest effektiva sättet att accelerera utvecklingen. Ett SDK sammanfattar implementeringsdetaljer på låg nivå, vilket gör det möjligt för utvecklare att koncentrera sig på sina projektuppgifter. För en omfattande lista över tillgängliga Aspose.Cells Cloud SDK:er, besök [website address missing][GitHub-arkiv](https://github.com/aspose-cells-cloud).

Följande kodexempel visar hur man gör API-anrop till Aspose.Cells-webbtjänster med hjälp av olika SDK:er:

{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_StorageExists.cs" >}}
{{< /tab >}}
{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_StorageExists.java" >}}
{{< /tab >}}
{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_StorageExists.php" >}}
{{< /tab >}}
{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_StorageExists.rb" >}}
{{< /tab >}}
{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_StorageExists.ts" >}}
{{< /tab >}}
{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_StorageExists.py" >}}
{{< /tab >}}
{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_StorageExists.pl" >}}
{{< /tab >}}
{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_StorageExists.go" >}}
{{< /tab >}}
{{< /tabs >}}
