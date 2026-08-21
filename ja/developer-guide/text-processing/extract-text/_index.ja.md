---
title: "Aspose.Cells Cloud Web API – テキスト抽出"
second_title: "Aspose.Cells Cloud – オンラインショートコード"
linktitle: "テキスト抽出"
type: docs
url: /ja/extract-text/
keywords: "Aspose.Cells Cloud, テキスト抽出, Excel API, セルテキスト抽出, REST API"
description: "Aspose.Cells Cloud API を使用して Excel セルから部分文字列、数値、文字を抽出します。before/after テキスト、位置ベースの抽出、および新規範囲への直接出力をサポートします。"
weight: 100
ArticleTitle: "Aspose.Cells Cloud テキスト抽出 API ドキュメント"
---

スプレッドシートのセルから部分文字列、文字、数値を別のセルへ抽出し、複雑な FIND、 MIN、 LEFT、 RIGHT 数式の使用を不要にします。

## **ExtractText API**

```http
PUT https://api.aspose.cloud/v4.0/cells/content/extract/text
```

### **セキュリティと認証**

Aspose.Cells Cloud API はセキュアであり、<a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT トークンベースの認証</a>を必要とします。

```bash
-H "Authorization: Bearer {access_token}"
```

### **ExtractText API のリクエストパラメータ**

| パラメータ名       | 型      | 位置               | 説明                                                                                                                             |
| ------------------ | ------- | ------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| Spreadsheet        | File    | FormData           | スプレッドシートファイルをアップロードします。                                                                                                                                                   |
| extractTextType    | String  | Query              | 抽出モードを示す列挙型。許可される値: `Before`, `After`, `BeforePosition`, `AfterPosition`。                                                                                                     |
| beforeText         | String  | Query              | 抽出する部分文字列の**前**に出現する必要のあるテキスト。`extractTextType=Before` の場合に使用されます。                                                                                           |
| afterText          | String  | Query              | 抽出する部分文字列の**後**に出現する必要のあるテキスト。`extractTextType=After` の場合に使用されます。                                                                                             |
| beforePosition     | Integer | Query              | セルの左端から返す文字数。`extractTextType=BeforePosition` の場合に使用されます。                                                                                                                 |
| afterPosition      | Integer | Query              | セルの右端から返す文字数。`extractTextType=AfterPosition` の場合に使用されます。                                                                                                                  |
| outPositionRange   | String  | Query              | 抽出されたテキストを書き込むターゲット範囲（例: `Sheet1!A1`）。                                                                                                                                   |
| worksheet          | String  | Query              | ソースセルを含むワークシートの名前。                                                                                                                                                             |
| range              | String  | Query              | ソースセルまたは範囲（例: `A1`）。                                                                                                                                                               |
| outPath            | String  | Query （オプション） | 結果のワークブックを保存するストレージ内のフォルダパス。指定されない場合、結果はレスポンス本体に返されます。                                                                                     |
| outStorageName     | String  | Query              | 出力ファイルに使用するストレージ名。                                                                                                                                                             |
| region             | String  | Query              | スプレッドシートの地域設定（例: `US`, `EU`）。                                                                                                                                                   |
| password           | String  | Query              | 保護されたワークブックを開くためのパスワード。                                                                                                                                                   |

**cURL リクエストのサンプル**

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/content/extract/text?extractTextType=Before&beforeText=Total&outPositionRange=Sheet1!B1&worksheet=Sheet1&range=A1" \
     -H "Authorization: Bearer {access_token}" \
     -F "Spreadsheet=@Sample.xlsx"
```

### **レスポンス**

リクエストが成功した場合、API は抽出されたテキストと書き込まれたセルのアドレスを含む JSON ペイロードを返します。

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

`outPath` パラメータが指定された場合、レスポンスにはステータスメッセージのみが含まれ、ワークブックは指定された場所に書き込まれます。

**`outPath` を省略した場合のレスポンスサンプル**

```json
{
  "Code": 200,
  "Status": "OK"
}
```

### エラーコード

- **200 OK** – 抽出が正常に完了しました。  
- **202 Accepted** – リクエストは非同期処理のために受け付けられました。  
- **400 Bad Request** – 無効な Aspose.Cells Cloud API URI、または必須パラメータが不足しています。  
- **401 Unauthorized** – 無効なアクセストークン、クライアント ID、またはクライアントシークレットです。  
- **404 Not Found** – 指定されたスプレッドシートファイルにアクセスできません。  
- **500 Server Error** – ワークブックの処理中に予期しないエラーが発生しました。

## OpenAPI 仕様

[OpenAPI 仕様](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/TextProcessing/ExtractText) はパブリックにアクセス可能なプログラミングインターフェースを定義し、Web ブラウザから直接 REST のやり取りを実行できるようにします。

### Aspose.Cells Cloud SDK の使用

SDK を使用することが開発を最速で進める最良の方法です。SDK が内部の詳細を処理するため、最小限のコードでセルの**テキスト抽出**を実装できます。Aspose.Cells Cloud SDK の完全なリストは [GitHub リポジトリ](https://github.com/aspose-cells-cloud) をご確認ください。

以下のコード例は、さまざまな SDK を使用して Aspose.Cells Web サービスを呼び出す方法を示しています。

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{<tab tabNum="1" >}}

```csharp
// C# の例 – テキスト抽出（簡潔さのためにコードは省略）
```

{{</tab>}}

{{<tab tabNum="2" >}}

```java
// Java の例 – テキスト抽出（簡潔さのためにコードは省略）
```

{{</tab>}}

{{<tab tabNum="3" >}}

```php
// PHP の例 – テキスト抽出（簡潔さのためにコードは省略）
```

{{</tab>}}

{{<tab tabNum="4" >}}

```ruby
# Ruby の例 – テキスト抽出（簡潔さのためにコードは省略）
```

{{</tab>}}

{{<tab tabNum="5" >}}

```javascript
// Node.js の例 – テキスト抽出（簡潔さのためにコードは省略）
```

{{</tab>}}

{{<tab tabNum="6" >}}

```python
# Python の例 – テキスト抽出（簡潔さのためにコードは省略）
```

{{</tab>}}

{{<tab tabNum="7" >}}

```perl
# Perl の例 – テキスト抽出（簡潔さのためにコードは省略）
```

{{</tab>}}

{{<tab tabNum="8" >}}

```go
// Go の例 – テキスト抽出（簡潔さのためにコードは省略）
```

{{</tab>}}

{{< /tabs >}}