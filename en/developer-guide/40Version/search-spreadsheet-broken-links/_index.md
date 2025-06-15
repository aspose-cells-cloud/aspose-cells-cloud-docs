# **Excel API : SearchSpreadsheetBrokenLinks **

Search broken links in the local spreadsheet. 


## **Interface Details**

### **Endpoint** 

```
PUT http://api.aspose.cloud/v4.0/cells/search/broken-links
```

### **Function Description**

This method searches for broken links within a local spreadsheet file.It scans through all sheets and cells to identify any hyperlinks that no longer point to valid destinations, such as dead URLs or missing references.The operation is performed cloudly, requiring no cloud storage.Ensure you have the necessary permissions to read the source file.If the source file cannot be accessed, contains unsupported formats, or if an error occurs during the search process, an appropriate exception will be thrown.Depending on the implementation, the method may return a list of broken links with details such as sheet name, cell coordinates, and the problematic URL.Users should review the results carefully to update or remove invalid links.

### The request parameters of **searchSpreadsheetBrokenLinks** API are: 

| Parameter Name | Type | Path/Query String/HTTPBody | Description | 
| :- | :- | :- |:- | 
|Spreadsheet|File|FormData|Upload spreadsheet file.|
|worksheet|String|Query|Specify the worksheet for the replace.|
|cellArea|String|Query|Specify the cell area for the replace.|
|regoin|String|Query|The spreadsheet region setting.|
|password|String|Query|The password for opening spreadsheet file.|


### **Response Description**
```json
{
  "Name": "BrokenLinksReponse",
  "Type": "Class",
  "ParentName": "CellsCloudResponse",
  "IsAbstract": false,
  "Properties": [
    {
      "Name": "BrokenLinks",
      "Nullable": true,
      "ReadOnly": false,
      "IsInherit": false,
      "DataType": {
        "Identifier": "Container",
        "Reference": "BrokenLink",
        "ElementDataType": {
          "Identifier": "Class",
          "Reference": "BrokenLink",
          "Name": "class:brokenlink"
        },
        "Name": "container"
      }
    },
    {
      "Name": "Code",
      "Nullable": true,
      "ReadOnly": false,
      "IsInherit": true,
      "DataType": {
        "Identifier": "Integer",
        "Name": "integer"
      }
    },
    {
      "Name": "Status",
      "Nullable": true,
      "ReadOnly": false,
      "IsInherit": true,
      "DataType": {
        "Identifier": "String",
        "Name": "string"
      }
    }
  ]
}
```

## OpenAPI Specification

The [OpenAPI Specification](https://reference.aspose.cloud/cells/#/SearchControllor/SearchSpreadsheetBrokenLinks) defines a publicly accessible programming interface and lets you carry out REST interactions directly from a web browser.

## Excel API SDK 

Using an SDK is the best way to speed up the development. An SDK takes care of low-level details and lets you focus on your project tasks. Please check out the [GitHub repository](https://github.com/aspose-cells-cloud) for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to make calls to Aspose.Cells web services using various SDKs:


{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
	{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_SearchSpreadsheetBrokenLinks.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
	{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_SearchSpreadsheetBrokenLinks.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
	{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_SearchSpreadsheetBrokenLinks.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
	{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_SearchSpreadsheetBrokenLinks.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
	{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_SearchSpreadsheetBrokenLinks.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
	{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_SearchSpreadsheetBrokenLinks.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
	{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_SearchSpreadsheetBrokenLinks.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
	{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_SearchSpreadsheetBrokenLinks.go" >}}
{{</tab>}}
{{< /tabs >}}


