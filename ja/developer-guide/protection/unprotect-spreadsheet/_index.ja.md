---
title: "Aspose.Cells Cloud Excel 解除保護 Web API – 開封用および変更用パスワードをプログラムで削除"
second_title: "ドキュメント"
ArticleTitle: "Excel パスワード保護を解除 – 開封用および変更用パスワードを即座に解除"
linktitle: "スプレッドシートの保護を解除"
type: docs
url: /unprotect-spreadsheet/
keywords: "保護解除, スプレッドシート, Aspose.Cells, API, Excel, パスワード削除"
description: "Aspose.Cells Cloud スプレッドシート保護解除 API を使用して、Excel ファイルの開封用および変更用パスワードをプログラムで削除します。.xlsx/.xls 形式、OAuth2 認証、バッチ処理をサポートします。"
weight: 100
---

スプレッドシート保護解除 API は、1 回の呼び出しで Excel ファイルの開封用および変更用パスワード保護を解除します。データパイプライン、ドキュメント管理システム、移行ワークフローに最適です。

## **スプレッドシート保護解除 API**

### **Web API**

```http
PUT https://api.aspose.cloud/v4.0/cells/unprotection/spreadsheet
```

### **セキュリティと認証**

Aspose.Cells Cloud API は安全であり、<a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT トークンベース認証</a>が必要です。

```bash
-H "Authorization: Bearer {access_token}"
```

### **リクエストパラメータ**

| パラメータ名       | タイプ   | 位置       | 説明                                                                 |
| ------------------ | -------- | ---------- | -------------------------------------------------------------------- |
| Spreadsheet        | ファイル | FormData   | 保護を解除する Excel ファイル。                                       |
| password           | 文字列   | クエリ     | ファイルの開封を保護するパスワード。                                 |
| modifyPassword     | 文字列   | クエリ     | ファイルの変更に必要なパスワード（開封用パスワードのみ設定されている場合は省略可）。 |
| outPath            | 文字列   | クエリ     | （オプション）保護を解除したワークブックを保存するフォルダーパス。   |
| outStorageName     | 文字列   | クエリ     | （オプション）出力ファイルを書き込むストレージ名。                   |
| region             | 文字列   | クエリ     | （オプション）スプレッドシートの地域設定。                           |

### **レスポンス**

```json
[
  {
    "Name": "ResponseFile",
    "DataType": {
      "Identifier": "File",
      "Reference": "Stream",
      "Name": "file"
    }
  }
]
```

正常なレスポンスは、保護を解除したファイルをストリームとして返します。ファイルは `outPath` / `outStorageName` で指定された場所に保存するか、レスポンスペイロードから直接取得できます。

**HTTP ステータスコード**

| コード | 意味                 | 説明                                                         |
| ------ | -------------------- | ------------------------------------------------------------ |
| 200    | OK                   | フィルターが正常に適用された。レスポンスには操作の詳細が含まれる。 |
| 400    | Bad Request          | パラメータが不足または無効（例：サポートされていないファイル形式）。 |
| 401    | Unauthorized         | JWT トークンが無効または不足。                               |
| 413    | Payload Too Large    | アップロードされたファイルがサイズ制限を超えた。             |
| 500    | Internal Server Error | 予期しないサーバーエラー。                                   |

## スプレッドシート保護解除 API の使用タイミング

- **ロックされたワークブックへのアクセスを復元** – 手動での操作なしに、忘れた開封用または変更用パスワードを迅速に解除。
- **一括解除の自動化** – データ移行やアーカイブプロジェクトで多数のファイルを一括で処理。
- **既存ワークフローとの統合** – ストレージ API や変換 API と組み合わせてエンドツーエンドのパイプライン（例：アップロード → 保護解除 → PDF 変換）を構築。
- **データセキュリティの維持** – 処理はサーバーサイドで実行されるため、元のファイルは安全に保たれ、保護を解除したバージョンはクラウドストレージに保存されます。

## SDK を使用したスプレッドシート保護解除 API の利用方法

### **OpenAPI 仕様**

[スプレッドシート保護解除 API 仕様](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Protection/ProtectSpreadsheet) は、Web ブラウザから直接 REST 通信を実行するための公開可能なプログラミングインターフェースを提供します。

cURL コマンドラインツールを使用して、Aspose.Cells Web サービスに簡単にアクセスできます。以下の例は、cURL を使用してクラウド API を呼び出す方法を示しています。

{{< tabs tabTotal="2" tabID="11" tabName11="リクエスト" tabName12="レスポンス" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/unprotection/spreadsheet?password=OldPass&modifyPassword=ModPass" \
     -H "Authorization: Bearer {access_token}" \
     -F "Spreadsheet=@myfile.xlsx"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```
{
  "type": "FileContentResult",
  "fileContents": "byte[] (Base64 エンコード)",
  "contentType": "MIME タイプ",
  "fileDownloadName": "オプションのファイル名"
}
```

{{< /tab >}}

{{< /tabs >}}

### **Aspose.Cells Cloud SDK の使用**

SDK を使用すると、認証、リクエスト構築、レスポンス解析を自動的に処理するため、API 呼び出しが簡素化されます。SDK は多くの言語で利用可能であり、スプレッドシートの保護解除用にあらかじめ用意されたメソッドを備えています。

以下のコード例は、さまざまな SDK を使用してスプレッドシート保護解除 API を呼び出す方法を示しています。

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_UnprotectSpreadsheet.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_UnprotectSpreadsheet.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_UnprotectSpreadsheet.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_UnprotectSpreadsheet.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_UnprotectSpreadsheet.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_UnprotectSpreadsheet.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_UnprotectSpreadsheet.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_UnprotectSpreadsheet.go" >}}
{{</tab>}}
{{< /tabs >}}