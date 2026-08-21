---
title: "ワークシートのページ設定を設定する"
second_title: "Document"
linktitle: "ページ設定を設定する"
type: docs
url: /set-page-setup/
keywords: "Aspose.Cells, Excel, ページ設定, REST API, ワークシート, クラウドSDK"
description: "Aspose.Cells Cloud REST API を使用して Excel ワークシートのページ設定を設定する方法を学びます。リクエストの詳細、安全な HTTPS cURL の例、レスポンスのステータスコード、および複数のプログラミング言語の SDK コードスニペットが含まれます。"
weight: 20
ArticleTitle: "ワークシートのページ設定を設定する – Aspose.Cells Cloud API ガイド"
---

前提条件: この API を呼び出すには、有効な JWT (OAuth) トークンが必要であり、ワークブックは、読み取り/書き込み権限を持つ Aspose Cloud ストレージの場所に配置されている必要があります。トークンが **Authorization** ヘッダーに含まれていること、およびアカウントに必要な API クォータがあることを確認してください。

この REST API は、Excel ワークシートのページ設定を設定します。

## REST API

```bash
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/pagesetup
```

### **セキュリティと認証**

Aspose.Cells Cloud API は安全であり、<a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT トークンベースの認証</a>を必要とします。

### **リクエストパラメーター**

| パラメーター名 | 型     | 位置   | 説明              |
| -------------- | ------ | ------ | ----------------- |
| name           | string | path   | ドキュメント名。  |
| sheetName      | string | path   | ワークシート名。  |
| pageSetup      | object | body   | ページ設定の説明。|
| folder         | string | query  | ドキュメントフォルダー。 |
| storageName    | string | query  | ストレージ名。    |

**`pageSetup` オブジェクトの JSON ペイロードの例**

```json
{
  "pageSetup": {
    "orientation": "Portrait",
    "paperSize": "A4",
    "fitToPagesTall": 1,
    "fitToPagesWide": 1,
    "centerHorizontally": true,
    "centerVertically": false
  }
}
```

<a href="https://reference.aspose.cloud/cells/#/PageSetup/PostPageSetup" target="_blank" rel="noopener noreferrer">OpenAPI 仕様</a> は、パブリックにアクセス可能なプログラミングインターフェースを定義し、Web ブラウザから直接 REST アクションを実行できるようにします。

cURL コマンドラインツールを使用して Aspose.Cells Web サービスに簡単にアクセスできます。以下の例は、cURL を使用してクラウド API にアクセスする方法を示しています。

{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/myWorkbook.xlsx/worksheets/Tasks/pagesetup" \
-X POST \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>" \
-d '{
  "pageSetup": {
    "orientation": "Portrait",
    "paperSize": "A4",
    "fitToPagesTall": 1,
    "fitToPagesWide": 1,
    "centerHorizontally": true,
    "centerVertically": false
  }
}'
```

{{< /tab >}}

{{< tab tabNum="2" >}}

API は、操作の結果を示す JSON オブジェクトを返します：

```json
{
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

**可能なレスポンスステータスコード**

| コード | 意味                        | 発生条件                                         |
|------|-----------------------------|--------------------------------------------------|
| 200  | OK                          | ページ設定の更新が成功した場合                   |
| 400  | Bad Request                 | 無効な JSON ペイロード、または必須フィールドが欠落している場合 |
| 401  | Unauthorized                | JWT トークンが欠落している、または無効な場合     |
| 404  | Not Found                   | ワークブックまたはワークシート名が存在しない場合 |
| 500  | Internal Server Error       | 予期しないサーバーエラーが発生した場合           |

## Cloud SDK Family

SDK を使用することは、開発を高速化する最良の方法です。SDK は低レベルの詳細を処理し、プロジェクトのタスクに集中できるようにします。Aspose.Cells Cloud SDK の完全な一覧については、<a href="https://github.com/aspose-cells-cloud" target="_blank" rel="noopener noreferrer">GitHub リポジトリ</a>をご確認ください。

以下のコード例は、さまざまな SDK を使用して Aspose.Cells Web サービスにアクセスする方法を示しています：

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example_PostPageSetup.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostPageSetup.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostPageSetup.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostPageSetup.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostPageSetup.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostPageSetup.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostPageSetup.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostPageSetup.go" >}}

{{< /tab >}}

{{< /tabs >}}