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

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNET-CSharp-Pictures-UpdateSpecificPictureWorksheet-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-pictures-UpdateSpecificPictureWorksheet-update-specfic-pictures-worksheet.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Pictures-PostWorkSheetPicture-.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Pictures-update_worksheet_picture_by_index-.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "UpdateSpecificPictureFromExcelWorksheet.py" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-Pictures-UpdateSpecificPictureWorksheet-1.js" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "9d725d4678edaac53f95c5208e17783c" "Examples-Android-pictures-UpdateSpecificPictureWorksheet-update-specfic-pictures-worksheet.java" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-Pictures-UpdateSpecificPictureWorksheet-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< gist "aspose-cells-cloud-gists" "216e6bfac2d1abdff4de59f3d32b22b1" >}}

{{< /tab >}}

{{< /tabs >}}
