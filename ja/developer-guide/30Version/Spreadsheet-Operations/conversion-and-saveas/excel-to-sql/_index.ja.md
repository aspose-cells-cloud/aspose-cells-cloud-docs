---
title: "ExcelからSQLへ"
second_title: "ドキュメント"
linktitle: "ExcelからSQLへ"
type: docs
url: /ja/convert-excel-file-to-sql-file/
keywords: "Aspose.Cells, Excel to SQL, クラウドAPI, スプレッドシート変換, REST"
description: "Aspose.Cells Cloud REST APIを使用して、ExcelスプレッドシートをSQLファイルに変換します。複数のSDKおよびプログラミング言語をサポートし、アプリケーションへのシームレスな統合を実現します。"
weight: 100
ArticleTitle: "ExcelをSQLに変換 – Aspose.Cells Cloud API"
---

このREST APIは、スプレッドシートファイルをSQL形式のファイルに変換します。

**前提条件**  
このエンドポイントを使用するには、<a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWTトークンベース認証</a>ガイドに従って有効なJWTトークンを生成しておく必要があります。このAPIは、サービスのドキュメントで定義されたサイズ制限内のExcelファイルをサポートし、`password` クエリパラメータを指定することでパスワードで保護されたワークブックの処理も可能です。

## PostConvertWorkbookToSQL API

```http
POST https://api.aspose.cloud/v3.0/cells/convert/sql
```

### **セキュリティと認証**

Aspose.Cells Cloud APIは安全であり、<a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWTトークンベース認証</a>を要求します。

### **クエリパラメータ**

| パラメータ名          | 型     | 説明                                                                 |
| --------------------- | ------ | ------------------------------------------------------------------- |
| password              | 文字列 | Excelファイルを開くために必要なパスワード。                           |
| storageName           | 文字列 | ファイルが保存されているストレージの名前。                             |
| checkExcelRestriction | 真偽値 | セル関連オブジェクトを変更する際にExcelファイルの制限をチェックするかどうかを示します。 |

### **リクエストボディパラメータ**

| パラメータ名 | 型        | 説明                                                       |
| ------------ | --------- | --------------------------------------------------------- |
| datafile     | データファイル | 変換対象のスプレッドシートファイル。リクエストの最初のパートとして含めます。 |

### レスポンス

APIは、生成されたSQLファイルを含む **FileInfo** オブジェクトを返します。

| フィールド        | 型     | 説明                                     |
| --------------- | ------ | --------------------------------------- |
| **Filename**    | 文字列 | SQLファイル名（例: `example.sql`）。     |
| **FileSize**    | 整数   | ファイルサイズ（バイト単位）。            |
| **FileContent** | 文字列 | SQLファイルのBase64エンコードされた内容。 |

[FileInfo](/cells/file-info/)

**HTTPステータスコード**

| コード | 意味            | 説明                                                 |
|------|----------------|----------------------------------------------------|
| 200  | OK             | フィルターが正常に適用された；レスポンスには操作の詳細が含まれる。 |
| 400  | Bad Request    | パラメータが不足または無効（例：サポートされていないファイル形式）。 |
| 401  | Unauthorized   | JWTトークンが無効または不足している。                      |
| 413  | Payload Too Large | アップロードされたファイルがサイズ制限を超えている。         |
| 500  | Internal Server Error | 予期せぬサーバーエラーが発生しました。                  |

## SDKを使用してPostConvertWorkbookToSQL APIを利用する方法

### PostConvertWorkbookToSQL API仕様

<a href="https://reference.aspose.cloud/cells/#/Conversion/PostConvertWorkbookToSQL" rel="noopener noreferrer">OpenAPI仕様</a>は、パブリックに利用可能なプログラミングインターフェースを定義し、ウェブブラウザから直接REST通信を実行できるようにします。

**cURL** コマンドラインツールを使用して、Aspose.Cellsウェブサービスに簡単にアクセスできます。以下の例は、cURLでCloud APIにアクセスする方法を示しています。

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/convert/sql" \
     -H "accept: multipart/form-data" \
     -H "Content-Type: multipart/form-data" \
     -H "x-aspose-client: curl" \
     -d '{"File":{}}'
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Filename": "example.sql",
  "FileSize": 1024,
  "FileContent": "base64_encoded_string"
}
```

{{< /tab >}}

{{< /tabs >}}

### Aspose.Cells Cloud SDKの利用

SDKを使用すると、開発スピードを大幅に向上させることができます。SDKが低レベルの詳細を処理するため、プロジェクトのタスクに集中できます。Aspose.Cells Cloud SDKの完全なリストについては、<a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHubリポジトリ</a>をご確認ください。

以下のコード例は、さまざまなSDKを使用してAspose.Cellsウェブサービスを呼び出す方法を示しています。
{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example_PostConvertWorkbookToSQL.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostConvertWorkbookToSQL.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostConvertWorkbookToSQL.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostConvertWorkbookToSQL.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostConvertWorkbookToSQL.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostConvertWorkbookToSQL.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostConvertWorkbookToSQL.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostConvertWorkbookToSQL.go" >}}

{{< /tab >}}

{{< /tabs >}}

## この機能を実装するその他のAPI

- **[POST /cells/{name}/saveAs](https://apireference.aspose.cloud/cells/#/SaveAs/PostDocumentSaveAs)** – ワークブックを別の形式で保存し、結果を指定されたストレージに格納します。

- **[PUT /cells/convert](https://apireference.aspose.cloud/cells/#/Workbook/PutConvertWorkBook)** – オプションの設定とともにワークブックを別の形式に変換し、結果をレスポンスとして返します。

- **[GET /cells/{name}](https://apireference.aspose.cloud/cells/#/Workbook/GetWorkBook)** – オプションの変換設定とともにワークブックを取得します。

**注意事項**  
- パスワードで保護されたExcelファイルを変換する際は、`password` クエリパラメータを必ず指定してください。指定しない場合、400エラーで変換が失敗します。  
- サービスはSQLファイルの内容をBase64形式で返します。`.sql` ファイルとして保存する前に、これをデコードしてください。  

**サンプルファイル**  
APIを迅速にテストするために、サンプルExcelワークブックを<a href="https://example.com/sample.xlsx">こちら</a>からダウンロードし、事前生成されたSQL結果を<a href="https://example.com/sample.sql">こちら</a>からダウンロードしてください。
---