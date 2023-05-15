---
title: Aspose.Cells Nota de la versión de Cloud 17.2
second_title: Aspose.Cells Cloud Documen
type: docs
url: /es/aspose-cells-cloud-17-2-release-notes/
aliases: [/aspose-cells-for-cloud-17-02-0-release-notes/]
description: Aspose.Cells La nube admite Excel para crear, convertir, fusionar, dividir, proteger, operación de objetos internos, etc.
weight: 90
---
{{% alert color="primary" %}} 

 Esta página contiene notas de la versión para[Aspose.Cells Nube 17.2](https://downloads.aspose.com/cells/cloud/new-releases/aspose.cells-for-cloud-17.02.0/).

{{% /alert %}} 

|**Llave**|**Resumen**|**Categoría**|
|:- |:- |:- |
|CELLSCLOUD-10011|Compatibilidad con filtros de tabla dinámica|Nueva caracteristica|
|CELLSCLOUD-10019|Admite la operación de tabla dinámica en el procesamiento de tareas|Nueva caracteristica|
|CELLSCLOUD-10022|Agregue el parámetro de recálculo para ocultar el elemento del campo pivote|Nueva caracteristica|
|CELLSCLOUD-10024|Objeto de lista - Convertir a rango|Nueva caracteristica|
|CELLSCLOUD-10025|Objeto de lista: resumir con tabla dinámica|Nueva caracteristica|
|CELLSCLOUD-10026|Mover tabla dinámica|Nueva caracteristica|
|CELLSCLOUD-10027|Mover campo de tabla dinámica|Nueva caracteristica|
## **Trabajar con filtros de pivote**
El siguiente código de muestra ilustra cómo trabajar con filtros dinámicos usando Aspose.Cells para Cloud.

```java

public void Run_PivotTable_PivotFilter()

{



    url = @"http://api.aspose.com/v1.1/storage/file/Temp/V17.02.00_01.xlsx";

    using (HttpWebResponse response = _helper.CallDelete(url, string.Empty, contentType))

    {

        Assert.AreEqual(response.StatusCode, HttpStatusCode.OK);

    }

    url = @"http://api.aspose.com/v1.1/cells/V17.02.00_01.xlsx?folder=Temp";

    using (HttpWebResponse response = _helper.CallPut(url, string.Empty, contentType))

    {

        Assert.AreEqual(response.StatusCode, HttpStatusCode.OK);

    }

    url = @"http://api.aspose.com/v1.1/cells/V17.02.00_01.xlsx/worksheets/PivotSheet?folder=Temp";

    using (HttpWebResponse response = _helper.CallPut(url, string.Empty, contentType))

    {

        Assert.AreEqual(response.StatusCode, HttpStatusCode.OK);

    }

    url = @"http://api.aspose.com/v1.1/cells/V17.02.00_01.xlsx/worksheets/Sheet2?folder=Temp";

    using (HttpWebResponse response = _helper.CallPut(url, string.Empty, contentType))

    {

        Assert.AreEqual(response.StatusCode, HttpStatusCode.OK);

    }



    url = @"http://api.aspose.com/v1.1/cells/V17.02.00_01.xlsx/importdata?folder=Temp";



    data = "{ \"BatchData\":[{\"rowIndex\":0,\"columnIndex\":0,\"type\":\"String\",\"value\":\"Sport\",\"style\":null},{\"rowIndex\":0,\"columnIndex\":1,\"type\":\"String\",\"value\":\"Year\",\"style\":null},{\"rowIndex\":0,\"columnIndex\":2,\"type\":\"String\",\"value\":\"Quarter\",\"style\":null},{\"rowIndex\":0,\"columnIndex\":3,\"type\":\"String\",\"value\":\"Sales\",\"style\":null},{\"rowIndex\":0,\"columnIndex\":4,\"type\":\"String\",\"value\":\"YearSales\",\"style\":null},{\"rowIndex\":1,\"columnIndex\":0,\"type\":\"String\",\"value\":\"Golf\",\"style\":null},{\"rowIndex\":2,\"columnIndex\":0,\"type\":\"String\",\"value\":\"Golf\",\"style\":null},{\"rowIndex\":3,\"columnIndex\":0,\"type\":\"String\",\"value\":\"Tennis\",\"style\":null},{\"rowIndex\":4,\"columnIndex\":0,\"type\":\"String\",\"value\":\"Tennis\",\"style\":null},{\"rowIndex\":5,\"columnIndex\":0,\"type\":\"String\",\"value\":\"Tennis\",\"style\":null},{\"rowIndex\":6,\"columnIndex\":0,\"type\":\"String\",\"value\":\"Tennis\",\"style\":null},{\"rowIndex\":7,\"columnIndex\":0,\"type\":\"String\",\"value\":\"Golf\",\"style\":null},{\"rowIndex\":1,\"columnIndex\":1,\"type\":\"int\",\"value\":\"2014\",\"style\":null},{\"rowIndex\":2,\"columnIndex\":1,\"type\":\"int\",\"value\":\"2014\",\"style\":null},{\"rowIndex\":3,\"columnIndex\":1,\"type\":\"int\",\"value\":\"2014\",\"style\":null},{\"rowIndex\":4,\"columnIndex\":1,\"type\":\"int\",\"value\":\"2013\",\"style\":null},{\"rowIndex\":5,\"columnIndex\":1,\"type\":\"int\",\"value\":\"2013\",\"style\":null},{\"rowIndex\":6,\"columnIndex\":1,\"type\":\"int\",\"value\":\"2013\",\"style\":null},{\"rowIndex\":7,\"columnIndex\":1,\"type\":\"int\",\"value\":\"2013\",\"style\":null},{\"rowIndex\":1,\"columnIndex\":2,\"type\":\"String\",\"value\":\"Qtr3\",\"style\":null},{\"rowIndex\":2,\"columnIndex\":2,\"type\":\"String\",\"value\":\"Qtr4\",\"style\":null},{\"rowIndex\":3,\"columnIndex\":2,\"type\":\"String\",\"value\":\"Qtr3\",\"style\":null},{\"rowIndex\":4,\"columnIndex\":2,\"type\":\"String\",\"value\":\"Qtr4\",\"style\":null},{\"rowIndex\":5,\"columnIndex\":2,\"type\":\"String\",\"value\":\"Qtr3\",\"style\":null},{\"rowIndex\":6,\"columnIndex\":2,\"type\":\"String\",\"value\":\"Qtr3\",\"style\":null},{\"rowIndex\":7,\"columnIndex\":2,\"type\":\"String\",\"value\":\"Qtr3\",\"style\":null},{\"rowIndex\":4,\"columnIndex\":3,\"type\":\"int\",\"value\":\"1500\",\"style\":null},{\"rowIndex\":2,\"columnIndex\":3,\"type\":\"int\",\"value\":\"2000\",\"style\":null},{\"rowIndex\":3,\"columnIndex\":3,\"type\":\"int\",\"value\":\"600\",\"style\":null},{\"rowIndex\":4,\"columnIndex\":3,\"type\":\"int\",\"value\":\"1500\",\"style\":null},{\"rowIndex\":5,\"columnIndex\":3,\"type\":\"int\",\"value\":\"4070\",\"style\":null},{\"rowIndex\":6,\"columnIndex\":3,\"type\":\"int\",\"value\":\"5000\",\"style\":null},{\"rowIndex\":7,\"columnIndex\":3,\"type\":\"int\",\"value\":\"6430\",\"style\":null},{\"rowIndex\":1,\"columnIndex\":4,\"type\":\"int\",\"value\":\"15000\",\"style\":null},{\"rowIndex\":2,\"columnIndex\":4,\"type\":\"int\",\"value\":\"20000\",\"style\":null},{\"rowIndex\":3,\"columnIndex\":4,\"type\":\"int\",\"value\":\"600\",\"style\":null},{\"rowIndex\":4,\"columnIndex\":4,\"type\":\"int\",\"value\":\"1500\",\"style\":null},{\"rowIndex\":5,\"columnIndex\":4,\"type\":\"int\",\"value\":\"4070\",\"style\":null},{\"rowIndex\":6,\"columnIndex\":4,\"type\":\"int\",\"value\":\"5000\",\"style\":null},{\"rowIndex\":7,\"columnIndex\":4,\"type\":\"int\",\"value\":\"6430\",\"style\":null}],\"DestinationWorksheet\":\"Sheet2\",\"IsInsert\":false}";

    using (HttpWebResponse response = _helper.CallPost(url, data, contentType))

    {

        Assert.AreEqual(response.StatusCode, HttpStatusCode.OK);

    }

    url = "http://api.aspose.com/v1.1/cells/V17.02.00_01.xlsx/worksheets/PivotSheet/pivottables?folder=Temp";

    data = "{\"Name\":\"TestPivot\",\"SourceData\":\"=Sheet2!A1:E8\",\"DestCellName\":\"C1\",\"UseSameSource\":true,\"PivotFieldRows\":[0,1],\"PivotFieldColumns\":[2],\"PivotFieldData\":[3,4]}";

    using (HttpWebResponse response = _helper.CallPut(url, data, contentType))

    {

        Assert.AreEqual(response.StatusCode, HttpStatusCode.OK);

    }

    url = "http://api.aspose.com/v1.1/cells/V17.02.00_01.xlsx/worksheets/PivotSheet/pivottables/0/PivotFilters?folder=Temp";

    data = "{\"AutoFilter\":null,\"EvaluationOrder\":null,\"FieldIndex\":1,\"FilterType\":\"Count\",\"MeasureFldIndex\":null,\"MemberPropertyFieldIndex\":null,\"Name\":null,\"Value1\":null,\"Value2\":null}";

    using (HttpWebResponse response = _helper.CallPut(url, data, contentType))

    {

        Assert.AreEqual(response.StatusCode, HttpStatusCode.OK);

    }



    url = "http://api.aspose.com/v1.1/cells/V17.02.00_01.xlsx/worksheets/PivotSheet/pivottables/0/PivotFilters/0?folder=Temp";

    using (HttpWebResponse response = _helper.CallGet(url, string.Empty, contentType))

    {

        Assert.AreEqual(response.StatusCode, HttpStatusCode.OK);

    }

    url = "http://api.aspose.com/v1.1/cells/V17.02.00_01.xlsx/worksheets/PivotSheet/pivottables/0/PivotFilters?folder=Temp";

    using (HttpWebResponse response = _helper.CallGet(url, string.Empty, contentType))

    {

        Assert.AreEqual(response.StatusCode, HttpStatusCode.OK);

    }



    url = "http://api.aspose.com/v1.1/cells/V17.02.00_01.xlsx/worksheets/PivotSheet/pivottables/0/PivotFilters/0?folder=Temp";

    using (HttpWebResponse response = _helper.CallDelete(url, string.Empty, contentType))

    {

        Assert.AreEqual(response.StatusCode, HttpStatusCode.OK);

    }



    url = "http://api.aspose.com/v1.1/cells/V17.02.00_01.xlsx/worksheets/PivotSheet/pivottables/0/PivotFilters?folder=Temp";

    using (HttpWebResponse response = _helper.CallDelete(url, string.Empty, contentType))

    {

        Assert.AreEqual(response.StatusCode, HttpStatusCode.OK);

    }



}

```
## **Trabajar con tabla dinámica usando la tarea CellsObjectOperate**
El siguiente código de ejemplo ilustra cómo trabajar con una tabla dinámica mediante el objeto de tarea CellsObjectOperate con Aspose.Cells para Cloud.

```java

public void Run_PivotTable_TaskPivot()

{

    string xml = "<?xml version=\"1.0\"?>" +

                "<TaskData xmlns:xsd=\"http://www.w3.org/2001/XMLSchema\" xmlns:xsi=\"http://www.w3.org/2001/XMLSchema-instance\">" +

                @"<Tasks>

                <TaskDescription>

                    <TaskType>ImportData</TaskType>

                    <ImportDataTaskParameter>

                    <Workbook>

                        <FileSourceType>CloudFileSystem</FileSourceType>

                        <FilePath>Book1.xlsx</FilePath>

                    </Workbook>

                    <ImportBatchDataOption>

                        <DestinationWorksheet>Sheet2</DestinationWorksheet>

                        <IsInsert>true</IsInsert>

                        <BatchData>

                        <CellValue>

                            <rowIndex>0</rowIndex>

                            <columnIndex>0</columnIndex>

                            <type>String</type>

                            <value>Sport</value>

                        </CellValue>

                        <CellValue>

                            <rowIndex>0</rowIndex>

                            <columnIndex>1</columnIndex>

                            <type>String</type>

                            <value>Year</value>

                        </CellValue>

                        <CellValue>

                            <rowIndex>0</rowIndex>

                            <columnIndex>2</columnIndex>

                            <type>String</type>

                            <value>Quarter</value>

                        </CellValue>

                        <CellValue>

                            <rowIndex>0</rowIndex>

                            <columnIndex>3</columnIndex>

                            <type>String</type>

                            <value>Sales</value>

                        </CellValue>

                        <CellValue>

                            <rowIndex>0</rowIndex>

                            <columnIndex>4</columnIndex>

                            <type>String</type>

                            <value>YearSales</value>

                        </CellValue>

                        <CellValue>

                            <rowIndex>1</rowIndex>

                            <columnIndex>0</columnIndex>

                            <type>String</type>

                            <value>Golf</value>

                        </CellValue>

                        <CellValue>

                            <rowIndex>2</rowIndex>

                            <columnIndex>0</columnIndex>

                            <type>String</type>

                            <value>Golf</value>

                        </CellValue>

                        <CellValue>

                            <rowIndex>3</rowIndex>

                            <columnIndex>0</columnIndex>

                            <type>String</type>

                            <value>Tennis</value>

                        </CellValue>

                        <CellValue>

                            <rowIndex>4</rowIndex>

                            <columnIndex>0</columnIndex>

                            <type>String</type>

                            <value>Tennis</value>

                        </CellValue>

                        <CellValue>

                            <rowIndex>5</rowIndex>

                            <columnIndex>0</columnIndex>

                            <type>String</type>

                            <value>Tennis</value>

                        </CellValue>

                        <CellValue>

                            <rowIndex>6</rowIndex>

                            <columnIndex>0</columnIndex>

                            <type>String</type>

                            <value>Tennis</value>

                        </CellValue>

                        <CellValue>

                            <rowIndex>7</rowIndex>

                            <columnIndex>0</columnIndex>

                            <type>String</type>

                            <value>Golf</value>

                        </CellValue>

                        <CellValue>

                            <rowIndex>1</rowIndex>

                            <columnIndex>1</columnIndex>

                            <type>int</type>

                            <value>2014</value>

                        </CellValue>

                        <CellValue>

                            <rowIndex>2</rowIndex>

                            <columnIndex>1</columnIndex>

                            <type>int</type>

                            <value>2014</value>

                        </CellValue>

                        <CellValue>

                            <rowIndex>3</rowIndex>

                            <columnIndex>1</columnIndex>

                            <type>int</type>

                            <value>2014</value>

                        </CellValue>

                        <CellValue>

                            <rowIndex>4</rowIndex>

                            <columnIndex>1</columnIndex>

                            <type>int</type>

                            <value>2013</value>

                        </CellValue>

                        <CellValue>

                            <rowIndex>5</rowIndex>

                            <columnIndex>1</columnIndex>

                            <type>int</type>

                            <value>2013</value>

                        </CellValue>

                        <CellValue>

                            <rowIndex>6</rowIndex>

                            <columnIndex>1</columnIndex>

                            <type>int</type>

                            <value>2013</value>

                        </CellValue>

                        <CellValue>

                            <rowIndex>7</rowIndex>

                            <columnIndex>1</columnIndex>

                            <type>int</type>

                            <value>2013</value>

                        </CellValue>

                        <CellValue>

                            <rowIndex>1</rowIndex>

                            <columnIndex>2</columnIndex>

                            <type>String</type>

                            <value>Qtr3</value>

                        </CellValue>

                        <CellValue>

                            <rowIndex>2</rowIndex>

                            <columnIndex>2</columnIndex>

                            <type>String</type>

                            <value>Qtr4</value>

                        </CellValue>

                        <CellValue>

                            <rowIndex>3</rowIndex>

                            <columnIndex>2</columnIndex>

                            <type>String</type>

                            <value>Qtr3</value>

                        </CellValue>

                        <CellValue>

                            <rowIndex>4</rowIndex>

                            <columnIndex>2</columnIndex>

                            <type>String</type>

                            <value>Qtr4</value>

                        </CellValue>

                        <CellValue>

                            <rowIndex>5</rowIndex>

                            <columnIndex>2</columnIndex>

                            <type>String</type>

                            <value>Qtr3</value>

                        </CellValue>

                        <CellValue>

                            <rowIndex>6</rowIndex>

                            <columnIndex>2</columnIndex>

                            <type>String</type>

                            <value>Qtr4</value>

                        </CellValue>

                        <CellValue>

                            <rowIndex>7</rowIndex>

                            <columnIndex>2</columnIndex>

                            <type>String</type>

                            <value>Qtr3</value>

                        </CellValue>

                        <CellValue>

                            <rowIndex>1</rowIndex>

                            <columnIndex>3</columnIndex>

                            <type>int</type>

                            <value>1500</value>

                        </CellValue>

                        <CellValue>

                            <rowIndex>2</rowIndex>

                            <columnIndex>3</columnIndex>

                            <type>int</type>

                            <value>2000</value>

                        </CellValue>

                        <CellValue>

                            <rowIndex>3</rowIndex>

                            <columnIndex>3</columnIndex>

                            <type>int</type>

                            <value>600</value>

                        </CellValue>

                        <CellValue>

                            <rowIndex>4</rowIndex>

                            <columnIndex>3</columnIndex>

                            <type>int</type>

                            <value>1500</value>

                        </CellValue>

                        <CellValue>

                            <rowIndex>5</rowIndex>

                            <columnIndex>3</columnIndex>

                            <type>int</type>

                            <value>4070</value>

                        </CellValue>

                        <CellValue>

                            <rowIndex>6</rowIndex>

                            <columnIndex>3</columnIndex>

                            <type>int</type>

                            <value>5000</value>

                        </CellValue>

                        <CellValue>

                            <rowIndex>7</rowIndex>

                            <columnIndex>3</columnIndex>

                            <type>int</type>

                            <value>6430</value>

                        </CellValue>

                        <CellValue>

                            <rowIndex>1</rowIndex>

                            <columnIndex>4</columnIndex>

                            <type>int</type>

                            <value>15000</value>

                        </CellValue>

                        <CellValue>

                            <rowIndex>2</rowIndex>

                            <columnIndex>4</columnIndex>

                            <type>int</type>

                            <value>20000</value>

                        </CellValue>

                        <CellValue>

                            <rowIndex>3</rowIndex>

                            <columnIndex>4</columnIndex>

                            <type>int</type>

                            <value>600</value>

                        </CellValue>

                        <CellValue>

                            <rowIndex>4</rowIndex>

                            <columnIndex>4</columnIndex>

                            <type>int</type>

                            <value>1500</value>

                        </CellValue>

                        <CellValue>

                            <rowIndex>5</rowIndex>

                            <columnIndex>4</columnIndex>

                            <type>int</type>

                            <value>4070</value>

                        </CellValue>

                        <CellValue>

                            <rowIndex>6</rowIndex>

                            <columnIndex>4</columnIndex>

                            <type>int</type>

                            <value>5000</value>

                        </CellValue>

                        <CellValue>

                            <rowIndex>7</rowIndex>

                            <columnIndex>4</columnIndex>

                            <type>int</type>

                            <value>6430</value>

                        </CellValue>

                        </BatchData>

                    </ImportBatchDataOption>

                    </ImportDataTaskParameter>

                </TaskDescription>

                <TaskDescription>

                    <TaskType>CellsObjectOperate</TaskType>

                    <CellsObjectOperateTaskParameter>

                    <OperateObject>

                        <OperateObjectType>ListObject</OperateObjectType>

                        <Position>

                        <Workbook>

                            <FileSourceType>InMemoryFiles</FileSourceType>

                            <FilePath>Book1.xlsx</FilePath>

                        </Workbook>

                        <SheetName>Sheet1</SheetName>

                        <ListObjectIndex>0</ListObjectIndex>

                        </Position>

                    </OperateObject>

                    <PivotTableOperateParameter>

                        <OperateType>Add</OperateType>

                        <SourceData>=Sheet2!A1:E8</SourceData>

                        <DestCellName>C1</DestCellName>

                        <TableName>TestPivot</TableName>

                        <UseSameSource>true</UseSameSource>

                        <PivotTableIndex>0</PivotTableIndex>

                        <PivotFieldRows>

                        <int>0</int>

                        <int>1</int>

                        </PivotFieldRows>

                        <PivotFieldColumns>

                        <int>2</int>

                        </PivotFieldColumns>

                        <PivotFieldData>

                        <int>3</int>

                        <int>4</int>

                        </PivotFieldData>

                    </PivotTableOperateParameter>

                    <DestinationWorkbook>

                        <FileSourceType>InMemoryFiles</FileSourceType>

                        <FilePath>Book001.xlsx</FilePath>

                    </DestinationWorkbook>

                    </CellsObjectOperateTaskParameter>

                </TaskDescription>

                <TaskDescription>

                    <TaskType>SaveResult</TaskType>

                    <SaveResultTaskParameter>

                    <ResultSource>InMemoryFiles</ResultSource>

                    <ResultDestination>

                        <DestinationType>OutputStream</DestinationType>

                        <InputFile>Book001.xlsx</InputFile>

                        <OutputFile>Output\ReportS004.xlsx</OutputFile>

                    </ResultDestination>

                    </SaveResultTaskParameter>

                </TaskDescription>

                </Tasks>

            </TaskData>";

    url = "http://api.aspose.com/v1.1/cells/task/runtask";

    using (HttpWebResponse response = _helper.CallPost(url, xml, "application/xml"))

    {

        Assert.AreEqual(response.StatusCode, HttpStatusCode.OK);

    }

}

```
## **Volver a calcular la tabla dinámica después de ocultar el elemento del campo dinámico**
El siguiente código de ejemplo ilustra cómo volver a calcular la tabla dinámica después de ocultar el elemento de campo dinámico mediante Aspose.Cells para la nube.

```java

public void Run_PivotTable_NeedReCalculate()

{

    url = @"http://api.aspose.com/v1.1/storage/file/Temp/V17.02.00_01.xlsx";

    using (HttpWebResponse response = _helper.CallDelete(url, string.Empty, contentType))

    {

        Assert.AreEqual(response.StatusCode, HttpStatusCode.OK);

    }

    url = @"http://api.aspose.com/v1.1/cells/V17.02.00_01.xlsx?folder=Temp";

    using (HttpWebResponse response = _helper.CallPut(url, string.Empty, contentType))

    {

        Assert.AreEqual(response.StatusCode, HttpStatusCode.OK);

    }

    url = @"http://api.aspose.com/v1.1/cells/V17.02.00_01.xlsx/worksheets/PivotSheet?folder=Temp";

    using (HttpWebResponse response = _helper.CallPut(url, string.Empty, contentType))

    {

        Assert.AreEqual(response.StatusCode, HttpStatusCode.OK);

    }

    url = @"http://api.aspose.com/v1.1/cells/V17.02.00_01.xlsx/worksheets/Sheet2?folder=Temp";

    using (HttpWebResponse response = _helper.CallPut(url, string.Empty, contentType))

    {

        Assert.AreEqual(response.StatusCode, HttpStatusCode.OK);

    }



    url = @"http://api.aspose.com/v1.1/cells/V17.02.00_01.xlsx/importdata?folder=Temp";



    data = "{ \"BatchData\":[{\"rowIndex\":0,\"columnIndex\":0,\"type\":\"String\",\"value\":\"Sport\",\"style\":null},{\"rowIndex\":0,\"columnIndex\":1,\"type\":\"String\",\"value\":\"Year\",\"style\":null},{\"rowIndex\":0,\"columnIndex\":2,\"type\":\"String\",\"value\":\"Quarter\",\"style\":null},{\"rowIndex\":0,\"columnIndex\":3,\"type\":\"String\",\"value\":\"Sales\",\"style\":null},{\"rowIndex\":0,\"columnIndex\":4,\"type\":\"String\",\"value\":\"YearSales\",\"style\":null},{\"rowIndex\":1,\"columnIndex\":0,\"type\":\"String\",\"value\":\"Golf\",\"style\":null},{\"rowIndex\":2,\"columnIndex\":0,\"type\":\"String\",\"value\":\"Golf\",\"style\":null},{\"rowIndex\":3,\"columnIndex\":0,\"type\":\"String\",\"value\":\"Tennis\",\"style\":null},{\"rowIndex\":4,\"columnIndex\":0,\"type\":\"String\",\"value\":\"Tennis\",\"style\":null},{\"rowIndex\":5,\"columnIndex\":0,\"type\":\"String\",\"value\":\"Tennis\",\"style\":null},{\"rowIndex\":6,\"columnIndex\":0,\"type\":\"String\",\"value\":\"Tennis\",\"style\":null},{\"rowIndex\":7,\"columnIndex\":0,\"type\":\"String\",\"value\":\"Golf\",\"style\":null},{\"rowIndex\":1,\"columnIndex\":1,\"type\":\"int\",\"value\":\"2014\",\"style\":null},{\"rowIndex\":2,\"columnIndex\":1,\"type\":\"int\",\"value\":\"2014\",\"style\":null},{\"rowIndex\":3,\"columnIndex\":1,\"type\":\"int\",\"value\":\"2014\",\"style\":null},{\"rowIndex\":4,\"columnIndex\":1,\"type\":\"int\",\"value\":\"2013\",\"style\":null},{\"rowIndex\":5,\"columnIndex\":1,\"type\":\"int\",\"value\":\"2013\",\"style\":null},{\"rowIndex\":6,\"columnIndex\":1,\"type\":\"int\",\"value\":\"2013\",\"style\":null},{\"rowIndex\":7,\"columnIndex\":1,\"type\":\"int\",\"value\":\"2013\",\"style\":null},{\"rowIndex\":1,\"columnIndex\":2,\"type\":\"String\",\"value\":\"Qtr3\",\"style\":null},{\"rowIndex\":2,\"columnIndex\":2,\"type\":\"String\",\"value\":\"Qtr4\",\"style\":null},{\"rowIndex\":3,\"columnIndex\":2,\"type\":\"String\",\"value\":\"Qtr3\",\"style\":null},{\"rowIndex\":4,\"columnIndex\":2,\"type\":\"String\",\"value\":\"Qtr4\",\"style\":null},{\"rowIndex\":5,\"columnIndex\":2,\"type\":\"String\",\"value\":\"Qtr3\",\"style\":null},{\"rowIndex\":6,\"columnIndex\":2,\"type\":\"String\",\"value\":\"Qtr3\",\"style\":null},{\"rowIndex\":7,\"columnIndex\":2,\"type\":\"String\",\"value\":\"Qtr3\",\"style\":null},{\"rowIndex\":4,\"columnIndex\":3,\"type\":\"int\",\"value\":\"1500\",\"style\":null},{\"rowIndex\":2,\"columnIndex\":3,\"type\":\"int\",\"value\":\"2000\",\"style\":null},{\"rowIndex\":3,\"columnIndex\":3,\"type\":\"int\",\"value\":\"600\",\"style\":null},{\"rowIndex\":4,\"columnIndex\":3,\"type\":\"int\",\"value\":\"1500\",\"style\":null},{\"rowIndex\":5,\"columnIndex\":3,\"type\":\"int\",\"value\":\"4070\",\"style\":null},{\"rowIndex\":6,\"columnIndex\":3,\"type\":\"int\",\"value\":\"5000\",\"style\":null},{\"rowIndex\":7,\"columnIndex\":3,\"type\":\"int\",\"value\":\"6430\",\"style\":null},{\"rowIndex\":1,\"columnIndex\":4,\"type\":\"int\",\"value\":\"15000\",\"style\":null},{\"rowIndex\":2,\"columnIndex\":4,\"type\":\"int\",\"value\":\"20000\",\"style\":null},{\"rowIndex\":3,\"columnIndex\":4,\"type\":\"int\",\"value\":\"600\",\"style\":null},{\"rowIndex\":4,\"columnIndex\":4,\"type\":\"int\",\"value\":\"1500\",\"style\":null},{\"rowIndex\":5,\"columnIndex\":4,\"type\":\"int\",\"value\":\"4070\",\"style\":null},{\"rowIndex\":6,\"columnIndex\":4,\"type\":\"int\",\"value\":\"5000\",\"style\":null},{\"rowIndex\":7,\"columnIndex\":4,\"type\":\"int\",\"value\":\"6430\",\"style\":null}],\"DestinationWorksheet\":\"Sheet2\",\"IsInsert\":false}";

    using (HttpWebResponse response = _helper.CallPost(url, data, contentType))

    {

        Assert.AreEqual(response.StatusCode, HttpStatusCode.OK);

    }

    url = "http://api.aspose.com/v1.1/cells/V17.02.00_01.xlsx/worksheets/PivotSheet/pivottables?folder=Temp";

    data = "{\"Name\":\"TestPivot\",\"SourceData\":\"=Sheet2!A1:E8\",\"DestCellName\":\"C1\",\"UseSameSource\":true,\"PivotFieldRows\":[0,1],\"PivotFieldColumns\":[2],\"PivotFieldData\":[3,4]}";

    using (HttpWebResponse response = _helper.CallPut(url, data, contentType))

    {

        Assert.AreEqual(response.StatusCode, HttpStatusCode.OK);

    }

    url = "http://api.aspose.com/v1.1/cells/V17.02.00_01.xlsx/worksheets/PivotSheet/pivottables/0/PivotField?pivotFieldType=Row&folder=Temp&needReCalculate=true";

    data = "{\"Data\":[1]}";

    using (HttpWebResponse response = _helper.CallPut(url, data, contentType))

    {

        Assert.AreEqual(response.StatusCode, HttpStatusCode.OK);

    }

}

```

## **Convertir objeto de lista o tabla en rango**
El siguiente código de ejemplo ilustra cómo convertir un objeto de lista o una tabla en un rango mediante Aspose.Cells para Cloud.

```java

public void Run_ListObject_ConvertToRange()

{

    url = @"http://api.aspose.com/v1.1/storage/file/Temp/V17.02.00_04.xlsx";

    using (HttpWebResponse response = _helper.CallDelete(url, string.Empty, contentType))

    {

        Assert.AreEqual(response.StatusCode, HttpStatusCode.OK);

    }



    url = @"http://api.aspose.com/v1.1/cells/V17.02.00_04.xlsx?folder=Temp";

    using (HttpWebResponse response = _helper.CallPut(url, string.Empty, contentType))

    {

        Assert.AreEqual(response.StatusCode, HttpStatusCode.OK);

    }



    url = @"http://api.aspose.com/v1.1/cells/V17.02.00_04.xlsx/worksheets/Sheet1?folder=Temp";

    using (HttpWebResponse response = _helper.CallPut(url, string.Empty, contentType))

    {

        Assert.AreEqual(response.StatusCode, HttpStatusCode.OK);

    }



    url = @"http://api.aspose.com/v1.1/cells/V17.02.00_04.xlsx/importdata?folder=Temp";

    data = "{\"BatchData\":[{\"rowIndex\":0,\"columnIndex\":0,\"type\":\"String\",\"value\":\"Sport\",\"style\":null},{\"rowIndex\":0,\"columnIndex\":1,\"type\":\"String\",\"value\":\"Year\",\"style\":null},{\"rowIndex\":0,\"columnIndex\":2,\"type\":\"String\",\"value\":\"Quarter\",\"style\":null},{\"rowIndex\":0,\"columnIndex\":3,\"type\":\"String\",\"value\":\"Sales\",\"style\":null},{\"rowIndex\":0,\"columnIndex\":4,\"type\":\"String\",\"value\":\"YearSales\",\"style\":null},{\"rowIndex\":1,\"columnIndex\":0,\"type\":\"String\",\"value\":\"Golf\",\"style\":null},{\"rowIndex\":2,\"columnIndex\":0,\"type\":\"String\",\"value\":\"Golf\",\"style\":null},{\"rowIndex\":3,\"columnIndex\":0,\"type\":\"String\",\"value\":\"Tennis\",\"style\":null},{\"rowIndex\":4,\"columnIndex\":0,\"type\":\"String\",\"value\":\"Tennis\",\"style\":null},{\"rowIndex\":5,\"columnIndex\":0,\"type\":\"String\",\"value\":\"Tennis\",\"style\":null},{\"rowIndex\":6,\"columnIndex\":0,\"type\":\"String\",\"value\":\"Tennis\",\"style\":null},{\"rowIndex\":7,\"columnIndex\":0,\"type\":\"String\",\"value\":\"Golf\",\"style\":null},{\"rowIndex\":1,\"columnIndex\":1,\"type\":\"int\",\"value\":\"2014\",\"style\":null},{\"rowIndex\":2,\"columnIndex\":1,\"type\":\"int\",\"value\":\"2014\",\"style\":null},{\"rowIndex\":3,\"columnIndex\":1,\"type\":\"int\",\"value\":\"2014\",\"style\":null},{\"rowIndex\":4,\"columnIndex\":1,\"type\":\"int\",\"value\":\"2013\",\"style\":null},{\"rowIndex\":5,\"columnIndex\":1,\"type\":\"int\",\"value\":\"2013\",\"style\":null},{\"rowIndex\":6,\"columnIndex\":1,\"type\":\"int\",\"value\":\"2013\",\"style\":null},{\"rowIndex\":7,\"columnIndex\":1,\"type\":\"int\",\"value\":\"2013\",\"style\":null},{\"rowIndex\":1,\"columnIndex\":2,\"type\":\"String\",\"value\":\"Qtr3\",\"style\":null},{\"rowIndex\":2,\"columnIndex\":2,\"type\":\"String\",\"value\":\"Qtr4\",\"style\":null},{\"rowIndex\":3,\"columnIndex\":2,\"type\":\"String\",\"value\":\"Qtr3\",\"style\":null},{\"rowIndex\":4,\"columnIndex\":2,\"type\":\"String\",\"value\":\"Qtr4\",\"style\":null},{\"rowIndex\":5,\"columnIndex\":2,\"type\":\"String\",\"value\":\"Qtr3\",\"style\":null},{\"rowIndex\":6,\"columnIndex\":2,\"type\":\"String\",\"value\":\"Qtr3\",\"style\":null},{\"rowIndex\":7,\"columnIndex\":2,\"type\":\"String\",\"value\":\"Qtr3\",\"style\":null},{\"rowIndex\":4,\"columnIndex\":3,\"type\":\"int\",\"value\":\"1500\",\"style\":null},{\"rowIndex\":2,\"columnIndex\":3,\"type\":\"int\",\"value\":\"2000\",\"style\":null},{\"rowIndex\":3,\"columnIndex\":3,\"type\":\"int\",\"value\":\"600\",\"style\":null},{\"rowIndex\":4,\"columnIndex\":3,\"type\":\"int\",\"value\":\"1500\",\"style\":null},{\"rowIndex\":5,\"columnIndex\":3,\"type\":\"int\",\"value\":\"4070\",\"style\":null},{\"rowIndex\":6,\"columnIndex\":3,\"type\":\"int\",\"value\":\"5000\",\"style\":null},{\"rowIndex\":7,\"columnIndex\":3,\"type\":\"int\",\"value\":\"6430\",\"style\":null},{\"rowIndex\":1,\"columnIndex\":4,\"type\":\"int\",\"value\":\"15000\",\"style\":null},{\"rowIndex\":2,\"columnIndex\":4,\"type\":\"int\",\"value\":\"20000\",\"style\":null},{\"rowIndex\":3,\"columnIndex\":4,\"type\":\"int\",\"value\":\"600\",\"style\":null},{\"rowIndex\":4,\"columnIndex\":4,\"type\":\"int\",\"value\":\"1500\",\"style\":null},{\"rowIndex\":5,\"columnIndex\":4,\"type\":\"int\",\"value\":\"4070\",\"style\":null},{\"rowIndex\":6,\"columnIndex\":4,\"type\":\"int\",\"value\":\"5000\",\"style\":null},{\"rowIndex\":7,\"columnIndex\":4,\"type\":\"int\",\"value\":\"6430\",\"style\":null}],\"DestinationWorksheet\":\"Sheet1\",\"IsInsert\":false}";

    using (HttpWebResponse response = _helper.CallPost(url, data, contentType))

    {

        Assert.AreEqual(response.StatusCode, HttpStatusCode.OK);

    }



    url = "http://api.aspose.com/v1.1/cells/V17.02.00_04.xlsx/worksheets/Sheet1/listobjects?startRow=0&startColumn=0&endRow=7&endColumn=4&hasHeaders=True&folder=Temp";

    using (HttpWebResponse response = _helper.CallPut(url, string.Empty, contentType))

    {

        Assert.AreEqual(response.StatusCode, HttpStatusCode.OK);

    }

    url = "http://api.aspose.com/v1.1/cells/V17.02.00_04.xlsx/worksheets/Sheet1/listobjects/0/ConvertToRange?folder=Temp";

    using (HttpWebResponse response = _helper.CallPost(url, string.Empty, contentType))

    {

        Assert.AreEqual(response.StatusCode, HttpStatusCode.OK);

    }

```
## **Crear nueva tabla dinámica con objeto de lista como datos de origen**
El siguiente código de ejemplo ilustra cómo crear una nueva tabla dinámica con un objeto de lista como datos de origen mediante Aspose.Cells para la nube.

```java

public void Run_ListObject_SummarizeWithPivotTable()

{

    url = @"http://api.aspose.com/v1.1/storage/file/Temp/V17.02.00_04.xlsx";

    using (HttpWebResponse response = _helper.CallDelete(url, string.Empty, contentType))

    {

        Assert.AreEqual(response.StatusCode, HttpStatusCode.OK);

    }



    url = @"http://api.aspose.com/v1.1/cells/V17.02.00_04.xlsx?folder=Temp";

    using (HttpWebResponse response = _helper.CallPut(url, string.Empty, contentType))

    {

        Assert.AreEqual(response.StatusCode, HttpStatusCode.OK);

    }



    url = @"http://api.aspose.com/v1.1/cells/V17.02.00_04.xlsx/worksheets/Sheet1?folder=Temp";

    using (HttpWebResponse response = _helper.CallPut(url, string.Empty, contentType))

    {

        Assert.AreEqual(response.StatusCode, HttpStatusCode.OK);

    }

    url = @"http://api.aspose.com/v1.1/cells/V17.02.00_04.xlsx/worksheets/Sheet2?folder=Temp";

    using (HttpWebResponse response = _helper.CallPut(url, string.Empty, contentType))

    {

        Assert.AreEqual(response.StatusCode, HttpStatusCode.OK);

    }



    url = @"http://api.aspose.com/v1.1/cells/V17.02.00_04.xlsx/importdata?folder=Temp";

    data = "{\"BatchData\":[{\"rowIndex\":0,\"columnIndex\":0,\"type\":\"String\",\"value\":\"Sport\",\"style\":null},{\"rowIndex\":0,\"columnIndex\":1,\"type\":\"String\",\"value\":\"Year\",\"style\":null},{\"rowIndex\":0,\"columnIndex\":2,\"type\":\"String\",\"value\":\"Quarter\",\"style\":null},{\"rowIndex\":0,\"columnIndex\":3,\"type\":\"String\",\"value\":\"Sales\",\"style\":null},{\"rowIndex\":0,\"columnIndex\":4,\"type\":\"String\",\"value\":\"YearSales\",\"style\":null},{\"rowIndex\":1,\"columnIndex\":0,\"type\":\"String\",\"value\":\"Golf\",\"style\":null},{\"rowIndex\":2,\"columnIndex\":0,\"type\":\"String\",\"value\":\"Golf\",\"style\":null},{\"rowIndex\":3,\"columnIndex\":0,\"type\":\"String\",\"value\":\"Tennis\",\"style\":null},{\"rowIndex\":4,\"columnIndex\":0,\"type\":\"String\",\"value\":\"Tennis\",\"style\":null},{\"rowIndex\":5,\"columnIndex\":0,\"type\":\"String\",\"value\":\"Tennis\",\"style\":null},{\"rowIndex\":6,\"columnIndex\":0,\"type\":\"String\",\"value\":\"Tennis\",\"style\":null},{\"rowIndex\":7,\"columnIndex\":0,\"type\":\"String\",\"value\":\"Golf\",\"style\":null},{\"rowIndex\":1,\"columnIndex\":1,\"type\":\"int\",\"value\":\"2014\",\"style\":null},{\"rowIndex\":2,\"columnIndex\":1,\"type\":\"int\",\"value\":\"2014\",\"style\":null},{\"rowIndex\":3,\"columnIndex\":1,\"type\":\"int\",\"value\":\"2014\",\"style\":null},{\"rowIndex\":4,\"columnIndex\":1,\"type\":\"int\",\"value\":\"2013\",\"style\":null},{\"rowIndex\":5,\"columnIndex\":1,\"type\":\"int\",\"value\":\"2013\",\"style\":null},{\"rowIndex\":6,\"columnIndex\":1,\"type\":\"int\",\"value\":\"2013\",\"style\":null},{\"rowIndex\":7,\"columnIndex\":1,\"type\":\"int\",\"value\":\"2013\",\"style\":null},{\"rowIndex\":1,\"columnIndex\":2,\"type\":\"String\",\"value\":\"Qtr3\",\"style\":null},{\"rowIndex\":2,\"columnIndex\":2,\"type\":\"String\",\"value\":\"Qtr4\",\"style\":null},{\"rowIndex\":3,\"columnIndex\":2,\"type\":\"String\",\"value\":\"Qtr3\",\"style\":null},{\"rowIndex\":4,\"columnIndex\":2,\"type\":\"String\",\"value\":\"Qtr4\",\"style\":null},{\"rowIndex\":5,\"columnIndex\":2,\"type\":\"String\",\"value\":\"Qtr3\",\"style\":null},{\"rowIndex\":6,\"columnIndex\":2,\"type\":\"String\",\"value\":\"Qtr3\",\"style\":null},{\"rowIndex\":7,\"columnIndex\":2,\"type\":\"String\",\"value\":\"Qtr3\",\"style\":null},{\"rowIndex\":4,\"columnIndex\":3,\"type\":\"int\",\"value\":\"1500\",\"style\":null},{\"rowIndex\":2,\"columnIndex\":3,\"type\":\"int\",\"value\":\"2000\",\"style\":null},{\"rowIndex\":3,\"columnIndex\":3,\"type\":\"int\",\"value\":\"600\",\"style\":null},{\"rowIndex\":4,\"columnIndex\":3,\"type\":\"int\",\"value\":\"1500\",\"style\":null},{\"rowIndex\":5,\"columnIndex\":3,\"type\":\"int\",\"value\":\"4070\",\"style\":null},{\"rowIndex\":6,\"columnIndex\":3,\"type\":\"int\",\"value\":\"5000\",\"style\":null},{\"rowIndex\":7,\"columnIndex\":3,\"type\":\"int\",\"value\":\"6430\",\"style\":null},{\"rowIndex\":1,\"columnIndex\":4,\"type\":\"int\",\"value\":\"15000\",\"style\":null},{\"rowIndex\":2,\"columnIndex\":4,\"type\":\"int\",\"value\":\"20000\",\"style\":null},{\"rowIndex\":3,\"columnIndex\":4,\"type\":\"int\",\"value\":\"600\",\"style\":null},{\"rowIndex\":4,\"columnIndex\":4,\"type\":\"int\",\"value\":\"1500\",\"style\":null},{\"rowIndex\":5,\"columnIndex\":4,\"type\":\"int\",\"value\":\"4070\",\"style\":null},{\"rowIndex\":6,\"columnIndex\":4,\"type\":\"int\",\"value\":\"5000\",\"style\":null},{\"rowIndex\":7,\"columnIndex\":4,\"type\":\"int\",\"value\":\"6430\",\"style\":null}],\"DestinationWorksheet\":\"Sheet1\",\"IsInsert\":false}";

    using (HttpWebResponse response = _helper.CallPost(url, data, contentType))

    {

        Assert.AreEqual(response.StatusCode, HttpStatusCode.OK);

    }



    url = "http://api.aspose.com/v1.1/cells/V17.02.00_04.xlsx/worksheets/Sheet1/listobjects?startRow=0&startColumn=0&endRow=7&endColumn=4&hasHeaders=True&folder=Temp";

    using (HttpWebResponse response = _helper.CallPut(url, string.Empty, contentType))

    {

        Assert.AreEqual(response.StatusCode, HttpStatusCode.OK);

    }



    url = "http://api.aspose.com/v1.1/cells/V17.02.00_04.xlsx/worksheets/Sheet1/listobjects/0/SummarizeWithPivotTable?destsheetName=Sheet2&folder=Temp";

    data = "{\"Name\":\"TestPivot\",\"DestCellName\":\"C1\",\"UseSameSource\":true,\"PivotFieldRows\":[0,1],\"PivotFieldColumns\":[2],\"PivotFieldData\":[3,4]}";

    using (HttpWebResponse response = _helper.CallPost(url, data, contentType))

    {

        Assert.AreEqual(response.StatusCode, HttpStatusCode.OK);

    }



    url = "http://api.aspose.com/v1.1/storage/file/Temp/V17.02.00_04.xlsx";

    using (HttpWebResponse response = _helper.CallGet(url, string.Empty))

    {

        using (var stream = System.IO.File.Create(@"V17.02.00_04.xlsx"))

        {

            response.GetResponseStream().CopyTo(stream);

        }

    }

}

```
## **Ejemplos de uso**
Consulte la lista de temas de ayuda agregados en los documentos Wiki Aspose.Cells:

1. [Trabajar con filtros de pivote](/cells/es/working-with-pivot-tables/)
1. [Trabajar con tabla dinámica usando la tarea CellsObjectOperate](/cells/es/working-with-pivot-table-using-cellsobjectoperate-task/)
1. [Volver a calcular la tabla dinámica después de ocultar el elemento del campo dinámico](/cells/es/hide-pivot-field-item/)
1. [Convertir objeto de lista o tabla en rango](/cells/es/convert-list-object-or-table-to-range/)
1. [Crear nueva tabla dinámica con objeto de lista como datos de origen](/cells/es/add-a-pivot-table-in-a-worksheet/)
