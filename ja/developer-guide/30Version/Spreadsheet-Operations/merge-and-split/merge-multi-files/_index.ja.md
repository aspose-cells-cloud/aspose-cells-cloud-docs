---
title: "複数のExcelファイルを1つのワークブックに統合する"
second_title: "Document"
linktitle: "複数のExcelファイルを統合"
type: docs
url: /merge-multi-files-into-excel/
aliases: [/merge/multi-files/]
keywords: "Aspose.Cells Cloud, 複数のExcelファイルを統合, REST API, スプレッドシートの統合, クラウドSDK"
description: "Aspose.Cells Cloud REST API (v3.0) を使用して複数のExcelワークブックを1つのファイルに統合する方法を学びます。HTTPSエンドポイント、cURLコマンド、SDKサンプル、必要なパラメータ、エラーハンドリングの詳細を含みます。"
weight: 32
---

## REST API

このREST APIは、複数のExcelファイルを1つのExcelワークブックに統合します。

```bash
POST https://api.aspose.cloud/v3.0/cells/merge
```

### **セキュリティと認証**

Aspose.Cells Cloud API は安全であり、<a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWTトークンベースの認証</a>を必要とします。

### リクエストパラメータ

| パラメータ名     | 型      | 位置       | 説明                                                                                     | 必須 |
|------------------|---------|------------|------------------------------------------------------------------------------------------|------|
| files[]          | file    | formData   | 統合する1つ以上のExcelワークブック。リクエストでは `file1`, `file2`, … を使用します。    | はい   |
| format           | string  | query      | 出力フォーマット（例: `xlsx`）。                                                          | はい   |
| mergeToOneSheet  | boolean | query      | `true` を設定すると、すべてのワークシートを1つのシートに統合します。デフォルトは `false` です。 | いいえ |

### **レスポンス**

```json
{
    "Status" : "OK",
    "Code" : 200,
    "Filename" : "[統合後のファイル名]",
    "Filesize" : [ファイルサイズ],
    "FileContent" : "[Base64文字列]"
}
```

**HTTPステータスコード**

| コード | 意味             | 説明                                                   |
|--------|------------------|--------------------------------------------------------|
| 200    | OK               | フィルターが正常に適用され、レスポンスには操作の詳細が含まれます。 |
| 400    | Bad Request      | パラメータが不足している、または無効です（例: 未サポートのファイル形式）。 |
| 401    | Unauthorized     | JWTトークンが無効または不足しています。                |
| 413    | Payload Too Large| アップロードされたファイルがサイズ制限を超えています。 |
| 500    | Internal Server Error | 予期しないサーバーエラーが発生しました。              |

## SDK を使用した PostMerge API の利用方法

### PostMerge API の仕様

[OpenAPI仕様](https://apireference.aspose.cloud/cells/#/LightCells/PostMerge) はパブリックに利用可能なプログラミングインタフェースを定義し、Webブラウザから直接RESTインタラクションを実行できるようにします。

cURLコマンドラインツールを使用してAspose.Cellsウェブサービスに簡単にアクセスできます。以下の例は、cURLでクラウドAPIを呼び出す方法を示しています。

{{< tabs tabTotal="2" tabID="11" tabName11="リクエスト" tabName12="レスポンス" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/merge?format=xlsx" \
  -X POST \
  -H "Authorization: Bearer <jwt token>" \
  -F "file1=@file1.xlsx" \
  -F "file2=@file2.xlsx"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  {
    "Filename": "file1.xlsx",
    "FileSize": 274022,
    "FileContent": "-----Base64文字列--------"
  }
}
```

{{< /tab >}}

{{< /tabs >}}

### Aspose.Cells Cloud SDK の使用

SDK を使用すると、開発を迅速化できます。SDK が低レベルの詳細を処理してくれるため、プロジェクトのタスクに集中できます。Aspose.Cells Cloud SDK の完全なリストについては、[GitHubリポジトリ](https://github.com/aspose-cells-cloud)をご確認ください。

以下のコード例は、さまざまな SDK を使用して Aspose.Cells ウェブサービスを呼び出す方法を示しています。

{{< tabs tabTotal="9" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Android" tabName7="Perl" tabName8="Go" tabName9="Python" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example-Merge.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example-Merge.java" >}}
{{< /tab >}}

{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-LightCells-Merge.php" >}}
{{< /tab >}}

{{< tab tabNum="4" >}}
{{< /tab >}}

{{< tab tabNum="5" >}}
{{< /tab >}}

{{< tab tabNum="6" >}}
{{< /tab >}}

{{< tab tabNum="7" >}}
{{< /tab >}}

{{< tab tabNum="8" >}}
{{< /tab >}}

{{< tab tabNum="9" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "LightCellsMerge.py" >}}
{{< /tab >}}

{{< /tabs >}}