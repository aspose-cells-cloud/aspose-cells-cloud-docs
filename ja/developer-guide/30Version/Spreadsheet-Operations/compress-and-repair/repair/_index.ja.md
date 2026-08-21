---
title: "Excel ファイルの修復"
second_title: "ドキュメント"
type: docs
linktitle: "Excel ファイルの修復"
url: /ja/repair-excel-files/
keywords: "Aspose Cells, Excel 修復 API, 修復された XLSX, スプレッドシート復旧, クラウド API"
description: "Aspose.Cells Cloud REST API を使用して破損した Excel ファイル (XLS、XLSX、XLSM、XLSB、ODS) を修復します。1 つまたは複数のファイルをアップロードし、出力形式を選択して、修復されたファイルを Base64 形式で受け取ります。インストールは不要です。"
weight: 39
---

この REST API を使用すると、Excel ファイルを**修復**できます。

- XLS、XLSX、XLSM、XLSB、ODS およびその他のスプレッドシート形式を修復します。  
- 単一のリクエストで複数のファイルをアップロードできます。

Aspose.Cells Cloud Excel 修復機能は、インストール不要で、オンラインで破損した Excel ファイルからデータを復旧します。破損した Excel ファイルは開けないため問題となります。Aspose.Cells Cloud Excel 修復アプリを使用して、これらのファイルからデータを復旧できます。

## REST API

**Excel ファイルの修復**エンドポイントは、破損したスプレッドシートファイルを修復し、修復された内容を返します。


```bash
POST https://api.aspose.cloud/v3.0/cells/repair
```

### **セキュリティと認証**

Aspose.Cells Cloud API は安全であり、<a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT トークンベースの認証</a>が必要です。

### リクエストパラメータ

| パラメータ名 | 型     | 位置                           | 説明                     |
|--------------|--------|--------------------------------|---------------------------|
| file         | file   | formData (multipart)           | アップロードするファイル   |
| format       | string | query                          | 期望する出力形式。省略された場合（null）、出力形式は入力ファイルと同じ形式がデフォルトになります。 |

### **レスポンス**

```json
{
    "Status" : "OK",
    "Code" : 200,
    "Filename" : "[結合されたファイル名]",
    "Filesize" : [ファイルサイズ],
    "FileContent" : "[Base64文字列]"
}
```

**HTTP ステータスコード**

| コード | 意味                     | 説明                                             |
|--------|--------------------------|--------------------------------------------------|
| 200    | OK                       | フィルターが正常に適用されました。レスポンスには操作の詳細が含まれます。 |
| 400    | Bad Request              | パラメータが不足または無効です（例：サポートされていないファイル形式）。 |
| 401    | Unauthorized             | JWT トークンが無効または不足しています。             |
| 413    | Payload Too Large        | アップロードされたファイルがサイズ制限を超えています。 |
| 500    | Internal Server Error    | 予期しないサーバーエラーが発生しました。             |

## SDK を使用した PostRepair API の使用方法

### PostRepair API 仕様

[OpenAPI 仕様](https://reference.aspose.cloud/cells/#/LightCells/PostRepair) は、パブリックにアクセス可能なプログラミングインターフェースを定義し、ウェブブラウザから直接 REST アクセスを実行できるようにします。

cURL コマンドラインツールを使用して、Aspose.Cells ウェブサービスに簡単にアクセスできます。以下の例では、cURL を使用してクラウド API に呼び出しを行う方法を示しています。

{{< tabs tabTotal="2" tabID="11" tabName11="リクエスト" tabName12="レスポンス" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/repair" \
  -X POST \
  -H "Content-Type: multipart/form-data" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>" \
  -F 'file1=@file1.xlsx' \
  -F 'file2=@file2.xlsx'
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Files": [
    {
      "Filename": "file1.xlsx",
      "FileSize": 274022,
      "FileContent": "-----Base64文字列--------"
    },
    {
      "Filename": "file2.xlsx",
      "FileSize": 274022,
      "FileContent": "-----Base64文字列--------"
    }
  ]
}
```

{{< /tab >}}

{{< /tabs >}}

正常終了時は、HTTP 200 が返され、JSON ペイロード内に `Files` 配列が含まれます。エラー発生時は、API は標準の HTTP ステータスコードを使用します：

- **400 Bad Request** – 無効なパラメータ、または復旧不可能なファイル。  
- **401 Unauthorized** – JWT トークンが不足または無効。  
- **413 Payload Too Large** – アップロードされたファイルが許可されたサイズを超えています。  
- **500 Internal Server Error** – 予期しないサーバーサイドのエラー。

## クラウド SDK ファミリー

SDK を使用することは、開発を高速化する最良の方法です。SDK は低レベルの詳細を処理し、プロジェクトのタスクに集中できるようにします。Aspose.Cells Cloud SDK の完全な一覧については、[GitHub リポジトリ](https://github.com/aspose-cells-cloud)をご確認ください。

以下のコード例は、さまざまな SDK を使用して Aspose.Cells ウェブサービスを呼び出す方法を示しています。

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostRepair.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostRepair.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostRepair.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostRepair.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostRepair.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostRepair.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostRepair.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostRepair.go" >}}

{{< /tab >}}

{{< /tabs >}}