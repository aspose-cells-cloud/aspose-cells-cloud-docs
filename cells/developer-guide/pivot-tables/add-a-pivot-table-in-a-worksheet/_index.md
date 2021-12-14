---
title: "Add a Pivot Table in a Worksheet"
type: docs
url: /add-a-pivot-table-in-a-worksheet/
weight: 30
---

## **Introduction**
This example shows how to add a pivot table in a worksheet, using Aspose.Cells Cloud API in your applications. You can use our REST API with any language: .NET, Java, PHP, Ruby, Rails, Python, jQuery and many more.
## **API Information**

|**API**|**Type**|**Description**|**Resource Link**|
| :- | :- | :- | :- |
|/cells/{name}/worksheets/{sheetName}/pivottables|PUT|Adds a pivot table in worksheet|[PutWorksheetPivotTable](https://apireference.aspose.cloud/cells/#/PivotTables/PutWorksheetPivotTable)|
### **cURL Example**
{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}

{{< tab tabNum="1" >}}

```java

curl -X PUT "http://api.aspose.com/v3.0/cells/Sample_Test_Book.xls/worksheets/Sheet1/pivottables" -d '{"Name":"MyPivot", "SourceData":"A5:E10", "DestCellName":"H20", "UseSameSource":true, "PivotFieldRows":[1], "PivotFieldColumns":[1], "PivotFieldData ":[1]}' -H "Content-Type: application/json" -H "Accept: application/json"

```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java

{

  "PivotTable": {

    "AutoFormatType": "Classic",

    "BaseFields": [

      {

        "AutoShowCount": 10,

        "AutoShowField": -1,

        "AutoSortField": -1,

        "BaseField": 0,

        "BaseIndex": 0,

        "BaseItem": 0,

        "BaseItemPosition": "Custom",

        "CurrentPageItem": 32765,

        "DataDisplayFormat": "Normal",

        "DragToColumn": false,

        "DragToData": false,

        "DragToHide": false,

        "DragToPage": false,

        "DragToRow": false,

        "Function": "Sum",

        "InsertBlankRow": false,

        "IsAscendShow": false,

        "IsAscendSort": false,

        "IsAutoShow": false,

        "IsAutoSort": false,

        "IsAutoSubtotals": false,

        "IsCalculatedField": false,

        "IsIncludeNewItemsInFilter": false,

        "IsInsertPageBreaksBetweenItems": false,

        "IsMultipleItemSelectionAllowed": false,

        "IsRepeatItemLabels": false,

        "ItemCount": 0,

        "Items": [



        ],

        "Name": "12",

        "Number": 0,

        "NumberFormat": "",

        "OriginalItems": [

          "23",

          "34",

          "45",

          "65"

        ],

        "PivotItems": [



        ],

        "Position": 0,

        "ShowAllItems": false,

        "ShowCompact": false,

        "ShowInOutlineForm": false,

        "ShowSubtotalAtTop": false

      },

      {

        "AutoShowCount": 10,

        "AutoShowField": -1,

        "AutoSortField": -1,

        "BaseField": 0,

        "BaseIndex": 1,

        "BaseItem": 0,

        "BaseItemPosition": "Custom",

        "CurrentPageItem": 32765,

        "DataDisplayFormat": "Normal",

        "DragToColumn": false,

        "DragToData": false,

        "DragToHide": false,

        "DragToPage": false,

        "DragToRow": false,

        "Function": "Sum",

        "InsertBlankRow": false,

        "IsAscendShow": false,

        "IsAscendSort": false,

        "IsAutoShow": false,

        "IsAutoSort": false,

        "IsAutoSubtotals": false,

        "IsCalculatedField": false,

        "IsIncludeNewItemsInFilter": false,

        "IsInsertPageBreaksBetweenItems": false,

        "IsMultipleItemSelectionAllowed": false,

        "IsRepeatItemLabels": false,

        "ItemCount": 4,

        "Items": [

          "22",

          "11",

          "43",

          "65"

        ],

        "Name": "23",

        "Number": 0,

        "NumberFormat": "",

        "OriginalItems": [

          "22",

          "11",

          "43",

          "65"

        ],

        "PivotItems": [

          {

            "Index": 0,

            "IsHidden": false,

            "Name": "22",

            "Value": "22"

          },

          {

            "Index": 1,

            "IsHidden": false,

            "Name": "11",

            "Value": "11"

          },

          {

            "Index": 2,

            "IsHidden": false,

            "Name": "43",

            "Value": "43"

          },

          {

            "Index": 3,

            "IsHidden": false,

            "Name": "65",

            "Value": "65"

          }

        ],

        "Position": 0,

        "ShowAllItems": false,

        "ShowCompact": false,

        "ShowInOutlineForm": false,

        "ShowSubtotalAtTop": false

      },

      {

        "AutoShowCount": 10,

        "AutoShowField": -1,

        "AutoSortField": -1,

        "BaseField": 0,

        "BaseIndex": 2,

        "BaseItem": 0,

        "BaseItemPosition": "Custom",

        "CurrentPageItem": 32765,

        "DataDisplayFormat": "Normal",

        "DragToColumn": false,

        "DragToData": false,

        "DragToHide": false,

        "DragToPage": false,

        "DragToRow": false,

        "Function": "Sum",

        "InsertBlankRow": false,

        "IsAscendShow": false,

        "IsAscendSort": false,

        "IsAutoShow": false,

        "IsAutoSort": false,

        "IsAutoSubtotals": false,

        "IsCalculatedField": false,

        "IsIncludeNewItemsInFilter": false,

        "IsInsertPageBreaksBetweenItems": false,

        "IsMultipleItemSelectionAllowed": false,

        "IsRepeatItemLabels": false,

        "ItemCount": 0,

        "Items": [



        ],

        "Name": "33",

        "Number": 0,

        "NumberFormat": "",

        "OriginalItems": [

          "33",

          "12",

          "54",

          "65",

          "27"

        ],

        "PivotItems": [



        ],

        "Position": 2,

        "ShowAllItems": false,

        "ShowCompact": false,

        "ShowInOutlineForm": false,

        "ShowSubtotalAtTop": false

      },

      {

        "AutoShowCount": 10,

        "AutoShowField": -1,

        "AutoSortField": -1,

        "BaseField": 0,

        "BaseIndex": 3,

        "BaseItem": 0,

        "BaseItemPosition": "Custom",

        "CurrentPageItem": 32765,

        "DataDisplayFormat": "Normal",

        "DragToColumn": false,

        "DragToData": false,

        "DragToHide": false,

        "DragToPage": false,

        "DragToRow": false,

        "Function": "Sum",

        "InsertBlankRow": false,

        "IsAscendShow": false,

        "IsAscendSort": false,

        "IsAutoShow": false,

        "IsAutoSort": false,

        "IsAutoSubtotals": false,

        "IsCalculatedField": false,

        "IsIncludeNewItemsInFilter": false,

        "IsInsertPageBreaksBetweenItems": false,

        "IsMultipleItemSelectionAllowed": false,

        "IsRepeatItemLabels": false,

        "ItemCount": 0,

        "Items": [



        ],

        "Name": "66",

        "Number": 0,

        "NumberFormat": "",

        "OriginalItems": [

          "77",

          "23",

          "88",

          "65",

          "22"

        ],

        "PivotItems": [



        ],

        "Position": 3,

        "ShowAllItems": false,

        "ShowCompact": false,

        "ShowInOutlineForm": false,

        "ShowSubtotalAtTop": false

      },

      {

        "AutoShowCount": 10,

        "AutoShowField": -1,

        "AutoSortField": -1,

        "BaseField": 0,

        "BaseIndex": 4,

        "BaseItem": 0,

        "BaseItemPosition": "Custom",

        "CurrentPageItem": 32765,

        "DataDisplayFormat": "Normal",

        "DragToColumn": false,

        "DragToData": false,

        "DragToHide": false,

        "DragToPage": false,

        "DragToRow": false,

        "Function": "Sum",

        "InsertBlankRow": false,

        "IsAscendShow": false,

        "IsAscendSort": false,

        "IsAutoShow": false,

        "IsAutoSort": false,

        "IsAutoSubtotals": false,

        "IsCalculatedField": false,

        "IsIncludeNewItemsInFilter": false,

        "IsInsertPageBreaksBetweenItems": false,

        "IsMultipleItemSelectionAllowed": false,

        "IsRepeatItemLabels": false,

        "ItemCount": 0,

        "Items": [



        ],

        "Name": "11",

        "Number": 0,

        "NumberFormat": "",

        "OriginalItems": [

          "31",

          "22",

          "36",

          "13",

          "32"

        ],

        "PivotItems": [



        ],

        "Position": 4,

        "ShowAllItems": false,

        "ShowCompact": false,

        "ShowInOutlineForm": false,

        "ShowSubtotalAtTop": false

      }

    ],

    "ColumnFields": [

      {

        "AutoShowCount": 10,

        "AutoShowField": -1,

        "AutoSortField": -1,

        "BaseField": 0,

        "BaseIndex": 1,

        "BaseItem": 0,

        "BaseItemPosition": "Custom",

        "CurrentPageItem": 32765,

        "DataDisplayFormat": "Normal",

        "DragToColumn": false,

        "DragToData": false,

        "DragToHide": false,

        "DragToPage": false,

        "DragToRow": false,

        "Function": "Sum",

        "InsertBlankRow": false,

        "IsAscendShow": false,

        "IsAscendSort": false,

        "IsAutoShow": false,

        "IsAutoSort": false,

        "IsAutoSubtotals": false,

        "IsCalculatedField": false,

        "IsIncludeNewItemsInFilter": false,

        "IsInsertPageBreaksBetweenItems": false,

        "IsMultipleItemSelectionAllowed": false,

        "IsRepeatItemLabels": false,

        "ItemCount": 4,

        "Items": [

          "22",

          "11",

          "43",

          "65"

        ],

        "Name": "23",

        "Number": 0,

        "NumberFormat": "",

        "OriginalItems": [

          "22",

          "11",

          "43",

          "65"

        ],

        "PivotItems": [

          {

            "Index": 0,

            "IsHidden": false,

            "Name": "22",

            "Value": "22"

          },

          {

            "Index": 1,

            "IsHidden": false,

            "Name": "11",

            "Value": "11"

          },

          {

            "Index": 2,

            "IsHidden": false,

            "Name": "43",

            "Value": "43"

          },

          {

            "Index": 3,

            "IsHidden": false,

            "Name": "65",

            "Value": "65"

          }

        ],

        "Position": 0,

        "ShowAllItems": false,

        "ShowCompact": false,

        "ShowInOutlineForm": false,

        "ShowSubtotalAtTop": false

      }

    ],

    "ColumnGrand": false,

    "ColumnRange": {

      "EndColumn": 12,

      "EndRow": 20,

      "StartColumn": 8,

      "StartRow": 19

    },

    "CustomListSort": false,

    "DataBodyRange": {

      "EndColumn": 12,

      "EndRow": 21,

      "StartColumn": 8,

      "StartRow": 21

    },

    "DataFields": [

      {

        "AutoShowCount": 10,

        "AutoShowField": -1,

        "AutoSortField": -1,

        "BaseField": 0,

        "BaseIndex": 1,

        "BaseItem": 0,

        "BaseItemPosition": "Custom",

        "CurrentPageItem": 32765,

        "DataDisplayFormat": "Normal",

        "DisplayName": "Sum of 23",

        "DragToColumn": false,

        "DragToData": false,

        "DragToHide": false,

        "DragToPage": false,

        "DragToRow": false,

        "Function": "Sum",

        "IsAscendShow": false,

        "IsAscendSort": false,

        "IsAutoShow": false,

        "IsAutoSort": false,

        "IsCalculatedField": false,

        "IsIncludeNewItemsInFilter": false,

        "IsMultipleItemSelectionAllowed": false,

        "IsRepeatItemLabels": false,

        "Name": "23",

        "Number": 0,

        "NumberFormat": "",

        "Position": 0,

        "ShowAllItems": false,

        "ShowCompact": false

      }

    ],

    "DataSource": [

      "Sheet1!$A$5:$E$10"

    ],

    "DisplayErrorString": false,

    "DisplayImmediateItems": false,

    "DisplayNullString": false,

    "EnableDataValueEditing": false,

    "EnableDrilldown": false,

    "EnableFieldDialog": false,

    "EnableFieldList": false,

    "EnableWizard": false,

    "ErrorString": "",

    "FieldListSortAscending": false,

    "GrandTotalName": "Grand Total",

    "HasBlankRows": false,

    "Indent": 2,

    "IsAutoFormat": false,

    "IsGridDropZones": false,

    "IsMultipleFieldFilters": false,

    "IsSelected": false,

    "ItemPrintTitles": false,

    "ManualUpdate": false,

    "MergeLabels": false,

    "MissingItemsLimit": "Automatic",

    "Name": "MyPivot",

    "NullString": "",

    "PageFieldOrder": "DownThenOver",

    "PageFields": [



    ],

    "PageFieldWrapCount": 0,

    "PivotFilters": [



    ],

    "PivotTableStyleType": "None",

    "PreserveFormatting": false,

    "PrintDrill": false,

    "PrintTitles": false,

    "RefreshDataFlag": false,

    "RefreshDataOnOpeningFile": false,

    "RowFields": [



    ],

    "RowGrand": false,

    "RowRange": {

      "EndColumn": 8,

      "EndRow": 21,

      "StartColumn": 7,

      "StartRow": 21

    },

    "SaveData": false,

    "ShowDataTips": false,

    "ShowDrill": false,

    "ShowEmptyCol": false,

    "ShowEmptyRow": false,

    "ShowMemberPropertyTips": false,

    "ShowPivotStyleColumnHeader": false,

    "ShowPivotStyleColumnStripes": false,

    "ShowPivotStyleLastColumn": false,

    "ShowPivotStyleRowHeader": false,

    "ShowPivotStyleRowStripes": false,

    "ShowRowHeaderCaption": false,

    "ShowValuesRow": false,

    "SubtotalHiddenPageItems": false,

    "TableRange1": {

      "EndColumn": 12,

      "EndRow": 21,

      "StartColumn": 7,

      "StartRow": 19

    },

    "TableRange2": {

      "EndColumn": 12,

      "EndRow": 21,

      "StartColumn": 7,

      "StartRow": 17

    },

    "link": {

      "Href": "http://api.aspose.cloud/v3.0/cells/Sample_Test_Book.xls/worksheets/Sheet1/0",

      "Rel": "self"

    }

  },

  "Code": "200",

  "Status": "OK"

}

```

{{< /tab >}}

{{< /tabs >}}
## **SDK Source**
The Aspose.Cells Cloud SDKs can be downloaded from the following page: [Available SDKs](/cells/available-sdks/)
### **SDK Examples**
{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cloud" "1e994f29ef29e752b6d02a2c5b63ea9b" "Examples-DotNET-CSharp-PivotTables-AddPivottableWorksheet-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cloud" "af3fea45644d431483f6df52cf3bfe26" "Examples-Java-pivottables-AddPivottableWorksheet-add-pivot-table-worksheet.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cloud" "5161752550311c9baf73ffa0a811ea0b" "AddPivotTableInw" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cloud" "04e9dd952c704f334a4eceb3925d479e" "Examples-Node.js-SDK-PivotTables-AddPivottableWorksheet-1.js" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cloud" "9d725d4678edaac53f95c5208e17783c" "Examples-Android-pivottables-AddPivottableWorksheet-add-pivot-table-worksheet.java" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cloud" "7effbad588b0c24b5f8ed2d7c7759b72" "Examples-Perl-PivotTables-AddPivottableWorksheet-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< gist "aspose-cloud" "980246b631d7816f257f2ad4664788ea" >}}

{{< /tab >}}

{{< /tabs >}}
