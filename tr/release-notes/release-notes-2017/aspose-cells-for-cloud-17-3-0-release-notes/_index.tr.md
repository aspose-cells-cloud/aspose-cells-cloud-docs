---
title: Aspose.Cells Bulut 17.3 Sürüm Notu
second_title: Aspose.Cells Cloud Documen
type: docs
url: /tr/aspose-cells-cloud-17-3-release-notes/
aliases: [/aspose-cells-for-cloud-17-3-0-release-notes/]
description: Aspose.Cells Bulut, oluşturma, dönüştürme, birleştirme, bölme, korumalı, iç nesne işlemi vb. için Excel'i destekler
weight: 80
---
{{% alert color="primary" %}} 

 Bu sayfa için sürüm notları içerir[Aspose.Cells Bulut 17.3](https://downloads.aspose.com/cells/cloud/new-releases/aspose.cells-for-cloud-17.3.0/).

{{% /alert %}} 

|**Anahtar**|**Özet**|**Kategori**|
|:- |:- |:- |
|CELLSCLOUD-10028|Excel çalışma sayfasına sayfa sonları ekle|Yeni özellik|
|CELLSCLOUD-10035|AutoFit satır yüksekliklerini destekler|Yeni özellik|
|CELLSCLOUD-10036|AutoFit sütun genişliğini destekler|Yeni özellik|
## **Çalışma Sayfası İçinde Yatay Sayfa Sonları Alın**
Aşağıdaki örnek kod, Bulut API için Aspose.Cells kullanarak Çalışma Sayfası içinde Yatay Sayfa Sonlarının nasıl alınacağını gösterir.

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
## **Çalışma Sayfası İçinde Dikey Sayfa Sonları Alın**
Aşağıdaki örnek kod, Bulut API için Aspose.Cells kullanılarak Çalışma Sayfası içinde Dikey Sayfa Sonlarının nasıl alınacağını gösterir.

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
## **Çalışma Sayfasının İçine Yatay Sayfa Sonu Ekle**
Aşağıdaki örnek kod, Bulut API için Aspose.Cells kullanılarak Çalışma Sayfasına Yatay Sayfa Sonunun nasıl ekleneceğini gösterir.

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
## **Çalışma Sayfasının İçine Dikey Sayfa Sonu Ekleme**
Aşağıdaki örnek kod, Bulut API için Aspose.Cells kullanılarak Çalışma Sayfasının içine Dikey Sayfa Sonunun nasıl ekleneceğini gösterir.

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
## **Çalışma Sayfası İçinde Yatay Sayfa Sonunu Sil**
Aşağıdaki örnek kod, Cloud API için Aspose.Cells kullanılarak Worksheet içinde Yatay Sayfa Sonunun nasıl silineceğini gösterir.

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
## **Çalışma Sayfası İçinde Dikey Sayfa Sonunu Sil**
Aşağıdaki örnek kod, Cloud API için Aspose.Cells kullanılarak Çalışma Sayfası içinde Dikey Sayfa Sonunun nasıl silineceğini gösterir.

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
## **Çalışma Sayfasının Tek Sütununu Otomatik Sığdır**
Aşağıdaki örnek kod, çalışma sayfasının tek sütununun otomatik olarak nasıl sığdırılacağını gösterir. otomatik sığar**C sütunu**.

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
## **Çalışma Sayfasının Birden Çok Sütununu Otomatik Sığdır**
Aşağıdaki örnek kod, çalışma sayfasının birden çok sütununun otomatik olarak nasıl sığdırılacağını gösterir. otomatik sığar**A, B, C, D, E ve F sütunları**.

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
## **Çalışma Sayfasının Tek Sırasını Otomatik Sığdır**
Aşağıdaki örnek kod, çalışma sayfasının tek satırının otomatik olarak nasıl sığdırılacağını gösterir. otomatik sığar**2. sıra**.

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
## **Çalışma Sayfasının Birden Çok Satırını Otomatik Sığdır**
Aşağıdaki örnek kod, çalışma sayfasının birden çok satırının otomatik olarak nasıl sığdırılacağını gösterir. 2. sıradan başlayarak 8. sıraya kadar olan birden fazla sırayı otomatik sığdırır.

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
