---
title: Aspose.Cells Cloud 17.3 Release Note
second_title: Aspose.Cells Cloud Documen
type: docs
url: /sv/aspose-cells-cloud-17-3-release-notes/
aliases: [/aspose-cells-for-cloud-17-3-0-release-notes/]
description: Aspose.Cells Cloud stöder Excel för att skapa, konvertera, sammanfoga, dela, skydda, inre objektoperation och så vidare
weight: 80
---
{{% alert color="primary" %}} 

 Den här sidan innehåller release notes för[Aspose.Cells Cloud 17.3](https://downloads.aspose.com/cells/cloud/new-releases/aspose.cells-for-cloud-17.3.0/).

{{% /alert %}} 

|**Nyckel**|**Sammanfattning**|**Kategori**|
|:- |:- |:- |
|CELLSCLOUD-10028|Infoga sidbrytningar i kalkylbladet Excel|Ny funktion|
|CELLSCLOUD-10035|Stöd för AutoFit radhöjder|Ny funktion|
|CELLSCLOUD-10036|Stöd för AutoFit-kolumnernas bredd|Ny funktion|
## **Få horisontella sidbrytningar i arbetsbladet**
Följande exempelkod illustrerar hur du får horisontella sidbrytningar i arbetsbladet med Aspose.Cells för Cloud API.

```java

//Your workbook and sheet name

string workbookName = "sampleExcelPageBreaks.xlsx";

string sheetName = "Sheet1";



//URL to Get Horizontal Page Breaks

string url = "http://api.aspose.com/v1.1/cells/"+ workbookName + "/worksheets/" + sheetName + "/horizontalpagebreaks";



//Call Get method with the following parameters

string data = "";

string contentType = "application/json";

using (HttpWebResponse response = _helper.CallGet(url, data, contentType))

{

    Assert.AreEqual(response.StatusCode, HttpStatusCode.OK);

}

```
## **Få vertikala sidbrytningar i arbetsbladet**
Följande exempelkod illustrerar hur du får vertikala sidbrytningar i arbetsbladet med Aspose.Cells för Cloud API.

```java

//Your workbook and sheet name

string workbookName = "sampleExcelPageBreaks.xlsx";

string sheetName = "Sheet1";



//URL to Get Horizontal Page Breaks

string url = "http://api.aspose.com/v1.1/cells/"+ workbookName + "/worksheets/" + sheetName + "/verticalpagebreaks";



//Call Get method with the following parameters

string data = "";

string contentType = "application/json";

using (HttpWebResponse response = _helper.CallGet(url, data, contentType))

{

    Assert.AreEqual(response.StatusCode, HttpStatusCode.OK);

}

```
## **Infoga horisontell sidbrytning i arbetsbladet**
Följande exempelkod illustrerar hur man infogar horisontell sidbrytning i arbetsbladet med Aspose.Cells för Cloud API.

```java

//Your workbook and sheet name

string workbookName = "sampleExcelPageBreaks.xlsx";

string sheetName = "Sheet1";



//Row index to insert horizontal page break

int idxRow = 18;



//URL to insert horizontal page break

string url = "http://api.aspose.com/v1.1/cells/" + workbookName + "/worksheets/" + sheetName + "/horizontalpagebreaks?row=" + idxRow;



//Call PUT method with the following parameters

string data = "";

string contentType = "application/json";

using (HttpWebResponse response = _helper.CallPut(url, data, contentType))

{

    Assert.AreEqual(response.StatusCode, HttpStatusCode.OK);

}

```
## **Infoga vertikal sidbrytning i arbetsbladet**
Följande exempelkod illustrerar hur man infogar vertikal sidbrytning i arbetsbladet med Aspose.Cells för Cloud API.

```java

//Your workbook and sheet name

string workbookName = "sampleExcelPageBreaks.xlsx";

string sheetName = "Sheet1";



//Column index to insert vertical page break

int idxCol = 9;



//URL to insert vertical page break

string url = "http://api.aspose.com/v1.1/cells/" + workbookName + "/worksheets/" + sheetName + "/verticalpagebreaks?column=" + idxCol;



//Call PUT method with the following parameters

string data = "";

string contentType = "application/json";

using (HttpWebResponse response = _helper.CallPut(url, data, contentType))

{

    Assert.AreEqual(response.StatusCode, HttpStatusCode.OK);

}

```
## **Ta bort horisontell sidbrytning i kalkylbladet**
Följande exempelkod illustrerar hur du tar bort horisontell sidbrytning i arbetsbladet med Aspose.Cells för Cloud API.

```java

//Your workbook and sheet name

string workbookName = "sampleExcelPageBreaks.xlsx";

string sheetName = "Sheet1";



//Your horizontal page break index

int idxHorizontalPageBreak = 0;



//URL to Delete Horizontal Page Break

string url = "http://api.aspose.com/v1.1/cells/" + workbookName + "/worksheets/" + sheetName + "/horizontalpagebreaks/" + idxHorizontalPageBreak;



//Call Delete method with the following parameters

string data = "";

string contentType = "application/json";

using (HttpWebResponse response = _helper.CallDelete(url, data, contentType))

{

    Assert.AreEqual(response.StatusCode, HttpStatusCode.OK);

}

```
## **Ta bort vertikal sidbrytning i kalkylbladet**
Följande exempelkod illustrerar hur du tar bort vertikal sidbrytning i arbetsbladet med Aspose.Cells för Cloud API.

```java

//Your workbook and sheet name

string workbookName = "sampleExcelPageBreaks.xlsx";

string sheetName = "Sheet1";



//Your vertical page break index

int idxVerticalPageBreak = 0;



//URL to Delete Vertical Page Break

string url = "http://api.aspose.com/v1.1/cells/" + workbookName + "/worksheets/" + sheetName + "/verticalpagebreaks/" + idxVerticalPageBreak;



//Call Delete method with the following parameters

string data = "";

string contentType = "application/json";

using (HttpWebResponse response = _helper.CallDelete(url, data, contentType))

{

    Assert.AreEqual(response.StatusCode, HttpStatusCode.OK);

}

```
## **Autopassa en kolumn av arbetsblad**
Följande exempelkod illustrerar hur man automatiskt anpassar en kolumn i kalkylbladet. Den passar automatiskt**kolumn C**.

```java

//Your workbook and sheet name

string workbookName = "sampleAutoFit.xlsx";

string sheetName = "Sheet1";



//URL to auto fit the column C

string url = "http://api.aspose.com/v1.1/cells/" + workbookName + "/worksheets/" + sheetName + "/autofitcolumns?firstColumn=2&lastColumn=2";



//Call POST method with the above URL

using (HttpWebResponse response = _helper.CallPost(url, string.Empty, contentType))

{

    Assert.AreEqual(response.StatusCode, HttpStatusCode.OK);

}

```
## **Autopassa flera kolumner av kalkylblad**
Följande exempelkod illustrerar hur du automatiskt anpassar flera kolumner i kalkylbladet. Den passar automatiskt**kolumnerna A, B, C, D, E och F**.

```java

//Your workbook and sheet name

string workbookName = "sampleAutoFit.xlsx";

string sheetName = "Sheet1";



//URL to auto fit the columns A, B, C, D, E and F

string url = "http://api.aspose.com/v1.1/cells/" + workbookName + "/worksheets/" + sheetName + "/autofitcolumns?firstColumn=0&lastColumn=5";



//Call POST method with the above URL

using (HttpWebResponse response = _helper.CallPost(url, string.Empty, contentType))

{

    Assert.AreEqual(response.StatusCode, HttpStatusCode.OK);

}

```
## **Autopassa en rad av arbetsblad**
Följande exempelkod illustrerar hur man automatiskt anpassar en rad i kalkylbladet. Den passar automatiskt**2:a raden**.

```java

//Your workbook and sheet name

string workbookName = "sampleAutoFitRow.xlsx";

string sheetName = "Sheet1";



//URL to auto fit the 2nd row

string url = "http://api.aspose.com/v1.1/cells/" + workbookName + "/worksheets/" + sheetName + "/autofitrow?rowIndex=1&firstColumn=1&lastColumn=10";



//Call POST method with the above URL

using (HttpWebResponse response = _helper.CallPost(url, string.Empty, contentType))

{

    Assert.AreEqual(response.StatusCode, HttpStatusCode.OK);

}

```
## **Autopassa flera rader av kalkylblad**
Följande exempelkod illustrerar hur du automatiskt anpassar flera rader i kalkylbladet. Den anpassar automatiskt flera rader från 2:a raden till 8:e raden.

```java

//Your workbook and sheet name

string workbookName = "sampleAutoFitRows.xlsx";

string sheetName = "Sheet1";



//URL to auto fit the multiple rows from 2nd to 8th

string url = "http://api.aspose.com/v1.1/cells/" + workbookName + "/worksheets/" + sheetName + "/autofitrows?onlyAuto=False&startRow=1&endRow=7";



//Call POST method with the above URL

using (HttpWebResponse response = _helper.CallPost(url, string.Empty, contentType))

{

    Assert.AreEqual(response.StatusCode, HttpStatusCode.OK);

}

```
