---
title: "Aspose.Cells Cloud データインポート API – Excel スプレッドシートに CSV、JSON、XML データを自動的にインポートするためのクラウドソリューション"
second_title: "ドキュメント"
ArticleTitle: "マルチソースデータ統合 Excel プラットフォーム – Aspose.Cells Cloud 自動化データインポート・変換 API"
linktitle: "スプレッドシートへのデータインポート"
type: docs
url: /import-data-into-spreadsheet/
keywords: "Aspose Cells, データインポート API, CSV to Excel, JSON to Excel, XML to Excel, クラウドスプレッドシート, REST API"
description: "Aspose.Cells Cloud REST API を使用して、CSV、JSON、または XML データを Excel スプレッドシートにインポートします。リクエスト形式、パラメータ、サンプル SDK コード、エラー処理について学習します。"
weight: 100
---

## 主な機能

### 多様なフォーマットのデータ対応

- **<a href="https://docs.fileformat.com/spreadsheet/csv/" rel="noopener noreferrer">CSV</a> データインポート**: さまざまな区切り文字をサポートし、エンコーディングを自動的に検出します。
- **<a href="https://docs.fileformat.com/web/json/" rel="noopener noreferrer">JSON</a> データ処理**: 複雑な JSON 構造を Excel テーブルに平坦化します。
- **<a href="https://docs.fileformat.com/web/xml/" rel="noopener noreferrer">XML</a> ファイル変換**: ノードデータを Excel の行・列構造にマッピングします。

## **スプレッドシートへのデータインポート API 説明**

### Web API

```http
PUT https://api.aspose.cloud/v4.0/cells/import/data
```

### **セキュリティと認証**

Aspose.Cells Cloud API は安全であり、<a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT トークンベースの認証</a>を要求します。

### リクエストパラメータ

| パラメータ名       | 型     | 位置         | 説明                                                                 |
| ------------------ | ------ | ------------ | ------------------------------------------------------------------- |
| datafile           | File   | FormData     | インポートするデータファイル（CSV、JSON、または XML）。              |
| spreadsheet        | File   | FormData     | インポートされたデータを受け取る宛先ワークブック。                   |
| worksheet          | string | Query        | データを配置するワークシート名。                                     |
| startCell          | string | Query        | インポート開始位置を示す左上セル（例: `A1`）。                        |
| insert             | bool   | Query        | 行を挿入する場合は `true`、既存データを上書きする場合は `false`。     |
| convertNumericData | bool   | Query        | インポート時に数値文字列を数値に変換する場合は `true`。              |
| splitter           | string | Query        | CSV 区切り文字（1 文字のみ、既定値は `,`）。                           |
| outPath            | string | Query（省略可） | 更新されたワークブックを保存するフォルダーパス。                      |
| outStorageName     | string | Query（省略可） | 出力ファイルの保存先ストレージ名。                                    |
| fontsLocation      | string | Query（省略可） | 必要に応じてカスタムフォントフォルダーのパス。                        |
| region             | string | Query（省略可） | スプレッドシートの地域設定（例: `ja-JP`）。                           |
| password           | string | Query（省略可） | 保護されたワークブックを開くためのパスワード。                        |

### レスポンス

```json
[
  {
    "Name": "ResponseFile",
    "DataType": {
      "Identifier": "File",
      "Reference": "Stream"
    }
  }
]
```

**HTTP ステータスコード**

| コード | 意味                 | 説明                                                       |
| ------ | -------------------- | ---------------------------------------------------------- |
| 200    | OK                   | フィルターが正常に適用されました；レスポンスには操作詳細が含まれます。 |
| 400    | Bad Request          | パラメータが不足または無効（例: 未対応のファイル形式）。      |
| 401    | Unauthorized         | JWT トークンが無効または不足しています。                     |
| 413    | Payload Too Large    | アップロードされたファイルがサイズ制限を超えています。       |
| 500    | Internal Server Error | 予期しないサーバーエラーが発生しました。                     |

## この API を使用すべき理由

- **効率的なデータ読み込み** – 中間ファイルを作成することなく、大規模なデータセットをワークブックに一括インポートできます。
- **幅広い SDK サポート** – .NET、Java、PHP、Ruby、Node.js、Python、Go、Perl 向けのクライアントライブラリを提供し、統合を簡素化します。
- **メモリ内処理** – 時間領域内で変換を実行し、一時ストレージの必要性を低減します。

## SDK を使用したスプレッドシートへのデータインポート API の使用方法

**注意事項／制限事項**: この API は 1 回のインポートあたり最大 1,000,000 行をサポートします。既定の CSV 区切り文字はコンマのみですが、`splitter` パラメータで他の 1 文字区切り文字を指定できます。大規模な XML ファイルは処理時間を増加させる可能性があります。

データエクスポートやワークブック形式変換などの関連操作については、「**Export Data**（データエクスポート）」および「**Convert Workbook**（ワークブック変換）」のドキュメントをご参照ください。

### スプレッドシートへのデータインポート API 仕様

<a href="https://reference.aspose.cloud/cells/#/DataProcessingController/ImportDataIntoSpreadsheet" rel="noopener noreferrer">スプレッドシートへのデータインポート API 仕様</a> はパブリックにアクセス可能なプログラミングインタフェースを提供し、Web ブラウザから直接 REST API を呼び出すことができます。
cURL コマンドラインツールを使用すると、Aspose.Cells ウェブサービスを簡単に利用できます。以下の例は、cURL を使用してクラウド API を呼び出す方法を示しています。

{{< tabs tabTotal="2" tabID="11" tabName11="リクエスト" tabName12="レスポンス" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/import/data?worksheet=Sheet1&startCell=A1&insert=true" \
  -H "Authorization: Bearer {access_token}" \
  -F "datafile=@/path/to/data.csv" \
  -F "spreadsheet=@/path/to/workbook.xlsx"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```
{
  "type": "FileContentResult",
  "fileContents": "byte[] (Base64 エンコード)",
  "contentType": "MIME タイプ",
  "fileDownloadName": "任意のファイル名"
}
```

{{< /tab >}}

{{< /tabs >}}

### Aspose.Cells Cloud SDK の使用

SDK を使用すると、低レベルの詳細を抽象化できるため、開発が最も迅速になります。短いコードでスプレッドシートのワークシートにデータをインポートできます。Aspose.Cells Cloud SDK の完全な一覧については、<a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub リポジトリ</a>をご確認ください。