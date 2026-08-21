---
title: "Aspose.Cells Cloud API – CellsObjectOperate タスクの使用方法 (REST)"
second_title: "ドキュメント"
type: docs
url: /tasks/cells-object-operate/
aliases: [/working-with-cellsobjectoperate-task/]
description: "Aspose.Cells Cloud API における CellsObjectOperate タスクの使い方を、パラメータのリファレンス、リクエスト／レスポンスの例、およびワークシート、チャート、ピボットテーブルにおけるベストプラクティスのヒントを交えて学びましょう。"
weight: 20
ArticleTitle: "Aspose.Cells Cloud API – CellsObjectOperate タスクの使用方法 (REST)"
keywords:
  - "Aspose CellsObjectOperate"
  - "CellsObjectOperate タスク"
  - "Aspose.Cells Cloud API"
  - "Excel REST API"
  - "chart operation"
  - "pivot table API"
  - "page break API"
---

**概要**  
**CellsObjectOperate** タスクでは、ワークブック、ワークシート、チャート、ピボットテーブル、図形、ページ区切りなどの Excel オブジェクトに対し、単一の REST 呼び出しで作成・読み取り・更新・削除（CRUD）操作を実行できます。`OperateObjectType` で対象オブジェクトの種類を指定し、対応するパラメータブロック（例：チャート関連の操作には `ChartOperateParameter`）を提供します。

---

**OperateObject**

| パラメータ名            | 型     | 説明 |
| ----------------------- | ------ | ----------- |
| OperateObjectType       | 文字列 | 操作対象とする Excel オブジェクトの種類。許可される値：`Workbook`, `Worksheet`, `PageSetup`, `Cells`, `Chart`, `Shape`, `ListObject`, `PivotTable`, `WorkbookSettings`, `PageBreak`。 |
| OperateObjectPosition   | オブジェクト | 対象オブジェクトの配置場所を識別するコンテナ（例：ワークブック名、ワークシート名、チャートのインデックス）。ほとんどの操作で必要です。 |

**OperateObjectPosition**

| パラメータ名     | 型     | 説明 |
| -------------- | ------ | ----------- |
| Workbook       | オブジェクト | 対象オブジェクトを含むワークブック。`FileName`（クラウドストレージ）または `FileContent`（Base64 エンコードされた内容）のいずれかを含める必要があります。 |
| SheetName      | 文字列 | 操作を適用するワークシートの名前。ワークシートレベルのオブジェクト（チャート、図形など）の場合に必要です。 |
| ChartIndex     | 整数   | ワークシート内におけるチャートの 0 から始まるインデックス（`OperateObjectType` が `Chart` の場合に使用）。 |
| ShapeIndex     | 整数   | ワークシート内における図形の 0 から始まるインデックス（`OperateObjectType` が `Shape` の場合に使用）。 |
| CellName       | 文字列 | A1 形式のセル参照（例：`A1`）。セルレベルの操作に使用されます。 |
| ListObjectIndex| 整数   | リストオブジェクト（テーブル）の 0 から始まるインデックス（`OperateObjectType` が `ListObject` の場合に使用）。 |

**ChartOperateParameter**

| パラメータ名          | 型     | 説明 |
| --------------------- | ------ | ----------- |
| ChartIndex            | 整数   | 変更するチャートのインデックス。既存のチャートを更新する場合に必要です。 |
| ChartType             | 文字列 | 作成するチャートの種類（例：`Bar`, `Line`, `Pie`）。 |
| UpperLeftRow          | 整数   | チャートの左上隅の行番号（0 から始まる）。 |
| UpperLeftColumn       | 整数   | チャートの左上隅の列番号（0 から始まる）。 |
| LowerRightRow         | 整数   | チャートの右下隅の行番号。 |
| LowerRightColumn      | 整数   | チャートの右下隅の列番号。 |
| Area                  | 文字列 | チャートのデータ範囲（例：`A1:B5`）。 |
| IsVertical            | 文字列 | チャートの向きが縦方向の場合は `true`、それ以外は `false`。 |
| CategoryData          | 文字列 | カテゴリ（X 軸）ラベルを提供する範囲。 |
| IsAutoGetSerialName   | 文字列 | シリーズ名を自動生成する場合は `true`、カスタム名を使用する場合は `false`。 |
| Title                 | 文字列 | チャートに表示されるタイトルのテキスト。 |

**ListObjectOperateParameter**

| パラメータ名 | 型     | 説明 |
| ------------ | ------ | ----------- |
| ListObject   | オブジェクト | リスト（テーブル）操作用の設定オブジェクト。`ShowHeader`, `ShowTotal`, `Style` などのプロパティを含みます。 |

**PageBreakOperateParameter**

| パラメータ名 | 型     | 説明 |
| ------------ | ------ | ----------- |
| PageBreakType| 文字列 | ページ区切りの種類（`Horizontal` または `Vertical`）。 |
| Index        | 整数   | 削除または変更するページ区切りの 0 から始まるインデックス。 |
| Row          | 整数   | 水平ページ区切りを配置する行番号。 |
| Column       | 整数   | 垂直ページ区切りを配置する列番号。 |
| StartIndex   | 整数   | 範囲ベースのページ区切り操作の開始インデックス。 |
| EndIndex     | 整数   | 範囲ベースのページ区切り操作の終了インデックス。 |

**PageSetupOperateParameter**

| パラメータ名 | 型     | 説明 |
| ------------ | ------ | ----------- |
| PageSetup    | オブジェクト | ページレイアウトの設定（余白、向き、用紙サイズなど）。 |

**PivotTableOperateParameter**

| パラメータ名     | 型          | 説明 |
| ---------------- | ----------- | ----------- |
| DestCellName     | 文字列      | ピボットテーブルの出力先範囲の左上セル（例：`C5`）。 |
| SourceData       | 文字列      | ピボットテーブルのソース範囲（例：`A1:D100`）。 |
| TableName        | 文字列      | 作成されたピボットテーブルに割り当てられる名前。 |
| UseSameSource    | 文字列      | 既存のソース範囲を再利用する場合は `true`、新規に作成する場合は `false`。 |
| PivotTableIndex  | 整数        | 更新するピボットテーブルのインデックス（変更・削除操作に必要）。 |
| PivotFieldRows   | 整数の配列  | 行領域に表示されるフィールドのインデックスのコレクション。 |
| PivotFieldColumns| 整数の配列  | 列領域に表示されるフィールドのインデックスのコレクション。 |
| PivotFieldData   | 整数の配列  | データ領域に表示されるフィールドのインデックスのコレクション。 |

**ShapeOperateParameter**

| パラメータ名 | 型     | 説明 |
| ------------ | ------ | ----------- |
| Shape        | オブジェクト | 図形の定義（種類、配置、サイズ、テキストなど）。 |

**WorkbookSettingsOperateParameter**

| パラメータ名     | 型     | 説明 |
| ---------------- | ------ | ----------- |
| WorkbookSettings | オブジェクト | ワークブック全体に影響する設定（例：計算モード、精度）。 |

**WorksheetOperateParameter**

| パラメータ名   | 型     | 説明 |
| -------------- | ------ | ----------- |
| Name           | 文字列 | 操作対象のワークシートの現在の名前。 |
| SheetType      | 文字列 | シートの種類（`Worksheet`, `Chart` など）。 |
| NewName        | 文字列 | ワークシートを名前変更する際の新しい名前。 |
| MovingRequest  | オブジェクト | ワークシートを移動するためのパラメータ（例：`FromIndex`, `ToIndex`）。 |

## REST API

| API                | 型   | 説明 | リソースリンク |
| ------------------ | ---- | ----------- | ------------- |
| /cells/task/runtask| POST | タスクの実行    | [PostRunTask](https://apireference.aspose.cloud/cells/#/Task/PostRunTask) |

[OpenAPI 仕様書](https://apireference.aspose.cloud/cells/#/Workbook/PostImportData) はパブリックにアクセス可能なプログラミングインターフェースを定義し、Web ブラウザから直接 REST によるやり取りを可能にします。

### 前提条件
- **認証** – 有効な `Authorization: Bearer <access_token>` ヘッダーを含めてください。  
- **ストレージ** – ソースワークブックは Aspose Cloud ストレージに保存されているか、リクエスト本文で Base64 エンコードされた内容として提供されている必要があります。  
- **API バージョン** – 本ドキュメントは Aspose.Cells Cloud API の **v3.0** を対象としています。

### サンプルリクエスト（cURL）

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/task/runtask" \
     -H "Authorization: Bearer {access_token}" \
     -H "Content-Type: application/json" \
     -d '{
           "OperateObject": {
               "OperateObjectType": "Chart",
               "OperateObjectPosition": {
                   "Workbook": { "FileName": "Sample.xlsx" },
                   "SheetName": "Sheet1"
               }
           },
           "ChartOperateParameter": {
               "ChartType": "Bar",
               "UpperLeftRow": 5,
               "UpperLeftColumn": 2,
               "LowerRightRow": 15,
               "LowerRightColumn": 8,
               "Area": "A1:B5",
               "Title": "Sales Chart",
               "IsVertical": "true"
           }
         }'
```

リクエスト本文は、以下で定義される **CellsObjectOperateRequest** スキーマに従います：

```json
{
  "$schema": "http://json-schema.org/draft-07/schema#",
  "title": "CellsObjectOperateRequest",
  "type": "object",
  "required": ["OperateObject"],
  "properties": {
    "OperateObject": {
      "type": "object",
      "required": ["OperateObjectType"],
      "properties": {
        "OperateObjectType": { "type": "string", "enum": ["Workbook","Worksheet","PageSetup","Cells","Chart","Shape","ListObject","PivotTable","WorkbookSettings","PageBreak"] },
        "OperateObjectPosition": { "$ref": "#/definitions/OperateObjectPosition" }
      }
    },
    "ChartOperateParameter": { "$ref": "#/definitions/ChartOperateParameter" },
    "ListObjectOperateParameter": { "$ref": "#/definitions/ListObjectOperateParameter" },
    "PageBreakOperateParameter": { "$ref": "#/definitions/PageBreakOperateParameter" },
    "PageSetupOperateParameter": { "$ref": "#/definitions/PageSetupOperateParameter" },
    "PivotTableOperateParameter": { "$ref": "#/definitions/PivotTableOperateParameter" },
    "ShapeOperateParameter": { "$ref": "#/definitions/ShapeOperateParameter" },
    "WorkbookSettingsOperateParameter": { "$ref": "#/definitions/WorkbookSettingsOperateParameter" },
    "WorksheetOperateParameter": { "$ref": "#/definitions/WorksheetOperateParameter" }
  },
  "definitions": {
    "OperateObjectPosition": {
      "type": "object",
      "properties": {
        "Workbook": { "type": "object" },
        "SheetName": { "type": "string" },
        "ChartIndex": { "type": "integer" },
        "ShapeIndex": { "type": "integer" },
        "CellName": { "type": "string" },
        "ListObjectIndex": { "type": "integer" }
      }
    },
    "ChartOperateParameter": {
      "type": "object",
      "properties": {
        "ChartIndex": { "type": "integer" },
        "ChartType": { "type": "string" },
        "UpperLeftRow": { "type": "integer" },
        "UpperLeftColumn": { "type": "integer" },
        "LowerRightRow": { "type": "integer" },
        "LowerRightColumn": { "type": "integer" },
        "Area": { "type": "string" },
        "IsVertical": { "type": "string", "enum": ["true","false"] },
        "CategoryData": { "type": "string" },
        "IsAutoGetSerialName": { "type": "string", "enum": ["true","false"] },
        "Title": { "type": "string" }
      }
    }
    /* 便宜上、他の定義は省略しています */
  }
}
```

### サンプルレスポンス（成功 – 200）

```json
{
  "Code": 200,
  "Status": "OK",
  "TaskId": "d9f2c4a1-5b6e-4a9c-8f2a-7e3b9c0e5f1a",
  "Result": {
    "ChartId": 0,
    "Message": "Chart created successfully."
  }
}
```

レスポンスには以下のフィールドが含まれます：

| フィールド       | 型     | 説明 |
| --------------- | ------ | ----------- |
| Code            | 整数   | タスクエンジンが返す HTTP 的なステータスコード。 |
| Status          | 文字列 | 人間が読める形式のステータス（例：`OK`）。 |
| TaskId          | 文字列 | 非同期タスクの識別子。 |
| Result          | オブジェクト | 操作固有の結果を保持するオブジェクト。 |
| Result.ChartId  | 整数   | 作成または変更されたチャートの識別子。 |
| Result.Message  | 文字列 | 結果を説明する短いメッセージ。 |

### エラーハンドリング

| HTTP ステータス | エラーコード | 説明 | 修正方法 |
| --------------- | ------------ | ----------- | ---------------- |
| 400             | InvalidParameter | 1 つ以上のリクエストパラメータが不足または不正な形式です。 | 必須フィールドとデータ型を確認してください。 |
| 401             | Unauthorized   | 無効または不足している認証トークンです。 | アクセストークンを再取得し、`Authorization` ヘッダーに含めてください。 |
| 404             | NotFound       | 指定されたワークブック、ワークシート、またはオブジェクトが存在しません。 | `FileName`, `SheetName`, オブジェクトインデックスを確認してください。 |
| 500             | ServerError    | サーバー上で予期せぬエラーが発生しました。 | リクエストを再試行してください。問題が続く場合はサポートへお問い合わせください。 |

### 共通ユースケース
- ワークシートに新しいチャートを追加する。  
- ワークシートの名前を変更する（`OperateObjectType = "Worksheet"` と `WorksheetOperateParameter.NewName` を使用）。  
- ページ区切りを挿入する（`OperateObjectType = "PageBreak"` と `PageBreakOperateParameter` を使用）。  
- ピボットテーブルのソースデータを更新する（`OperateObjectType = "PivotTable"` と `PivotTableOperateParameter.SourceData` を使用）。  
- 計算モードなどのワークブック設定を変更する（`OperateObjectType = "WorkbookSettings"` を使用）。  

---  

*すべての説明は、公式の Aspose.Cells Cloud OpenAPI 仕様書に基づいています。*