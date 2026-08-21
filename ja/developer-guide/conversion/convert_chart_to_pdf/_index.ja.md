---
title: "チャートをPDFに変換"
ArticleTitle: "チャートをPDFに変換 – Aspose.Cells Cloud API"
second_title: "ドキュメント"
linktitle: "ConvertChartToPdf"
type: docs
url: /ja/cells/convert/chart/pdf
aliases: []
keywords: "ConvertChartToPdf, Aspose.Cells, PDF, チャート変換"
description: "ローカルドライブ上のスプレッドシートのチャートをPDFに変換します。"
weight: 100
---

## Aspose.Cells Cloud Web サービスによるチャートをPDFに変換

このメソッドは、ローカルファイルのアップロードを通じて提供されたスプレッドシートファイルからチャートを読み取り、PDF形式に変換して変換結果を返します。この処理はクラウドサーバー上で完全に実行されるため、中間ストレージは不要です。ソースファイルのパスとターゲット形式が正しく、ソースファイルを読み込むための適切な権限が必要です。ファイルが見つからない、アクセスに問題がある、または変換に失敗した場合などのエラーは、適切なHTTPエラー応答として返されます。

### Web API エンドポイント

```http
PUT https://api.aspose.cloud/v4.0/cells/convert/chart/pdf
```

### **セキュリティと認証**

Aspose.Cells Cloud API は安全であり、<a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT トークンベースの認証</a>が必要です。

### リクエストパラメータ

| パラメータ名     | 型     | パス/クエリ文字列/HTTP ボディ | 説明 |
|------------------|--------|-----------------------------|-------------|
| Spreadsheet      | ファイル | FormData                    | スプレッドシートファイルをアップロードします。 |
| worksheet        | 文字列 | クエリ                      | スプレッドシートのワークシート名。 |
| chartIndex       | 整数  | クエリ                      | ワークシート内のチャートのインデックス。 |
| outPath          | 文字列 | クエリ                      | (任意) ワークブックが保存されるフォルダのパス。デフォルトは null です。 |
| outStorageName   | 文字列 | クエリ                      | 出力ファイルのストレージ名。 |
| fontsLocation    | 文字列 | クエリ                      | カスタムフォントを使用します。 |
| region           | 文字列 | クエリ                      | スプレッドシートの地域/言語設定（例: `en-US`, `fr-FR`）。数値の書式設定、日付の解析、地域固有の動作に影響します。 |
| password         | 文字列 | クエリ                      | スプレッドシートファイルを開くためのパスワード。 |

### リクエストボディパラメータ

| パラメータ名 | 型     | 説明 |
| ------------ | ---- | ----------- |
| Spreadsheet  | ファイル | スプレッドシートファイルをアップロードします。 |

### **応答**

```json
{
  "ResponseFile": "バイナリ PDF ファイルストリーム"
}
```

**応答ステータスコード**

| コード | 意味 | 説明 |
|------|------|-------------|
| 200 | OK | チャートが正常にPDFに変換され、バイナリPDFファイルが返されました。 |
| 400 | Bad Request | 無効なリクエストパラメータ、または不正な形式のURLです。 |
| 401 | Unauthorized | 認証に失敗したか、認証情報が提供されていません。 |
| 404 | Not Found | ソースファイルにアクセスできません。 |
| 413 | Payload Too Large | アップロードされたファイルが許可されたサイズ制限を超えています。 |
| 500 | Internal Server Error | 変換処理中にエラーが発生しました。 |

## SDK を使用したチャートをPDFに変換する方法

### チャートをPDFに変換する仕様

[Convert Chart to PDF API 仕様](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Conversion/ConvertChartToPdf) は、パブリックにアクセス可能なプログラミングインターフェースを定義し、Web ブラウザから直接 REST アクセスを実行できるようにします。

cURL コマンドラインツールを使用すると、Aspose.Cells Web サービスに簡単にアクセスできます。以下の例は、cURL を使用してクラウド API にリクエストを送信する方法を示しています。

{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}
{< tab tabNum="1" >}
```bash
# セキュアな接続には HTTPS を使用します
curl -v "https://api.aspose.cloud/v4.0/cells/convert/chart/pdf?worksheet={worksheet}&chartIndex={chartIndex}&outPath={outPath}&outStorageName={outStorageName}&fontsLocation={fontsLocation}&region={region}&password={password}" \
  -X PUT \
  -H "Content-Type: multipart/form-data" \
  -H "Accept: application/pdf" \
  -H "Authorization: Bearer <jwt token>" \
  -F "Spreadsheet=@sample.xlsx"
```
{< /tab >}
{< tab tabNum="2" >}
```json
{
  "ResponseFile": "バイナリ PDF ファイルストリーム"
}
```
{< /tab >}
{< /tabs >}

### Aspose Cells Cloud SDK の使用

SDK を使用すると、開発を最も迅速に加速できます。SDK は低レベルの詳細を抽象化し、プロジェクトのタスクに集中できるようにします。Aspose.Cells Cloud SDK の完全なリストについては、<a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub リポジトリ</a>をご確認ください。

以下のコード例は、さまざまな SDK を使用して Aspose Cells Cloud Web サービスを呼び出す方法を示しています：
`[TBD]`
---