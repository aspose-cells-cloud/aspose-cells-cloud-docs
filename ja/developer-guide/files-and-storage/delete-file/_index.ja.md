---
title: "Aspose.Cells Cloud – ファイル削除 API"
second_title: "ドキュメント"
ArticleTitle: "Aspose.Cells Cloud – ファイル削除 API"
linktitle: "ファイル削除"
type: docs
url: /delete-file/
keywords: "Aspose Cells, ファイル削除 API, Excel クラウドストレージ, REST API, ファイル管理"
description: "Aspose.Cells Cloud ストレージから Excel ファイルを RESTful ファイル削除 API を使用して削除します。エンドポイント、パラメータ、認証、サンプルコードを含みます。"
weight: 100
---

**deleteFile** API は、クラウドストレージから指定されたファイルを削除し、リソースとデータを効率的に管理できるようにします。

## **Excel API: ファイル削除**

### Web API

```http
DELETE https://api.aspose.cloud/v4.0/cells/storage/file/{path}
```

### **セキュリティと認証**

Aspose.Cells Cloud API は安全で、<a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT トークンベースの認証</a>を必要とします。

```bash
-H "Authorization: Bearer {access_token}"
```

### リクエストパラメータ

| パラメータ名     | 型     | 位置   | 説明                                                                                           |
| :-------------- | :----- | :----- | :--------------------------------------------------------------------------------------------- |
| `path`          | string | パス   | 削除するファイルの URL エンコードされたパス                                                    |
| `storageName`   | string | クエリ | ファイルが存在するストレージの名前。デフォルトストレージを使用する場合は省略可能です。         |
| `versionId`     | string | クエリ | 削除する特定のファイルバージョンの識別子。省略した場合、最新バージョンが削除されます。           |

### レスポンスの説明

成功したリクエストは、空のレスポンスボディとともに **HTTP 200** を返します。JSON ペイロードは返されません。

```json
{}
```

**HTTP ステータスコード**

| コード | 意味                 | 説明                                                     |
| ------ | -------------------- | -------------------------------------------------------- |
| 200    | OK                   | フィルターが正常に適用されました。レスポンスには操作詳細が含まれます。 |
| 400    | Bad Request          | パラメータが不足している、または無効です（例：サポートされていないファイル形式）。 |
| 401    | Unauthorized         | JWT トークンが無効または不足しています。                 |
| 413    | Payload Too Large    | アップロードされたファイルがサイズ制限を超えています。   |
| 500    | Internal Server Error| 予期しないサーバーエラーが発生しました。                 |

## OpenAPI 仕様

[OpenAPI 仕様](https://reference.aspose.cloud/cells/#/FileController/DeleteFile) は、パブリックにアクセス可能なプログラミングインターフェースを定義し、ウェブブラウザから直接 REST のやり取りを実行できるようにします。

cURL コマンドラインツールを使用して、Aspose.Cells ウェブサービスに簡単にアクセスできます。以下の例は、cURL を使用してクラウド API にリクエストを送信する方法を示しています。

{{< tabs tabTotal="2" tabID="11" tabName11="リクエスト" tabName12="レスポンス" >}}

{{< tab tabNum="11" >}}

```bash
curl -X DELETE "https://api.aspose.cloud/v4.0/cells/storage/file/Example.xlsx?storageName=MyStorage" \
     -H "Authorization: Bearer YOUR_ACCESS_TOKEN" \
     -H "Accept: application/json"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```
{
}
```

{{< /tab >}}

{{< /tabs >}}

### Aspose.Cells Cloud SDK の使用

SDK を使用すると、開発を迅速に進めることができます。SDK は低レベルの詳細を管理し、プロジェクトのタスクに集中できるようにします。Aspose.Cells Cloud SDK の完全な一覧については、[GitHub リポジトリ](https://github.com/aspose-cells-cloud)をご確認ください。

以下のコード例は、さまざまな SDK を使用して Aspose.Cells ウェブサービスにリクエストを送信する方法を示しています。

---