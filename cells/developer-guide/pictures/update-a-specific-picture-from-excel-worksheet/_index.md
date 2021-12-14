---
title: "Update a specific Picture from Excel Worksheet"
type: docs
url: /update-a-specific-picture-from-excel-worksheet/
weight: 30
---

## **Introduction**
This example shows how to update a image in a worksheet, using Aspose.Cells Cloud API in your applications. You can use our REST API with any language: .NET, Java, PHP, Ruby, Rails, Python, jQuery and many more.
## **API Information**

|**API**|**Type**|**Description**|**Resource Link**|
| :- | :- | :- | :- |
|/cells/{name}/worksheets/{sheetName}/pictures/{pictureIndex}|POST|Update picture in an Excel Worksheet|[PostWorkSheetPicture](https://apireference.aspose.cloud/cells/#/Pictures/PostWorkSheetPicture)|
### **cURL Example** 
{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}

{{< tab tabNum="1" >}}

```java

curl -X POST "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet2/pictures/1" -H "accept: application/json" -H "Content-Type: application/json" -d "{ \"UpperLeftRow\": 10, \"Top\": 0, \"UpperLeftColumn\": 1, \"Left\": 0, \"LowerRightRow\": 0, \"Bottom\": 0, \"LowerRightColumn\": 3, \"ImageFormat\": \"jpg\", \"SourceFullName\": \"download.jpg\"}"

```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java

{

  "Picture": {

    "BorderLineColor": {

      "A": 255,

      "R": 0,

      "G": 0,

      "B": 0

    },

    "BorderWeight": 0.75,

    "OriginalHeight": 0,

    "OriginalWidth": 0,

    "ImageFormat": "Unknown",

    "SourceFullName": "download.jpg",

    "Name": "Picture 2",

    "MsoDrawingType": null,

    "AutoShapeType": null,

    "Placement": "Move",

    "UpperLeftRow": 10,

    "Top": 0,

    "UpperLeftColumn": 1,

    "Left": 0,

    "LowerRightRow": 15,

    "Bottom": 19,

    "LowerRightColumn": 3,

    "Right": 51,

    "Width": 179,

    "Height": 119,

    "X": 64,

    "Y": 200,

    "RotationAngle": 0,

    "HtmlText": null,

    "Text": null,

    "AlternativeText": "",

    "TextHorizontalAlignment": null,

    "TextHorizontalOverflow": null,

    "TextOrientationType": null,

    "TextVerticalAlignment": null,

    "TextVerticalOverflow": null,

    "IsGroup": false,

    "IsHidden": false,

    "IsLockAspectRatio": true,

    "IsLocked": true,

    "IsPrintable": true,

    "IsTextWrapped": null,

    "IsWordArt": null,

    "LinkedCell": null,

    "ZOrderPosition": 1,

    "link": {

      "Href": "/test.xlsx/worksheets/Sheet2/pictures/1",

      "Rel": "self",

      "Title": null,

      "Type": null

    }

  },

  "Code": 200,

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

{{< gist "aspose-cloud" "1e994f29ef29e752b6d02a2c5b63ea9b" "Examples-DotNET-CSharp-Pictures-UpdateSpecificPictureWorksheet-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cloud" "af3fea45644d431483f6df52cf3bfe26" "Examples-Java-pictures-UpdateSpecificPictureWorksheet-update-specfic-pictures-worksheet.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cloud" "5c1a68c4cea73845b221ff0d3b9ec9df" "Examples-PHP-Pictures-PostWorkSheetPicture-.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cloud" "3c5c9f9fff9898bb8251aa7ee9191641" "Examples-Ruby-Pictures-update_worksheet_picture_by_index-.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cloud" "5161752550311c9baf73ffa0a811ea0b" "UpdateSpecificPictureFromExcelWorksheet.py" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cloud" "04e9dd952c704f334a4eceb3925d479e" "Examples-Node.js-SDK-Pictures-UpdateSpecificPictureWorksheet-1.js" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cloud" "9d725d4678edaac53f95c5208e17783c" "Examples-Android-pictures-UpdateSpecificPictureWorksheet-update-specfic-pictures-worksheet.java" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cloud" "7effbad588b0c24b5f8ed2d7c7759b72" "Examples-Perl-Pictures-UpdateSpecificPictureWorksheet-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< gist "aspose-cloud" "216e6bfac2d1abdff4de59f3d32b22b1" >}}

{{< /tab >}}

{{< /tabs >}}
