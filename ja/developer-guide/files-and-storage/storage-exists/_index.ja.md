---
title: "ストレージの存在を確認する – Aspose.Cells Cloud API（v4.0）"
second_title: "ドキュメント"
ArticleTitle: "クラウドベースのExcelファイル管理 – ストレージの存在を確認する"
linktype: "ストレージの存在"
type: docs
url: /ja/storage-exists/
keywords: "Aspose.Cells、ストレージの存在、クラウドストレージAPI、REST、Excel"
description: "Aspose.Cells Cloudでストレージコンテナが存在するかを確認します。GET /v4.0/cells/storage/{storageName}/exist エンドポイント、必要なパラメータ、レスポンス形式について学び、C#、Java、Python などでのSDKサンプルを参照してください。"
weight: 100
---

`storageExists` API は、指定されたストレージが Aspose.Cells クラウドサービス内に存在するかを確認します。この機能は、ストレージに依存するすべての操作がエラーなく実行できることを保証するために重要です。
**概要** – `storageExists` エンドポイントを使用すると、特定のストレージコンテナが Aspose.Cells Cloud に存在するかどうかを確認できます。ファイル関連の操作を実行する前にこれを使用することで、ランタイムエラーを回避できます。

## ストレージの存在を確認する（storageExists）

### Web API

```
GET https://api.aspose.cloud/v4.0/cells/storage/{storageName}/exist
```

### **セキュリティと認証**

Aspose.Cells Cloud API は安全であり、<a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT トークンベースの認証</a>が必要です。

### リクエストパラメータ

| パラメータ名 | 型     | 位置   | 説明                             |
| ------------ | ------ | ------ | --------------------------------- |
| storageName  | 文字列 | パス   | 存在を確認するストレージの名前。 |

### **レスポンス**

```json
{
  "Name": "StorageExist",
  "Description": ["指定されたストレージが存在するかどうかを示します。"],
  "Type": "Class",
  "IsAbstract": false,
  "Properties": [
    {
      "Name": "Exists",
      "Description": [
        "ストレージが存在するかどうかを示します。",
        "このプロパティは、ストレージが存在する場合に true を返し、それ以外の場合は false を返します。"
      ],
      "Nullable": true,
      "ReadOnly": false,
      "IsInherit": false,
      "DataType": {
        "Identifier": "Boolean",
        "Name": "boolean"
      }
    }
  ]
}
```

**HTTP ステータスコード**

| コード | 意味                 | 説明                                                   |
| ------ | -------------------- | ------------------------------------------------------ |
| 200    | OK（成功）           | フィルターが正常に適用されました；レスポンスに操作詳細が含まれます。 |
| 400    | Bad Request（不正なリクエスト） | パラメータが不足または無効です（例：サポートされていないファイル形式）。 |
| 401    | Unauthorized（認証エラー）     | JWT トークンが無効または不足しています。               |
| 413    | Payload Too Large（ペイロードが大きすぎます） | アップロードされたファイルがサイズ制限を超えています。 |
| 500    | Internal Server Error（内部サーバーエラー） | 予期しないサーバーエラーが発生しました。               |

## SDK を使用して storage exists API を利用するには？

### OpenAPI 仕様

<a href="https://reference.aspose.cloud/cells/#/StorageController/StorageExists" rel="nofollow noopener noreferrer">OpenAPI 仕様</a> は、パブリックにアクセス可能なプログラミングインターフェースを定義しており、開発者が Web ブラウザから REST API にシームレスにアクセスできるようになります。

cURL コマンドラインツールを使用すると、Aspose.Cells Web サービスに簡単にアクセスできます。以下の例は、cURL を使用してクラウド API に呼び出しを行う方法を示しています。

{{< tabs tabTotal="2" tabID="11" tabName11="リクエスト" tabName12="レスポンス" >}}

{{< tab tabNum="11" >}}

```bash
curl -X GET "https://api.aspose.cloud/v4.0/cells/storage/{storageName}/exist" \
     -H "Authorization: Bearer {access_token}"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Exists": true
}
```

{{< /tab >}}

{{< /tabs >}}

### Aspose.Cells Cloud SDK を使用する

SDK を使用することが開発を加速する最も効率的な方法です。SDK は低レベルの実装詳細を抽象化し、開発者がプロジェクトのタスクに集中できるようにします。利用可能な Aspose.Cells Cloud SDK の完全な一覧については、<a href="https://github.com/aspose-cells-cloud" rel="nofollow noopener noreferrer">GitHub リポジトリ</a> をご覧ください。

以下のコード例は、さまざまな SDK を使用して Aspose.Cells Web サービスに API 呼び出しを行う方法を示しています。

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_StorageExists.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_StorageExists.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_StorageExists.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_StorageExists.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_StorageExists.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_StorageExists.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_StorageExists.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_StorageExists.go" >}}
{{</tab>}}
{{< /tabs >}}

---