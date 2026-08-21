---
title: "Aspose.Cells Cloud – スプレッドシートの統合・分割・データのインポート"
second_title: "ドキュメント"
ArticleTitle: "スプレッドシートデータ処理 – 統合・分割・インポート"
linktitle: "データ処理"
type: docs
url: /data-processing/
keywords: "Aspose.Cells Cloud, スプレッドシートデータ処理, Excel 統合, Excel 分割, CSV インポート, JSON インポート, API"
description: "Aspose.Cells Cloud REST API を使用した CSV/JSON データのインポート、リモート Excel ワークブックの統合、大規模なスプレッドシートの分割に関する詳細ガイド。リクエスト／レスポンスの例も含みます。"
weight: 30
---

**Aspose.Cells Cloud** は、クラウド上で Excel ファイルをプログラムで操作可能にする RESTful サービスです。複数のフォーマットからのデータインポート、ワークブックの統合、大規模スプレッドシートの分割をサポートしています。

Aspose.Cells Cloud API の **データ処理** セクションでは、スプレッドシートデータをプログラムでインポート・統合・分割できます。以下のエンドポイントを使用して、CSV/JSON のインポート処理、ワークブックの統合、または大規模ファイルを管理しやすいサイズに分割できます。

## データのインポートと管理

- **[Excel ファイルへ CSV、JSON、XML データをインポートする](https://docs.aspose.cloud/cells/import-data-into-spreadsheet/)**  

インポート操作は CSV、JSON、または XML のペイロードを受け取り、ターゲットワークブック内に新しいワークシートを作成（または既存のワークシートを更新）します。

**エンドポイント詳細**

| HTTP メソッド | エンドポイント | リクエストボディ | 成功時のレスポンス |
|-------------|----------|--------------|------------------|
| POST | `https://api.aspose.cloud/v3.0/cells/{fileName}/import` | `application/json` または `text/csv`（フォーマットによる） | `200 OK` と更新されたワークブックのメタデータを含む JSON |
| GET | `https://api.aspose.cloud/v3.0/cells/{fileName}?format=excel` | *なし* | 処理済みのワークブックファイルを返却 |

**cURL リクエストのサンプル（CSV インポート）**

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/MyWorkbook.xlsx/import" \
     -H "Authorization: Bearer {access_token}" \
     -H "Content-Type: text/csv" \
     --data-binary @data.csv
```

**JSON レスポンスのサンプル**

```json
{
  "Code": 200,
  "Status": "OK",
  "Workbook": {
    "FileName": "MyWorkbook.xlsx",
    "Worksheets": 3
  }
}
```

> **前提条件**：OAuth2 アクセストークンが必要です。ソースファイルは Aspose Cloud ストレージ内に配置されているか、multipart アップロードで提供されている必要があります。

## ファイルの統合操作

- **[リモートの Excel ファイルを指定されたワークブックに統合する](https://docs.aspose.cloud/cells/merge-remote-spreadsheet/)**
- **[複数の Excel ファイルを1つのワークブックに統合する](https://docs.aspose.cloud/cells/merge-spreadsheets/)**
- **[リモートフォルダ内の条件に一致する Excel ファイルを統合する](https://docs.aspose.cloud/cells/merge-spreadsheets-in-remote-folder/)**  

統合操作では、2つ以上のワークブックを1つのターゲットワークブックに統合します。API は明示的なファイルリストの指定と、ストレージフォルダ内のパターンベースでの統合をサポートしています。

**エンドポイント詳細**

| HTTP メソッド | エンドポイント | パラメータ | 成功時のレスポンス |
|-------------|----------|------------|------------------|
| POST | `https://api.aspose.cloud/v3.0/cells/merge` | `files`（ファイル名の配列）、`target`（オプション：ターゲットワークブック名） | `200 OK` と統合されたワークブックの詳細を含む JSON |
| POST | `https://api.aspose.cloud/v3.0/cells/merge/remote` | `sourceFolder`、`pattern`、`target` | `200 OK` と統合されたワークブックのメタデータ |

**cURL リクエストのサンプル（明示的なリストを統合）**

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/merge" \
     -H "Authorization: Bearer {access_token}" \
     -H "Content-Type: application/json" \
     -d '{
           "files": ["Book1.xlsx", "Book2.xlsx"],
           "target": "Combined.xlsx"
         }'
```

**JSON レスポンスのサンプル**

```json
{
  "Code": 200,
  "Status": "OK",
  "MergedWorkbook": {
    "FileName": "Combined.xlsx",
    "Worksheets": 10
  }
}
```

> **前提条件**：すべてのソースワークブックは同じクラウドストレージの場所に保存されている必要があり、呼び出し側には読み取り／書き込み権限が必要です。

## ファイルの分割操作

- **[ワークシート単位で Excel ファイルを複数のファイルに分割する](https://docs.aspose.cloud/cells/split-remote-spreadsheet/)**
- **[カスタムルールに従って Excel ファイルを分割する](https://docs.aspose.cloud/cells/split-spreadsheet/)**  

分割操作では、個別のワークシートまたは行／列のグループを別々のワークブックファイルとして抽出します。

**エンドポイント詳細**

| HTTP メソッド | エンドポイント | パラメータ | 成功時のレスポンス |
|-------------|----------|------------|------------------|
| POST | `https://api.aspose.cloud/v3.0/cells/{fileName}/split` | `splitBy`（例：`worksheet`）、`outputFolder` | `200 OK` と生成されたファイル URL のリスト |
| POST | `https://api.aspose.cloud/v3.0/cells/{fileName}/split/custom` | カスタムルールの JSON（ページサイズ、行範囲など） | `200 OK` と分割されたファイルの詳細 |

**cURL リクエストのサンプル（ワークシート単位で分割）**

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/BigReport.xlsx/split" \
     -H "Authorization: Bearer {access_token}" \
     -H "Content-Type: application/json" \
     -d '{
           "splitBy": "worksheet",
           "outputFolder": "Splits/"
         }'
```

**JSON レスポンスのサンプル**

```json
{
  "Code": 200,
  "Status": "OK",
  "Splits": [
    {"FileName": "BigReport_Sheet1.xlsx", "Url": "https://storage.aspose.cloud/..."},
    {"FileName": "BigReport_Sheet2.xlsx", "Url": "https://storage.aspose.cloud/..."}
  ]
}
```

> **前提条件**：ソースワークブックは Aspose Cloud ストレージからアクセス可能である必要があり、呼び出し側は出力先フォルダに対する書き込み権限が必要です。