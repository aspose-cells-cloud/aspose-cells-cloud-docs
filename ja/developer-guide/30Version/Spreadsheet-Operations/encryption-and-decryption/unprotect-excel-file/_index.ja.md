---
title: "Excel ワークブックの保護を解除 – Aspose.Cells Cloud API"
second_title: "ドキュメント"
linktitle: "Excel ファイルの保護を解除"
type: docs
url: /ja/excel-file-unprotect/
aliases:
  - /unprotect-excel-workbooks/
  - /workbook/unprotect/
keywords: "Aspose Cells, Excel 保護解除 API, ワークブック保護の解除, REST API, クラウド スプレッドシート"
description: "Aspose.Cells Cloud REST API を使用して Excel ワークブックの保護を解除する方法を学びます。リクエスト構文、パラメーター、cURL の例、および複数の言語での SDK コードを含みます。"
weight: 60
ArticleTitle: "Excel ワークブックの保護を解除 – Aspose.Cells Cloud API"
---

この REST API を使用して Excel ワークブックの保護を解除します。

## DeleteUnProtectWorkbook API

```http
DELETE https://api.aspose.cloud/v3.0/cells/{name}/protection
```

### **セキュリティと認証**

Aspose.Cells Cloud API は安全であり、<a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT トークンベースの認証</a>が必要です。

### パスパラメーター

| パラメーター | 型     | 説明                                      | 必須 |
| ----------- | ------ | ----------------------------------------- | ---- |
| **name**    | string | ワークブックファイル名（拡張子を含む）。 | はい   |

### クエリパラメーター

| パラメーター名   | 型     | 説明                                      |
| --------------- | ------ | ----------------------------------------- |
| folder          | string | 元のワークブックが格納されているフォルダーへのパス。 |
| storageName     | string | ワークブックが存在するストレージサービスの名前。   |

### リクエストボディパラメーター

| パラメーター名 | 型                        | 説明                                    |
| -------------- | ------------------------- | --------------------------------------- |
| protection     | WorkbookProtectionRequest | 保護設定を指定するオブジェクト（解除対象）。 |

#### WorkbookProtectionRequest

| パラメーター名   | 型     | 説明                                                                                         |
| --------------- | ------ | -------------------------------------------------------------------------------------------- |
| ProtectionType  | string | 解除する保護の種類（`ALL`, `CONTENTS`, `NONE`, `OBJECTS`, `SCENARIOS`, `STRUCTURE`, `WINDOWS`）。 |
| Password        | string | 保護を解除するために必要なパスワード（オプション）。                                          |

#### cURL の例

```bash
curl -X DELETE "https://api.aspose.cloud/v3.0/cells/test.xlsx/protection?folder=MyFolder&storageName=MyStorage" \
     -H "Authorization: Bearer <access_token>" \
     -H "accept: application/json" \
     -H "Content-Type: application/json" \
     -d '{ "ProtectionType": "ALL", "Password": "aspose"}'
```

#### レスポンス（成功）

```json
{
  "Code": 200,
  "Status": "OK"
}
```

### HTTPS ステータスエラーレスポンス

| HTTP ステータス | コード                | 説明                                     |
| --------------- | --------------------- | ---------------------------------------- |
| 400             | BadRequest            | パラメーターが不足または無効です。       |
| 401             | Unauthorized          | アクセストークンが無効または不足しています。 |
| 404             | NotFound              | 指定されたワークブックが、指定されたフォルダー/ストレージに見つかりません。 |
| 500             | InternalServerError   | 予期しないサーバーエラーが発生しました。   |

## SDK を使用して DeleteUnProtectWorkbook API を利用する方法

### DeleteUnProtectWorkbook API 仕様

[OpenAPI 仕様](https://apireference.aspose.cloud/cells/#/Protection/DeleteUnProtectWorkbook) はパブリックにアクセス可能なプログラミングインターフェースを定義し、ウェブブラウザから直接 REST のやり取りを実行できるようにします。

cURL コマンドラインツールを使用して、Aspose.Cells ウェブサービスに簡単にアクセスできます。以下の例では、cURL を使用してクラウド API にリクエストを送信する方法を示しています。

### Aspose.Cells Cloud SDK を使用する

SDK を使用すると、統合が簡略化され、ボイラープレートコードが削減されます。Aspose.Cells Cloud SDK の完全な一覧については、[GitHub リポジトリ](https://github.com/aspose-cells-cloud)をご覧ください。

以下のコード例では、さまざまな SDK を使用して Aspose.Cells ウェブサービスを呼び出す方法を示しています。

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleDeleteUnProtectWorkbook.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_DeleteUnProtectWorkbook.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_DeleteUnProtectWorkbook.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_DeleteUnProtectWorkbook.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_DeleteUnProtectWorkbook.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_DeleteUnProtectWorkbook.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_DeleteUnProtectWorkbook.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_DeleteUnProtectWorkbook.go" >}}

{{< /tab >}}

{{< /tabs >}}