---
title: "Excel ファイルの保護"
second_title: "Document"
linktitle: "Excel ファイルの暗号化"
type: docs
url: /ja/protect-excel-files/
aliases:
  [
    "/protect/without-storage/",
    "/protect/without-using-storage/",
    "/protect/without-using-storage/",
  ]
keywords: "Aspose.Cells, Excel 保護 API, Excel ワークブックの暗号化, クラウドスプレッドシートのセキュリティ, REST API"
description: "Aspose.Cells Cloud REST API を使用して Excel ファイルを保護します。このガイドでは、2026 年現在、HTTP POST、cURL、および複数のプログラミング言語向け SDK を介してワークブックを暗号化する方法を示します。"
weight: 40
---

この REST API は Excel ファイルを保護します。

## REST API

```bash
POST http://api.aspose.cloud/v3.0/cells/protect
```

### セキュリティと認証

Aspose.Cells Cloud API は安全であり、[JWT トークンベースの認証](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/)が必要です。

### リクエストパラメータ

| パラメータ名 | 型     | 位置                 | 説明                           |
|------------|--------|----------------------|--------------------------------|
| file       | file   | formData (body)      | アップロードするファイル         |
| password   | string | クエリ文字列 (`password`) | ワークブックを保護するために使用するパスワード |

### レスポンス

```json
{
  "Status": "OK",
  "Code": 200,
  "Files": [
    {
      "Filename": "protected filename: smaple1.xlsx",
      "FileSize": size,
      "FileContent": "-----sample1 の Base64 文字列-----"
    },
    {
      "Filename": "protected filename: sample2.xlsx",
      "FileSize": size,
      "FileContent": "-----sample2 の Base64 文字列-----"
    }
  ]
}
```

**HTTP ステータスコード**

| コード | 意味                         | 説明                                             |
|-------|-----------------------------|--------------------------------------------------|
| 200   | OK                          | フィルターが正常に適用されました；レスポンスには操作の詳細が含まれます。 |
| 400   | Bad Request                 | パラメータが不足または無効です（例：サポートされていないファイル形式）。 |
| 401   | Unauthorized                | JWT トークンが無効または不足しています。 |
| 413   | Payload Too Large           | アップロードされたファイルがサイズ制限を超えています。 |
| 500   | Internal Server Error       | 予期しないサーバーエラーが発生しました。 |

## SDK を使用して PostProtect API を利用する方法

### PostProtect API 仕様

[OpenAPI 仕様](https://apireference.aspose.cloud/cells/#/LightCells/PostProtect) はパブリックにアクセス可能なプログラミングインターフェースを定義し、ウェブブラウザから直接 REST アクセスを実行できるようにします。

cURL コマンドラインツールを使用して Aspose.Cells ウェブサービスに簡単にアクセスできます。以下の例は、cURL を使用してクラウド API を呼び出す方法を示しています。

{{< tabs tabTotal="2" tabID="1" tabName1="リクエスト" tabName2="レスポンス" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "http://api.aspose.cloud/v3.0/cells/protect?password=MySecretPwd" \
  -X POST \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>" \
  -F 'file1=@sample1.xlsx' \
  -F 'file2=@sample2.xlsx'
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Files": [
    {
      "Filename": "sample1.xlsx",
      "FileSize": 274022,
      "FileContent": "-----sample1 の Base64 文字列-----"
    },
    {
      "Filename": "sample2.xlsx",
      "FileSize": 274022,
      "FileContent": "-----sample2 の Base64 文字列-----"
    }
  ]
}
```

{{< /tab >}}

{{< /tabs >}}

### **エラーハンドリング**

– API は以下のステータスコードを返すことがあります：

| HTTP コード | 意味                                     | 例：JSON エラーペイロード                          |
|------------|-----------------------------------------|---------------------------------------------------|
| 400        | Bad request（例：ファイルが不足）        | `{"Code":400,"Message":"File is required."}`        |
| 401        | Unauthorized（無効または不足するトークン） | `{"Code":401,"Message":"Invalid access token."}`    |
| 403        | Forbidden（権限が不十分）                | `{"Code":403,"Message":"Access denied."}`           |
| 500        | Internal server error                   | `{"Code":500,"Message":"Unexpected server error."}` |

### Aspose.Cells Cloud SDK を使用する

SDK を使用すると、開発が最も迅速になります。SDK が低レベルの詳細を処理するため、プロジェクトのタスクに集中できます。Aspose.Cells Cloud SDK の完全な一覧については、[GitHub リポジトリ](https://github.com/aspose-cells-cloud) をご確認ください。

以下のコード例は、さまざまな SDK を使用して Aspose.Cells ウェブサービスを呼び出す方法を示しています：

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostProtect.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostProtect.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostProtect.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostProtect.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostProtect.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostProtect.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostProtect.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostProtect.go" >}}

{{< /tab >}}

{{< /tabs >}}