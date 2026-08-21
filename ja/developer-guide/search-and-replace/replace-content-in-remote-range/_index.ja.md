---
title: "Aspose.Cells Cloud 置換 Web API – リモートスプレッドシートの範囲内のテキストを更新"
secondtitle: "ドキュメント"
articletitle: "クラウド Excel ファイルでの範囲内テキストの一括置換 – 検索 & 置換 API"
linktitle: "リモート範囲のコンテンツを置換"
type: docs
url: /replace-content-in-remote-range/
keywords: "リモート Excel 範囲のテキスト置換, Aspose.Cells Cloud API, Excel の検索と置換, クラウドスプレッドシート編集, リモート Excel ファイルの更新"
description: "Aspose.Cells Cloud を使用して、リモート Excel ファイルの特定範囲内にあるテキストを検索・置換します。認証、エラーハンドリング、多言語 SDK をサポートします。"
weight: 100
---

クラウド上に保存されたリモート Excel ファイルに対して、一括テキスト置換を実行します。Aspose.Cells の検索・置換 API を使用して、指定した範囲内の特定のテキスト文字列を効率的に検索・更新します。

## **リモート範囲のコンテンツ置換 API**

### Web API

```
PUT https://api.aspose.cloud/v4.0/cells/{name}/worksheets/{worksheet}/ranges/{cellArea}/replace/content
```

### **セキュリティと認証**

Aspose.Cells Cloud API は安全であり、<a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT トークンベースの認証</a>が必要です。

```bash
-H "Authorization: Bearer {access_token}"
```

### **リクエストパラメータ**

| パラメータ名     | 型     | パス / クエリ文字列 / HTTP ボディ | 説明                                                                                                                                                 |
| :------------- | :----- | :-------------------------- | :---------------------------------------------------------------------------------------------------------------------------------------------------------- |
| name           | 文字列 | パス                        | クラウドストレージに保存されている、変更対象のワークブックファイル名（例: `"report.xlsx"`）。                                                               |
| searchText     | 文字列 | クエリ                      | 指定されたワークシートおよびセル範囲内で検索するテキスト文字列。完全一致検索をサポートします。                                                   |
| replaceText    | 文字列 | クエリ                      | 指定された範囲内で `searchText` に一致するすべての箇所を置換するテキスト文字列。                                                           |
| worksheet      | 文字列 | パス                        | 検索と置換操作を実行するワークシート名。                                                                           |
| cellArea       | 文字列 | パス                        | テキスト検索と置換を実行する特定のセル範囲（例: `"A1:D20"`）。                                                                |
| folder         | 文字列 | クエリ                      | ソースワークブックが配置されているクラウドストレージのフォルダーパス。                                                                                         |
| storageName    | 文字列 | クエリ                      | _（オプション）_ ワークブックが存在するクラウドストレージの名前。省略した場合、デフォルトのクラウドストレージが使用されます。                                       |
| region         | 文字列 | クエリ                      | _（オプション）_ テキスト処理用のロケールを設定します。これにより、検索操作における大文字・小文字の区別や文字エンコーディングに影響を与える可能性があります（例: `"en-US"`, `"tr-TR"`）。 |
| password       | 文字列 | クエリ                      | _（オプション）_ ワークブックがパスワードで保護されている場合、ファイルのオープンおよび編集に必要なパスワードを指定します。                                                       |

### **レスポンス**

```json
{
  "Name": "CellsCloudResponse",
  "Type": "Class",
  "Properties": [
    {
      "Name": "Code",
      "DataType": {
        "Identifier": "Integer"
      }
    },
    {
      "Name": "Status",
      "DataType": {
        "Identifier": "String"
      }
    }
  ]
}
```

正常な呼び出しは、以下の具体的な JSON ペイロードを返します。

```json
{
  "Code": 200,
  "Status": "OK"
}
```


### エラーコード

| コード | メッセージ      | 発生条件                                          |
| ---- | ------------ | ------------------------------------------------------- |
| 400  | Bad Request  | リクエスト URI またはパラメータが不正な形式です。            |
| 401  | Unauthorized | 認証トークンが欠落している、または無効です。                |
| 404  | Not Found    | 指定されたワークブックが見つからない、またはアクセスできません。     |
| 500  | Server Error | ワークブック処理中に内部サーバーエラーが発生しました。 |

## どこで「リモートスプレッドシートの範囲コンテンツ置換 API」を使用すべきか？

- **バッチクラウドファイル更新**: AWS S3 や Azure Blob などのクラウドストレージに保存された複数の Excel ファイルの内容を一括で変更します。
- **クラウドテンプレートの動的データ埋め込み**: クラウドに保存されたレポートテンプレートに対して、動的データを一括で埋め込みます。
- **クロスリージョンファイル同期**: 異なる地理的リージョン間でクラウドストレージ内の Excel ファイルの内容の一貫性を同期します。

## なぜ「リモートスプレッドシートの範囲コンテンツ置換 API」を使用すべきか？

- **開発者フレンドリー**: Aspose.Cells Cloud は多言語向け SDK ライブラリを提供しており、迅速な開発と包括的なドキュメントが可能です。独自ソリューションを構築する場合と比較して、開発作業を大幅に削減できます。
- **人件費の削減**: 文書統合処理を担当する専任の役職を削減できます。
- **従量課金制**: 初期投資は不要で、実際に使用した API 呼び出しのみに課金されます。
- **メンテナンスコストゼロ**: サーバーの保守、ソフトウェアの更新、互換性問題への対応が不要です。
- **複雑な Excel 書式を PDF 形式で維持**: PDF 形式で出力することで、複雑な Excel 書式を維持しながら、汎用的にアクセス可能な形式を提供します。

## SDK を使用して「リモートスプレッドシートの範囲コンテンツ置換 API」を実行する方法

### OpenAPI 仕様

[OpenAPI 仕様](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Search/ReplaceContentInRemoteRange) は、パブリックにアクセス可能なプログラミングインターフェースを定義し、Web ブラウザから直接 REST アクセスを実行できるようにします。

### Aspose.Cells Cloud SDK の使用

SDK を使用するのが開発を加速する最良の方法です。SDK は内部処理を自動で処理するため、最小限のコードでセルスプレッドシートの内容置換を実装できます。Aspose.Cells Cloud SDK の完全な一覧は [GitHub リポジトリ](https://github.com/aspose-cells-cloud) をご参照ください。

以下のコード例は、さまざまな SDK を使用して Aspose.Cells Web サービスを呼び出す方法を示しています。

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}

```csharp
```

{{</tab>}}
{{<tab tabNum="2" >}}

```java
```

{{</tab>}}
{{<tab tabNum="3" >}}

```php
```

{{</tab>}}
{{<tab tabNum="4" >}}

```ruby
```

{{</tab>}}
{{<tab tabNum="5" >}}

```javascript
```

{{</tab>}}
{{<tab tabNum="6" >}}

```python
```

{{</tab>}}
{{<tab tabNum="7" >}}

```perl
```

{{</tab>}}
{{<tab tabNum="8" >}}

```go
```

{{</tab>}}
{{< /tabs >}}