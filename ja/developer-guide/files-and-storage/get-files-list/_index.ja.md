---
title: "Aspose.Cells Cloud API – ファイル一覧の取得（フォルダの内容）"
description: "Aspose.Cells Cloud ストレージ内の特定のフォルダからファイルおよびサブフォルダのリストを取得します。"
keywords:
  - Aspose.Cells
  - API
  - ファイル一覧の取得
  - クラウドストレージ
  - Excel
  - REST
type: docs
weight: 100
---

**ファイル一覧の取得** 操作は、Aspose.Cells Cloud ストレージの指定されたフォルダ内に格納されているファイルとサブフォルダのコレクションを返します。  
この操作は、クラウド上にある Excel ワークブック、アーカイブ、その他のサポートされているファイルタイプをブラウジングする際の主要なエントリーポイントです。

## Aspose.Cells Cloud API – ファイル一覧の取得（フォルダの内容）

```
GET https://api.aspose.cloud/v4.0/cells/storage/folder/{path}
```

### **セキュリティと認証**

Aspose.Cells Cloud API は安全であり、<a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT トークンベースの認証</a>が必要です。

### リクエストパラメータ

| 名前              | 位置   | 型      | 必須 | 説明                                                           |
| ----------------- | ------ | ------- | ---- | -------------------------------------------------------------- |
| **path**          | パス   | 文字列  | はい | クラウドストレージ内のフォルダへのパス。                       |
| **storageName**   | クエリ | 文字列  | いいえ | 使用するストレージ名。省略された場合、デフォルトのストレージが使用されます。 |
| **pageSize**      | クエリ | 整数    | いいえ | 1 ページあたりに返されるアイテムの最大数（デフォルト: 100）。    |
| **pageNumber**    | クエリ | 整数    | いいえ | 取得するページ番号（1 から始まり、デフォルト: 1）。             |

- **値** – `StorageFile` オブジェクトの配列。各オブジェクトには以下の情報が含まれます。
  - `Name` – ファイル名またはフォルダ名。
  - `IsFolder` – エントリがフォルダの場合は `true`。
  - `Size` – バイト単位のサイズ（フォルダの場合は `0`）。
  - `ModifiedDate` – 最終更新タイムスタンプ（ISO 8601 形式）。

### **レスポンス**

**HTTP ステータスコード**

| HTTP コード | HTTP ステータス       | 説明                                                           |
| ----------- | --------------------- | -------------------------------------------------------------- |
| 200         | OK                    | Web API が正常に呼び出された。レスポンスには操作の詳細が含まれます。 |
| 400         | Bad Request           | パラメータが不足または無効（例：サポートされていないファイル形式）。 |
| 401         | Unauthorized          | JWT トークンが無効または不足しています。                         |
| 413         | Payload Too Large     | アップロードされたファイルがサイズ制限を超えています。           |
| 500         | Internal Server Error | サーバーで予期しないエラーが発生しました。                       |
|             |                       |                                                                |

## OpenAPI 仕様

[OpenAPI 仕様](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Folder/GetFilesList) は、パブリックにアクセス可能なプログラミングインターフェースを定義し、Web ブラウザから直接 REST によるやり取りを実行できるようにします。

cURL コマンドラインツールを使用して、Aspose.Cells Web サービスに簡単にアクセスできます。以下の例では、cURL を使用してクラウド API を呼び出す方法を示しています。

{{< tabs tabTotal="2" tabID="11" tabName11="リクエスト" tabName12="レスポンス" >}}

{{< tab tabNum="11" >}}

```bash
curl -X GET "https://api.aspose.cloud/v4.0/cells/storage/folder/{path}?storageName=MyStorage&pageSize=100&pageNumber=1" \
     -H "Authorization: Bearer <your_access_token>"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Value": [
    {
      "Name": "Report.xlsx",
      "IsFolder": false,
      "Size": 124578,
      "ModifiedDate": "2024-03-10T12:34:56Z"
    },
    {
      "Name": "Archives",
      "IsFolder": true,
      "Size": 0,
      "ModifiedDate": "2024-02-01T08:00:00Z"
    }
  ]
}
```

{{< /tab >}}

{{< /tabs >}}

### Aspose.Cells Cloud SDK の使用

SDK を使用すると、開発を迅速化できます。SDK は低レベルの詳細を管理し、プロジェクトのタスクに集中できるようになります。Aspose.Cells Cloud SDK の完全な一覧については、<a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub リポジトリ</a>をご確認ください。

以下のコード例は、さまざまな SDK を使用して Aspose.Cells Web サービスを呼び出す方法を示しています。

---