---
title: "ConvertRangeToPdf"
ArticleTitle: "範囲をPDFに変換 – Aspose.Cells Cloud API"
second_title: "Document"
linktype: "docs"
url: /cells/convert/range/pdf
aliases: []
keywords: "Aspose.Cells, 範囲をPDFに変換, API"
description: "Aspose.Cells Cloud を使ってスプレッドシートの指定された範囲を PDF に変換します。"
weight: 1
---

## Aspose.Cells Cloud Web サービスの ConvertRangeToPdf

ローカルドライブ上のスプレッドシートの特定範囲を PDF ファイルに変換します。

### Web API エンドポイント

```http
PUT https://api.aspose.cloud/v4.0/cells/convert/range/pdf
```

### **セキュリティと認証**

Aspose.Cells Cloud API は安全であり、<a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT トークンベースの認証</a>が必要です。

### リクエストパラメータ

| パラメータ名     | 型     | パス／クエリ文字列／HTTP リクエストボディ | 説明                                                                                                                                    |
|------------------|--------|-------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| Spreadsheet      | ファイル | FormData                                  | スプレッドシートファイルをアップロードします。                                                                                          |
| worksheet        | 文字列  | クエリ                                    | スプレッドシート内のワークシート名。                                                                                                    |
| range            | 文字列  | クエリ                                    | セル範囲（例: A1:C10）                                                                                                                  |
| outPath          | 文字列  | クエリ                                    | （オプション）ブックが保存されるフォルダーパス。既定値は null です。                                                                   |
| outStorageName   | 文字列  | クエリ                                    | 出力ファイルのストレージ名。                                                                                                            |
| fontsLocation    | 文字列  | クエリ                                    | カスタムフォントを使用します。                                                                                                          |
| AutoRowsFit      | 真偽値 | クエリ                                    | （オプション）ワークシート内のすべての行を自動調整します。                                                                              |
| AutoColumnsFit   | 真偽値 | クエリ                                    | （オプション）ワークシート内のすべての列を自動調整します。                                                                              |
| region           | 文字列  | クエリ                                    | スプレッドシートの地域／言語設定（例: `en-US`、`fr-FR`）。数値の書式設定、日付の解析、地域固有の動作に影響します。                         |
| password         | 文字列  | クエリ                                    | スプレッドシートファイルの開錠に使用するパスワード。                                                                                    |

### リクエストボディパラメータ

| パラメータ名 | 型     | 説明                     |
|--------------|--------|--------------------------|
| Spreadsheet  | ファイル | スプレッドシートファイルをアップロードします。 |

### **レスポンス**

```json
{
  "file": "<バイナリPDF内容>"
}
```

**レスポンスステータスコード**

| コード | 意味         | 説明                                     |
|--------|--------------|------------------------------------------|
| 200    | OK           | 変換成功。生成された PDF ファイルのストリームを返します。 |
| 400    | Bad Request  | 無効な URL。                             |
| 401    | Unauthorized | 認証に失敗したか、資格情報が提供されていません。 |
| 413    | Payload Too Large | アップロードされたファイルが許容サイズ上限を超えています。 |
| 500    | Internal Server Error | スプレッドシート内で変換データの取得中に異常が発生しました。 |

## SDK を使った ConvertRangeToPdf の使用方法

### ConvertRangeToPdf の仕様

[ConvertRangeToPdf API 仕様](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Conversion/ConvertRangeToPdf) は公開可能なプログラミングインターフェースを定義し、Web ブラウザから直接 REST 通信を実行できるようにします。

cURL コマンドラインツールを使用すると、Aspose Cells Cloud Web サービスへ簡単にアクセスできます。以下の例では、cURL を使って Cloud API へリクエストを送信する方法を示しています。

{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}

{< tab tabNum="1" >}

```bash
# セキュアな接続には HTTPS を使用
curl -v "https://api.aspose.cloud/v4.0/cells/convert/range/pdf?worksheet=Sheet1&range=A1:C10" \
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
  "file": "<バイナリPDF内容>"
}
```

{< /tab >}

{< /tabs >}

### Aspose Cells Cloud SDK の使用

SDK を使用すると、開発を最速で加速できます。SDK は低レベルの詳細を抽象化し、プロジェクトのタスクに集中できるようにします。Aspose.Cells Cloud SDK の完全な一覧については、<a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub リポジトリ</a>をご確認ください。

以下のコード例では、さまざまな SDK を使って Aspose Cells Cloud Web サービスを呼び出す方法を示しています：

```csharp
// C# 用 SDK サンプルコード
var apiInstance = new ConversionApi();
var file = File.OpenRead("sample.xlsx");
var result = apiInstance.ConvertRangeToPdf(file, "Sheet1", "A1:C10", outPath: null, outStorageName: null, fontsLocation: null, autoRowsFit: null, autoColumnsFit: null, region: null, password: null);
File.WriteAllBytes("output.pdf", result);
```

```java
// Java 用 SDK サンプルコード
ConversionApi api = new ConversionApi();
File file = new File("sample.xlsx");
byte[] result = api.convertRangeToPdf(file, "Sheet1", "A1:C10", null, null, null, null, null, null, null);
Files.write(Paths.get("output.pdf"), result);
```

```python
# Python 用 SDK サンプルコード
api_instance = conversion_api.ConversionApi()
with open("sample.xlsx", "rb") as f:
    result = api_instance.convert_range_to_pdf(f, worksheet="Sheet1", range="A1:C10")
    with open("output.pdf", "wb") as out_file:
        out_file.write(result)
```

```javascript
// JavaScript/Node.js 用 SDK サンプルコード
const fs = require('fs');
const { ConversionApi } = require('asposecellscloud');
const apiInstance = new ConversionApi();

let file = fs.createReadStream('sample.xlsx');
apiInstance.convertRangeToPdf(file, { worksheet: 'Sheet1', range: 'A1:C10' })
    .then((result) => {
        fs.writeFileSync('output.pdf', result);
    })
    .catch((error) => console.error(error));
```

`[TBD]`
---