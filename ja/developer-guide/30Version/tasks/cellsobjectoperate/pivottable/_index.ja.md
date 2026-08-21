---
title: "CellsObjectOperate タスクを使用したピボットテーブルの操作"
type: docs
url: /tasks/cells-object-operate/pivottable/
aliases: [/working-with-pivot-table-using-cellsobjectoperate-task/]
keywords: "Aspose Cells ピボットテーブル API、CellsObjectOperate、Excel REST API"
description: "Aspose.Cells Cloud の CellsObjectOperate タスクを使って Excel でピボットテーブルを生成する方法を学びます。cURL のサンプル、パラメータガイド、SDK 参照を含みます。"
weight: 10
---

この REST API は、**CellsObjectOperate** タスクを使用してピボットテーブルを**作成**します。

**PivotTableOperateParameter**

| パラメータ名          | 型            | 説明                                                                 |
|-----------------------|---------------|----------------------------------------------------------------------|
| DestCellName          | string        | ピボットテーブルの左上セル（例：`C1`）                               |
| SourceData            | string        | ソースデータを含む範囲（例：`Sheet2!A1:E8`）                         |
| TableName             | string        | 新規ピボットテーブルに割り当てられる名前                              |
| UseSameSource         | string        | `true` / `false` — ピボットテーブルが同じソースワークブックを使用するかどうか |
| PivotTableIndex       | integer       | シート内に複数のピボットテーブルが存在する場合のインデックス          |
| PivotFieldRows        | integer[]     | 行エリアに配置するフィールドの 0 始まりのインデックス                |
| PivotFieldColumns     | integer[]     | 列エリアに配置するフィールドの 0 始まりのインデックス                |
| PivotFieldData        | integer[]     | 集計対象のデータとして使用するフィールドの 0 始まりのインデックス     |

## REST API

| **API**               | **タイプ** | **説明**       | **リソースリンク** |
|-----------------------|------------|----------------|--------------------|
| /cells/task/runtask   | POST       | タスクの実行     | [PostRunTask](https://apireference.aspose.cloud/cells/#/Task/PostRunTask) |

[OpenAPI スペック](https://apireference.aspose.cloud/cells/#/Workbook/PostImportData) は公開可能なプログラミングインターフェースを定義し、Web ブラウザから直接 REST 通信を実行できるようにします。

### 前提条件
API を呼び出す前に、以下の手順を実施してください：

1. Aspose.Cloud アカウントを登録し、アプリケーションを作成して **クライアント ID** と **クライアントシークレット** を取得します。  
2. クライアント認証情報を使って `/connect/token` エンドポイントから **JWT トークン** を取得します。  
3. すべてのリクエストの `Authorization: Bearer <jwt token>` ヘッダーにトークンを含めます。  

これで、**cURL** コマンドラインツールを使って Aspose.Cells Web サービスにアクセスできるようになりました。

{{< tabs tabTotal="2" tabID="1" tabName1="リクエスト" tabName2="レスポンス" >}}

{{< tab tabNum="1" >}}

```bash
# cURL サンプル – データのインポート（ステップ 1）
curl -v "https://api.aspose.cloud/v3.0/cells/task/runtask" \
  -X POST \
  -H "accept: application/xml" \
  -H "Content-Type: application/xml" \
  -H "Authorization: Bearer <jwt token>" \
  -d '
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
            <!-- サンプル行 – 簡潔さのため一部のみ表示 -->
            <CellValue><rowIndex>0</rowIndex><columnIndex>0</columnIndex><type>String</type><value>スポーツ</value></CellValue>
            <CellValue><rowIndex>0</rowIndex><columnIndex>1</columnIndex><type>String</type><value>年</value></CellValue>
            <CellValue><rowIndex>0</rowIndex><columnIndex>2</columnIndex><type>String</type><value>四半期</value></CellValue>
            <CellValue><rowIndex>0</rowIndex><columnIndex>3</columnIndex><type>String</type><value>売上</value></CellValue>
            <!-- …追加行は省略… -->
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
          <PivotFieldRows><int>0</int><int>1</int></PivotFieldRows>
          <PivotFieldColumns><int>2</int></PivotFieldColumns>
          <PivotFieldData><int>3</int><int>4</int></PivotFieldData>
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
          <OutputFile>Output/ReportS004.xlsx</OutputFile>
        </ResultDestination>
      </SaveResultTaskParameter>
    </TaskDescription>
  </Tasks>
</TaskData>'
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```text
返される可能性のある HTTP ステータスコード：
- **200 OK** — ピボットテーブルが正常に作成されました。レスポンス本文には操作ステータスを照会するために使用できる `TaskId` が含まれます。
- **400 Bad Request** — 無効な XML ペイロード、または必須パラメータが不足しています。
- **401 Unauthorized** — JWT トークンが不足している、または無効です。
- **500 Internal Server Error** — サーバー側で予期せぬエラーが発生しました。

成功レスポンスの例（XML）：

<?xml version="1.0" encoding="UTF-8"?>
<TaskResponse>
  <TaskId>12345</TaskId>
  <Status>Completed</Status>
  <Result>
    <ResultSource>InMemoryFiles</ResultSource>
    <ResultDestination>Output/ReportS004.xlsx</ResultDestination>
  </Result>
</TaskResponse>
```

{{< /tab >}}

{{< /tabs >}}

## Cloud SDK Family
SDK を使用すると、開発を最適化できます。SDK は低レベルの詳細を処理し、プロジェクトのタスクに集中できるようにします。Aspose.Cells Cloud SDK の完全なリストについては、[GitHub リポジトリ](https://github.com/aspose-cells-cloud) を参照してください。

以下のコード例は、さまざまな SDK を使って Aspose.Cells Web サービスを呼び出す方法を示しています：