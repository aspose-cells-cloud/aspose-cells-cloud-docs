---
title: "Aspose.Cells Cloud API – ディスク使用量の取得 | リアルタイムのストレージメトリック"
second_title: "ドキュメント"
ArticleTitle: "クラウドベースの Excel ファイル管理ソリューション – クラウド上でディスク使用量をすばやく取得するためのインターフェース"
linktype: "Get Disk Usage"
type: docs
url: /ja/get-disk-usage/
keywords: "Aspose Cells, Cloud API, ディスク使用量, ストレージメトリック, Excel, REST"
description: "Aspose.Cells Cloud のリアルタイムディスク使用量を取得します。GET /v4.0/cells/storage/disk エンドポイント、必要な認証、およびサンプル応答について学びます。"
weight: 100
---

**Get Disk Usage** 操作は、Aspose.Cells Cloud アカウントのリアルタイムストレージメトリックを返します。このエンドポイントを使用して、消費されたディスク容量と総ディスク容量を監視します。

- Aspose Cloud 環境における Excel API の現在のディスク使用量を取得します。
- 開発者がアプリケーションが消費したストレージ容量を監視できるようにします。
- ストレージ制限の事前対応管理およびコスト制御を可能にします。

## Excel API: GetDiskUsage

### Web API

```http
GET https://api.aspose.cloud/v4.0/cells/storage/disk
```

### **セキュリティと認証**

Aspose.Cells Cloud API は安全であり、<a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT トークンベースの認証</a>を必要とします。

### リクエストパラメータ

| パラメータ名 | 型     | 位置   | 説明                                      | 必須     |
|------------|------|------|------------------------------------------|--------|
| storageName | 文字列 | クエリ | 使用量を取得するストレージの名前。             | 任意   |

### **応答**

```json
{
  "Name": "DiskUsage",
  "Description": ["ディスク容量情報を格納するクラス。"],
  "Type": "Class",
  "IsAbstract": false,
  "Properties": [
    {
      "Name": "UsedSize",
      "Description": ["アプリケーションが使用しているディスク容量。"],
      "Nullable": true,
      "ReadOnly": false,
      "IsInherit": false,
      "DataType": {
        "Identifier": "Long",
        "Name": "long"
      }
    },
    {
      "Name": "TotalSize",
      "Description": ["利用可能な総ディスク容量。"],
      "Nullable": true,
      "ReadOnly": false,
      "IsInherit": false,
      "DataType": {
        "Identifier": "Long",
        "Name": "long"
      }
    }
  ]
}
```

**HTTP ステータスコード**

| コード | 意味                  | 説明                                                              |
|------|-----------------------|-------------------------------------------------------------------|
| 200  | OK                    | フィルターが正常に適用されました。応答には操作の詳細が含まれます。          |
| 400  | Bad Request           | パラメータが不足または無効です（例：サポートされていないファイル形式）。        |
| 401  | Unauthorized          | JWT トークンが無効または不足しています。                                     |
| 413  | Payload Too Large     | アップロードされたファイルがサイズ制限を超えています。                         |
| 500  | Internal Server Error | サーバーで予期しないエラーが発生しました。                                    |

## OpenAPI 仕様

[OpenAPI 仕様](https://reference.aspose.cloud/cells/#/StorageController/GetDiskUsage) はパブリックにアクセス可能なプログラミングインターフェースを定義し、ウェブブラウザから直接 REST 操作を実行できるようにします。

cURL コマンドラインツールを使用して、Aspose.Cells ウェブサービスに簡単にアクセスできます。以下の例では、cURL を使用して Cloud API にアクセスする方法を示しています。

{{< tabs tabTotal="2" tabID="11" tabName11="リクエスト" tabName12="応答" >}}

{{< tab tabNum="11" >}}

```bash
curl -X GET "https://api.aspose.cloud/v4.0/cells/storage/disk?storageName=MyStorage" \
     -H "Authorization: Bearer YOUR_ACCESS_TOKEN"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "UsedSize": 12345678,
  "TotalSize": 10737418240
}
```

{{< /tab >}}

{{< /tabs >}}

### Aspose.Cells Cloud SDK の使用

SDK を使用すると、開発を最適化できます。SDK は低レベルの詳細を処理するため、プロジェクトのタスクに集中できます。Aspose.Cells Cloud SDK の完全な一覧については、[GitHub リポジトリ](https://github.com/aspose-cells-cloud) を確認してください。

以下のコード例は、さまざまな SDK を使用して Aspose.Cells ウェブサービスにアクセスする方法を示しています。

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_GetDiskUsage.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_GetDiskUsage.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_GetDiskUsage.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_GetDiskUsage.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_GetDiskUsage.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_GetDiskUsage.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_GetDiskUsage.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_GetDiskUsage.go" >}}
{{</tab>}}
{{< /tabs >}}