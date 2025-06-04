## **Excel API : SearchBrokenLinks **

Search broken links in the local spreadsheet. 

```bash

PUT http://api.aspose.cloud/v4.0/cells/searchBrokenLinks

```

This method searches for broken links within a local spreadsheet file.It scans through all sheets and cells to identify any hyperlinks that no longer point to valid destinations, such as dead URLs or missing references.The operation is performed cloudly, requiring no cloud storage.Ensure you have the necessary permissions to read the source file.If the source file cannot be accessed, contains unsupported formats, or if an error occurs during the search process, an appropriate exception will be thrown.Depending on the implementation, the method may return a list of broken links with details such as sheet name, cell coordinates, and the problematic URL.Users should review the results carefully to update or remove invalid links.

## The request parameters of **searchBrokenLinks** API are: 

| Parameter Name | Type | Path/Query String/HTTPBody | Description | 
| :- | :- | :- |:- | 
|Spreadsheet|File|FormData|Upload spreadsheet file.|
|sheetname|String|Query|Specify the worksheet for the replace.|
|cellarea|String|Query|Specify the cell area for the replace.|
|regoin|String|Query|The spreadsheet region setting.|
|password|String|Query|The password for opening spreadsheet file.|


The [OpenAPI Specification](https://reference.aspose.cloud/cells/#/SearchControllor/SearchBrokenLinks) defines a publicly accessible programming interface and lets you carry out REST interactions directly from a web browser.


## Excel API SDK 

Using an SDK is the best way to speed up the development. An SDK takes care of low-level details and lets you focus on your project tasks. Please check out the [GitHub repository](https://github.com/aspose-cells-cloud) for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to make calls to Aspose.Cells web services using various SDKs:

