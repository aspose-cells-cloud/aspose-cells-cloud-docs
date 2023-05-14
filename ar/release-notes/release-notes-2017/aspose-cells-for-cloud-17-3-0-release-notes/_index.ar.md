---
title: Aspose.Cells Cloud 17.3 ملاحظات الإصدار
second_title: Aspose.Cells Cloud Documen
type: docs
url: /ar/aspose-cells-cloud-17-3-release-notes/
aliases: [/aspose-cells-for-cloud-17-3-0-release-notes/]
description: Aspose.Cells Cloud يدعم Excel لإنشاء وتحويل ودمج وتقسيم وحماية وتشغيل الكائن الداخلي وما إلى ذلك
weight: 80
---
{{% alert color="primary" %}} 

 تحتوي هذه الصفحة على ملاحظات الإصدار لـ[Aspose.Cells كلاود 17.3.2007](https://downloads.aspose.com/cells/cloud/new-releases/aspose.cells-for-cloud-17.3.0/).

{{% /alert %}} 

|**مفتاح**|**ملخص**|**فئة**|
|:- |:- |:- |
|CELLSCLOUD-10028|أدخل فواصل الصفحات في ورقة عمل Excel|ميزة جديدة|
|CELLSCLOUD-10035|دعم ارتفاعات الصفوف AutoFit|ميزة جديدة|
|CELLSCLOUD-10036|دعم عرض أعمدة AutoFit|ميزة جديدة|
## **احصل على فواصل صفحات أفقية داخل ورقة العمل**
يوضح نموذج الكود التالي كيفية الحصول على فواصل الصفحات الأفقية داخل ورقة العمل باستخدام Aspose.Cells لـ Cloud API.

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
## **احصل على فواصل الصفحات العمودية داخل ورقة العمل**
يوضح نموذج التعليمات البرمجية التالي كيفية الحصول على فواصل الصفحات العمودية داخل ورقة العمل باستخدام Aspose.Cells لـ Cloud API.

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
## **أدخل فاصل صفحة أفقيًا داخل ورقة العمل**
يوضح نموذج الكود التالي كيفية إدراج فاصل صفحات أفقي داخل ورقة العمل باستخدام Aspose.Cells لـ Cloud API.

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
## **قم بإدراج فاصل صفحة عمودي داخل ورقة العمل**
يوضح نموذج التعليمات البرمجية التالي كيفية إدراج "فاصل الصفحة العمودية" داخل ورقة العمل باستخدام Aspose.Cells لـ Cloud API.

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
## **احذف فاصل الصفحة الأفقي داخل ورقة العمل**
يوضح نموذج الكود التالي كيفية الحصول على حذف Horizontal Page Break داخل ورقة العمل باستخدام Aspose.Cells لـ Cloud API.

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
## **حذف فاصل الصفحة العمودية داخل ورقة العمل**
يوضح نموذج التعليمات البرمجية التالي كيفية الحصول على حذف "فاصل الصفحة العمودية" داخل ورقة العمل باستخدام Aspose.Cells لـ Cloud API.

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
## **احتواء تلقائي عمود واحد من ورقة العمل**
يوضح نموذج التعليمات البرمجية التالي كيفية الاحتواء التلقائي لعمود واحد من ورقة العمل. يتلاءم مع**العمود ج**.

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
## **احتواء تلقائي لأعمدة متعددة من ورقة العمل**
يوضح نموذج التعليمات البرمجية التالي كيفية احتواء أعمدة متعددة في ورقة العمل تلقائيًا. يتلاءم مع**الأعمدة A و B و C و D و E و F**.

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
## **احتواء تلقائي لصف واحد من ورقة العمل**
يوضح نموذج التعليمات البرمجية التالي كيفية احتواء صف واحد من ورقة العمل تلقائيًا. يتلاءم مع**الصف الثاني**.

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
## **احتواء تلقائي لصفوف متعددة من ورقة العمل**
يوضح نموذج التعليمات البرمجية التالي كيفية احتواء صفوف متعددة من ورقة العمل تلقائيًا. يتناسب تلقائيًا مع الصفوف المتعددة بدءًا من الصف الثاني إلى الصف الثامن.

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
