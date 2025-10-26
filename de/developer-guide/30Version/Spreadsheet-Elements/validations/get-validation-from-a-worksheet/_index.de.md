---
title: Holen Sie sich eine Arbeitsblattvalidierung per Index aus einem Excel-Arbeitsblatt
second_title: Documen
linktitle: Ge
type: docs
url: /de/validations/get/
aliases: [/get-validation-from-a-worksheet/]
keywords: Get a worksheet validation by index from an Excel worksheet
description: Aspose.Cells Cloud REST API unterstützt die Validierung eines Arbeitsblatts nach Index aus einem Excel Arbeitsblatt. SDK unterstützt verschiedene Entwicklungssprachen. Dazu gehören Android, C#, Go, Java, NodeJS, Perl, PHP, Python, Ruby und Swift
weight: 10
kwords: Excel, Office Cloud, REST API, Tabellenkalkulation, PDF, CSV, Json, Markdown, Holen Sie sich eine Arbeitsblattvalidierung per Index aus einem Excel-Arbeitsblatt
---
Dieser REST API gibt an, dass eine Arbeitsblattvalidierung nach Index auf einem Excel-Arbeitsblatt erfolgen soll.

## RSET API

```bash
 
GET http://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/validations/{validationIndex}
 
```

Die Anforderungsparameter sind:

| Parametername| Typ| Pfad/Abfragezeichenfolge/HTTPBody|Beschreibung|
|:- |:- |:- |:- |
| Name| Schnur| Weg| Dokumentname.|
| Blattname| Schnur| Weg| Arbeitsblattname.|
| Validierungsindex| ganze Zahl| Weg| Der Validierungsindex.|
| Ordner| Schnur| Abfrage| Ordner des Dokuments.|
| Speichername| Schnur| Abfrage| Speichername.|

 Der[OpenAPI-Spezifikation](https://apireference.aspose.cloud/cells/#/WorksheetValidations/GetWorksheetValidation) definiert eine öffentlich zugängliche Programmierschnittstelle und ermöglicht Ihnen die Durchführung von REST-Interaktionen direkt von einem Webbrowser aus.

Mit dem Befehlszeilentool cURL können Sie problemlos auf die Webdienste Aspose.Cells zugreifen. Das folgende Beispiel zeigt, wie Sie mit cURL Aufrufe an Cloud API tätigen.

{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}

{{< tab tabNum="1" >}}

```bash
 
curl -v "http://api.aspose.com/v3.0/cells/myWorkBook.xlsx/worksheets/Sheet1/validations/0" \
-X GET \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"
 
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```bash
{

  "Validation": {

    "AlertStyle": "Stop",

    "AreaList": [

      {

        "EndColumn": 0,

        "EndRow": 0,

        "StartColumn": 0,

        "StartRow": 0

      },

      {

        "EndColumn": 27,

        "EndRow": 0,

        "StartColumn": 26,

        "StartRow": 0

      }

    ],

    "IgnoreBlank": false,

    "InCellDropDown": false,

    "Operator": "None",

    "ShowError": false,

    "ShowInput": false,

    "Type": "AnyValue",

    "link": {

      "Href": "http://api.aspose.cloud/v3.0/cells/myWorkBook.xlsx/worksheets/Sheet1/Validations/0",

      "Rel": "self"

    }

  },

  "Code": "200",

  "Status": "OK"

}
 
```

{{< /tab >}}

{{< /tabs >}}

## Cloud SDK-Familie

 Die Verwendung eines SDKs beschleunigt die Entwicklung am besten. Ein SDK kümmert sich um die Details auf niedriger Ebene und ermöglicht es Ihnen, sich auf Ihre Projektaufgaben zu konzentrieren. Bitte beachten Sie die[GitHub-Repository](https://github.com/aspose-cells-cloud) für eine vollständige Liste der Aspose.Cells Cloud SDKs.

Die folgenden Codebeispiele zeigen, wie Sie mithilfe verschiedener SDKs Aufrufe an Aspose.Cells-Webdienste tätigen:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetWorksheetValidation.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetWorksheetValidation.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetWorksheetValidation.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetWorksheetValidation.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_GetWorksheetValidation.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetWorksheetValidation.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetWorksheetValidation.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetWorksheetValidation.go" >}}

{{< /tab >}}

{{< /tabs >}}
