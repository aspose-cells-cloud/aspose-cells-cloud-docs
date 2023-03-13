---
title: Travailler avec un tableau croisé dynamique à l'aide de CellsObjectOperate tas
second_title: Aspose.Cells Cloud Documen
type: docs
url: /fr/tasks/cells-object-operate/pivottable/
aliases: [/working-with-pivot-table-using-cellsobjectoperate-task/]
keywords: REST API, pivot table, spreadsheets, exce
description: "Cells.Cloud API pour Excel opérer : créer un tableau croisé dynamique à l'aide de la tâche CellsObjectOperate"
weight: 10
---
Ce REST API crée `pivot table` à l'aide de l'objet cellules fonctionne `task`.

**PivotTableOperateParameterPivotTableOperateParameterPivotTableOperateParameter**


|Le nom du paramètre|Taper|Description|
|:- |:- |:- |
| NomCelluleDest| chaîne||
| Données source| chaîne||
| Nom de la table| chaîne||
| UtiliserMêmeSource| chaîne| vrai faux|
| Index de tableau croisé dynamique| entier||
| PivotFieldRows|entier[]||
| PivotFieldColumns|entier[]||
|PivotFieldData|entier[]||


## REPOS API

|**API**|**Taper**|**Description**|**Lien vers la ressource**|
|:- |:- |:- |:- |
|/cellules/tâche/runtask|POSTE|Exécuter la tâche|[Post-exécution de la tâche](https://apireference.aspose.cloud/cells/#/Task/PostRunTask)|

 Le[Spécification OpenAPI](https://apireference.aspose.cloud/cells/#/Workbook/PostImportData) définit une interface de programmation accessible au public et permet d'effectuer des interactions REST directement depuis un navigateur Web.

 Vous pouvez utiliser**cURL** outil de ligne de commande pour accéder facilement aux services Web Aspose.Cells. L'exemple suivant montre comment passer des appels vers le Cloud API avec cURL.


{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}

{{< tab tabNum="1" >}}

```bash
# cURL example to create pivot table using cells object operate task
curl -v  "https://api.aspose.cloud/v3.0/cells/task/runtask" \
-X POST \
-H "accept: application/xml" \
-H "Content-Type: application/xml" \
-H "Authorization: Bearer <jwt token>" \ 
-d "{
<TaskData>
  <Tasks>
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
</TaskData>
}"

```

{{< /tab >}}

{{< tab tabNum="2" >}}

```bash

HttpResponseMessage with the operation result.

```

{{< /tab >}}

{{< /tabs >}}

## Famille SDK Cloud

 L'utilisation d'un SDK est le meilleur moyen d'accélérer le développement. Un SDK prend en charge les détails de bas niveau et vous permet de vous concentrer sur les tâches de votre projet. Veuillez consulter le[Référentiel GitHub](https://github.com/aspose-cells-cloud) pour obtenir la liste complète des SDK Cloud Aspose.Cells.

Les exemples de code suivants montrent comment effectuer des appels vers les services Web Aspose.Cells à l'aide de divers SDK :

