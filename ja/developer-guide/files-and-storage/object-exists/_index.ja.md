---
title: "Object Exists API – Aspose.Cells Cloud でのファイル／フォルダーの存在を確認"
second_title: "Document"
ArticleTitle: "Object Exists API – Aspose.Cells Cloud でのファイルまたはフォルダーの存在を検証"
linktitle: "Object Exists"
type: docs
url: /object-exists/
keywords: "Aspose.Cells, クラウドストレージ, object exists, ファイル存在確認, フォルダー存在確認, API"
description: "Object Exists API を使用して、Aspose.Cells Cloud ストレージ内にファイルまたはフォルダーが存在するかどうかを迅速に確認します。ストレージ名とバージョン ID のオプション指定をサポートし、バージョン管理対応オブジェクトで動作します。"
weight: 100
---

**Object Exists API** を使用すると、開発者は Aspose.Cells Cloud ストレージ内に特定のファイルまたはフォルダーが存在するかどうかを判断できます。この API は、存在の有無およびパスがフォルダーを指しているかどうかを示すシンプルなブール値を返します。

## **Excel API: Object Exists**

### Web API

```http
GET https://api.aspose.cloud/v5.0/cells/storage/exist/{path}
```

_`{path}`_ は、ストレージ内のファイルまたはフォルダーへの完全なパスです。

### **セキュリティと認証**

Aspose.Cells Cloud API はセキュアであり、<a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT トークンベースの認証</a>が必要です。

### リクエストパラメータ

| パラメータ名   | 型     | 位置   | 必須 | 説明                                                                 |
| -------------- | ------ | ------ | ---- | -------------------------------------------------------------------- |
| `path`         | 文字列 | パス   | はい  | ファイルまたはフォルダーへの完全なパス。                             |
| `storageName`  | 文字列 | クエリ | いいえ | ストレージ名。指定しない場合は、デフォルトでプライマリストレージが使用されます。 |
| `versionId`    | 文字列 | クエリ | いいえ | ファイルの特定のバージョン識別子（バージョン管理が有効な場合）。      |

**HTTP ステータスコード**

| HTTP コード | HTTP ステータス       | 説明                                                             |
| ----------- | --------------------- | ---------------------------------------------------------------- |
| 200         | OK                    | Web API の呼び出しが成功しました。応答には操作の詳細が含まれます。 |
| 400         | Bad Request           | パラメータが不足している、または無効です（例：サポートされていないファイル形式）。 |
| 401         | Unauthorized          | JWT トークンが無効または不足しています。                           |
| 413         | Payload Too Large     | アップロードされたファイルがサイズ制限を超えています。             |
| 500         | Internal Server Error | サーバーで予期しないエラーが発生しました。                         |

### **応答**

正常な呼び出しは、2 つのプロパティを含む JSON ペイロードを返します：

```json
{
  "Exists": true,
  "IsFolder": false
}
```

- **Exists** – ファイルまたはフォルダーが存在する場合は `true`、それ以外の場合は `false`。
- **IsFolder** – パスがフォルダーを指している場合は `true`、ファイルの場合は `false`。

## OpenAPI 仕様

[OpenAPI 仕様](https://reference.aspose.cloud/cells/#/StorageController/ObjectExists) は、パブリックにアクセス可能なプログラミングインタフェースを定義し、Web ブラウザから直接 REST 操作を実行できるようにします。

cURL コマンドラインツールを使用すると、Aspose.Cells Web サービスに簡単にアクセスできます。以下の例は、cURL を使用して Cloud API に呼び出しを行う方法を示しています。

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/storage/exist/myFolder/subFolder" \
     -H "Authorization: Bearer {access_token}" \
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

SDK を使用すると、開発を高速化できます。SDK は低レベルの詳細を処理し、プロジェクトのタスクに集中できるようにします。Aspose.Cells Cloud SDK の完全な一覧については、[GitHub リポジトリ](https://github.com/aspose-cells-cloud)をご確認ください。

以下のコード例は、さまざまな SDK を使用して Aspose.Cells Web サービスに呼び出しを行う方法を示しています。Gist が読み込まれない場合は、各タブの下に静的例が提供されています。

---