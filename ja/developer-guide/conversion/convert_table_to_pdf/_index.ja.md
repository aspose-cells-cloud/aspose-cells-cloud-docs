---
title: "テーブルを PDF に変換"
ArticleTitle: "テーブルを PDF に変換 – Aspose.Cells Cloud API"
second_title: "ドキュメント"
linktitle: "テーブルを PDF に変換"
type: docs
url: /ja/cells/convert/table/pdf
aliases: []
keywords: "テーブル PDF 変換, Aspose.Cells, API"
description: "ローカルドライブ上のスプレッドシートのテーブルを Aspose.Cells Cloud を使用して PDF ファイルに変換します。"
weight: 1000
---

## Aspose.Cells Cloud Web サービスのテーブルを PDF に変換機能

この操作は、ローカルファイルシステムからスプレッドシートファイルを読み取り、指定されたテーブルを PDF ドキュメントに変換し、変換結果を返します。この処理はクラウドサーバー上で完全に実行されるため、クラウドストレージへの中間アップロードは不要です。この API は、出力場所、カスタムフォント、行/列の自動調整、地域設定、パスワードで保護されたワークブックに関するオプションパラメータをサポートしています。

### Web API エンドポイント

```http
PUT https://api.aspose.cloud/v4.0/cells/convert/table/pdf
```

### **セキュリティと認証**

Aspose.Cells Cloud API は安全であり、<a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT トークンベースの認証</a>を必要とします。

### リクエストパラメータ

| パラメータ名     | タイプ   | パス / クエリ文字列 / HTTP ボディ | 説明                                                                                                                                                     |
|------------------|----------|-----------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Spreadsheet      | ファイル | FormData                          | スプレッドシートファイルをアップロードします。                                                                                                           |
| worksheet        | 文字列   | クエリ                            | スプレッドシートのワークシート名。                                                                                                                       |
| tableName        | 文字列   | クエリ                            | テーブル名。                                                                                                                                              |
| outPath          | 文字列   | クエリ                            | (オプション) ワークブックが保存されるフォルダのパス。デフォルトは null です。                                                                           |
| outStorageName   | 文字列   | クエリ                            | 出力ファイルのストレージ名。                                                                                                                              |
| fontsLocation    | 文字列   | クエリ                            | カスタムフォントを使用します。                                                                                                                            |
| AutoRowsFit      | 真偽値   | クエリ                            | (オプション) ワークシート内のすべての行を自動調整します。                                                                                               |
| AutoColumnsFit   | 真偽値   | クエリ                            | (オプション) ワークシート内のすべての列を自動調整します。                                                                                               |
| region           | 文字列   | クエリ                            | スプレッドシートの地域/言語設定 (例: `en-US`, `fr-FR`)。数値の書式設定、日付の解析、ロケール固有の動作に影響を与えます。                                  |
| password         | 文字列   | クエリ                            | スプレッドシートファイルを開くためのパスワード。                                                                                                         |

### リクエストボディパラメータ

| パラメータ名 | タイプ | 説明 |
|--------------|--------|------|
| *なし*       | *なし* | *JSON ボディは不要です。ファイルは multipart/form-data 経由で送信されます。* |

### **レスポンス**

```json
{
  "file": "<バイナリ PDF コンテンツ>"
}
```

**レスポンスステータスコード**

| コード | 意味             | 説明 |
|--------|------------------|------|
| 200    | OK               | テーブルが正常に PDF に変換されました。レスポンスボディには PDF ファイルストリームが含まれます。 |
| 400    | Bad Request      | 無効なリクエストパラメータ、または不正な形式の URL です。 |
| 401    | Unauthorized     | 認証に失敗したか、資格情報が提供されていません。 |
| 404    | Not Found        | ソースファイルにアクセスできない、またはワークシート/テーブルが見つかりません。 |
| 413    | Payload Too Large| アップロードされたスプレッドシートが許可されたサイズ制限を超えています。 |
| 500    | Internal Server Error | スプレッドシートを PDF に変換中にエラーが発生しました。 |

## SDK を使用したテーブルを PDF に変換の使用方法

### テーブルを PDF に変換の仕様

[テーブルを PDF に変換 API 仕様](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Conversion/ConvertTableToPdf) は、パブリックにアクセス可能なプログラミングインターフェースを定義し、Web ブラウザから直接 REST のやり取りを実行できるようにします。

cURL コマンドラインツールを使用して Aspose.Cells Cloud Web サービスに簡単にアクセスできます。以下の例は、cURL を使用してクラウド API に呼び出しを行う方法を示しています。

{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}

{< tab tabNum="1" >}

```bash
# セキュアな接続に HTTPS を使用
curl -v "https://api.aspose.cloud/v4.0/cells/convert/table/pdf?worksheet={worksheet}&tableName={tableName}&outPath={outPath}&outStorageName={outStorageName}&fontsLocation={fontsLocation}&AutoRowsFit={AutoRowsFit}&AutoColumnsFit={AutoColumnsFit}&region={region}&password={password}" \
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
  "file": "<バイナリ PDF コンテンツ>"
}
```

{< /tab >}

{< /tabs >}

### Aspose Cells Cloud SDK の使用

SDK を使用すると、開発を最も迅速に加速できます。SDK は低レベルの詳細を抽象化し、プロジェクトのタスクに集中できるようにします。Aspose.Cells Cloud SDK の完全な一覧については、<a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub リポジトリ</a>をご確認ください。

以下のコード例は、さまざまな SDK を使用して Aspose.Cells Cloud Web サービスを呼び出す方法を示しています。

```csharp
// C# 用 SDK サンプルコード
var apiInstance = new ConversionApi();
var file = File.ReadAllBytes("sample.xlsx");
var response = apiInstance.ConvertTableToPdf(
    file,
    worksheet: "Sheet1",
    tableName: "Table1",
    outPath: null,
    outStorageName: null,
    fontsLocation: null,
    AutoRowsFit: null,
    AutoColumnsFit: null,
    region: null,
    password: null);
File.WriteAllBytes("output.pdf", response);
```

```java
// Java 用 SDK サンプルコード
ConversionApi apiInstance = new ConversionApi();
byte[] file = Files.readAllBytes(Paths.get("sample.xlsx"));
byte[] result = apiInstance.convertTableToPdf(
    file,
    "Sheet1",
    "Table1",
    null,
    null,
    null,
    null,
    null,
    null,
    null);
Files.write(Paths.get("output.pdf"), result);
```

```python
# Python 用 SDK サンプルコード
api_instance = conversion_api.ConversionApi()
with open("sample.xlsx", "rb") as f:
    file_bytes = f.read()
pdf_bytes = api_instance.convert_table_to_pdf(
    file=file_bytes,
    worksheet="Sheet1",
    table_name="Table1")
with open("output.pdf", "wb") as out_file:
    out_file.write(pdf_bytes)
```

`[TBD]`
---