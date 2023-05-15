---
title: Aspose.Cells Cloud 17.3 Nota di rilascio
second_title: Aspose.Cells Cloud Documen
type: docs
url: /it/aspose-cells-cloud-17-3-release-notes/
aliases: [/aspose-cells-for-cloud-17-3-0-release-notes/]
description: Aspose.Cells Cloud supporta Excel per creare, convertire, unire, dividere, proteggere, operare su oggetti interni e così via
weight: 80
---
{{% alert color="primary" %}} 

 Questa pagina contiene le note di rilascio per[Aspose.Cells Nuvola 17.3](https://downloads.aspose.com/cells/cloud/new-releases/aspose.cells-for-cloud-17.3.0/).

{{% /alert %}} 

|**Chiave**|**Riepilogo**|**Categoria**|
|:- |:- |:- |
|CELLSCLOUD-10028|Inserisci interruzioni di pagina nel foglio di lavoro Excel|Nuova caratteristica|
|CELLSCLOUD-10035|Supporta le altezze delle righe AutoFit|Nuova caratteristica|
|CELLSCLOUD-10036|Supporta la larghezza delle colonne AutoFit|Nuova caratteristica|
## **Ottieni interruzioni di pagina orizzontali all'interno del foglio di lavoro**
Il seguente codice di esempio illustra come ottenere interruzioni di pagina orizzontali all'interno del foglio di lavoro utilizzando Aspose.Cells per Cloud API.

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
## **Ottieni interruzioni di pagina verticali all'interno del foglio di lavoro**
Il codice di esempio seguente illustra come ottenere interruzioni di pagina verticali all'interno del foglio di lavoro utilizzando Aspose.Cells per Cloud API.

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
## **Inserisci un'interruzione di pagina orizzontale all'interno del foglio di lavoro**
Il seguente codice di esempio illustra come inserire un'interruzione di pagina orizzontale all'interno del foglio di lavoro utilizzando Aspose.Cells per Cloud API.

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
## **Inserisci un'interruzione di pagina verticale all'interno del foglio di lavoro**
Il codice di esempio seguente illustra come inserire l'interruzione di pagina verticale all'interno del foglio di lavoro utilizzando Aspose.Cells per Cloud API.

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
## **Elimina l'interruzione di pagina orizzontale all'interno del foglio di lavoro**
Il codice di esempio seguente illustra come eliminare l'interruzione di pagina orizzontale all'interno del foglio di lavoro utilizzando Aspose.Cells per Cloud API.

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
## **Elimina l'interruzione di pagina verticale all'interno del foglio di lavoro**
Il seguente codice di esempio illustra come eliminare l'interruzione di pagina verticale all'interno del foglio di lavoro utilizzando Aspose.Cells per Cloud API.

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
## **Adatta automaticamente una singola colonna del foglio di lavoro**
Il codice di esempio seguente illustra come adattare automaticamente una singola colonna del foglio di lavoro. Si adatta automaticamente al**colonna C**.

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
## **Adatta automaticamente più colonne del foglio di lavoro**
Il codice di esempio seguente illustra come adattare automaticamente più colonne del foglio di lavoro. Si adatta automaticamente al**colonne A, B, C, D, E e F**.

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
## **Adatta singola riga del foglio di lavoro**
Il codice di esempio seguente illustra come adattare automaticamente una singola riga del foglio di lavoro. Si adatta automaticamente al**2a fila**.

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
## **Adatta automaticamente più righe del foglio di lavoro**
Il codice di esempio seguente illustra come adattare automaticamente più righe del foglio di lavoro. Si adatta automaticamente alle righe multiple a partire dalla seconda riga fino all'ottava riga.

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
