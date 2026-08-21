---
title: "UnpivotRange"
ArticleTitle: "UnpivotRange – Aspose.Cells Cloud"
second_title: "ドキュメント"
linktype: "docs"
url: /cells/unpivot/range
aliases: []
keywords: "Aspose.Cells, UnpivotRange, API"
description: "スプレッドシート内で行と列を切り替えます。"
weight: 10
---

## Aspose.Cells Cloud Web サービスの UnpivotRange

スプレッドシート内で行と列を切り替えます。

### Web API エンドポイント

```http
PUT https://api.aspose.cloud/v4.0/cells/unpivot/range
```

### **セキュリティと認証**

Aspose.Cells Cloud API は安全であり、<a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT トークンベースの認証</a>が必要です。

### リクエストパラメータ

| パラメータ名     | 型     | パス/クエリ文字列/HTTP ボディ | 説明                                                                                                                                                     |
|------------------|--------|-----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Spreadsheet      | ファイル | FormData                    | スプレッドシートファイルをアップロードします。                                                                                                                                         |
| worksheet        | 文字列 | クエリ                       | シート名。                                                                                                                                              |
| cellArea         | 文字列 | クエリ                       | 指定されたデータ範囲。                                                                                                                                          |
| skipEmptyValue   | 真偽値 | クエリ                       | true の場合、空の値をスキップします。既定値: true。                                                                                                                      |
| outPath          | 文字列 | クエリ                       | （オプション）ワークブックが保存されるフォルダのパス。既定値は null です。                                                                                   |
| outStorageName   | 文字列 | クエリ                       | 出力ファイルのストレージ名。                                                                                                                                       |
| region           | 文字列 | クエリ                       | スプレッドシートの地域/言語設定（例: `en-US`、`fr-FR`）。数値書式、日付解析、地域固有の動作に影響を与えます。                        |
| password         | 文字列 | クエリ                       | スプレッドシートファイルを開くためのパスワード。                                                                                                                      |

### リクエストボディパラメータ

| パラメータ名 | 型 | 説明 |
|----------------|------|-------------|
| — | — | — |

### **応答**

```json
{
  "File": "バイナリストリーム"
}
```

**応答ステータスコード**

| コード | 意味 | 説明 |
|------|---------|-------------|
| 200 | OK | 列と行が逆転されたスプレッドシートファイルが返されます。 |
| 400 | Bad Request | 無効なリクエストパラメータ。 |
| 401 | Unauthorized | 認証に失敗しました。 |
| 413 | Payload Too Large | アップロードされたファイルがサイズ制限を超えています。 |
| 500 | Internal Server Error | サーバーが予期しない状況に遭遇しました。 |

## SDK を使用した UnpivotRange の利用方法

### UnpivotRange 仕様

[UnpivotRange API 仕様](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/{Transform}/{UnpivotRange}) は、パブリックにアクセス可能なプログラミングインターフェースを定義し、Web ブラウザから直接 REST アクセスを実行できます。

cURL コマンドラインツールを使用して Aspose.Cells Cloud Web サービスに簡単にアクセスできます。以下の例は、cURL を使用してクラウド API にリクエストを送信する方法を示しています。

{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}

{< tab tabNum="1" >}

```bash
# セキュアな接続には HTTPS を使用
curl -v "https://api.aspose.cloud/v4.0/cells/unpivot/range?worksheet=Sheet1&cellArea=A1:C10&skipEmptyValue=true&outPath=output%2Ffolder&outStorageName=MyStorage&region=en-US&password=yourPassword" -X PUT -H "Content-Type: multipart/form-data" -H "Accept: application/octet-stream" -H "Authorization: Bearer <jwt token>" -F 'Spreadsheet=@sample.xlsx'
```

{< /tab >}

{< tab tabNum="2" >}

```json
{
  "FileUrl": "https://example.com/output/unpivoted.xlsx"
}
```

{< /tab >}

{< /tabs >}

### Aspose Cells Cloud SDK の使用

SDK を使用すると、開発を最も迅速に加速できます。SDK は低レベルの詳細を抽象化し、プロジェクトのタスクに集中できるようにします。Aspose.Cells Cloud SDK の完全なリストについては、<a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub リポジトリ</a>をご確認ください。

以下のコード例は、さまざまな SDK を使用して Aspose Cells Cloud Web サービスを呼び出す方法を示しています：
 `[TBD]`
---