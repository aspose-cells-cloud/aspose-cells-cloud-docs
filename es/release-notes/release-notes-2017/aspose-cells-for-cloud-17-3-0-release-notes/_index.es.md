---
title: Aspose.Cells Nota de la versión de Cloud 17.3
second_title: Aspose.Cells Cloud Documen
type: docs
url: /es/aspose-cells-cloud-17-3-release-notes/
aliases: [/aspose-cells-for-cloud-17-3-0-release-notes/]
description: Aspose.Cells La nube admite Excel para crear, convertir, fusionar, dividir, proteger, operación de objetos internos, etc.
weight: 80
---
{{% alert color="primary" %}} 

 Esta página contiene notas de la versión para[Aspose.Cells Nube 17.3](https://downloads.aspose.com/cells/cloud/new-releases/aspose.cells-for-cloud-17.3.0/).

{{% /alert %}} 

|**Llave**|**Resumen**|**Categoría**|
|:- |:- |:- |
|CELLSCLOUD-10028|Insertar saltos de página en la hoja de trabajo Excel|Nueva caracteristica|
|CELLSCLOUD-10035|Admite alturas de fila de ajuste automático|Nueva caracteristica|
|CELLSCLOUD-10036|Admite el ancho de las columnas AutoFit|Nueva caracteristica|
## **Obtenga saltos de página horizontales dentro de la hoja de trabajo**
El siguiente código de muestra ilustra cómo obtener saltos de página horizontales dentro de la hoja de trabajo usando Aspose.Cells para Cloud API.

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
## **Obtenga saltos de página verticales dentro de la hoja de trabajo**
El siguiente código de muestra ilustra cómo obtener saltos de página verticales dentro de la hoja de trabajo usando Aspose.Cells para Cloud API.

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
## **Insertar salto de página horizontal dentro de la hoja de trabajo**
El siguiente código de ejemplo ilustra cómo insertar un salto de página horizontal dentro de la hoja de trabajo usando Aspose.Cells para Cloud API.

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
## **Insertar salto de página vertical dentro de la hoja de trabajo**
El siguiente código de ejemplo ilustra cómo insertar salto de página vertical dentro de la hoja de trabajo usando Aspose.Cells para Cloud API.

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
## **Eliminar salto de página horizontal dentro de la hoja de trabajo**
El siguiente código de ejemplo ilustra cómo eliminar el salto de página horizontal dentro de la hoja de trabajo usando Aspose.Cells para Cloud API.

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
## **Eliminar salto de página vertical dentro de la hoja de trabajo**
El siguiente código de muestra ilustra cómo eliminar el salto de página vertical dentro de la hoja de trabajo usando Aspose.Cells para Cloud API.

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
## **Autoajustar una sola columna de la hoja de trabajo**
El siguiente código de ejemplo ilustra cómo ajustar automáticamente una sola columna de la hoja de trabajo. Se autoajusta al**columna C**.

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
## **Autoajustar varias columnas de la hoja de trabajo**
El siguiente código de ejemplo ilustra cómo autoajustar varias columnas de la hoja de cálculo. Se autoajusta al**columnas A, B, C, D, E y F**.

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
## **Autoajustar una sola fila de la hoja de trabajo**
El siguiente código de ejemplo ilustra cómo ajustar automáticamente una sola fila de la hoja de cálculo. Se autoajusta al**2da fila**.

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
## **Autoajustar varias filas de la hoja de trabajo**
El siguiente código de ejemplo ilustra cómo ajustar automáticamente varias filas de la hoja de cálculo. Se ajusta automáticamente a las múltiples filas desde la 2.ª fila hasta la 8.ª fila.

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
