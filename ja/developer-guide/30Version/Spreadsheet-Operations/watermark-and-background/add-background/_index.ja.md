---
title: "ワークブックに背景画像を追加する"
second_title: "Document"
linktitle: "追加"
type: docs
url: /add-background-in-excel-file/
aliases:
  - /add-background-in-workbook/
  - /workbook/add-background/
  - /workbook/background/add/
keywords: "Aspose.Cells, 背景画像の追加, Excel API, REST, クラウドSDK, cURL, ワークブック背景"
description: "Aspose.Cells Cloud REST API を使用して Excel ワークブックに背景画像を追加する方法を学びます。必要なパラメーター、認証詳細、完全な cURL の例、およびエラー処理情報が含まれます。"
weight: 160
---

## REST API

この REST API は、Excel ワークブックに**背景画像**を追加します。

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/background
```

### **セキュリティと認証**

Aspose.Cells Cloud API は安全であり、<a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT トークンベースの認証</a>が必要です。


### クエリパラメーター

| パラメーター名 | 型     | 説明                                        |
| -------------- | ------ | --------------------------------------------- |
| `picPath`      | 文字列 | 背景として使用する画像ファイルへのパス。       |
| `folder`       | 文字列 | 元のワークブックが格納されているフォルダー。   |
| `storageName`  | 文字列 | ファイルが存在するストレージの名前。           |

### リクエストボディパラメーター

| パラメーター名 | 型   | 説明                                                |
| -------------- | ---- | ----------------------------------------------------- |
| `datafile`     | ファイル | 背景を適用するワークブックファイル。                   |

**パスパラメーター** – URL 内の `{name}` は**ワークブックファイル名**（例：`Book1.xlsx`）を表します。


### **レスポンス**

```json
{
    "Status" : "OK",
    "Code" : 200
}
```

**HTTP ステータスコード**

| コード | 意味                         | 説明                                             |
|------|-----------------------------|--------------------------------------------------|
| 200  | OK                          | フィルターが正常に適用された。レスポンスには操作の詳細が含まれる。 |
| 400  | Bad Request                 | パラメーターが不足または無効（例：サポートされていないファイル形式）。 |
| 401  | Unauthorized                | JWT トークンが無効または不足している。 |
| 413  | Payload Too Large           | アップロードされたファイルがサイズ制限を超過している。 |
| 500  | Internal Server Error       | 予期しないサーバーエラーが発生した。 |
## SDK を使用した PutWorkbookBackground API の利用方法

### PutWorkbookBackground API の仕様

[OpenAPI 仕様](https://apireference.aspose.cloud/cells/#/Workbook/PutWorkbookBackground) は、Web ブラウザーから直接 REST アクセスを実行できる公開可能なプログラミングインターフェースを定義しています。

**cURL** コマンドラインツールを使用すると、Aspose.Cells Web サービスに簡単にアクセスできます。以下の例では、マルチパートファイルアップロードフラグと必要な認証ヘッダーを含む完全なリクエストを示しています。

{{< tabs tabTotal="2" tabID="1" tabName1="リクエスト" tabName2="レスポンス" >}}

{{< tab tabNum="1" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/background?picPath=DotnetFiles%2FWaterMark.png&folder=DotnetFiles" \
     -H "Authorization: Bearer <access_token>" \
     -H "accept: multipart/form-data" \
     -H "Content-Type: multipart/form-data" \
     -F "datafile=@/path/to/Book1.xlsx"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}


### Aspose.Cells Cloud SDK の使用

SDK を使用すると、開発を最速で行えます。SDK は低レベルの詳細を抽象化し、ビジネスロジックに集中できます。Aspose.Cells Cloud SDK の完全なリストについては、[GitHub リポジトリー](https://github.com/aspose-cells-cloud) を参照してください。

以下のコード例は、さまざまな SDK を使用して Aspose.Cells Web サービスを呼び出す方法を示しています。

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePutWorkbookBackground.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PutWorkbookBackground.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PutWorkbookBackground.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PutWorkbookBackground.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PutWorkbookBackground.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PutWorkbookBackground.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PutWorkbookBackground.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PutWorkbookBackground.go" >}}

{{< /tab >}}

{{< /tabs >}}

---