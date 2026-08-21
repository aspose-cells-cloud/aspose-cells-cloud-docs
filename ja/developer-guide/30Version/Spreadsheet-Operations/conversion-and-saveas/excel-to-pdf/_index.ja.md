---
title: "Excel を PDF に変換 – Aspose.Cells Cloud API"
ArticleTitle: "Excel を PDF に変換 – Aspose.Cells Cloud API"
second_title: "ドキュメント"
linktype: "docs"
url: /ja/convert-excel-file-to-pdf-file/
aliases: [  /ja/convert-excel-file-to-pdf-in-cloud/ , /ja/convert/excel-to-pdf/ ]
keywords: "Aspose, Cells, Excel, PDF, 変換, Cloud API"
description: "Aspose.Cells Cloud REST API を使用して Excel ワークブックを PDF に変換する方法を学びます。cURL、SDK サンプル（C#、Java、Python）および認証ガイドを含みます。"
weight: 80
---

この REST API は、スプレッドシート ファイルを PDF 形式のファイルに変換します。**前提条件:** 有効な JWT アクセス トークンを取得し、ソースの Excel ファイルがサポートされているストレージに保存されていること、および変換エンドポイントを呼び出すための適切な権限を持っていることを確認してください。

## PostConvertWorkbookToPDF API

```http
POST https://api.aspose.cloud/v3.0/cells/convert/pdf
```

### **セキュリティと認証**

Aspose.Cells Cloud API は安全であり、<a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT トークンベースの認証</a>を必要とします。

### **クエリ パラメーター**

| パラメーター名          | タイプ   | 説明                                                                 |
| :-------------------- | :----- | :------------------------------------------------------------------- |
| password              | string | Excel ファイルを開くためのパスワード。                                          |
| storageName           | string | ファイルが配置されているストレージの名前。                                      |
| checkExcelRestriction | bool   | セル関連オブジェクトを変更する際に、Excel ファイルの制限を適用するかどうか。           |

`checkExcelRestriction` は省略された場合、既定値は `false` です。

### **リクエスト ボディ パラメーター**

| パラメーター名 | タイプ | 説明                                     |
| :------------- | :--- | :--------------------------------------- |
| datafile       | file | マルチパート コンテンツの最初の部分として保存されるデータ ファイル。 |

### **レスポンス**

[FileInfo](/cells/file-info/)

レスポンスは、ファイル メタデータを含む JSON オブジェクトを返します。PDF ファイル自体は、提供された `FileContent`（base64 エンコード文字列）または `FileInfo` リンクを使用してダウンロードできます。API は **FileInfo** タイプの JSON オブジェクトを返します：

- **FileInfo** – 生成された **PDF** ファイルの名前、サイズ、および base64 エンコードされた内容を含むオブジェクト。

```json
{
  "Filename": "example.pdf",
  "FileSize": 12345,
  "FileContent": "base64_encoded_string"
}
```

**HTTP ステータス コード**

| コード | 意味                         | 説明                                               |
|------|-----------------------------|----------------------------------------------------|
| 200  | OK                          | フィルターが正常に適用され、レスポンスに操作の詳細が含まれます。 |
| 400  | Bad Request                 | パラメーターが不足または無効（例：サポートされていないファイル形式）。 |
| 401  | Unauthorized                | JWT トークンが無効または不足しています。                   |
| 413  | Payload Too Large           | アップロードされたファイルがサイズ制限を超えています。            |
| 500  | Internal Server Error       | 予期しないサーバー エラーが発生しました。                   |

## SDK を使用した PostConvertWorkbookToPDF API の利用方法

### PostConvertWorkbookToPDF API スペック

[OpenAPI スペック](https://reference.aspose.cloud/cells/#/Conversion/PostConvertWorkbookToPDF) は、パブリックにアクセス可能なプログラミング インターフェースを定義し、Web ブラウザーから直接 REST 通信を実行できるようにします。

**リクエスト ヘッダー**

| ヘッダー        | タイプ   | 説明                                          |
| :------------ | :----- | :-------------------------------------------- |
| Authorization | string | JWT 認証で取得したベアラー トークン。            |
| Content-Type  | string | ファイル アップロードの場合は `multipart/form-data` 必須。 |
| Accept        | string | レスポンス メタデータを受信する場合は `application/json`。 |

**cURL** コマンドライン ツールを使用して、Aspose.Cells Web サービスに簡単にアクセスできます。`Authorization` ヘッダーにアクセストークンを含め、以下のリクエストを実行してください。

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/convert/pdf" \
     -H "accept: multipart/form-data" \
     -H "Content-Type: multipart/form-data" \
     -H "Authorization: Bearer <access_token>" \
     -F "datafile=@sample.xlsx"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Filename": "xxxxxx.pdf",
  "FileSize": xxxx,
  "FileContent": "File Content: base64_encoded_string"
}
```

{{< /tab >}}

{{< /tabs >}}


### Aspose.Cells Cloud SDK の使用

SDK を使用すると、低レベルの詳細を処理することで開発を簡素化できます。Aspose.Cells Cloud SDK の完全な一覧については、[GitHub リポジトリ](https://github.com/aspose-cells-cloud)をご確認ください。

以下のコード例は、さまざまな SDK を使用して Aspose.Cells Web サービスを呼び出す方法を示しています：
{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example_PostConvertWorkbookToPDF.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostConvertWorkbookToPDF.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostConvertWorkbookToPDF.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostConvertWorkbookToPDF.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostConvertWorkbookToPDF.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostConvertWorkbookToPDF.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostConvertWorkbookToPDF.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostConvertWorkbookToPDF.go" >}}

{{< /tab >}}

{{< /tabs >}}

## この機能を実装するその他の API

| **API**        | **タイプ** | **説明**                                                    | **Swagger リンク**                                                                          |
| :------------- | :------- | :---------------------------------------------------------- | :------------------------------------------------------------------------------------------ |
| /cells/convert | PUT      | リクエスト本文のワークブックを指定された形式に変換します。              | [PutConvertWorkBook](https://apireference.aspose.cloud/cells/#/Workbook/PutConvertWorkBook) |

[POST /cells/{name}/saveAs](https://apireference.aspose.cloud/cells/#/SaveAs/PostDocumentSaveAs) API を使用すると、追加設定で MS Excel ファイルを PDF として保存し、結果をストレージに格納できます。

この REST API は、Excel ファイルを PDF に変換します。

[PUT /cells/convert](https://apireference.aspose.cloud/cells/#/Workbook/PutConvertWorkBook) API を使用すると、追加設定で MS Excel ファイルを PDF に変換し、結果をレスポンスとして返すことができます。

[GET /cells/{name}](https://apireference.aspose.cloud/cells/#/Workbook/GetWorkBook) API を使用すると、追加設定で MS Excel ファイルを PDF に変換し、結果をレスポンスとして返すことができます。

これらの [PutConvertWorkBook](https://apireference.aspose.cloud/cells/#/Workbook/PutConvertWorkBook)、[GetWorkBook](https://apireference.aspose.cloud/cells/#/Workbook/GetWorkBook)、および [PostDocumentSaveAs](https://apireference.aspose.cloud/cells/#/SaveAs/PostDocumentSaveAs) API は、パブリックにアクセス可能なプログラミング インターフェースを定義し、Web ブラウザーから直接 REST 通信を実行できるようにします。

その他の変換オプションについては、[保存オプション](/cells/save-options/) ページをご覧ください。
---