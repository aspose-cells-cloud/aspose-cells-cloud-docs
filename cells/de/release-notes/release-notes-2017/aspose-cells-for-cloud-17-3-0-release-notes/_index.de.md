---
title: Aspose.Cells Cloud 17.3-Versionshinweis
second_title: Aspose.Cells Cloud Documen
type: docs
url: /de/aspose-cells-cloud-17-3-release-notes/
aliases: [/aspose-cells-for-cloud-17-3-0-release-notes/]
description: Aspose.Cells Cloud unterstützt Excel zum Erstellen, Konvertieren, Zusammenführen, Aufteilen, Schützen, inneren Objektvorgang usw
weight: 80
---
{{% alert color="primary" %}} 

 Diese Seite enthält Versionshinweise für[Aspose.Cells Wolke 17.3](https://downloads.aspose.com/cells/cloud/new-releases/aspose.cells-for-cloud-17.3.0/).

{{% /alert %}} 

|**Taste**|**Zusammenfassung**|**Kategorie**|
|:- |:- |:- |
|CELLSCLOUD-10028|Seitenumbrüche in Arbeitsblatt Excel einfügen|Neue Funktion|
|CELLSCLOUD-10035|Unterstützung von AutoFit-Zeilenhöhen|Neue Funktion|
|CELLSCLOUD-10036|Unterstützt die Breite von AutoFit-Spalten|Neue Funktion|
## **Erhalten Sie horizontale Seitenumbrüche innerhalb des Arbeitsblatts**
Der folgende Beispielcode veranschaulicht, wie Sie horizontale Seitenumbrüche innerhalb des Arbeitsblatts mithilfe von Aspose.Cells für Cloud API erhalten.

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
## **Erhalten Sie vertikale Seitenumbrüche innerhalb des Arbeitsblatts**
Der folgende Beispielcode veranschaulicht, wie vertikale Seitenumbrüche innerhalb des Arbeitsblatts mithilfe von Aspose.Cells für Cloud API abgerufen werden.

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
## **Horizontalen Seitenumbruch in Arbeitsblatt einfügen**
Der folgende Beispielcode veranschaulicht, wie Sie einen horizontalen Seitenumbruch in ein Arbeitsblatt einfügen, indem Sie Aspose.Cells für Cloud API verwenden.

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
## **Vertikalen Seitenumbruch in Arbeitsblatt einfügen**
Der folgende Beispielcode veranschaulicht, wie Sie mithilfe von Aspose.Cells für Cloud API einen vertikalen Seitenumbruch in ein Arbeitsblatt einfügen.

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
## **Löschen Sie den horizontalen Seitenumbruch im Arbeitsblatt**
Der folgende Beispielcode veranschaulicht, wie Sie den horizontalen Seitenumbruch innerhalb des Arbeitsblatts mithilfe von Aspose.Cells für Cloud API löschen können.

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
## **Löschen Sie den vertikalen Seitenumbruch im Arbeitsblatt**
Der folgende Beispielcode veranschaulicht, wie Sie mithilfe von Aspose.Cells für Cloud API den vertikalen Seitenumbruch innerhalb des Arbeitsblatts löschen können.

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
## **Einzelne Spalte des Arbeitsblatts automatisch anpassen**
Der folgende Beispielcode veranschaulicht, wie einzelne Spalten des Arbeitsblatts automatisch angepasst werden. Es passt die automatisch an**Spalte C**.

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
## **Mehrere Spalten des Arbeitsblatts automatisch anpassen**
Der folgende Beispielcode veranschaulicht, wie mehrere Spalten des Arbeitsblatts automatisch angepasst werden. Es passt die automatisch an**Spalten A, B, C, D, E und F**.

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
## **Einzelne Zeile des Arbeitsblatts automatisch anpassen**
Der folgende Beispielcode veranschaulicht, wie einzelne Zeilen des Arbeitsblatts automatisch angepasst werden. Es passt die automatisch an**2. Reihe**.

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
## **Mehrere Zeilen des Arbeitsblatts automatisch anpassen**
Der folgende Beispielcode veranschaulicht, wie mehrere Zeilen des Arbeitsblatts automatisch angepasst werden. Es passt die mehreren Reihen ab der 2. Reihe bis zur 8. Reihe automatisch an.

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
