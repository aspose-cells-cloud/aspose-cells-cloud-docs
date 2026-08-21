---
title: "Aspose.Cells Cloud フォルダ移動 API – クラウド内でフォルダを素早く移動"
second_title: "ドキュメント"
ArticleTitle: "クラウドベースの Excel ファイル管理 – クラウド内でフォルダを素早く移動"
linktitle: "フォルダ移動"
type: docs
url: /ja/move-folder/
keywords: "Aspose.Cells, フォルダ移動, クラウドストレージ, Excel API"
description: "RESTful フォルダ移動 API を通じて Aspose.Cells Cloud ストレージ内のフォルダを移動する方法を学びます。エンドポイント、パラメータ、サンプル cURL、エラーコード、C#、Java、Python などの SDK 例を含みます。"
weight: 100
---

この API は、Aspose.Cells Cloud ストレージ内でフォルダをある場所から別の場所へ移動します。ファイルの整理やクラウドストレージの効率的な管理を支援します。

## **Excel API：フォルダ移動**

### Web API

```http
PUT https://api.aspose.cloud/v4.0/cells/storage/folder/move/{srcPath}
```

**cURL リクエストの例**

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/storage/folder/move/FolderA?destPath=FolderB" \
     -H "Authorization: Bearer {access_token}"
```

### **セキュリティと認証**

Aspose.Cells Cloud API は安全であり、<a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT トークンベースの認証</a>を必要とします。

### **moveFolder** API のリクエストパラメータ

| パラメータ名      | 型     | 位置   | 説明                                                                 |
| ----------------- | ------ | ------ | -------------------------------------------------------------------- |
| srcPath           | 文字列 | パス   | 移動するフォルダの完全なパス（例: `FolderA/`）                      |
| destPath          | 文字列 | クエリ | フォルダを移動する先のパス（例: `FolderB/`）                        |
| srcStorageName    | 文字列 | クエリ | （オプション）ソースストレージの名前                                |
| destStorageName   | 文字列 | クエリ | （オプション）宛先ストレージの名前                                  |

**パラメータの詳細**

- **srcPath** – 必須。移動元のフォルダパス。
- **destPath** – 必須。移動先のフォルダパス。
- **srcStorageName** – オプション。ソースストレージの識別子。
- **destStorageName** – オプション。宛先ストレージの識別子。

### **レスポンス**

成功した場合、API は空のレスポンスボディと HTTP ステータス **200 OK** を返します。エラーは `error` フィールドを含む JSON オブジェクトとして返されます。

**HTTP ステータスコード**

| HTTP コード | HTTP ステータス       | 説明                                                               |
| ----------- | --------------------- | ------------------------------------------------------------------ |
| 200         | OK                    | Web API の呼び出しが成功；レスポンスには操作の詳細が含まれます。   |
| 400         | Bad Request           | パラメータが不足または不正（例: 未サポートのファイル形式）         |
| 401         | Unauthorized          | JWT トークンが不正または不足                                       |
| 413         | Payload Too Large     | アップロードされたファイルがサイズ制限を超えています               |
| 500         | Internal Server Error | 予期しないサーバーエラー                                           |

## OpenAPI 仕様

[OpenAPI 仕様](https://reference.aspose.cloud/cells/#/FolderController/MoveFolder) は公開可能なプログラミングインタフェースを定義し、Web ブラウザから直接 REST 通信を実行できるようにします。

cURL コマンドラインツールを使用して、Aspose.Cells Web サービスに簡単にアクセスできます。以下の例は、cURL を使って Cloud API にリクエストを送信する方法を示しています。

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/storage/folder/move/{srcPath}?destPath={destPath}" \
     -H "Authorization: Bearer {access_token}"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{}
```

{{< /tab >}}

{{< /tabs >}}

SDK を使用すると、開発を最適化できます。SDK は低レベルの詳細を処理し、プロジェクトのタスクに集中できるようにします。Aspose.Cells Cloud SDK の完全な一覧については、[GitHub リポジトリ](https://github.com/aspose-cells-cloud) をご確認ください。

以下のコード例は、さまざまな SDK を使用して Aspose.Cells Web サービスにリクエストを送信する方法を示しています。