﻿---
title: Obtenir la dernière cellule de la feuille de calcul Excel
type: docs
url: /fr/get-last-cell-of-excel-worksheet/
weight: 30
---
Ce REST API indique que les émissions obtiennent un `endcell` dans un fichier Excel lorsque le paramètre `cellOrMethodName` est `endcell`.

- **cURL Exemple**


{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```java

curl -X GET "http://api.aspose.com/v3.0/cells/myWorkbook.xlsx/worksheets/Sheet1/cells/endcell" -H "Content-Type: application/json" -H "Accept: application/json" 

```

{{< /tab >}}

{{< tab tabNum="12" >}}

```java

{

  "Cell": {

    "Name": "F341",

    "Row": 340,

    "Column": 5,

    "Value": "<More Info>",

    "Type": "IsString",

    "Formula": "=HYPERLINK(SUBSTITUTE(HelpURLTemplate,\"xxxxxxxxxx\",[Help Topic]),\"<More Info>\")",

    "IsFormula": false,

    "IsMerged": false,

    "IsArrayHeader": false,

    "IsInArray": false,

    "IsErrorValue": false,

    "IsInTable": false,

    "IsStyleSet": false,

    "HtmlString": "<Font Style=\"TEXT-DECORATION: underline;FONT-FAMILY: Calibri;FONT-SIZE: 11pt;COLOR: #000000;\">&lt;More Info&gt;</Font>",

    "Style": {

      "link": {

        "Href": "/style",

        "Rel": "self"

      }

    }

  },

  "Code": "200",

  "Status": "OK"

}

```

{{< /tab >}}

{{< /tabs >}}


- **Famille SDK Cloud**

 L'utilisation d'un SDK est le meilleur moyen d'accélérer le développement. Un SDK prend en charge les détails de bas niveau et vous permet de vous concentrer sur les tâches de votre projet. Veuillez consulter le[Référentiel GitHub](https://github.com/aspose-cells-cloud) pour obtenir la liste complète des SDK Cloud Aspose.Cells.

Les exemples de code suivants montrent comment effectuer des appels vers les services Web Aspose.Cells à l'aide de divers SDK :


{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNET-CSharp-Cells-GetLastCellWorksheet-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-cells-GetEndCellWorksheet-get-last-cell-excel-worksheet.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Cells-GetWorksheetLastCell.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Cells-get_worksheet_last_cell.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "GetLastCellOfExcelWorksheet.py" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-Cells-GetLastCellWorksheet-1.js" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "9d725d4678edaac53f95c5208e17783c" "Examples-Android-cells-GetEndCellWorksheet-get-last-cell-excel-worksheet.java" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-Cells-GetLastCellWorksheet-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< gist "aspose-cells-cloud-gists" "3cf3e145c223fd6f6f3d9f6377092db5" >}}

{{< /tab >}}

{{< /tabs >}}
